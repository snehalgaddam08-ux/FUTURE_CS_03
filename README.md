FUTURE_CS_03 — API Security Risk Analysis
Overview

This project was completed as part of the Future Interns Cyber Security Internship — Task 3.

The objective of this task is to perform a practical API security assessment using Postman and identify security-relevant observations related to authentication, authorization, data exposure, HTTP status codes, response headers, rate limiting, and API behavior.
Objectives

    Analyze API endpoints using Postman
    Review authentication and authorization behavior
    Perform object-level access testing
    Check for excessive data exposure
    Analyze HTTP response status codes
    Review security-related response headers
    Observe rate-limiting controls
    Test GET and POST API operations
    Document security observations and recommendations

Tools & Technologies

    Postman
    REST API
    JSON
    HTTP/HTTPS
    GitHub

API Tested

JSONPlaceholder — Public Demo REST API

Base URL:

https://jsonplaceholder.typicode.com

The API was used only as a public educational/testing target.
Tests Performed
1.⁠ ⁠GET Users

Tested:

GET /users

Verified the API response, JSON structure, HTTP status code, and returned data.
2.⁠ ⁠User Object Access

Tested:

GET /users/1

GET /users/2

The responses were compared to demonstrate object-level access testing.
3.⁠ ⁠Invalid Object ID

Tested:

GET /users/99999

The API returned:

404 Not Found

This demonstrates handling of a nonexistent resource.
4.⁠ ⁠Authentication Review

The tested requests were configured with:

No Auth

Because JSONPlaceholder is a public demo API, this is treated as an educational observation rather than a confirmed vulnerability.
5.⁠ ⁠Response Header Analysis

Response headers were reviewed for security-related controls, caching behavior, server information, and rate-limit information.
6.⁠ ⁠Rate-Limit Observation

Rate-limit headers such as:

    X-Ratelimit-Limit
    X-Ratelimit-Remaining
    X-Ratelimit-Reset

were observed in the API responses.
7.⁠ ⁠POST Request Testing

Tested:

POST /posts

The API returned:

201 Created

This was used to validate successful resource-creation behavior and HTTP status-code testing.
Security Observations

The assessment demonstrated several areas that should be considered when testing a production SaaS API:

    Authentication should protect private resources.
    Server-side authorization should be enforced for every object.
    API responses should expose only necessary data.
    Invalid resource requests should be handled consistently.
    Rate limiting should be implemented according to endpoint sensitivity.
    Input validation should be applied to write operations.
    Security-relevant headers should be reviewed.
    API security tests should be integrated into the development lifecycle.

Important Note

JSONPlaceholder is a public mock/demo API designed for testing and learning. Therefore, the observations documented in this project should not be interpreted as confirmed vulnerabilities in a production application.

The project demonstrates the methodology and evidence-collection process used during an API security assessment.
Evidence

Screenshots captured during the Postman assessment are included in the Evidence folder.

The final detailed assessment report is also included in this repository.
