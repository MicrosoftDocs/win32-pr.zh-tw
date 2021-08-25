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
ms.openlocfilehash: 967f111107549fd0e6352f0e93d3a747b287c040ea7d5e6cee48415aa7f7925f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637718"
---
# <a name="query-interfaces"></a>查詢介面

有三種類型的 ADSI 介面可以用來執行目錄搜尋。 應用程式環境和其他需求可能會指出所使用的介面。

-   [**>Idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)。 **>Idirectorysearch** 是僅適用于 c/c + + 程式設計人員的基本 COM 介面。 如需詳細資訊，請參閱 [使用 >idirectorysearch 介面搜尋](searching-with-idirectorysearch.md)。
-   ADO。  (ADO) 介面的 ActiveX 資料物件是使用 OLE DB 的自動化介面。 在依賴自動化的應用程式內使用 ADO 進行查詢。 這些包括 Visual Basic 的應用程式、使用中的伺服器頁面等等。 如需詳細資訊，請參閱[使用 ActiveX Data Objects 搜尋](searching-with-activex-data-objects-ado.md)。
-   OLE DB。 OLE DB 是一組用來查詢資料庫的 C/c + + 介面。 藉由支援這些介面，ADSI 提供者可以實行 advanced OLE DB 功能，例如與其他 OLE DB 提供者的分散式查詢。 如需詳細資訊，請參閱 [使用 OLE DB 搜尋](searching-with-ole-db.md)。

 

 




