<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TEIS Repository README Generator</title>
    <style>
        body {
            font-family: sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 960px;
            margin: 20px auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }

        h1 {
            text-align: center;
            color: #007bff;
            margin-bottom: 20px;
        }

        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }

        input[type="text"],
        textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }

        button {
            background-color: #007bff;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s ease;
        }

        button:hover {
            background-color: #0056b3;
        }

        #preview {
            margin-top: 20px;
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
            background-color: #f9f9f9;
            white-space: pre-wrap;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
        }

        th, td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: left;
        }

        th {
            background-color: #f2f2f2;
        }

        tr:nth-child(even) {
            background-color: #f9f9f9;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .container {
                padding: 10px;
                margin: 10px;
            }

            input[type="text"],
            textarea {
                padding: 8px;
                margin-bottom: 10px;
            }

            button {
                padding: 8px 16px;
                font-size: 14px;
            }
        }

        /* Chart Styles (Simple Placeholder) */
        #chartContainer {
            width: 100%;
            height: 300px;
            background-color: #eee;
            margin-top: 20px;
            border-radius: 5px;
            text-align: center;
            line-height: 300px;
            color: #888;
        }

        /* Hover Effects */
        input[type="text"]:hover,
        textarea:hover {
            border-color: #007bff;
            box-shadow: 0 0 5px rgba(0, 123, 255, 0.2);
        }

        table tr:hover {
            background-color: #e9ecef;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>TEIS Repository README Generator</h1>

        <label for="repoName">Repository Name:</label>
        <input type="text" id="repoName" placeholder="Enter repository name">

        <label for="description">Description:</label>
        <textarea id="description" rows="4" placeholder="Enter a brief description of the repository"></textarea>

        <button onclick="generateReadme()">Generate README</button>

        <h2>Preview</h2>
        <div id="preview"></div>

        <h2>Interactive Table</h2>
        <table>
            <thead>
                <tr>
                    <th>Header 1</th>
                    <th>Header 2</th>
                    <th>Header 3</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Row 1, Cell 1</td>
                    <td>Row 1, Cell 2</td>
                    <td>Row 1, Cell 3</td>
                </tr>
                <tr>
                    <td>Row 2, Cell 1</td>
                    <td>Row 2, Cell 2</td>
                    <td>Row 2, Cell 3</td>
                </tr>
                 <tr>
                    <td>Row 3, Cell 1</td>
                    <td>Row 3, Cell 2</td>
                    <td>Row 3, Cell 3</td>
                </tr>
            </tbody>
        </table>

        <h2>Interactive Chart</h2>
        <div id="chartContainer">
            Placeholder for Chart
        </div>
    </div>

    <script>
        function generateReadme() {
            const repoName = document.getElementById("repoName").value;
            const description = document.getElementById("description").value;

            let readmeContent = `# ${repoName}\
\
${description}`;

            document.getElementById("preview").textContent = readmeContent;
        }
    </script>
</body>
</html>