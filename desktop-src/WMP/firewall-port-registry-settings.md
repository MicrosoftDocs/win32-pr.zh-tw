---
title: 防火牆埠登錄設定
description: 防火牆埠登錄設定
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player，防火牆埠登錄設定
- Windows Media Player，埠登錄設定
- Windows Media Player，登錄
- 登錄，防火牆通訊埠設定
- 登錄，埠設定
- 登錄，Windows Media Player 的設定
- 防火牆埠登錄設定
- 埠登錄設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140f55a4008a03c2b3bc4184e2eca92129a5e30dc69f0871da856b4555daec73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576765"
---
# <a name="firewall-port-registry-settings"></a>防火牆埠登錄設定

Windows Media Player 將專案放在登錄中，讓防火牆可以決定是否要開啟或關閉媒體媒體櫃共用所使用的埠。

**AcceptedEULA 登錄專案**

Windows Media Player 使用下列登錄專案，指出使用者是否已接受使用者授權合約 (EULA) 。


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



值為1時，表示使用者已接受授權合約。 值為0表示使用者尚未接受授權合約。

**WMPNSSFirewallPortsOpen 登錄專案**

Windows Media Player 使用下列登錄專案，指出使用者是否已選擇與家用網路上的其他電腦共用其媒體媒體櫃。


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



值為1時，表示使用者已選擇要共用程式庫。 值為0表示使用者已選擇不共用程式庫。

**與媒體媒體櫃共用相關的埠**

在 Windows Vista 中，如果 **WMPNSSFirewallPortsOpen** 登錄專案的值為1，則應該開啟下列埠。



| 連接埠          | 通訊協定                  | 處理序                         | 方向            |
|---------------|---------------------------|---------------------------------|----------------------|
| 554           | TCP RTSP                  | wmpnetwk.exe                    | 輸入和輸出 |
| 8554-8558   | TCP RTSP                  | wmpnetwk.exe                    | 輸入和輸出 |
| 5004、5005    | UDP RTCP/RTP              | wmpnetwk.exe                    | 輸入和輸出 |
| 50004-50013 | UDP RTCP/RTP              | wmpnetwk.exe                    | 輸入和輸出 |
| 1900          | UDP SSDP                  | svchost.exe 中的 SSDPsrv          | 輸入和輸出 |
| 2869          | TCP SSDP、UPnP            | svchost.exe 中的 SSDPsrv/UPnPHost | 進入              |
| 10280-10284 | UDP WMDRM-ND 註冊 | wmpnetwk.exe                    | 輸入和輸出 |
| 10243         | TCP HTTP                  | wmpnetwk.exe                    | 進入              |
| 2177          | TCP UDP qWAVE             | svchost.exe                     | 輸入和輸出 |



 

在 Windows Vista 中，如果 **AcceptedEULA** 登錄專案的值為1，則應該開啟下列埠。



| 連接埠          | 通訊協定       | 處理序                         | 方向            |
|---------------|----------------|---------------------------------|----------------------|
| 所有 UDP 埠 | UDP RTP、MSB   | wmplayer.exe，任何子網        | 進入              |
| 1900          | UDP SSDP       | svchost.exe 中的 SSDPsrv/UPnPHost | 輸入和輸出 |
| 2869          | TCP SSDP、UPnP | SSDPsrv，UPnPHost               | 進入              |



 

在 Microsoft Windows XP 上，如果 **WMPNSSFirewallPortsOpen** 登錄專案的值為1，則應該開啟下列埠。



| 連接埠          | 通訊協定                  | 處理序                         | 方向            |
|---------------|---------------------------|---------------------------------|----------------------|
| 1900          | UDP SSDP                  | svchost.exe 中的 SSDPsrv          | 輸入和輸出 |
| 2869          | TCP SSDP、UPnP            | svchost.exe 中的 SSDPsrv/UPnPHost | 進入              |
| 10280-10284 | UDP WMDRM-ND 註冊 | wmpnetwk.exe                    | 輸入和輸出 |
| 10243         | TCP HTTP                  | wmpnetwk.exe                    | 進入              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**登錄設定**](registry-settings.md)
</dt> </dl>

 

 




