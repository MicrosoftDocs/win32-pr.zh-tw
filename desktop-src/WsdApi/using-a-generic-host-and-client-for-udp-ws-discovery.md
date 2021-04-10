---
description: 如果用戶端和主機無法在網路上看到彼此，則泛型主機和用戶端可以替代自訂主機和用戶端，以協助對問題進行疑難排解。
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: 使用泛型主機和用戶端進行 UDP WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3289f5205e4e417fe8162b401be6c608432cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191722"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a>使用泛型主機和用戶端進行 UDP WS-Discovery

如果用戶端和主機無法在網路上看到彼此，則泛型主機和用戶端可以替代自訂主機和用戶端，以協助對問題進行疑難排解。 如果裝置位址未出現在 WSD Debug 用戶端輸出中，則網路環境可能會造成失敗。 如需泛型主機和用戶端的詳細資訊，請參閱 [調試](debugging-tools.md)程式。

如果主機或用戶端是在電腦上執行的應用程式，則泛型主機或用戶端應該在與實際主機或用戶端相同的安全性內容中執行。 例如，如果實際的主機或用戶端以系統管理員身分執行，則泛型主機或用戶端必須以系統管理員身分執行。 此外，如果主機或用戶端是獨立裝置，則應該由執行泛型主機或用戶端的電腦完全取代。

**使用泛型主機和用戶端對 UDP WS-MANAGEMENT 進行疑難排解**

1.  開啟 [命令提示字元] 視窗。
2.  執行下列命令： **WSDDebug \_host.exe/mode 中繼資料/start**

    > [!Note]  
    > 可能會出現 **Windows 安全性警示** ] 對話方塊。 如果是的話，請按一下 [ **解除封鎖** ]，以允許 WSD Debug 主機執行。

     

    此命令會產生類似下列的輸出。 記下裝置識別碼。

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  執行下列命令： **WSDDebug \_client.exe/mode metadata/hello off/resolve** *<id>* 。 取代 *<id>* 為在步驟2中識別的裝置識別碼。
    > [!Note]  
    > 可能會出現 **Windows 安全性警示** ] 對話方塊。 如果是，請按一下 [ **解除封鎖** ]，以允許 WSD Debug 用戶端執行。

     

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
```

WSD Debug 用戶端可能會在具有許多 DPWS 裝置的網路上產生大量的輸出。 輸出可以重新導向至檔案，以方便分析。 在 WSD Debug Client 提示字元中輸入 **log t** *<filename>* ，以將輸出重新導向至檔案。 在 WSD Debug 用戶端提示字元中輸入 **log t stop** ，即可停止輸出重新導向。

請記下 (EPR) 位址的端點參考。 此 EPR 位址應符合上述步驟2中識別的裝置識別碼。 如果是這種情況，則應用程式失敗可能與作業系統或網路環境無關。 以自訂主機和用戶端取代一般主機和用戶端，並遵循 [使用 WSD Debug 用戶端驗證多播流量](using-wsddebug-client-to-verify-multicast-traffic.md)的程式，繼續進行疑難排解。

如果裝置識別碼與 EPR 位址不符，則應用程式失敗可能與作業系統或網路環境有關。 失敗可能有一或多個下列原因：

-   應用程式正在錯誤的安全性內容中執行。 請確認應用程式使用正確的認證，而且用戶端和主機具有足夠的許可權可存取網路。
-   防火牆設定錯誤。 遵循 [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md) 中的指示，確認 Windows 防火牆設定正確無誤，而且沒有任何其他規則捨棄封包。 您也可以將用戶端和主機複製到「初始化」電腦， (一個預設作業系統安裝尚未加入網域) 的電腦，以便嘗試重現失敗。
-   IPSec 原則封鎖了應用程式。 將用戶端和主機複製到不受 IPSec 原則影響的電腦上，然後嘗試重現失敗。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WSDAPI 診斷程式](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



