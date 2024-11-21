### Decrease Ping on Roblox (PC)

1. Go to `Device Manager > Network adapters > Your Network Controller > Power Management` and turn everything off.
2. Go to the `Advanced` tab and copy the following settings to the best of your ability:
```
D = Disabled
E = Enabled

Advanced EEE: D
ARP Offload: D
EEE Max Support Speed: 2.5Gbps Full Duplex
Energy-Efficient Ethernet: D
Flow Control: D
Gigabit Lite: D
Green Ethernet: D
Interrupt Moderation: D
IPv4 Checksum Offload: D
Jumbo Frame: 16128 Bytes
Large Send Offload v2 (IPv4): D
Large Send Offload v2 (IPv6): D
Maximum Number of RSS Queues: D
Network Address: Not Present
NS Offload: D
Power Saving Mode: D
Priority & VLAN: Priority & VLAN Enabled
Receive Buffers: 4096
Receive Side Scaling: D
Shutdown Wake-On-Lan: D
Speed & Duplex: 2.5 Gbps Full Duplex
TCP Checksum Offload (IPv4): D
TCP Checksum Offload (IPv6): D
Transmit Buffers: 4096
UDP Checksum Offload (IPv4): D
UDP Checksum Offload (IPv6): D
VLAN ID: 0
Wake on Magic Packet: D
Wake on pattern match: D
WOL & Shutdown Link Speed: Not Speed Down
```
###### If anything says that "the number is too high" or the numbers listed are too high, just pick the largest number possible in the settings.

3. Download and install [Bloxstap](https://bloxstraplabs.com/).
4. Go to `Bloxstrap > Engine Settings > Fast Flag Editor` and click `Add new`.
5. In the `Add Fast Flag` menu, click `Import JSON` and import the following data:
```json
{
  "FFlagDebugDisableTelemetryEphemeralCounter": "True",
  "FIntRakNetResendBufferArrayLength": "128",
  "DFIntConnectionMTUSize": "900",
  "FFlagDebugGraphicsPreferD3D11": "True",
  "FFlagDebugSkyGray": "True",
  "DFIntRakNetResendRttMultiple": "1",
  "DFFlagTextureQualityOverrideEnabled": "True",
  "FIntFRMMinGrassDistance": "0",
  "DFIntTextureQualityOverride": "3",
  "DFIntDebugFRMQualityLevelOverride": "1",
  "FIntRenderGrassDetailStrands": "0",
  "FFlagFastGPULightCulling3": "True",
  "DFIntRaknetBandwidthPingSendEveryXSeconds": "1",
  "FFlagDebugDisableTelemetryEphemeralStat": "True",
  "FFlagDebugDisableTelemetryEventIngest": "True",
  "FFlagDebugDisableTelemetryPoint": "True",
  "FFlagDebugDisableTelemetryV2Counter": "True",
  "FFlagDebugDisableTelemetryV2Event": "True",
  "FFlagDebugDisableTelemetryV2Stat": "True",
  "FIntRobloxGuiBlurIntensity": "0",
  "FIntFullscreenTitleBarTriggerDelayMillis": "18000000",
  "FFlagDebugGraphicsDisableVulkan": "True",
  "DFIntMaxFrameBufferSize": "4",
  "FFlagDisablePostFx": "True",
  "FIntFRMMaxGrassDistance": "0",
  "FFlagNewLightAttenuation": "True",
  "DFIntClientLightingTechnologyChangedTelemetryHundredthsPercent": "0",
  "FFlagDebugGraphicsDisableVulkan11": "True",
  "FFlagDebugGraphicsDisableOpenGL": "True",
  "FLogNetwork": "7",
  "FFlagHandleAltEnterFullscreenManually": "False"
}
```

6. Click `Save` and close Bloxstrap.
7. Go to `Windows Defender Firewall with Advanced Security > Inbound Rules`.
8. Right-click `Inbound Rules` and click `New Rule...`.
9. Select the following options:
```
What type of rule would you like to create?
Port

Does this apply to TCP or UDP?
UDP

Does this apple to all local ports or specific local ports?
Specific local ports: 49152-65535

What action should be taken when a connection matches the specified conditions?
Allow the connection

Where does this rule apply?
Domain
Private
Public

Name:
Roblox UDP Ports
```

10. Enjoy your low ping!

If you have any questions, feel free to ask me.
