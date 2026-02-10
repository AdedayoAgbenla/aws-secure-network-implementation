<h1>Secure AWS Network Architecture Implementation</h1>
<h3>AWS Enterprise Environment</h3>

<h2>Overview</h2>
<p>
  This repository documents the design and implementation of a secure AWS network architecture where only the public load balancer
  is internet-facing, while application and database resources remain private. The solution was built to tightly control traffic,
  reduce exposure, and support monitoring and incident response in a regulated environment.
</p>

<hr/>

<h2>Key Responsibilities</h2>
<ul>
  <li>Designed and deployed a multi-AZ VPC (10.0.0.0/16) with separate public, private application, and private database subnets</li>
  <li>Configured Internet Gateway and public route tables for internet-facing resources only</li>
  <li>Deployed NAT Gateways per Availability Zone and routed private subnet egress through same-AZ NAT for high availability</li>
  <li>Implemented tiered Security Groups to enforce least-privilege traffic paths (ALB → App → Database)</li>
  <li>Configured Network ACLs for public and private subnets to add subnet-level controls and reduce misconfiguration risk</li>
  <li>Provisioned private EC2 (app tier) and private RDS PostgreSQL (data tier) to validate secure connectivity</li>
  <li>Performed end-to-end testing using AWS Session Manager to confirm private connectivity and block public database access</li>
  <li>Enabled monitoring and governance controls using VPC Flow Logs, AWS Security Hub, and AWS Config</li>
  <li>Documented an incident response approach for exposure detection, containment, and post-incident validation</li>
</ul>

<hr/>

<h2>Tools &amp; Technologies</h2>
<ul>
  <li>Amazon VPC (Subnets, Route Tables, Internet Gateway)</li>
  <li>NAT Gateway</li>
  <li>Security Groups</li>
  <li>Network ACLs (NACLs)</li>
  <li>Elastic Load Balancing (Application Load Balancer)</li>
  <li>Amazon EC2</li>
  <li>Amazon RDS (PostgreSQL)</li>
  <li>AWS Systems Manager (Session Manager)</li>
  <li>VPC Flow Logs</li>
  <li>AWS Security Hub</li>
  <li>AWS Config</li>
  <li>Amazon CloudWatch Logs</li>
</ul>

<hr/>

<h2>Impact</h2>
<ul>
  <li>Reduced attack surface by keeping application and database tiers private</li>
  <li>Enforced controlled traffic flow across tiers using security groups and NACLs</li>
  <li>Improved resilience with multi-AZ design and per-AZ NAT Gateways</li>
  <li>Strengthened visibility through network logging, centralized findings, and configuration tracking</li>
  <li>Validated secure isolation by confirming private app-to-db connectivity and blocking public database access</li>
</ul>

<hr/>

<h2>Author</h2>
<p>
  <strong>Adedayo</strong><br/>
  AWS Cloud Architect | Cloud Security Specialist
</p>

<hr/>

<h2>Disclaimer</h2>
<p>
  All documentation is anonymized and does not contain confidential or proprietary information.
</p>
