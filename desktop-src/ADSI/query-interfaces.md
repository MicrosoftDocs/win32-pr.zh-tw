---
title: 查詢介面
description: 有三種類型的 ADSI 介面可以用來執行目錄搜尋。 應用程式環境和其他需求可能會指出所使用的介面。
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- 查詢介面 ADSI
- 查詢 ADSI、查詢介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805303a972b4a8140a9e632857287aeebca9b32f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839144"
---
# <a name="query-interfaces"></a>查詢介面

有三種類型的 ADSI 介面可以用來執行目錄搜尋。 應用程式環境和其他需求可能會指出所使用的介面。

-   [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)。 **>idirectorysearch** 是僅適用于 c/c + + 程式設計人員的基本 COM 介面。 如需詳細資訊，請參閱 [使用 >idirectorysearch 介面搜尋](searching-with-idirectorysearch.md)。
-   Ado。 ActiveX Data 物件 (ADO) 介面是使用 OLE DB 的自動化介面。 在依賴自動化的應用程式內使用 ADO 進行查詢。 這些包括 Visual Basic 的應用程式、使用中的伺服器頁面等等。 如需詳細資訊，請參閱 [使用 ActiveX Data Objects 搜尋](searching-with-activex-data-objects-ado.md)。
-   OLE DB。 OLE DB 是一組用來查詢資料庫的 C/c + + 介面。 藉由支援這些介面，ADSI 提供者可以實行 advanced OLE DB 功能，例如與其他 OLE DB 提供者的分散式查詢。 如需詳細資訊，請參閱 [使用 OLE DB 搜尋](searching-with-ole-db.md)。

 

 




