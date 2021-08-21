---
title: 非同步搜尋
description: 在 GetFirstRow 的呼叫中啟用非同步 (非同步) 搜尋結果，或在從伺服器傳回第一個專案之前，先呼叫 GetNextRow 區塊。
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- 非同步搜尋 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bca36a30b3b0a46f983da54ecaee753a4b15a455b0e69f9399eacdec68aecd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082782"
---
# <a name="asynchronous-searches"></a>非同步搜尋

在 **GetFirstRow** 的呼叫中啟用非同步 (非同步) 搜尋結果，或在從伺服器傳回第一個專案之前，先呼叫 **GetNextRow** 區塊。 也就是說，如果伺服器上的搜尋需要很長的時間，則會快速傳回前幾個結果。 使用搜尋結果填入清單方塊時，這會有所説明。 搜尋結果會在傳回時顯示。

如果已停用 async，則第一次呼叫 **GetFirstRow** 或 **GetNextRow** 將會封鎖，直到伺服器計算整個結果集並傳回為止。 只有傳回的第一個資料列。 如果預期結果集很大，則不建議這樣做。

如果同時啟用分頁和非同步，則第一次對 **GetFirstRow** 或 **GetNextRow** 的呼叫將會封鎖，直到伺服器產生並傳送結果的第一頁為止。 如果設定合理的頁面大小，則會立即顯示結果。 更重要的是，如果搜尋結果預期會很大，而且您搜尋特定的專案，就不需要在找出您感興趣的專案之後，從伺服器要求更多結果。

分頁的非同步搜尋提供搜尋的精確控制。 如果搜尋結果可能很大，而且需要從伺服器大量時間，這就很有用。

如需有關使用非同步搜尋與特定搜尋介面的詳細資訊，請參閱：

-   [使用 >idirectorysearch 進行同步和非同步搜尋](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [使用 ActiveX Data Objects 搜尋](searching-with-activex-data-objects-ado.md)
-   [使用 OLE DB 搜尋](searching-with-ole-db.md)

 

 




