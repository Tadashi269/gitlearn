<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Disaster Report Form</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <style>
        .dark-mode {
            background-color: #1a202c;
            color: #cbd5e0;
        }
        .dark-mode input, .dark-mode select, .dark-mode textarea {
            background-color: #2d3748;
            border-color: #4a5568;
            color: #cbd5e0;
        }
        .dark-mode input::placeholder, .dark-mode textarea::placeholder {
            color: #a0aec0;
        }
        .dark-mode button {
            background-color: #4a5568;
        }
        .dark-mode button:hover {
            background-color: #2d3748;
        }
    </style>
</head>
<body class="dark-mode p-6">
    <div class="max-w-lg mx-auto bg-gray-800 rounded-lg shadow-lg">
        <div class="bg-blue-800 text-white p-4 rounded-t-lg">
            <h2 class="text-2xl font-bold">Disaster Report Form</h2>
        </div>
        <div class="p-8">
            <form action="/submit-disaster-report" method="post">
                <div class="mb-4">
                    <label for="disaster-type" class="block text-gray-400">Type of Disaster:</label>
                    <select id="disaster-type" name="disaster-type" class="mt-1 block w-full border-gray-600 rounded-md shadow-sm focus:ring-indigo-500 focus:border-indigo-500" required>
                        <option value="earthquake">Earthquake</option>
                        <option value="flood">Flood</option>
                        <option value="hurricane">Hurricane</option>
                        <option value="wildfire">Wildfire</option>
                        <option value="other">Other</option>
                    </select>
                </div>
                <div class="mb-4">
                    <label for="location" class="block text-gray-400">Location:</label>
                    <input type="text" id="location" name="location" class="mt-1 block w-full border-gray-600 rounded-md shadow-sm focus:ring-indigo-500 focus:border-indigo-500" required>
                </div>
                <div class="mb-4">
                    <label for="date" class="block text-gray-400">Date:</label>
                    <input type="date" id="date" name="date" class="mt-1 block w-full border-gray-600 rounded-md shadow-sm focus:ring-indigo-500 focus:border-indigo-500" required>
                </div>
                <div class="mb-4">
                    <label for="description" class="block text-gray-400">Description of Damage:</label>
                    <textarea id="description" name="description" rows="5" class="mt-1 block w-full border-gray-600 rounded-md shadow-sm focus:ring-indigo-500 focus:border-indigo-500" required></textarea>
                </div>
                <div class="mb-4">
                    <label for="contact-name" class="block text-gray-400">Contact Name:</label>
                    <input type="text" id="contact-name" name="contact-name" class="mt-1 block w-full border-gray-600 rounded-md shadow-sm focus:ring-indigo-500 focus:border-indigo-500" required>
                </div>
                <div class="mb-4">
                    <label for="contact-email" class="block text-gray-400">Contact Email:</label>
                    <input type="email" id="contact-email" name="contact-email" class="mt-1 block w-full border-gray-600 rounded-md shadow-sm focus:ring-indigo-500 focus:border-indigo-500" required>
                </div>
                <div class="mb-4">
                    <button type="submit" class="w-full bg-indigo-600 text-white py-2 px-4 rounded-md hover:bg-indigo-700">Submit Report</button>
                </div>
            </form>
        </div>
    </div>
</body>
</html>
