---
description: 您可以指定搜尋查詢中使用的語言。
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: 指定語言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50b3f65a41670989d41e235831ec8c008a6d8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511088"
---
# <a name="specifying-languages"></a>指定語言

您可以指定搜尋查詢中使用的語言。 在 WHERE 子句中，FREETEXT 和包含述詞都支援指定語言。 您可以藉由在 CONTAINS 或 FREETEXT 述詞中提供數位語言代碼識別碼 (LCID) 來指出查詢語言。 此 LCID 會指定要使用哪個斷詞工具來剖析查詢字串。 其使用下列語法：


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



如需詳細資訊，請參閱 [CONTAINS](-search-sql-contains.md) 和 [FREETEXT](-search-sql-freetext.md) 述詞的語法。

 

 



