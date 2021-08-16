---
title: " (用戶端) 快取結果"
description: 用戶端快取會將結果集儲存在用戶端記憶體中，以提供用戶端的效能增強功能。
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- 快取 (用戶端) ADSI 的結果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c2394c4f9e3213261bc52e15ada6fa9416703706fedeccaf144493821133e1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840498"
---
# <a name="caching-the-result-client-side"></a> (用戶端) 快取結果

用戶端快取會將結果集儲存在用戶端記憶體中，以提供用戶端的效能增強功能。 用戶端可以重複使用物件，而不需要多次往返伺服器。 根據預設，ADSI 會快取用戶端的結果集。 這可讓 ADSI 提供具有類似 SQL 的資料指標支援的用戶端。 您可以逐一查看指定的結果集數次。

ADSI 也可讓用戶端關閉快取，以降低記憶體需求。 如果用戶端快取已停用，用戶端就不會在記憶體中維護結果集。 每個資料列會在應用程式抓取之後釋放。 停用用戶端快取可能有助於減少用戶端記憶體需求，例如，當您只想要透過結果集進行單一傳遞時。 不過，當用戶端選擇不快取結果時，它們會提供資料指標支援。

如需有關使用特定搜尋介面的結果快取的詳細資訊，請參閱：

-   [使用 >idirectorysearch 的結果快取](result-caching-with-idirectorysearch.md)
-   [使用 ActiveX Data Objects 搜尋](searching-with-activex-data-objects-ado.md)
-   [使用 OLE DB 搜尋](searching-with-ole-db.md)

 

 




