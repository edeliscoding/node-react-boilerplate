When setting up your React frontend:
Ensure it's configured to include credentials in requests (e.g., credentials: 'include' in fetch calls).

To use credentials: true in React example.

fetch('https://your-backend.com/api/data', {
method: 'GET', // or POST, PUT, DELETE, etc.
credentials: 'include', // This ensures cookies or credentials are sent
headers: {
'Content-Type': 'application/json',
},
})
.then(response => {
if (!response.ok) {
throw new Error('Network response was not ok');
}
return response.json();
})
.then(data => {
console.log('Data:', data);
})
.catch(error => {
console.error('There was a problem with your fetch operation:', error);
});
