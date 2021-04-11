---
description: 深入瞭解：關於可擴充儲存引擎
title: 關於可擴充儲存引擎
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 17e2277deaef54c04bf6a53a8464479fd67295a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936574"
---
# <a name="about-extensible-storage-engine"></a>關於可擴充儲存引擎


_**適用于：** Exchange Server 2013 |Windows |Windows Server_

## <a name="about-extensible-storage-engine"></a>關於可擴充儲存引擎

可延伸儲存引擎 (ESE) 是一種資料庫引擎，可將資訊儲存在邏輯順序中。 您可以依序或藉由存取定義的索引來抓取資訊。 資料庫的更新會透過交易來執行，以確保安全的作業。 ESE 可同時存取多個資料庫，包括可用於系統復原的交易記錄檔資料庫。 ESE 可以擴充至大型或小型應用程式。 下列功能適用于 ESE 應用程式設計介面 (API) ：

  - 備份與還原：應用程式可以在線上和主動修改資料狀態時，建立一致的資料狀態複本。

  - 資料指標流覽：應用程式可以流覽資料指標，以順序或使用索引來存取資料。

  - 資料庫：以單一單位備份和還原的資料表集合。

  - 記錄和損毀復原： ESE API 可確保即使在系統損毀時，仍會接受應用程式定義的資料一致性。

  - 資料表：用來儲存資料的 ESE 資料庫的基礎結構。

  - 交易： ESE 資料庫引擎提供不可部分完成的一致性隔離持久 (ACID) 交易，讓應用程式只從可靠的資料狀態取出資料，並在發生非預期的進程終止或系統關機時維持資料一致性。

  - 可擴充：應用程式可以建立大小為 100 GB 或小至1MB 的資料庫。

