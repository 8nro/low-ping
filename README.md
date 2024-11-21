<h3>Decrease Ping on Roblox (PC)</h3>

<ol>
<li>Go to <code>Device Manager > Network adapters > Your Network Controller > Power Management</code> and turn everything off.</li>
<li>Go to the <code>Advanced</code> tab and copy the following settings to the best of your ability:</li>
<br>
<pre>
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
</pre>
<h6>If anything says that "the number is too high" or the numbers listed are too high, just pick the largest number possible in the settings.</h6>

<li>Download and install <a href="https://bloxstraplabs.com/">Bloxstrap</a>.</li>
<li>Go to <code>Bloxstrap > Engine Settings > Fast Flag Editor</code> and click <code>Add new</code>.</li>
<li>In the <code>Add Fast Flag</code> menu, click <code>Import JSON</code> and import the following data:</li>
<br>
<pre>
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
</pre>

<li>Click <code>Save</code> and close Bloxstrap.</li>
<li>Go to <code>Windows Defender Firewall with Advanced Security > Inbound Rules</code>.</li>
<li>Right-click <code>Inbound Rules</code> and click <code>New Rule...</code>.</li>
<li>Select the following options:</li>
<br>
<pre>
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
</pre>

<li>Enjoy your low ping!</li>
</ol>

<p>If you have any questions, feel free to ask me.</p>
