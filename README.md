# Helpline_for_suicide
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Suicide Helpline Numbers</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }
        .container {
            max-width: 600px;
            margin: 20px auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
        }
        #state-selector {
            width: 100%;
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
            outline: none;
        }
        #helpline-numbers {
            list-style-type: none;
            padding: 0;
        }
        #helpline-numbers li {
            margin-bottom: 10px;
        }
        #helpline-numbers li strong {
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Suicide Helpline Numbers</h1>
        <select id="state-selector">
            <option value="" disabled selected>Select state</option>
            <option value="Andaman and Nicobar Islands">Andaman and Nicobar Islands</option>
            <option value="Andhra Pradesh">Andhra Pradesh</option>
            <option value="Arunachal Pradesh">Arunachal Pradesh</option>
            <option value="Assam">Assam</option>
	        <option value="Bihar">Bihar</option>
	        <option value="Chandigarh">Chandigarh</option>
	        <option value="Dadra and Nagar Haveli and Daman and Diu">Dadra and Nagar Haveli and Daman and Diu</option>
	        <option value="Delhi">Delhi</option>
	        <option value="Goa">Goa</option>
	        <option value="Gujarat">Gujarat</option>
	        <option value="Haryana">Haryana</option>
	        <option value="Himachal Pradesh">Himachal Pradesh</option>
	        <option value="Jammu and Kashmir">Jammu and Kashmir</option>
	        <option value="Jharkhand">Jharkhand</option>
	        <option value="Karnataka">Karnataka</option>
	        <option value="Kerala">Kerala</option>
	        <option value="Ladakh">Ladakh</option>
	        <option value="Lakshadweep">Lakshadweep</option>
	        <option value="Madhya Pradesh">Madhya Pradesh</option>
	        <option value="Maharashtra">Maharashtra</option>
	        <option value="Manipur">Manipur</option>
	        <option value="Meghalaya">Meghalaya</option>
	        <option value="Mizoram">Mizoram</option>
	        <option value="Nagaland">Nagaland</option>
	        <option value="Odisha">Odisha</option>
	        <option value="Puducherry">Puducherry</option>
	        <option value="Punjab">Punjab</option>
	        <option value="Rajasthan">Rajasthan</option>
	        <option value="Sikkim">Sikkim</option>
	        <option value="Tamil Nadu">Tamil Nadu</option>
	        <option value="Telangana">Telangana</option>
	        <option value="Tripura">Tripura</option>
	        <option value="Uttar Pradesh">Uttar Pradesh</option>
	        <option value="Uttarakhand">Uttarakhand</option>
	        <option value="West Bengal">West Bengal</option>
        
        </select>
        <ul id="helpline-numbers"></ul>
    </div>

    <script>
        const helplineNumbers =  {
    "India": 
          {"Andaman and Nicobar Islands": "03192-230239" ,
          "Andhra Pradesh":"1800-425-2908" ,
          "Arunachal Pradesh": "9436055743" ,
          "Assam":"0361-2540446" ,
          "Bihar": "0612-2219205"  ,
          "Chandigarh": "0172-2749900"  ,
          "Chhattisgarh" : "1800-233-3330"  ,
          "Dadra and Nagar Haveli and Daman and Diu": "0260-2642566"  ,
          "Delhi" : "011-23389090"  ,
          "Goa" : "0832-2412648"  ,
          "Gujarat" : "1800-233-3330"  ,
          "Haryana" : "1800-180-1817"  ,
          "Himachal Pradesh" : "9418170816"  ,
          "Jammu and Kashmir" : " 0191-2571616"  ,
          "Jharkhand" : "0651-2282201"  ,
          "Karnataka" : "080-6565-5555"  ,
          "Kerala" : "1056"  ,
          "Ladakh" : "01982-257416"  ,
          "Lakshadweep" : "04896-263681"  ,
          "Madhya Pradesh" : "1800-233-3330"  ,
          "Maharashtra" : "022-27546669"  ,
          "Manipur" : "104"  ,
          "Meghalaya" : "1800-345-3731"  ,
          "Mizoram" : "0389-2335000"  ,
          "Nagaland" : "03862-220218"  ,
          "Odisha" : "9439994859"  ,
          "Puducherry" : "104"  ,
          "Punjab" : "104"  ,
          "Rajasthan" : "0141-2752443"  ,
          "Sikkim" : "1800-345-3745"  ,
          "Tamil Nadu" : "104"  ,
          "Telangana" : "104"  ,
          "Tripura" : "0381-2323355"  ,
          "Uttar Pradesh" : "1800-180-5444"  ,
          "Uttarakhand" : "104"  ,
          "West Bengal" : "033-23598004"  
        }
    
    }
   

        const stateSelector = document.getElementById("state-selector");
        const helplineList = document.getElementById("helpline-numbers");

        stateSelector.addEventListener("change", () => {
            
            const selectedstate = stateSelector.value;
            console.log(selectedstate);
            helplineList.innerHTML = "";
            if (selectedstate && helplineNumbers.India[selectedstate]) {
                console.log(selectedstate);
                    const listItem = document.createElement("li");
                    listItem.innerHTML = `<strong>${selectedstate}:</strong> ${helplineNumbers.India[selectedstate]}`;
                    helplineList.appendChild(listItem);
            } else {
                const listItem = document.createElement("li");
                listItem.textContent = "No helpline numbers available for this state.";
                helplineList.appendChild(listItem);
            }
        });
    </script>
</body>
</html>
