---
description: 如果用戶端和主機無法交換中繼資料，則可以將泛型主機和用戶端替換為自訂主機和用戶端，以協助對問題進行疑難排解。
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: 使用泛型主機和用戶端來取得 HTTP 中繼資料 Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10040f4834df1a77115a361d23d82ec3dfcc6c57
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883172"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a>使用泛型主機和用戶端來取得 HTTP 中繼資料 Exchange

如果用戶端和主機無法交換中繼資料，則可以將泛型主機和用戶端替換為自訂主機和用戶端，以協助對問題進行疑難排解。 如果裝置位址或裝置中繼資料未出現在 WSD Debug 用戶端輸出中，則提供的傳輸位址或網路環境可能會造成失敗。 如需泛型主機和用戶端的詳細資訊，請參閱 [調試](debugging-tools.md)程式。

如果已驗證泛型主機和用戶端可以同時完成 WS-Discovery 和 HTTP 中繼資料交換，則可以跳過此診斷程式，並遵循 [使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)的程式，繼續進行疑難排解。

如果主機或用戶端是在電腦上執行的應用程式，則泛型主機或用戶端應該在與實際主機或用戶端相同的安全性內容中執行。 例如，如果實際的主機或用戶端以系統管理員身分執行，則泛型主機或用戶端必須以系統管理員身分執行。 此外，如果主機或用戶端是獨立裝置，則應該由執行泛型主機或用戶端的電腦完全取代為可保證無限制網路存取的安全性內容 (例如，以系統管理員身分執行) 。

**使用泛型主機和用戶端對 HTTP 中繼資料交換進行疑難排解**

1.  開啟命令提示字元視窗。
2.  執行下列命令： **WSDDebug \_host.exe/mode 中繼資料/start**

    > [!Note]  
    > 可能會出現 **Windows 安全性警示**] 對話方塊。 如果是的話，請按一下 [ **解除封鎖** ]，以允許 WSD Debug 主機執行。

     

    此命令會產生類似下列的輸出。 記下裝置識別碼。

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  執行下列命令： **WSDDebug \_client.exe/mode metadata/hello off/resolve** *&lt; id &gt;*。 將 *&lt; 識別碼 &gt;* 取代為步驟2中識別的裝置識別碼。
    > [!Note]  
    > 可能會出現 **Windows 安全性警示**] 對話方塊。 如果是，請按一下 [ **解除封鎖** ]，以允許 WSD Debug 用戶端執行。

     

WSD Debug 用戶端會產生類似下列的輸出。

``` syntax
WSDAPI Debug Client
Copyright (C) Microsoft Corporation 2007.  All rights reserved.
Client ID is urn:uuid:0f571af7-6b0e-4daf-8054-f2233ac27910
Hello mode is disabled
Client metadata>
*****************************************************************************
Add at 02/28/07 15:16:51
+ EPR:
  + Address:                 urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Types:
    (wsdp) https://schemas.xmlsoap.org/ws/2006/02/devprof:Device
+ XAddrs:
  https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Metadata version:          2
+ Instance ID:               1
+ Probe/Resolve tag:         WSDAPI debug_client
+ Remote transport address:  [::1]:3702
+ Local transport address:   ::1
+ Local interface GUID:      42133cd4-6a70-11db-bbc9-806e6f6e6963
Client metadata>
*****************************************************************************
Getting metadata for host at 02/28/07 15:16:51:
+ Endpoint reference:
  + Address:
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
Client metadata>
*****************************************************************************
Metadata for host:
+ Endpoint reference:
  + Address:           urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice
  + Friendly name:
    [no lang]: Debugging Host
  + Firmware version:  1.0
  + Serial number:     00000000
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel
  + Manufacturer:
    [no lang]: Microsoft Corporation
  + Manufacturer URL:  https://www.microsoft.com/
  + Model names:
    [no lang]: Microsoft Debugging Host
  + Model number:      https://www.microsoft.com/
End of metadata
Client metadata>
```

WSD Debug 用戶端可能會在具有許多 DPWS 裝置的網路上產生大量的輸出。 輸出可以重新導向至檔案，以方便分析。 在 WSD Debug Client 提示字元中輸入 **log t** *&lt; 檔案名 &gt;* ，以將輸出重新導向至檔案。 在 WSD Debug 用戶端提示字元中輸入 **log t stop** ，即可停止輸出重新導向。

請記下 (EPR) 位址的端點參考。 此 EPR 位址應符合上述步驟2中識別的裝置識別碼。 此外，請確認 WSD 偵錯工具用戶端已完全列印裝置的中繼資料。 裝置中繼資料的開頭 `Metadata for host` 和結尾是 `End of metadata` 。

如果裝置識別碼和裝置中繼資料正確地出現在 WSD Debug 用戶端輸出中，則應用程式失敗可能與提供的傳輸位址、作業系統或網路環境無關。 使用自訂主機和用戶端來取代一般主機和用戶端，並遵循 [使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)的程式，繼續進行疑難排解。

如果裝置位址和裝置中繼資料未出現在 WSD Debug 用戶端輸出中，則失敗可能會有下列一或多個原因：

-   主機所公告的傳輸位址不正確或格式不正確。 WSD Debug 用戶端會嘗試從 [ProbeMatches](probematches-message.md)或 [ResolveMatches](resolvematches-message.md)訊息的 **XADDRS** 元素所提供的 URL 取得裝置中繼資料。 用於中繼資料交換的 URL 會出現在 WSD Debug 用戶端輸出中，並在前面加上片語 `Using xAddr` 。 下列範例顯示在上述 WSD Debug 用戶端輸出中用於中繼資料交換的 XAddrs。

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    如果提供的 XAddrs 不符合 [XAddr 驗證規則](xaddr-validation-rules.md)，則 WSD Debug 用戶端無法取得裝置的中繼資料。

-   應用程式正在錯誤的安全性內容中執行。 請確認應用程式使用正確的認證，而且用戶端和主機具有足夠的許可權可存取網路。
-   防火牆設定錯誤。 遵循[檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)中的指示，確認 Windows 防火牆設定是否正確，以及是否沒有任何其他規則捨棄封包。 您也可以將用戶端和主機複製到「初始化」電腦， (一個預設作業系統安裝尚未加入網域) 的電腦，以便嘗試重現失敗。
-   IPSec 原則封鎖了應用程式。 將用戶端和主機複製到不受 IPSec 原則影響的電腦，然後嘗試重現失敗。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WSDAPI 診斷程式](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



