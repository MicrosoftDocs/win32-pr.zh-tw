---
title: 關於遠端桌面服務
description: 遠端桌面服務 (前身為終端機服務) 提供的功能類似于以終端為基礎、集中式主機或大型主機，也就是多個終端機連接到主機電腦的環境。
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- 遠端桌面服務遠端桌面服務，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4644170cfca3b4bacdd6db647e35549d56844e9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966413"
---
# <a name="about-remote-desktop-services"></a>關於遠端桌面服務

遠端桌面服務 (前身為終端機服務) 提供的功能類似于以終端為基礎、集中式主機或大型主機，也就是多個終端機連接到主機電腦的環境。 每個終端機都會在使用者與主機電腦之間提供輸入和輸出的管道。 使用者可以在終端機登入，然後在主機電腦上執行應用程式，存取檔案、資料庫、網路資源等等。 每個終端機會話都是獨立的，而且主機作業系統會管理多個使用者爭用共用資源之間的衝突。

遠端桌面服務與傳統大型主機環境之間的主要差異，在於大型主機環境中的啞端子只提供以字元為基礎的輸入和輸出。 遠端桌面連線 (RDC) 用戶端或模擬器提供完整的圖形化使用者介面，包括 Windows 作業系統桌面，以及各種輸入裝置（例如鍵盤和滑鼠）的支援。

在遠端桌面服務環境中，應用程式完全是在遠端桌面工作階段主機 (RD 工作階段主機) server (先前稱為終端機伺服器) 上執行。 RDC 用戶端不會執行應用程式軟體的本機處理。 伺服器會將圖形化使用者介面傳送給用戶端。 用戶端會將使用者的輸入傳送回伺服器。

如需詳細資訊，請參閱下列主題。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[修改裝置重新導向預設值](modify-device-redirection-default-.md)
</dt> <dd>

因為遠端桌面閘道伺服器在將用戶端連線傳遞到遠端桌面工作階段主機伺服器之前，嘗試強制執行安全的裝置重新導向原則，所以在某些情況下，您可能需要停用此預設值。

</dd> <dt>

[遠端桌面通訊協定](remote-desktop-protocol.md)
</dt> <dd>

Microsoft 遠端桌面通訊協定 (RDP) 針對在伺服器上執行的 Windows 應用程式，提供網路連線的遠端顯示和輸入功能。

</dd> <dt>

[遠端桌面服務 API](terminal-services-api.md)
</dt> <dd>

遠端桌面服務 API 主要適用于遠端桌面服務管理的用戶端/伺服器應用程式和應用程式。

</dd> <dt>

[遠端桌面服務管理應用程式](terminal-services-management-applications.md)
</dt> <dd>

描述遠端桌面服務支援的管理應用程式。

</dd> <dt>

[遠端桌面服務程式設計指導方針](terminal-services-programming-guidelines.md)
</dt> <dd>

本主題提供在遠端桌面服務環境中開發應用程式的指導方針。

</dd> <dt>

[遠端桌面會話](terminal-services-sessions.md)
</dt> <dd>

因為每次登入遠端桌面連線 (RDC) 用戶端會收到個別的會話識別碼，所以使用者體驗類似于同時登入多部電腦;例如，辦公室電腦和家用電腦。

</dd> <dt>

[遠端桌面網頁連線](remote-desktop-web-connection.md)
</dt> <dd>

說明如何安裝遠端桌面網頁連線。

</dd> <dt>

[遠端桌面工作階段主機伺服器上的資源](resources-on-a-terminal-server.md)
</dt> <dd>

多個使用者可以同時登入單一 RD 工作階段主機伺服器，並共用伺服器的硬體和軟體資源。

</dd> <dt>

[遠端桌面服務的新功能](what-s-new-in-terminal-services.md)
</dt> <dd>

描述每個遠端桌面服務 API 版本中變更的主題。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用遠端桌面連線連接到其他電腦](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




