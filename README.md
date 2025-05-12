# Open-trail-cam-
Multispectral wildlife Cam 
# OpenTrailCam  
**An open-source wildlife camera with EMF/thermal anomaly detection.**  

![TrailCam Image](images/trailcam_proto.jpg) *[Show only exterior—no PCB close-ups]*  

## **Key Features**  
- **Multispectral Imaging:** FLIR Lepton (thermal) + Sony IMX487 (UV)  
- **EMF "Disturbance" Detection:** TriField-compatible 3-axis sensor  
- **Low False Positives:** Triggers only on EMF+thermal/UV mismatches  
- **Open Hardware:** Schematics, 3D models, and basic firmware  

---

## **Sanitized Block Diagram**  
```plaintext  
[PIR Motion Sensor] → [Trigger Logic]  
                          ↓  
[FLIR Lepton 3.5] → [FPGA Cross-Check] → [MicroSD]  
[IMX487 (UV)]    →            ↑  
[TriField EMF]   → [Artix-7 FPGA]
