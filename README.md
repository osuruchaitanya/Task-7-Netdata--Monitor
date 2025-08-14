# Task 7 - Monitor System Resources Using Netdata

## 📌 Objective
Install *Netdata* using Docker and visualize system and application performance metrics in real time.

---

## ⚙ Steps Performed

1. *Installed & Ran Netdata Container*
   ```bash
   docker run -d --name=netdata \
     -p 19999:19999 \
     --cap-add=SYS_PTRACE \
     --security-opt apparmor=unconfined \
     netdata/netdata

2. Verified Running Container

docker ps

Confirmed that the netdata/netdata container was running.


3. Accessed Dashboard

Opened browser and navigated to:

http://localhost:19999

Dashboard successfully displayed real-time metrics.



4. Explored Metrics

CPU usage (per-core load & usage %)

Memory usage (RAM & swap)

Disk I/O (read/write operations)

Network traffic (incoming/outgoing bandwidth)

Docker containers (individual container resource usage)



5. Checked Logs inside Container

docker exec -it netdata bash
cd /var/log/netdata
ls

Found log files like access.log, collector.log, error.log, daemon.log.




---

📷 Deliverable

Screenshot of the Netdata Dashboard with running metrics (attached in this repo).



---

🎯 Outcome

Successfully installed and monitored system resources using Netdata.
Gained experience in:

Setting up monitoring tools via Docker

Viewing real-time performance metrics

Exploring logs for deeper insights
