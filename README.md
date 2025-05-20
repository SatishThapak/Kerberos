# Kerberos Setup & Implementation in Kafka, MariaDB, PostgreSQL, and Kerberos High Availability (HA)
For system administrators, DevOps engineers, or architects setting up secure environments.

# Domain Setup
We’re going to set up an MIT Kerberos domain with the following details (you can modify these to suit your environment):

# Realm: EXAMPLE.COM
# Primary KDC (main server): kdc1.example.com
# Secondary KDC (backup server): kdc2.example.com
# User account (principal): ubuntu
# Admin account (principal): ubuntu/admin

# 🛠️ Prerequisites
Before installing the Kerberos server, ensure the following:

✅ DNS is correctly configured for your domain.
The Kerberos realm typically matches your domain name.
In this example, we use EXAMPLE.COM

✅ System time is synchronized across all hosts.
Kerberos is time-sensitive. If a client’s clock differs from the server’s by more than 5 minutes, authentication will fail.
To prevent this, all machines should use the same NTP (Network Time Protocol) server.
Refer to the NTP section for configuration details.

