1. Create domain in **panel**
2. Add **ssl** for that domain in **panel**
3. Add **nat and rule** in **pfsense** in order to route request to **kong**
4. Add **gateway services** in **kong**
5. Add **cert key** from that domain to **kong** and add **pem key** from that domain to **kong certificates** 
6. Add **sni** for that **certificates** in **kong sni**
7. Add **route** for that **domain** in **kong Routes**