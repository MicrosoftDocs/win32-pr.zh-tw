---
title: 連接點
description: 連接點物件包含網路上可用的一或多個服務實例的相關資料。
ms.assetid: eb810e6d-c220-4a24-ae12-b12ace237413
ms.tgt_platform: multiple
keywords:
- 連接點廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc61c4c5b7dd74626ab1f3884ad403cfa20b843
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023277"
---
# <a name="connection-points"></a>連接點

連接點物件包含網路上可用的一或多個服務實例的相關資料。 [**ConnectionPoint**](/windows/desktop/ADSchema/c-connectionpoint)物件類別是抽象基類，代表 Active Directory Domain Services 中可連接資源的物件。 下圖顯示衍生自 **connectionPoint** 物件類別的部分物件類別。

![衍生自 connectionpoint 物件類別的物件類別](images/connection-points.png)

下表列出 [**connectionPoint**](/windows/desktop/ADSchema/c-connectionpoint) 類別的直屬子類別。



| 物件類別                                                    | Description                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) | 服務連接點 (SCP) 物件，用來發佈用戶端應用程式用來系結至服務的資料。 如需詳細資訊，請參閱 [使用服務連接點發行 (scp) ](publishing-with-service-connection-points.md)。                                                                               |
| [**rpcEntry**](/windows/desktop/ADSchema/c-rpcentry)                             | 由 RPC 名稱服務使用子類別的抽象類別 (Ns) 透過 WIN32 API 中的 **RpcNs \*** 函式存取。 如需詳細資訊，請參閱 [使用 RPC 名稱服務發行 (RpcNs) ](publishing-with-the-rpc-name-service-rpcns.md)。                                                          |
| [**serviceInstance**](/windows/desktop/ADSchema/c-serviceinstance)               | Windows 通訊端註冊和解析所使用的連接點物件 (RnR) 名稱服務，可透過 Windows 套 **接字 \* WSA** api 存取。 如需詳細資訊，請參閱 [使用 Windows 通訊端註冊和解析發行 (RnR) ](publishing-with-windows-sockets-registration-and-resolution.md)。 |
| [**列印**](/windows/desktop/ADSchema/c-printqueue)                         | 用來發佈網路印表機的連接點物件。 如需詳細資訊，請參閱 [**IADsPrintQueue**](/windows/desktop/api/iads/nn-iads-iadsprintqueue)。                                                                                                                                                                                           |
| [**體積**](/windows/desktop/ADSchema/c-volume)                                 | 用來發行檔案服務的連接點物件。                                                                                                                                                                                                                                                                   |



 

請注意，以 COM 為基礎的服務不會使用連接點物件來通告本身。 這些服務會在類別存放區中發行。 Windows 2000 類別存放區是以目錄為基礎的存放庫，適用于所有以 COM 為基礎的應用程式、介面，以及提供應用程式發行和指派的 Api。 如需詳細資訊，請參閱 [發行 COM + 服務](publishing-com-services.md)。

 

 