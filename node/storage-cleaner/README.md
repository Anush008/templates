# Node.js Storage Cleaner Function

Storage cleaner function to remove all files from the buckets older than X number of days.

## 🧰 Usage

### GET /

Remove the files older than X number of days from all buckets.

**Response**

Sample `200` Response: Buckets cleaned

## ⚙️ Configuration

| Setting           | Value         |
| ----------------- | ------------- |
| Runtime           | Node (18.0)   |
| Entrypoint        | `src/main.js` |
| Build Commands    | `npm install` |
| Permissions       | `any`         |
| CRON              | `0 1 * * *`   |
| Timeout (Seconds) | 900           |

## 🔒 Environment Variables

### RETENTION_PERIOD_DAYS

The number of days you want to retain a file.

| Question     | Answer |
| ------------ | ------ |
| Required     | Yes    |
| Sample Value | `1`    |

### APPWRITE_API_KEY

API Key to talk to Appwrite backend APIs.

| Question      | Answer                                                                                             |
| ------------- | -------------------------------------------------------------------------------------------------- |
| Required      | Yes                                                                                                |
| Sample Value  | `d1efb...aec35`                                                                                    |
| Documentation | [Appwrite: Getting Started for Server](https://appwrite.io/docs/getting-started-for-server#apiKey) |

### APPWRITE_ENDPOINT

The URL endpoint of the Appwrite server. If not provided, it defaults to the Appwrite Cloud server: `https://cloud.appwrite.io/v1`.

| Question     | Answer                         |
| ------------ | ------------------------------ |
| Required     | No                             |
| Sample Value | `https://cloud.appwrite.io/v1` |
