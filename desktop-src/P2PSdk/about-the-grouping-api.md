---
description: 對等群組 API 結合了 PNRP 命名空間提供者 API 和圖形 API 的技術。
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: 關於群組 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b4cd1b2783d7605f9198e3c8171177e70b531944a8f2f707def5750dd6d985
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612792"
---
# <a name="about-the-grouping-api"></a>關於群組 API

對等群組 API 結合了 [PNRP 命名空間提供者 api](pnrp-namespace-provider-api.md) 和 [圖形 API](graphing-api.md)的技術。 群組新增下列兩項技術：

-   多工層，可讓多個應用程式使用一個圖形、一個埠和一個記錄資料庫。
-   安全性可確保只有受邀加入群組的對等，才能在群組的整個存留期內加入並連接。

分組可讓您輕鬆存取對等網路，因為直接呼叫流程和安全訊息。 此 API 會使用 PNRP 進行群組探索和標準 PKI 型安全性提供者，而不需要開發人員執行。 但是，如果您的應用程式在安全性選項方面要求更大的彈性，請考慮使用 [圖形 API](about-the-graphing-api.md)。

下表識別此群組 API 區段中的主題：

| 主題                                                                | 描述                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [如何使用群組](how-to-work-with-groups.md)               | 說明對等群組應用程式中從啟動到關機的呼叫流程。         |
| [群組安全性的運作方式](how-group-security-works.md)             | 描述對等群組成員資格和資料交換如何受到保護。                      |
| [邀請對等群組](inviting-a-peer-to-a-group.md)         | 描述對等受邀並新增至對等群組的進程。              |
| [如何連線到對等群組](how-to-connect-to-a-peer-group.md) | 描述對等互連如何連接至對等群組並與之互動。                        |
| [管理群組記錄](managing-group-records.md)                 | 描述對等群組記錄，以及如何以成員和系統管理員的身分來管理它們。 |



 

> [!Note]  
> 在具有防火牆的環境中使用群組 API 的應用程式需要例外狀況群組，其中涵蓋應用程式專屬的埠，以及適用于 PNRP 的群組 API 和3540埠 ' 3587-TCP ' 的埠 '-TCP '。 每當應用程式執行時，都應啟用這些例外狀況群組。

 

 

 



