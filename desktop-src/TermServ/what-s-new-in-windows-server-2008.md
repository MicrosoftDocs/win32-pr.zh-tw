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
# <a name="whats-new-in-windows-server-2008"></a><span data-ttu-id="653c0-103">Windows Server 2008 的新功能</span><span class="sxs-lookup"><span data-stu-id="653c0-103">What's New in Windows Server 2008</span></span>

<span data-ttu-id="653c0-104">Windows Server 2008 為終端機服務引進了下列新的程式設計項目。</span><span class="sxs-lookup"><span data-stu-id="653c0-104">Windows Server 2008 introduces the following new programming elements for Terminal Services.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="653c0-105">程式設計元素</span><span class="sxs-lookup"><span data-stu-id="653c0-105">Programming element</span></span></th>
<th><span data-ttu-id="653c0-106">Description</span><span class="sxs-lookup"><span data-stu-id="653c0-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="653c0-107">動態虛擬通道參考</span><span class="sxs-lookup"><span data-stu-id="653c0-107">Dynamic Virtual Channels Reference</span></span><br/></td>
<td><span data-ttu-id="653c0-108">動態虛擬通道 (DVC) Api 擴充終端機服務的現有虛擬通道 Api，稱為靜態虛擬通道 (SVC) Api。</span><span class="sxs-lookup"><span data-stu-id="653c0-108">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Terminal Services, known as static virtual channel (SVC) APIs.</span></span><br/>
<ul>
<li><span data-ttu-id="653c0-109"><a href="dynamic-virtual-channels.md">動態虛擬通道</a></span><span class="sxs-lookup"><span data-stu-id="653c0-109"><a href="dynamic-virtual-channels.md">Dynamic Virtual Channels</a></span></span></li>
<li><span data-ttu-id="653c0-110"><a href="dynamic-virtual-channels-reference.md">動態虛擬通道參考</a></span><span class="sxs-lookup"><span data-stu-id="653c0-110"><a href="dynamic-virtual-channels-reference.md">Dynamic Virtual Channels Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="653c0-111">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="653c0-111">Remote Desktop Web Connection Reference</span></span><br/></td>
<td><span data-ttu-id="653c0-112">下列介面 (以及其相關聯的方法和屬性) 已加入 <a href="remote-desktop-web-connection-reference.md">遠端桌面網頁連線參考</a>中：</span><span class="sxs-lookup"><span data-stu-id="653c0-112">The following interfaces (and their associated methods and properties) were added to <a href="remote-desktop-web-connection-reference.md">Remote Desktop Web Connection Reference</a>:</span></span><br/>
<ul>
<li><span data-ttu-id="653c0-113"><a href="imsrdpclient5.md"><strong>IMsRdpClient5 介面</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-113"><a href="imsrdpclient5.md"><strong>IMsRdpClient5 Interface</strong></a></span></span></li>
<li><span data-ttu-id="653c0-114"><a href="imsrdpclient6.md"><strong>IMsRdpClient6 介面</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-114"><a href="imsrdpclient6.md"><strong>IMsRdpClient6 Interface</strong></a></span></span></li>
<li><span data-ttu-id="653c0-115"><a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5 介面</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-115"><a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5 Interface</strong></a></span></span></li>
<li><span data-ttu-id="653c0-116"><a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6 介面</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-116"><a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6 Interface</strong></a></span></span></li>
<li><span data-ttu-id="653c0-117"><a href="imsrdpclientnonscriptable3.md"><strong>IMsRdpClientNonScriptable3 介面</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-117"><a href="imsrdpclientnonscriptable3.md"><strong>IMsRdpClientNonScriptable3 Interface</strong></a></span></span></li>
<li><span data-ttu-id="653c0-118"><a href="imsrdpclientshell.md"><strong>IMsRdpClientShell 介面</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-118"><a href="imsrdpclientshell.md"><strong>IMsRdpClientShell Interface</strong></a></span></span></li>
<li><span data-ttu-id="653c0-119"><a href="imsrdpclienttransportsettings.md"><strong>IMsRdpClientTransportSettings 介面</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-119"><a href="imsrdpclienttransportsettings.md"><strong>IMsRdpClientTransportSettings Interface</strong></a></span></span></li>
<li><span data-ttu-id="653c0-120"><a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2 介面</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-120"><a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2 Interface</strong></a></span></span></li>
<li><span data-ttu-id="653c0-121"><a href="imsrdpdevice.md"><strong>IMsRdpDevice 介面</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-121"><a href="imsrdpdevice.md"><strong>IMsRdpDevice Interface</strong></a></span></span></li>
<li><span data-ttu-id="653c0-122"><a href="imsrdpdevicecollection.md"><strong>IMsRdpDeviceCollection 介面</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-122"><a href="imsrdpdevicecollection.md"><strong>IMsRdpDeviceCollection Interface</strong></a></span></span></li>
<li><span data-ttu-id="653c0-123"><a href="imsrdpdrive.md"><strong>IMsRdpDrive 介面</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-123"><a href="imsrdpdrive.md"><strong>IMsRdpDrive Interface</strong></a></span></span></li>
<li><span data-ttu-id="653c0-124"><a href="imsrdpdrivecollection.md"><strong>IMsRdpDriveCollection 介面</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-124"><a href="imsrdpdrivecollection.md"><strong>IMsRdpDriveCollection Interface</strong></a></span></span></li>
<li><span data-ttu-id="653c0-125"><a href="itsremoteprogram.md"><strong>ITSRemoteProgram 介面</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-125"><a href="itsremoteprogram.md"><strong>ITSRemoteProgram Interface</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="653c0-126">終端機服務 API 參考</span><span class="sxs-lookup"><span data-stu-id="653c0-126">Terminal Services API Reference</span></span><br/></td>
<td><span data-ttu-id="653c0-127">下列功能已新增至 <a href="terminal-services-api-reference.md">終端機服務 API 參考</a>：</span><span class="sxs-lookup"><span data-stu-id="653c0-127">The following functions were added to <a href="terminal-services-api-reference.md">Terminal Services API Reference</a>:</span></span><br/>
<ul>
<li><span data-ttu-id="653c0-128"><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona"><strong>WTSConnectSession 函式</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-128"><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona"><strong>WTSConnectSession Function</strong></a></span></span></li>
<li><span data-ttu-id="653c0-129"><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex"><strong>WTSRegisterSessionNotificationEx 函式</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-129"><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex"><strong>WTSRegisterSessionNotificationEx Function</strong></a></span></span></li>
<li><span data-ttu-id="653c0-130"><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona"><strong>WTSStartRemoteControlSession 函式</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-130"><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona"><strong>WTSStartRemoteControlSession Function</strong></a></span></span></li>
<li><span data-ttu-id="653c0-131"><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession"><strong>WTSStopRemoteControlSession 函式</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-131"><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession"><strong>WTSStopRemoteControlSession Function</strong></a></span></span></li>
<li><span data-ttu-id="653c0-132"><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex"><strong>WTSUnRegisterSessionNotificationEx 函式</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-132"><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex"><strong>WTSUnRegisterSessionNotificationEx Function</strong></a></span></span></li>
<li><span data-ttu-id="653c0-133"><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex"><strong>WTSVirtualChannelOpenEx 函式</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-133"><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex"><strong>WTSVirtualChannelOpenEx Function</strong></a></span></span></li>
</ul>
<span data-ttu-id="653c0-134">已新增下列結構：</span><span class="sxs-lookup"><span data-stu-id="653c0-134">The following structures were added:</span></span><br/>
<ul>
<li><span data-ttu-id="653c0-135"><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta"><strong>WTSCLIENT 結構</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-135"><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta"><strong>WTSCLIENT Structure</strong></a></span></span></li>
<li><span data-ttu-id="653c0-136"><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa"><strong>WTSINFO 結構</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-136"><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa"><strong>WTSINFO Structure</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="653c0-137">終端機服務 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="653c0-137">Terminal Services WMI Provider</span></span><br/></td>
<td><span data-ttu-id="653c0-138">下列類別和方法已新增至終端機 <a href="terminal-services-wmi-provider.md">服務 WMI 提供者</a>。</span><span class="sxs-lookup"><span data-stu-id="653c0-138">The following classes and methods were added to the <a href="terminal-services-wmi-provider.md">Terminal Services WMI Provider</a>.</span></span><br/>
<ul>
<li><span data-ttu-id="653c0-139"><a href="terminal-services-gateway-classes.md">終端機服務閘道類別 (和相關聯的方法) </a></span><span class="sxs-lookup"><span data-stu-id="653c0-139"><a href="terminal-services-gateway-classes.md">Terminal Services Gateway Classes (and associated methods)</a></span></span></li>
<li><span data-ttu-id="653c0-140"><a href="terminal-services-license-server-classes.md">終端機服務授權伺服器類別 (和相關聯的方法) </a></span><span class="sxs-lookup"><span data-stu-id="653c0-140"><a href="terminal-services-license-server-classes.md">Terminal Services License Server Classes (and associated methods)</a></span></span></li>
<li><span data-ttu-id="653c0-141"><a href="terminal-services-remoteapp-classes.md">RemoteApp 類別 (和相關聯的方法) </a></span><span class="sxs-lookup"><span data-stu-id="653c0-141"><a href="terminal-services-remoteapp-classes.md">RemoteApp Classes (and associated methods)</a></span></span></li>
<li><span data-ttu-id="653c0-142"><a href="win32-tsdiscoveredlicenseserver.md"><strong>Win32_TSDiscoveredLicenseServer 類別</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-142"><a href="win32-tsdiscoveredlicenseserver.md"><strong>Win32_TSDiscoveredLicenseServer Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-143"><a href="create-win32-terminal.md"><strong>Win32_Terminal 類別的 Create 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-143"><a href="create-win32-terminal.md"><strong>Create Method of the Win32_Terminal Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-144"><a href="delete-win32-terminal.md"><strong>Win32_Terminal 類別的 Delete 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-144"><a href="delete-win32-terminal.md"><strong>Delete Method of the Win32_Terminal Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-145"><a href="canaccesslicenseserver-win32-terminalservicesetting.md"><strong>Win32_TerminalServiceSetting 類別的 CanAccessLicenseServer 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-145"><a href="canaccesslicenseserver-win32-terminalservicesetting.md"><strong>CanAccessLicenseServer Method of the Win32_TerminalServiceSetting Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-146"><a href="findlicenseservers-win32-terminalservicesetting.md"><strong>Win32_TerminalServiceSetting 類別的 FindLicenseServers 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-146"><a href="findlicenseservers-win32-terminalservicesetting.md"><strong>FindLicenseServers Method of the Win32_TerminalServiceSetting Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-147"><a href="getdomain-win32-terminalservicesetting.md"><strong>Win32_TerminalServiceSetting 類別的 GetDomain 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-147"><a href="getdomain-win32-terminalservicesetting.md"><strong>GetDomain Method of the Win32_TerminalServiceSetting Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-148"><a href="getgraceperioddays-win32-terminalservicesetting.md"><strong>Win32_TerminalServiceSetting 類別的 GetGracePeriodDays 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-148"><a href="getgraceperioddays-win32-terminalservicesetting.md"><strong>GetGracePeriodDays Method of the Win32_TerminalServiceSetting Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-149"><a href="getwinstationdrivernames-win32-terminalservicesetting.md"><strong>Win32_TerminalServiceSetting 類別的 GetWinstationDriverNames 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-149"><a href="getwinstationdrivernames-win32-terminalservicesetting.md"><strong>GetWinstationDriverNames Method of the Win32_TerminalServiceSetting Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-150"><a href="pinglicenseserver-win32-terminalservicesetting.md"><strong>Win32_TerminalServiceSetting 類別的 PingLicenseServer 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-150"><a href="pinglicenseserver-win32-terminalservicesetting.md"><strong>PingLicenseServer Method of the Win32_TerminalServiceSetting Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-151"><a href="updatedirectconnectlicenseserver-win32-terminalservicesetting.md"><strong>Win32_TerminalServiceSetting 類別的 UpdateDirectConnectLicenseServer 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-151"><a href="updatedirectconnectlicenseserver-win32-terminalservicesetting.md"><strong>UpdateDirectConnectLicenseServer Method of the Win32_TerminalServiceSetting Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-152"><a href="setuserauthenticationrequired-win32-tsgeneralsetting.md"><strong>Win32_TSGeneralSetting 類別的 SetUserAuthenticationRequired 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-152"><a href="setuserauthenticationrequired-win32-tsgeneralsetting.md"><strong>SetUserAuthenticationRequired Method of the Win32_TSGeneralSetting Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-153"><a href="getcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>Win32_TSSessionDirectory 類別的 GetCurrentRedirectableAddresses 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-153"><a href="getcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>GetCurrentRedirectableAddresses Method of the Win32_TSSessionDirectory Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-154"><a href="setcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>Win32_TSSessionDirectory 類別的 SetCurrentRedirectableAddresses 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-154"><a href="setcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>SetCurrentRedirectableAddresses Method of the Win32_TSSessionDirectory Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-155"><a href="getredirectableaddresses-win32-tssessiondirectory.md"><strong>Win32_TSSessionDirectory 類別的 GetRedirectableAddresses 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-155"><a href="getredirectableaddresses-win32-tssessiondirectory.md"><strong>GetRedirectableAddresses Method of the Win32_TSSessionDirectory Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-156"><a href="pingsessiondirectory-win32-tssessiondirectory.md"><strong>Win32_TSSessionDirectory 類別的 PingSessionDirectory 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-156"><a href="pingsessiondirectory-win32-tssessiondirectory.md"><strong>PingSessionDirectory Method of the Win32_TSSessionDirectory Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-157"><a href="setloadbalancingstate-win32-tssessiondirectory.md"><strong>Win32_TSSessionDirectory 類別的 SetLoadBalancingState 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-157"><a href="setloadbalancingstate-win32-tssessiondirectory.md"><strong>SetLoadBalancingState Method of the Win32_TSSessionDirectory Class</strong></a></span></span></li>
<li><span data-ttu-id="653c0-158"><a href="setserverweight-win32-tssessiondirectory.md"><strong>Win32_TSSessionDirectory 類別的 SetServerWeight 方法</strong></a></span><span class="sxs-lookup"><span data-stu-id="653c0-158"><a href="setserverweight-win32-tssessiondirectory.md"><strong>SetServerWeight Method of the Win32_TSSessionDirectory Class</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="653c0-159">終端機服務會話代理人外掛程式參考</span><span class="sxs-lookup"><span data-stu-id="653c0-159">Terminal Services Session Broker Plug-in Reference</span></span><br/></td>
<td><span data-ttu-id="653c0-160">終端機服務會話代理人 (TS 會話代理人) 外掛程式用來擴充 TS 會話代理人的功能。</span><span class="sxs-lookup"><span data-stu-id="653c0-160">The Terminal Services Session Broker (TS Session Broker) plug-in is used to extend the capabilities of TS Session Broker.</span></span><br/>
<ul>
<li><span data-ttu-id="653c0-161"><a href="/windows/desktop/TermServ/terminal-services-virtualization-api-reference">終端機服務會話代理人外掛程式參考</a></span><span class="sxs-lookup"><span data-stu-id="653c0-161"><a href="/windows/desktop/TermServ/terminal-services-virtualization-api-reference">Terminal Services Session Broker Plug-in Reference</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

