const express = require('express');
const app = express();

// Sample user data
const users = [
    { id: 1, name: 'Louise', email: 'louise@example.com' },
    { id: 2, name: 'Aaron', email: 'Aaron@example.com' },
    { id: 3, name: 'Kevin', email: 'kevin@example.com' },
    { id: 4, name: 'Davey', email: 'davey@example.com' },
    { id: 5, name: 'Dwayne', email: 'Dwayne@example.com' },
];

// Helper function to filter by search term
function filterUsers(users, search) {
    if (!search) return users;
    const [key, value] = search.split(':');
    return users.filter(user => user[key] && user[key].includes(value));
}

// Helper function to sort users
function sortUsers(users, sort) {
    if (!sort) return users;
    const [key, order] = sort.split(':');
    return users.sort((a, b) => {
        if (a[key] < b[key]) return order === 'asc' ? -1 : 1;
        if (a[key] > b[key]) return order === 'asc' ? 1 : -1;
        return 0;
    });
}

// Helper function to paginate users
function paginateUsers(users, pageNumber, pageSize) {
    const startIndex = (pageNumber - 1) * pageSize;
    return users.slice(startIndex, startIndex + pageSize);
}

// Endpoint to get users with pagination, search, and sort
app.get('/users', (req, res) => {
    const { page_number, page_size, search, sort } = req.query;
    const pageNumber = parseInt(page_number, 10) || 1; // Default to 1 if not provided
    const pageSize = parseInt(page_size, 10) || 10; // Default to 10 if not provided

    
});

const PORT = process.env.PORT || 3000;
app.listen(PORT, () => {
    console.log(`Server is running on port ${PORT}`);
});
