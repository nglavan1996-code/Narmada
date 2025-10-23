# Narmada
Build the following API requests
a) Provide a user story from your project or sample userstory--> ask to convert into non-functional testcases
Request:
{
  "messages": [
    {
      "role": "user",
      "content": "**User Story 1: Vehicle Search & Filtering**\n\n**As a** car shopper  \n**I want to** search and filter the vehicle inventory  \n**So that** I can easily find cars that match my specific preferences and requirements\n\n**Acceptance Criteria:**\n- Can filter by make, model, year, price range, and mileage\n- Can sort results by price (low to high, high to low), newest first, and mileage\n- View clear vehicle cards with images, key specs, and pricing\n- See the total number of matching vehicles in search results\n- Pagination or infinite scroll for browsing multiple results"
    },
     {
      "role": "system",
      "content": "As a AI assistant ,  convert into non-functional testcases"
    }
  ],
  "model": "llama-3.3-70b-versatile",
  "max_tokens" : 100
  }
Response:

{
    "id": "chatcmpl-96d2b12a-899f-4a25-b840-264a8df3b348",
    "object": "chat.completion",
    "created": 1761192160,
    "model": "llama-3.3-70b-versatile",
    "choices": [
        {
            "index": 0,
            "message": {
                "role": "assistant",
                "content": "### Non-Functional Test Cases for Vehicle Search & Filtering\n\n#### Performance Test Cases\n\n1. **Search Response Time**\n\t* Precondition: The user is on the vehicle search page.\n\t* Steps:\n\t\t1. Enter a search query with multiple filters (e.g., make, model, year, price range, and mileage).\n\t\t2. Measure the time it takes for the search results to load.\n\t* Expected Result: The search results load within 2 seconds.\n2"
            },
            "logprobs": null,
            "finish_reason": "length"
        }
    ],
    "usage": {
        "queue_time": 0.054939667,
        "prompt_tokens": 172,
        "prompt_time": 0.009338053,
        "completion_tokens": 100,
        "completion_time": 0.24448257,
        "total_tokens": 272,
        "total_time": 0.253820623
    },
    "usage_breakdown": null,
    "system_fingerprint": "fp_6507bcfb6f",
    "x_groq": {
        "id": "req_01k87kqarkfpnbvn99ctq50nj7"
    },
    "service_tier": "on_demand"
}


Result in deep seek after pasting this response :


Performance Test Cases (continued)
1. Search Response Time Under Load
    * Precondition: System under simulated load of 100 concurrent users
    * Steps: Execute multiple simultaneous search requests with different filters
    * Expected Result: 95% of requests complete within 3 seconds under load
2. Filter Application Performance
    * Precondition: Search results are displayed
    * Steps: Apply multiple filters sequentially and measure response time
    * Expected Result: Each filter application responds within 1 second
Load & Stress Test Cases
1. Concurrent User Load
    * Objective: Verify system handles 500 concurrent users searching vehicles
    * Success Criteria: Response time < 4 seconds, error rate < 1%
2. Peak Load Handling
    * Objective: Handle sudden traffic spikes during promotional events
    * Success Criteria: System remains stable with 1000+ concurrent users
Security Test Cases
1. SQL Injection Prevention
    * Precondition: Access to search input fields
    * Steps: Attempt SQL injection in search parameters
    * Expected Result: Input sanitized, no database errors exposed
2. XSS Vulnerability Testing
    * Steps: Inject malicious scripts in search inputs
    * Expected Result: Scripts properly escaped, no execution in browser
Usability Test Cases
1. Mobile Responsiveness
    * Objective: Verify search interface works on various screen sizes
    * Success Criteria: All elements accessible and functional on mobile devices
2. Accessibility Compliance
    * Objective: Ensure WCAG 2.1 AA compliance
    * Success Criteria: Screen reader compatible, keyboard navigable
Compatibility Test Cases
1. Cross-Browser Compatibility
    * Browsers: Chrome, Firefox, Safari, Edge
    * Expected Result: Consistent functionality across all supported browsers
Reliability Test Cases
1. Error Handling
    * Steps: Introduce network failures during search
    * Expected Result: Graceful error messages, no application crashes
2. Data Consistency
    * Objective: Ensure search results match database records
    * Success Criteria: 100% data accuracy in displayed results


