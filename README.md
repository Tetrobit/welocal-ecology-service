# WeLocal Ecology Service

Environmental monitoring and management service for the WeLocal platform, built with Node.js and Express.

## Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: PostgreSQL
- **Authentication**: JWT (JSON Web Tokens)
- **API Documentation**: Swagger/OpenAPI
- **Testing**: Jest
- **Logging**: Winston
- **Validation**: Joi
- **ORM**: TypeORM
- **File Storage**: AWS S3
- **Maps Integration**: OpenStreetMap API

## Features

- Environmental data collection and monitoring
- Pollution level tracking
- Waste management system
- Green initiatives management
- Environmental reports generation
- Map-based visualization
- File upload for environmental documents
- Real-time alerts and notifications
- Environmental impact assessment
- Community engagement features

## Prerequisites

- Node.js (v18 or higher)
- PostgreSQL
- npm or yarn
- AWS S3 bucket (for file storage)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-org/welocal-ecology-service.git
   cd welocal-ecology-service
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Create environment file:
   ```bash
   cp .env.example .env
   ```

4. Configure environment variables in `.env`:
   ```env
   NODE_ENV=development
   PORT=8081
   DATABASE_URL=postgresql://welocal:welocal123@localhost:5432/welocal
   AWS_ACCESS_KEY_ID=your-aws-access-key
   AWS_SECRET_ACCESS_KEY=your-aws-secret-key
   AWS_REGION=your-aws-region
   AWS_S3_BUCKET=your-s3-bucket
   OPENSTREETMAP_API_KEY=your-api-key
   ```

## Running the Service

### Development Mode
```bash
npm run dev
# or
yarn dev
```

### Production Mode
```bash
npm run build
npm start
# or
yarn build
yarn start
```

### Docker
```bash
docker build -t welocal-ecology-service .
docker run -p 8081:8081 welocal-ecology-service
```

## API Endpoints

### Environmental Data
- `GET /api/v1/environment/data` - Get environmental data
- `POST /api/v1/environment/data` - Submit environmental data
- `GET /api/v1/environment/reports` - Get environmental reports
- `POST /api/v1/environment/reports` - Create environmental report

### Pollution Monitoring
- `GET /api/v1/pollution/levels` - Get pollution levels
- `POST /api/v1/pollution/alert` - Create pollution alert
- `GET /api/v1/pollution/history` - Get pollution history

### Waste Management
- `GET /api/v1/waste/collection-points` - Get waste collection points
- `POST /api/v1/waste/collection-request` - Request waste collection
- `GET /api/v1/waste/schedule` - Get collection schedule

### Green Initiatives
- `GET /api/v1/initiatives` - Get green initiatives
- `POST /api/v1/initiatives` - Create green initiative
- `PUT /api/v1/initiatives/:id` - Update initiative status

## API Documentation

API documentation is available at `/api-docs` when running the service.

## Testing

### Unit Tests
```bash
npm run test
# or
yarn test
```

### Integration Tests
```bash
npm run test:integration
# or
yarn test:integration
```

### E2E Tests
```bash
npm run test:e2e
# or
yarn test:e2e
```

## Project Structure

```
src/
├── config/           # Configuration files
├── controllers/      # Route controllers
├── middleware/       # Custom middleware
├── models/          # Database models
├── routes/          # API routes
├── services/        # Business logic
├── utils/           # Utility functions
├── validators/      # Request validation
├── maps/            # Maps integration
├── storage/         # File storage handling
└── app.js           # Application entry point
```

## Security Features

- JWT token-based authentication
- Rate limiting
- CORS configuration
- Helmet security headers
- Input validation
- SQL injection prevention
- XSS protection
- File upload validation
- Secure file storage

## Monitoring

The service exposes the following endpoints for monitoring:
- `/health` - Health check
- `/metrics` - Prometheus metrics
- `/status` - Service status

## Logging

Logs are written to:
- Console (development)
- File (production)

Log levels:
- ERROR
- WARN
- INFO
- DEBUG

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

[Your License Here]

## Support

For support, please contact [Your Contact Information] 