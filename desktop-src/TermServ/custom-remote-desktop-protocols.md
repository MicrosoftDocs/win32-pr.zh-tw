---
title: 遠端桌面通訊協定提供者 API
description: 您可以使用遠端桌面通訊協定提供者 API 來建立通訊協定，以提供遠端桌面服務服務與多個用戶端之間的通訊。
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aed1c6866f3078c3761ad8ec631ef23b43a9ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931803"
---
# <a name="remote-desktop-protocol-provider-api"></a>遠端桌面通訊協定提供者 API

您可以使用遠端桌面通訊協定提供者 API 來建立通訊協定，以提供遠端桌面服務服務與多個用戶端之間的通訊。

當 Windows Server 載入時，遠端桌面服務服務 (也稱為遠端連線管理員 (RCM) ) 啟動。 服務也會啟動遠端桌面通訊協定提供者的接聽程式物件，這些提供者接著會接聽用戶端連接。 服務和通訊協定提供者是使用者模式物件，會使用本檔中討論的 Api 進行通訊。 通訊協定提供者可以使用 (IOCTLs) 的輸入/輸出控制項，與核心模式驅動程式進行通訊。 這會顯示在下圖中。

![自訂通訊協定 api 架構](images/protocol-architecture.png)

Microsoft 已實行遠端桌面通訊協定 (RDP) ，以提供遠端桌面服務服務與用戶端連線之間的通訊。 您可以使用組成遠端桌面通訊協定提供者 API 的介面、結構、等位和列舉類型，來建立自己的通訊協定。 如需詳細資訊，請參閱下列主題。

<dl> <dt>

[建立遠端桌面通訊協定提供者](creating-a-custom-remote-protocol.md)
</dt> <dd>

建立遠端桌面通訊協定提供者的相關資訊。 通訊協定管理員會實作為 COM 伺服器，並在遠端桌面服務服務啟動時搜尋的位置註冊。

</dd> <dt>

[遠端桌面通訊協定提供者參考](custom-remote-protocol-reference.md)
</dt> <dd>

包含介面、結構、等位和列舉類型，可讓您建立自訂的遠端桌面通訊協定 (RDP) 。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於遠端桌面服務](about-terminal-services.md)
</dt> </dl>

 

 




