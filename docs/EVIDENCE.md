# Evidence register

This gallery contains **19 historical screenshots** from the supplied NET3034 report: setup Figures 1-9 and authentication Figures 60-69. They are historical evidence, not a new test run. Seventeen images are unchanged. In Figures 64 and 65, the cookie header lines are covered with solid black boxes; all pixels outside those boxes are unchanged.

Captions describe the visible content. Some original report captions differ: Figures 4 and 5 show database setup, Figure 9 shows a local Nmap scan, Figure 61 shows a successful response, and Figure 63 shows a failed response. Original figure numbers preserve traceability.

Visible addresses and sample passwords belong to the local training lab. Historical container screenshots show ports bound to all interfaces; use the loopback-only configuration in the [recreation guide](LAB_SETUP.md). A short attempt sequence does not establish the absence of throttling or lockout under every condition.

## Part 1 environment setup

### Figure 1: Docker version on Ubuntu

![Report Figure 1: Docker version on Ubuntu](evidence/docker-version.png)

### Figure 2: Historical container download and startup

![Report Figure 2: Historical container download and startup](evidence/figure-02.png)

### Figure 3: DVWA login page

![Report Figure 3: DVWA login page](evidence/figure-03.png)

### Figure 4: Database setup checks

![Report Figure 4: Database setup checks](evidence/figure-04.png)

### Figure 5: Database setup and module navigation

![Report Figure 5: Database setup and module navigation](evidence/figure-05.png)

### Figure 6: Low security level selected

![Report Figure 6: Low security level selected](evidence/figure-06.png)

### Figure 7: Ubuntu and Docker network interfaces

![Report Figure 7: Ubuntu and Docker network interfaces](evidence/figure-07.png)

### Figure 8: Running container and published ports

![Report Figure 8: Running container and published ports](evidence/figure-08.png)

### Figure 9: Local service verification with Nmap

![Report Figure 9: Local service verification with Nmap](evidence/figure-09.png)

## Authentication assessment

### Figure 60: Failed test login

![Report Figure 60: Failed test login](evidence/failed-login.png)

### Figure 61: Protected-area response in the browser

![Report Figure 61: Protected-area response in the browser](evidence/figure-61.png)

### Figure 62: Browser history of sample login attempts

![Report Figure 62: Browser history of sample login attempts](evidence/figure-62.png)

### Figure 63: Failed login with another sample password

![Report Figure 63: Failed login with another sample password](evidence/figure-63.png)

### Figure 64: Intruder password parameter position

![Report Figure 64: Intruder password parameter position](evidence/figure-64-redacted.png)

Cookie header redacted with a solid black box.

### Figure 65: Intruder training payload list

![Report Figure 65: Intruder training payload list](evidence/figure-65-redacted.png)

Cookie header redacted with a solid black box.

### Figure 66: Intruder results and response-length comparison

![Report Figure 66: Intruder results and response-length comparison](evidence/figure-66.png)

### Figure 67: Protected-area message in the successful response

![Report Figure 67: Protected-area message in the successful response](evidence/figure-67.png)

### Figure 68: Failed response and recorded attempt results

![Report Figure 68: Failed response and recorded attempt results](evidence/figure-68.png)

### Figure 69: Successful login confirmation

![Report Figure 69: Successful login confirmation](evidence/successful-login.png)

## Publication scope

The full report, cover sheet, student identifiers, contribution marks, raw Burp sessions, request exports, VM disks, and database dumps are excluded. Other vulnerability assessments and the network-design section are outside this individual portfolio selection. See the [case study](CASE_STUDY.md) and [contribution statement](../CONTRIBUTIONS.md).
