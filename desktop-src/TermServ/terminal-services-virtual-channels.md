---
title: 遠端桌面服務虛擬通道
description: 虛擬通道是軟體延伸模組，可用來將功能增強功能新增至遠端桌面服務應用程式。
ms.assetid: f7bdebec-ecc3-4f28-9327-f0d2f169c142
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce78331841a41502aa337de19e9879d42d85fe1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300728"
---
# <a name="remote-desktop-services-virtual-channels"></a>遠端桌面服務虛擬通道

*虛擬通道* 是軟體延伸模組，可用來將功能增強功能新增至遠端桌面服務應用程式。 功能增強功能的範例可能包括：支援特殊類型的硬體、音訊或其他遠端桌面服務 [遠端桌面通訊協定](remote-desktop-protocol.md) (RDP) 所提供的核心功能。 RDP 通訊協定提供多個虛擬通道的多重管理管理。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[使用遠端桌面服務的虛擬通道](using-terminal-services-virtual-channels.md)
</dt> <dd>

若要執行虛擬通道，您可以提供虛擬通道應用程式的伺服器和用戶端模組。

</dd> <dt>

[動態虛擬通道參考](dynamic-virtual-channels-reference.md)
</dt> <dd>

遠端桌面服務支援動態虛擬通道 (DVC) 用戶端介面。

</dd> <dt>

[圖形虛擬通道參考](graphics-virtual-channels-reference.md)
</dt> <dd>

圖形虛擬通道參考包含可讓您建立虛擬圖形通道的程式設計項目。

</dd> </dl>

虛擬通道應用程式有兩個部分：用戶端模組和伺服器模組。 伺服器模組是在遠端桌面工作階段主機 (RD 工作階段主機) server 上執行的可執行程式。 用戶端模組是在遠端桌面連線 (RDC) 用戶端程式執行時，必須載入至用戶端電腦記憶體的 DLL。

虛擬通道可以在與 RDP 通訊協定無關的遠端桌面連線 (RDC) 用戶端上新增功能增強功能。 透過虛擬通道支援，您可以新增新功能，而不需要更新用戶端或伺服器軟體或 RDP 通訊協定。

已識別出虛擬通道使用者的四個主要類別：

-   一般核心模式驅動程式，例如序列或印表機驅動程式。
-   檔案系統重新導向 (這只是一般核心模式驅動程式) 的特殊案例。
-   使用者模式應用程式，例如遠端剪下和貼上。
-   音訊裝置。

如需詳細資訊，請參閱 [使用遠端桌面服務的虛擬通道](using-terminal-services-virtual-channels.md)。

如果您已在遠端桌面服務部署中啟用虛擬通道應用程式，可以透過遠端桌面 Microsoft ActiveX 控制項，讓應用程式可供存取 RD 工作階段主機伺服器的用戶端電腦使用。 如需詳細資訊，請參閱可 [編寫腳本的虛擬通道](scriptable-virtual-channels.md) 和 [使用具有虛擬通道的遠端桌面 ActiveX 控制項](using-the-remote-desktop-activex-control-with-virtual-channels.md)。

 

 




