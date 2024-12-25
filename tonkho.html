<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Google Sheets Data with Conditional Logic</title>
  <style>
    /* General styles */
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 20px;
      background-color: #f4f4f9;
      color: #333;
    }

    h1 {
      text-align: center;
      color: #555;
    }

    label, select {
      font-size: 16px;
    }

    select {
      padding: 8px 12px;
      margin: 20px 0;
      border: 1px solid #ccc;
      border-radius: 4px;
      width: 100%;
      max-width: 400px;
    }

    /* Table styles */
    table {
      width: 100%;
      border-collapse: collapse;
      margin: 20px 0;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      background-color: #fff;
    }

    table, th, td {
      border: 1px solid #ddd;
    }

    th {
      background-color: #0078D4; /* Primary color */
      color: white;
      text-align: left;
      padding: 12px 15px;
    }

    td {
      padding: 12px 15px;
      text-align: left;
      word-wrap: break-word;
    }

    tr:nth-child(even) {
      background-color: #f9f9f9;
    }

    tr:hover {
      background-color: #f1f1f1;
    }

    /* Responsive styles for mobile */
    @media screen and (max-width: 768px) {
      table {
        font-size: 14px;
      }

      th, td {
        padding: 10px;
      }

      th:first-child, td:first-child {
        word-wrap: break-word;
      }
    }
  </style>
</head>
<body>
  <h1>Kiểm Tra Tồn Kho Nhanh Nhất</h1>

  <!-- Dropdown for selecting group -->
  <label for="custom-filter"> Lọc Theo Nhóm Hàng:</label>
  <select id="custom-filter">
    <option value="all">Tất Cả</option>
    <option value="group1">Group 1</option>
    <option value="group2">Group 2</option>
    <option value="group3">Group 3</option>
  </select>

  <table id="data-table">
    <thead>
      <tr>
        <th>Mã Hàng</th>
        <th>Tên Hàng</th>
        <th>Tồn</th>
        <th>Giá Bán</th>
      </tr>
    </thead>
    <tbody>
      <!-- Data will be inserted here -->
    </tbody>
  </table>

  <script>
    async function fetchData() {
      const url = "https://docs.google.com/spreadsheets/d/1nnPF_KgzMSZji6BM5QuaNYfQwPMVf2DAfSVo7HW2ebs/export?format=csv&gid=130871701";
      const response = await fetch(url);
      const data = await response.text();

      const rows = data.split("\n").slice(1); // Skip the header row
      const tableBody = document.getElementById("data-table").querySelector("tbody");
      const customFilter = document.getElementById("custom-filter");

      // Define custom groups
      const groups = {
        group1: ["23051910","23051912"],
        group2: ["19061019"],
        group3: ["20100904"]
      };

      // Parse data and store in an array
      const allData = rows.map(row => {
        const cols = row.split(",");
        if (cols.length >= 4) {
          const code = cols[0].trim(); // Code (Column 1)
          const product = cols[1].trim(); // Product (Column 2)
          const price = parseFloat(cols[2].trim()) || 0; // Price (Column 3), default to 0
          let description = cols[3]?.trim(); // Description (Column 4)

          // Logic for column 4
          if (price === 0) {
            description = "Hết hàng"; // Always set to "Hết hàng" if price is 0
          } else if (price >= 1 && !description) {
            description = "Liên hệ"; // Set to "Liên hệ" if column 4 is empty
          }

          return { code, product, price, description };
        }
        return null;
      }).filter(item => item); // Remove null values

      // Function to render table data based on selected group
      function renderTable(selectedGroup) {
        tableBody.innerHTML = ""; // Clear current table rows
        allData.forEach(item => {
          const inGroup = selectedGroup === "all" || groups[selectedGroup]?.includes(item.code);
          if (inGroup) {
            const tr = document.createElement("tr");
            tr.innerHTML = `
              <td>${item.code}</td>
              <td>${item.product}</td>
              <td>${item.price}</td>
              <td>${item.description}</td>
            `;
            tableBody.appendChild(tr);
          }
        });
      }

      // Event listener for custom filter
      customFilter.addEventListener("change", (e) => {
        renderTable(e.target.value);
      });

      // Initial render with all data
      renderTable("all");
    }

    // Fetch and render data on page load
    fetchData();
  </script>
</body>
</html>
