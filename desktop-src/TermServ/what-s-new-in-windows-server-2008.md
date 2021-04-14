---
title: Windows Server 2008 的新功能
description: Windows Server 2008 為終端機服務引進了下列新的程式設計項目。
ms.assetid: a2299b03-5e06-4984-a33f-b44c7cded513
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab74f22c41fa88147a1ef30a8f55f158e34990c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104383066"
---
# <a name="whats-new-in-windows-server-2008"></a>Windows Server 2008 的新功能

Windows Server 2008 為終端機服務引進了下列新的程式設計項目。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>程式設計元素</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>動態虛擬通道參考<br/></td>
<td>動態虛擬通道 (DVC) Api 擴充終端機服務的現有虛擬通道 Api，稱為靜態虛擬通道 (SVC) Api。<br/>
<ul>
<li><a href="dynamic-virtual-channels.md">動態虛擬通道</a></li>
<li><a href="dynamic-virtual-channels-reference.md">動態虛擬通道參考</a></li>
</ul></td>
</tr>
<tr class="even">
<td>遠端桌面網頁連線參考<br/></td>
<td>下列介面 (以及其相關聯的方法和屬性) 已加入 <a href="remote-desktop-web-connection-reference.md">遠端桌面網頁連線參考</a>中：<br/>
<ul>
<li><a href="imsrdpclient5.md"><strong>IMsRdpClient5 介面</strong></a></li>
<li><a href="imsrdpclient6.md"><strong>IMsRdpClient6 介面</strong></a></li>
<li><a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5 介面</strong></a></li>
<li><a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6 介面</strong></a></li>
<li><a href="imsrdpclientnonscriptable3.md"><strong>IMsRdpClientNonScriptable3 介面</strong></a></li>
<li><a href="imsrdpclientshell.md"><strong>IMsRdpClientShell 介面</strong></a></li>
<li><a href="imsrdpclienttransportsettings.md"><strong>IMsRdpClientTransportSettings 介面</strong></a></li>
<li><a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2 介面</strong></a></li>
<li><a href="imsrdpdevice.md"><strong>IMsRdpDevice 介面</strong></a></li>
<li><a href="imsrdpdevicecollection.md"><strong>IMsRdpDeviceCollection 介面</strong></a></li>
<li><a href="imsrdpdrive.md"><strong>IMsRdpDrive 介面</strong></a></li>
<li><a href="imsrdpdrivecollection.md"><strong>IMsRdpDriveCollection 介面</strong></a></li>
<li><a href="itsremoteprogram.md"><strong>ITSRemoteProgram 介面</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>終端機服務 API 參考<br/></td>
<td>下列功能已新增至 <a href="terminal-services-api-reference.md">終端機服務 API 參考</a>：<br/>
<ul>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona"><strong>WTSConnectSession 函式</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex"><strong>WTSRegisterSessionNotificationEx 函式</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona"><strong>WTSStartRemoteControlSession 函式</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession"><strong>WTSStopRemoteControlSession 函式</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex"><strong>WTSUnRegisterSessionNotificationEx 函式</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex"><strong>WTSVirtualChannelOpenEx 函式</strong></a></li>
</ul>
已新增下列結構：<br/>
<ul>
<li><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta"><strong>WTSCLIENT 結構</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa"><strong>WTSINFO 結構</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>終端機服務 WMI 提供者<br/></td>
<td>下列類別和方法已新增至終端機 <a href="terminal-services-wmi-provider.md">服務 WMI 提供者</a>。<br/>
<ul>
<li><a href="terminal-services-gateway-classes.md">終端機服務閘道類別 (和相關聯的方法) </a></li>
<li><a href="terminal-services-license-server-classes.md">終端機服務授權伺服器類別 (和相關聯的方法) </a></li>
<li><a href="terminal-services-remoteapp-classes.md">RemoteApp 類別 (和相關聯的方法) </a></li>
<li><a href="win32-tsdiscoveredlicenseserver.md"><strong>Win32_TSDiscoveredLicenseServer 類別</strong></a></li>
<li><a href="create-win32-terminal.md"><strong>Win32_Terminal 類別的 Create 方法</strong></a></li>
<li><a href="delete-win32-terminal.md"><strong>Win32_Terminal 類別的 Delete 方法</strong></a></li>
<li><a href="canaccesslicenseserver-win32-terminalservicesetting.md"><strong>Win32_TerminalServiceSetting 類別的 CanAccessLicenseServer 方法</strong></a></li>
<li><a href="findlicenseservers-win32-terminalservicesetting.md"><strong>Win32_TerminalServiceSetting 類別的 FindLicenseServers 方法</strong></a></li>
<li><a href="getdomain-win32-terminalservicesetting.md"><strong>Win32_TerminalServiceSetting 類別的 GetDomain 方法</strong></a></li>
<li><a href="getgraceperioddays-win32-terminalservicesetting.md"><strong>Win32_TerminalServiceSetting 類別的 GetGracePeriodDays 方法</strong></a></li>
<li><a href="getwinstationdrivernames-win32-terminalservicesetting.md"><strong>Win32_TerminalServiceSetting 類別的 GetWinstationDriverNames 方法</strong></a></li>
<li><a href="pinglicenseserver-win32-terminalservicesetting.md"><strong>Win32_TerminalServiceSetting 類別的 PingLicenseServer 方法</strong></a></li>
<li><a href="updatedirectconnectlicenseserver-win32-terminalservicesetting.md"><strong>Win32_TerminalServiceSetting 類別的 UpdateDirectConnectLicenseServer 方法</strong></a></li>
<li><a href="setuserauthenticationrequired-win32-tsgeneralsetting.md"><strong>Win32_TSGeneralSetting 類別的 SetUserAuthenticationRequired 方法</strong></a></li>
<li><a href="getcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>Win32_TSSessionDirectory 類別的 GetCurrentRedirectableAddresses 方法</strong></a></li>
<li><a href="setcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>Win32_TSSessionDirectory 類別的 SetCurrentRedirectableAddresses 方法</strong></a></li>
<li><a href="getredirectableaddresses-win32-tssessiondirectory.md"><strong>Win32_TSSessionDirectory 類別的 GetRedirectableAddresses 方法</strong></a></li>
<li><a href="pingsessiondirectory-win32-tssessiondirectory.md"><strong>Win32_TSSessionDirectory 類別的 PingSessionDirectory 方法</strong></a></li>
<li><a href="setloadbalancingstate-win32-tssessiondirectory.md"><strong>Win32_TSSessionDirectory 類別的 SetLoadBalancingState 方法</strong></a></li>
<li><a href="setserverweight-win32-tssessiondirectory.md"><strong>Win32_TSSessionDirectory 類別的 SetServerWeight 方法</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>終端機服務會話代理人外掛程式參考<br/></td>
<td>終端機服務會話代理人 (TS 會話代理人) 外掛程式用來擴充 TS 會話代理人的功能。<br/>
<ul>
<li><a href="/windows/desktop/TermServ/terminal-services-virtualization-api-reference">終端機服務會話代理人外掛程式參考</a></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

