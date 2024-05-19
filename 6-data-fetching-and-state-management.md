# Data Fetching and State Management

Example usage of Redux Query:

```javascript
import { useQuery } from "react-query";

const fetchUserProfile = async () => {
  const response = await fetch("/api/students/123/profile");
  return response.json();
};

function UserProfile() {
  const { data, isLoading, error } = useQuery("userProfile", fetchUserProfile);

  if (isLoading) return "Loading...";
  if (error) return "Error occurred while fetching user profile";

  return (
    <div>
      <h2>{data.name}</h2>
      <p>{data.email}</p>
      {/* Render other profile data */}
    </div>
  );
}
```
