# Backend Validation

Example validation schema using `express-validator`:

```javascript
const { body } = require("express-validator");

exports.createUserValidation = [
  body("name").notEmpty().withMessage("Name is required"),
  body("email").isEmail().withMessage("Invalid email address"),
  // Add more validation rules as needed
];
```
