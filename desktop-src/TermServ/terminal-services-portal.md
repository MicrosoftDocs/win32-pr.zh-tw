---
title: '遠端桌面服務 (遠端桌面服務) '
description: Microsoft 遠端桌面服務是支援遠端桌面存取的遠端電腦存取軟體。 遠端桌面服務會將多個用戶端連接至遠端桌面工作階段主機 (RD 工作階段主機) 伺服器。
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- 遠端桌面服務遠端桌面服務
- 遠端桌面服務遠端桌面服務，首頁
- 終端機服務查看遠端桌面服務遠端桌面服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525f62433c10c8c4f750a8ae1abbfa9496f2f096139c182a677c9dbf69ce4a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999898"
---
# <a name="remote-desktop-services-remote-desktop-services"></a>遠端桌面服務 (遠端桌面服務) 

## <a name="purpose"></a>目的

Windows Server 2012R2、Windows Server 2012、Windows Server 2008 R2 或 Windows Server 2008 搭配先前稱為終端機服務的遠端桌面服務 (，可讓伺服器同時裝載多個用戶端會話。 遠端桌面使用遠端桌面服務技術，讓單一會話可以從遠端執行。 使用者可以使用 () RDC 遠端桌面連線用戶端軟體，連接到遠端桌面工作階段主機 (RD 工作階段主機) server (先前稱為終端機伺服器) 。 遠端桌面網頁連線將遠端桌面服務的技術延伸至網路。

> [!Note]  
> 本主題適用于軟體發展人員。 如果您要尋找遠端桌面連線的使用者資訊，請參閱 [遠端桌面連線：常見問題](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8)。

 

## <a name="where-applicable"></a>適用時

遠端桌面連線 (RDC) 用戶端可以存在於各種不同的表單中。 執行內嵌 Windows 型作業系統的瘦用戶端硬體裝置可以執行 RDC 用戶端軟體，以連線到 RD 工作階段主機伺服器。 Windows 的、Macintosh 或 UNIX 型電腦可以執行 RDC 用戶端軟體，以連線到 RD 工作階段主機伺服器以顯示 Windows 型應用程式。 這種 RDC 用戶端組合可讓您從幾乎任何作業系統存取 Windows 應用程式。

## <a name="developer-audience"></a>開發人員對象

使用遠端桌面服務的開發人員應該熟悉 C 和 c + + 程式設計語言，以及以 Windows 為基礎的程式設計環境。 需要熟悉用戶端/伺服器架構。 遠端桌面網頁連線包含可編寫腳本的介面，可在遠端桌面服務 Web 應用程式中建立和部署可編寫腳本的虛擬通道。

## <a name="run-time-requirements"></a>執行階段需求求

使用遠端桌面服務的應用程式需要 Windows Server 2012 R2、Windows 8.1、Windows Server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows server 2008 或 Windows Vista。 若要使用遠端桌面網頁連線的功能，遠端桌面服務用戶端應用程式需要 Internet Explorer 和全球 Web 的連接。 如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[遠端桌面 ActiveX 控制項](remote-desktop-activex-control.md)
</dt> <dd>

說明如何使用遠端桌面 ActiveX 控制項。

</dd> <dt>

[遠端桌面通訊協定提供者 API](custom-remote-desktop-protocols.md)
</dt> <dd>

您可以使用遠端桌面通訊協定提供者 API 來建立通訊協定，以提供遠端桌面服務服務與多個用戶端之間的通訊。

</dd> <dt>

[遠端桌面服務虛擬通道](terminal-services-virtual-channels.md)
</dt> <dd>

*虛擬通道* 是軟體延伸模組，可用來將功能增強功能新增至遠端桌面服務應用程式。

</dd> <dt>

[RemoteFX媒體重新導向 API](remotefx-api.md)
</dt> <dd>

在遠端桌面會話中使用 RemoteFX 媒體重新導向 API，以識別顯示快速變更內容之伺服器的區域，例如影片。 然後，此內容可以編碼並以編碼格式傳送至用戶端。

</dd> <dt>

[遠端桌面連線代理人用戶端 API](connection-broker-client-api.md)
</dt> <dd>

說明如何使用遠端桌面連線代理人用戶端 API。

</dd> <dt>

[個人桌面工作代理程式 API 參考](task-agent-api-reference.md)
</dt> <dd>

個人桌面工作代理程式 API 會用來處理對個人虛擬桌面的排程更新。

</dd> <dt>

[關於遠端桌面服務](about-terminal-services.md)
</dt> <dd>

遠端桌面服務 (前身為終端機服務) 提供的功能類似于以終端為基礎、集中式主機或大型主機，也就是多個終端機連接到主機電腦的環境。

</dd> <dt>

[遠端桌面管理服務提供者](rdms-api-reference.md)
</dt> <dd>

遠端桌面管理服務 (RDMS) 提供者會管理 (VDI) 環境的虛擬桌面基礎結構。

</dd> <dt>

[遠端桌面服務參考](terminal-services-reference.md)
</dt> <dd>

您可以用來檢查和設定遠端桌面服務使用者屬性的屬性方法檔。 也記載了遠端桌面服務函式、結構和遠端桌面網頁連線可編寫腳本的介面。

</dd> <dt>

[遠端桌面服務快速鍵](terminal-services-shortcut-keys.md)
</dt> <dd>

遠端桌面服務快速鍵的清單。

</dd> <dt>

[遠端桌面服務 WMI 提供者](terminal-services-wmi-provider.md)
</dt> <dd>

遠端桌面服務 WMI 提供者可透過程式設計的方式，存取遠端桌面服務設定/連線 Microsoft Management Console (MMC) 嵌入式管理單元所公開的資訊和設定。

</dd> <dt>

[使用遠端桌面服務](using-terminal-services.md)
</dt> <dd>

如何在遠端桌面服務環境中進行程式設計，以及如何使用遠端桌面網頁連線將先前稱為終端機服務) 技術的遠端桌面服務 (延伸至網路。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[終端機服務現在遠端桌面服務](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




