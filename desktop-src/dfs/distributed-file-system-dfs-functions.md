---
title: 分散式檔案系統 (DFS) 函式
description: 分散式檔案系統 (DFS) 函式可讓您以邏輯方式將多部伺服器上的共用群組在一起，並以透明方式將共用連結至單一階層命名空間。 DFS 會在樹狀結構中組織網路上的共用資源。
ms.assetid: a29cde3e-483a-4658-94d4-27398f66abfb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898d44ecfaeb99145570230e49156440dc9e2aac02051baa47bb496a0f58b2b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119380578"
---
# <a name="distributed-file-system-dfs-functions"></a>分散式檔案系統 (DFS) 函式

分散式檔案系統 (DFS) 函式可讓您以邏輯方式將多部伺服器上的共用群組在一起，並以透明方式將共用連結至單一階層命名空間。 DFS 會在樹狀結構中組織網路上的共用資源。

DFS 支援 *獨立* DFS 命名空間、具有一部主機伺服器的網域，以及具有多部主機伺服器和高可用性的 *網域型* 命名空間。 以網域為基礎的命名空間的 DFS *拓撲資料* 會儲存在 Active Directory 中。 資料包含 DFS 根目錄、DFS 連結和 DFS 目標。

每個 DFS 樹狀結構都有一或多個 *根目標*。 根目標是執行 DFS 服務的主機伺服器。 DFS 樹狀結構可以包含一或多個 *dfs 連結*。 每個 DFS 連結都會指向網路上的一個或多個共用資料夾。 您可以新增、修改和刪除 DFS 命名空間的 DFS 連結。 當您移除與 DFS 連結相關聯的最後一個目標時，DFS 會刪除 DFS 命名空間中的 DFS 連結。  (在先前的檔中，DFS 連結稱為連接點。 ) 

DFS 連結可以指向一或多個共用資料夾;這些資料夾稱為 *目標*。 當使用者存取 DFS 連結時，DFS 伺服器會根據用戶端的網站資訊來選取一組目標。 用戶端會存取集合中第一個可用的目標。 這有助於將用戶端要求分散到可能的目標，並可為使用者提供持續的可存取性，即使某些伺服器失敗亦同。

應用程式可以使用 DFS 功能來：

- 新增 dfs 根目錄的 DFS 連結。
- 建立或移除獨立和網域型 DFS 命名空間。
- 將目標新增至現有的 DFS 連結。
- 從 DFS 根目錄移除 DFS 連結。
- 從 DFS 連結移除目標。
- 查看及設定 DFS 根目錄和連結的相關資訊。

如需 DFS 函式的清單，請參閱 [分散式檔案系統](distributed-file-system-functions.md)函式。

如需 DFS 結構的清單，請參閱 [分散式檔案系統結構](distributed-file-system-structures.md)。

在執行 Microsoft Windows 的電腦上，您可以在 DFS 命名空間中發佈目標。 您也可以發佈任何可在 DFS 命名空間中使用用戶端重新導向程式的非 Microsoft 共用。 不過，與在執行 Windows server 的伺服器上發佈的共用不同，它們無法裝載 dfs 根目錄或提供其他 dfs 目標的參考。

DFS 使用 Windows Server 檔案複寫服務來複製複寫目標之間的變更。 使用者可以修改儲存在某個目標上的檔案，而且檔案複寫服務會將變更傳播到其他指定的目標。 服務會保留檔或檔案的最新變更。
