---
description: 您可以指定搜尋查詢中使用的語言。
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: 指定語言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ab2b5b5c5da4e9f71e49330d966895415467a671289bd4f5607e1265d22a7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226813"
---
# <a name="specifying-languages"></a>指定語言

您可以指定搜尋查詢中使用的語言。 在 WHERE 子句中，FREETEXT 和包含述詞都支援指定語言。 您可以藉由在 CONTAINS 或 FREETEXT 述詞中提供數位語言代碼識別碼 (LCID) 來指出查詢語言。 此 LCID 會指定要使用哪個斷詞工具來剖析查詢字串。 其使用下列語法：


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



如需詳細資訊，請參閱 [CONTAINS](-search-sql-contains.md) 和 [FREETEXT](-search-sql-freetext.md) 述詞的語法。

 

 



