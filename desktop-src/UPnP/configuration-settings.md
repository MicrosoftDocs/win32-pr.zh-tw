---
title: 組態設定
description: 您可以藉由變更登錄中的設定來修改控制點 API 和裝置主機 API 的行為。
ms.assetid: 81893cde-d28f-41ec-a6c1-159b3eb84274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68438f6eb425da253aa7f59af3b7d060bacacadb865d4546ddbc0f37fecd9ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008108"
---
# <a name="configuration-settings"></a>組態設定

您可以藉由變更登錄中的設定來修改 [控制點 API](control-point-api.md) 和 [裝置主機 API](device-host-api.md) 的行為。

有七個會影響行為的登錄值：

-   **DownloadScope**
-   **DeviceLifeTime**
-   \\**UPnP 裝置主機** \\檔案 **大小限制**
-   \\**Windows** \\**CurrentVersion** \\**UPnP** \\檔案 **大小限制**
-   **MaxCache**
-   **TTL**
-   **ReceiveScope**

有兩個登錄值（稱為檔案 **大小限制**），一個用於描述檔，另一個則用於使用簡單物件存取通訊協定 (SOAP) 的回應。

登錄中每個值的位置如下所示：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         UPnPControl Point
            DownloadScope
         UPnP Device Host
            Devices
               DeviceLifeTime
            File Size Limit
         Windows
            CurrentVersion
               UPnP
                  File Size Limit
   SYSTEM
      CurentControlSet
         Services
            SSDPSRV
               Parameters
                  MaxCache
                  TTL
                  ReceiveScope
```

## <a name="registry-value-descriptions"></a>登錄值描述

下列清單將說明登錄值。 每個登錄值都是 **REG \_ DWORD** (32 位整數) 。 每個值的作用都是全域的。

<dl> <dt>

<span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**
</dt> <dd>

指定適用于裝置描述檔 URL 的 IP 位址。 如果描述檔 URL 中所指定主機的 IP 位址不在 **DownloadScope** 指定的範圍內，則該 ip 位址無效，且不會建立裝置物件。

有效的值如下表所示。 預設值為 1。



| **DownloadScope** 的值 | 意義                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                          | 主機的 IP 位址必須是子網位址。                                                                                                                                                                |
| 1                          | 主機的 IP 位址必須是子網位址或私用位址，也就是其中一個10。*x*。*x*。*x*、192.168。*x*。*x*、172.16。*x*。*x* (，如 RFC 1918) 或169.254 所指定。*x*。*x* (，如 RFC 3330) 所指定。 |
| 2                          | 主機的 IP 位址必須是子網位址、私人位址，或是來自控制點的存留時間 (TTL) 躍點內的位址。                                                              |
| 3                          | 主機的 IP 位址可以是任何位址。                                                                                                                                                                      |
| >3                      | 與值0相同。                                                                                                                                                                              |



 

</dd> <dt>

<span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**
</dt> <dd>

選擇性。 指定裝置的存留期（以秒為單位），以覆寫裝置公告訊息中提供的值。 如果有 **DeviceLifeTime** ，則會忽略裝置宣告中指定的值，而改為使用登錄值。 這適用于所有裝置。

有效的值範圍從900到 **最大的 \_ DWORD**。 預設值是 1800秒。 如果 **DeviceLifeTime** 設為0，則會使用預設值。

</dd> <dt>

<span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**UPnP 裝置主機** \\檔案 **大小限制**
</dt> <dd>

指定每個描述檔的大小上限（以位元組為單位）。 這項設定無法在 Windows XP Service Pack 2 之前的 Windows 版本中進行設定。 在先前的版本中，此設定是硬式編碼為102400。

有效的值範圍從10240到 **最大的 \_ DWORD**。 預設值為102400。

</dd> <dt>

<span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows** \\**CurrentVersion** \\**UPnP** \\檔案 **大小限制**
</dt> <dd>

指定可接受之 SOAP 回應的大小上限（以位元組為單位）。 這項設定無法在 Windows XP Service Pack 2 之前的 Windows 版本中進行設定。 在先前的版本中，此設定是硬式編碼為102400。

有效的值範圍從10240到 **最大的 \_ DWORD**。 預設值為102400。

</dd> <dt>

<span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**
</dt> <dd>

指定簡易服務探索通訊協定中允許的最大專案數 (SSDP) 快取。

有效的值範圍從10到30000。 預設值為 1000。

</dd> <dt>

<span id="TTL"></span><span id="ttl"></span>**TTL**
</dt> <dd>

指定 SSDP 封包的存留時間。 亦即， **TTL** 會指定封包允許的躍點數目。

有效的值範圍從1到255。 預設值為 1。

</dd> <dt>

<span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**
</dt> <dd>

指定哪些 IP 位址是訊息的有效來源。 如果傳入訊息源自于 **ReceiveScope** 所指定之範圍內的位址，則會忽略該訊息。 這項設定無法在 Windows XP Service Pack 2 之前的 Windows 版本中進行設定。 在先前的版本中，會接受訊息，而不考慮其來源。

有效的值如下表所示。 預設值為 1。



| **ReceiveScope** 的值 | 意義                                                                                                                                                                                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                         | 寄件者的 IP 位址必須是子網位址。                                                                                                                                                                |
| 1                         | 寄件者的 IP 位址必須是子網位址或私用位址，也就是其中一個10。*x*。*x*。*x*、192.168。*x*。*x*、172.16。*x*。*x* (，如 RFC 1918) 或169.254 所指定。*x*。*x* (，如 RFC 3330) 所指定。 |
| 2                         | 未使用。 如果 **ReceiveScope** 設定為2，則會使用預設值。                                                                                                                                        |
| 3                         | 寄件者的 IP 位址可以是任何位址。                                                                                                                                                                      |



 

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[UPnP 架構總覽](overview-of-universal-plug-and-play.md)
</dt> </dl>

 

 




