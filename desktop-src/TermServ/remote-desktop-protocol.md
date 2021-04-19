---
title: 遠端桌面通訊協定
description: Microsoft 遠端桌面通訊協定 (RDP) 針對在伺服器上執行的 Windows 應用程式，提供網路連線的遠端顯示和輸入功能。
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- 遠端桌面通訊協定 (RDP) 遠端桌面服務
- 'RDP (請參閱遠端桌面通訊協定) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7895163a5ee92a6cc756dca9b097db8498d02e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967901"
---
# <a name="remote-desktop-protocol"></a>遠端桌面通訊協定

Microsoft 遠端桌面通訊協定 (RDP) 針對在伺服器上執行的 Windows 應用程式，提供網路連線的遠端顯示和輸入功能。 RDP 的設計是為了支援不同類型的網路拓撲和多個 LAN 通訊協定。

> [!Note]  
> 本主題適用于軟體發展人員。 如果您要尋找遠端桌面的使用者資訊，請參閱 [Windows 支援](https://windows.microsoft.com/windows/support#1TC=windows-8)。 如果您要尋找遠端桌面的 IT 專業人員資訊，請參閱 [TechNet 上的遠端桌面服務](/windows/deployment/deploy-whats-new)。

 

## <a name="basic-architecture"></a>基本架構

RDP 是根據 ITU T. 120 系列通訊協定的擴充功能。 RDP 是支援多通道的通訊協定，可讓不同的虛擬通道攜帶裝置通訊和來自伺服器的簡報資料，以及加密的用戶端滑鼠和鍵盤資料。 RDP 提供可延伸的基底，並支援最多64000個不同的通道，以進行資料傳輸和 multipoint 傳輸的布建。

在伺服器上，RDP 使用自己的視頻驅動程式來轉譯顯示輸出，其方式是使用 RDP 通訊協定將轉譯資訊建立到網路封包，並透過網路將其傳送至用戶端。 在用戶端上，RDP 會接收轉譯資料，並將封包轉譯成對應的 Microsoft Windows 圖形裝置介面 (GDI) API 呼叫。 針對輸入路徑，用戶端滑鼠和鍵盤事件會從用戶端重新導向至伺服器。 在伺服器上，RDP 使用自己的鍵盤和滑鼠驅動程式來接收這些鍵盤和滑鼠事件。

在遠端桌面會話中，所有環境變數（例如，決定色彩深度和壁紙啟用和停用的變數）都是由 RCP-Tcp 連接設定所決定。 這適用于在 [遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md) 中設定環境變數的所有函數和方法，以及 [遠端桌面服務 WMI 提供者介面](terminal-services-wmi-provider-reference.md)。

## <a name="features"></a>功能

Microsoft RDP 包含下列特性和功能：

<dl> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>加密
</dt> <dd>

RDP 使用 RSA 安全性的 RC4 密碼，這是專為有效率地加密少量資料而設計的資料流程加密。 RC4 是針對透過網路的安全通訊所設計。 系統管理員可以選擇使用56或128位金鑰來加密資料。

</dd> <dt>

<span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>頻寬減少功能
</dt> <dd>

RDP 支援各種機制來減少透過網路連線傳輸的資料量。 機制包括資料壓縮、持續快取點陣圖，以及在 RAM 中快取圖像和片段。 持續性點陣圖快取可大幅改善低頻寬連接的效能，特別是在執行大量使用大型點陣圖的應用程式時。

</dd> <dt>

<span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>漫遊中斷連線
</dt> <dd>

使用者可以手動中斷與遠端桌面會話的連線，而不需要登出。 當使用者從相同的裝置或不同的裝置登入系統時，會自動重新連線到中斷連線的會話。 當網路或用戶端失敗意外終止使用者的會話時，使用者就會中斷連線，但不會登出。

</dd> <dt>

<span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>剪貼簿對應
</dt> <dd>

使用者可以刪除、複製和貼上在本機電腦上執行的應用程式，以及在遠端桌面會話中執行的應用程式，以及會話之間的文字和圖形。

</dd> <dt>

<span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>列印重新導向
</dt> <dd>

在遠端桌面會話中執行的應用程式可以列印到連接到用戶端裝置的印表機。

</dd> <dt>

<span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>虛擬通道
</dt> <dd>

藉由使用 RDP 虛擬通道架構，您可以擴充現有的應用程式，並開發新的應用程式來新增需要用戶端裝置與遠端桌面會話中執行之應用程式之間通訊的功能。

</dd> <dt>

<span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>遙控
</dt> <dd>

電腦支援人員可以查看及控制遠端桌面會話。 在兩個遠端桌面會話之間共用輸入和顯示圖形，可讓支援人員能夠從遠端診斷和解決問題。

</dd> <dt>

<span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>網路負載平衡
</dt> <dd>

RDP 會利用 (NLB) 的網路負載平衡（如果有的話）。

</dd> </dl>

此外，RDP 包含下列功能：

-   支援24位色彩。
-   藉由減少頻寬來改善低速度的撥號連線效能。
-   透過遠端桌面服務的智慧卡驗證。
-   鍵盤掛鉤。 將特殊 Windows 按鍵組合（以全螢幕模式）導向本機電腦或遠端電腦的能力。
-   音效、磁片磁碟機、埠和網路印表機重新導向。 在用戶端電腦上執行 RDC 用戶端時，可能會聽到遠端電腦上發生的音效，遠端桌面會話將可看到本機用戶端磁片磁碟機。

 

 