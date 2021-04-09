---
description: 在關係資料庫中，搜尋查詢所傳回的資料列必須符合查詢所呼叫的所有條件。 相反地，Windows Search 查詢可能會將符合搜尋條件的檔傳回不同的程度。
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: 瞭解相關性值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a24c71ad523ad869c6ff05b81ff75367031ad38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847807"
---
# <a name="understanding-relevance-values"></a>瞭解相關性值

在關係資料庫中，搜尋查詢所傳回的資料列必須符合查詢所呼叫的所有條件。 相反地，Windows Search 查詢可能會將符合搜尋條件的檔傳回不同的程度。

例如，在關係資料庫中搜尋「程式」一詞，會產生包含該單字特定拼寫的記錄。 記錄是否包含一或100的單字實例不會影響結果。 相反地，Windows Search 會傳回與相符檔相關聯的關聯性值。 標題中具有「程式」的檔相關性高於最後一個段落中只包含單字的檔。 同樣地，包含搜尋詞彙變化的檔（例如「程式」和「程式設計」）也會相符，並由查詢傳回。

Windows Search 查詢會在名為 "rank" 的資料行中傳回整數關聯值。

此外：

-   查詢所傳回的排名值是介於0到1000之間的整數。
-   排名較高的值表示符合搜尋條件的檔。
-   排名值只適用于目前的查詢，因此無法在查詢之間進行比較。
-   排名值會相對於符合查詢的其他檔。 因此，特定檔的排名值取決於也符合查詢的其他檔。
-   符合單純關聯式述詞之專案的等級值為1000。

您可以使用 [CONTAINS](-search-sql-contains.md) 和 [FREETEXT](-search-sql-freetext.md) WHERE 子句述詞中的資料行權數，以及 rank by 子句，來操作傳回的等級值。

 

 



