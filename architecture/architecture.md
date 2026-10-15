# Expense Tracker — Three-Tier Architecture

## Request Flow
Browser → Nginx Load Balancer → Nginx Frontend → Node.js Backend → MySQL Database

## Components
1. Load Balancer: Nginx on EC2, listens on port 80.
2. Frontend: Nginx serves HTML, CSS, and JavaScript.
3. Backend: Node.js 24 provides REST APIs on port 8080.
4. Database: MySQL 8 stores expense transactions on port 3306.

## Security
- Public traffic enters through the load balancer.
- The frontend accepts traffic from the load balancer.
- The backend accepts traffic from the frontend.
- MySQL accepts traffic from the backend only.

## Important
This project uses four EC2 instances: one each for the load balancer, frontend, backend, and database.
EOFmkdir -p architecture

cat > architecture/architecture.md <<'EOF'
# Expense Tracker — Three-Tier Architecture

## Request Flow
Browser → Nginx Load Balancer → Nginx Frontend → Node.js Backend → MySQL Database

## Components
1. Load Balancer: Nginx on EC2, listens on port 80.
2. Frontend: Nginx serves HTML, CSS, and JavaScript.
3. Backend: Node.js 24 provides REST APIs on port 8080.
4. Database: MySQL 8 stores expense transactions on port 3306.

## Security
- Public traffic enters through the load balancer.
- The frontend accepts traffic from the load balancer.
- The backend accepts traffic from the frontend.
- MySQL accepts traffic from the backend only.

## Important
This project uses four EC2 instances: one each for the load balancer, frontend, backend, and database.
