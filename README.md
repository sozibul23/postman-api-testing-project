# Postman API Testing

**Author:** Sozibul Islam  
**Date:** 2025-08-22  

-------------------

## Project Overview
This project demonstrates **API testing** using Postman with automated test scripts.  
It validates:
- Status codes  
- Response time  
- Content-Type  
- JSON response body  
- Positive & negative scenarios  

------------------------------------

## Test Scripts Examples
```javascript 
pm.test("Status code is 200", () => pm.response.to.have.status(200));
pm.test("Content-Type is JSON", () => pm.expect(pm.response.headers.get("Content-Type")).to.match(/application\/json/));
pm.test("Response has ID and name", () => pm.expect(pm.response.json()).to.include.keys("id", "name"));

