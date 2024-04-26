# 🐱 Performance Testing with JMeter on The Cat API 🐾

This project consists of performance tests carried out on The Cat API using Apache JMeter. The tests focus on evaluating the API's performance in handling requests for cat images and verifying the integrity of the JSON responses.

## 🛠️ Environment Setup

To run the performance tests, you need to set up the environment and obtain an API key from The Cat API.

### 🗝️ Getting an API Key

1. Go to [The Cat API - View Account](https://developers.thecatapi.com/view-account/ylX4blBYT9FaoVd6OhvR?report=gpN-ReBkp).
2. Log in to your account or create a new one.
3. Copy your API key.

### ⚙️ Configuring JMeter

1. Download and install Apache JMeter on your computer. You can find JMeter [here](https://jmeter.apache.org/download_jmeter.cgi).
2. Open JMeter.
3. Create a new Test Plan: `File` > `New Test Plan`.
4. Add a Thread Group: Right-click on Test Plan > `Add` > `Threads (Users)` > `Thread Group`.
5. Add an HTTP Request: Right-click on the Thread Group > `Add` > `Sampler` > `HTTP Request`.
   - Protocol: `https`
   - Server Name or IP: `api.thecatapi.com`
   - Method: `GET`
   - Path: `/v1/images/search`
   - Parameters:
     - `api_key`: `<Your API Key>`
6. Add Assertions:
   - JSON Assertion to verify the JSON response.
   - Response Assertion to verify the status.
7. Add Listeners to view test results.

## 🚀 Running the Tests

1. Save the Test Plan: `File` > `Save Test Plan As...`.
2. Execute the Test Plan: `Run` > `Start`.

# 😻 Test Plan Details 🐾

## 🧪 Tests with JSON and Response Assertions 🐾

We have included JSON assertions to verify the integrity of the JSON response from The Cat API. These assertions ensure that the response contains the expected JSON structure and data.

### JSON Assertion 🐾

🔍 We have added JSON assertions to verify the integrity of the JSON response. These assertions ensure that the response contains the expected JSON structure and data.

### Response Assertion 🐱

🔍 In addition to JSON assertions, we have also added Response assertions to verify the status of the response. These assertions check if the response status is as expected, ensuring that the API is functioning correctly.

With these assertions, we ensure that the API responses are valid and consistent, providing reliable data for our applications. 🚀

