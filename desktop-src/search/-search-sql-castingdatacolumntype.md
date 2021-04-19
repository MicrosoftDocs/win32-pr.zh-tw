---
description: 深入瞭解：轉換資料行的資料類型
ms.assetid: 78a137a9-ef69-4ce3-8a96-73e722951300
title: 轉換資料行的資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71a72a84c915d066d4b088719808687a965d86b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974015"
---
# <a name="casting-the-data-type-of-a-column"></a>轉換資料行的資料類型

有時您可能需要將從檔中解壓縮的字串資料轉換成另一種資料類型，以便進行適當的比較。 使用下列語法，將識別碼或常值轉換為另一個資料類型：


```
CAST (<identifier> | <literal> AS <datatype>)
```



例如：


```
CAST ('10000' AS DBTYPE_I4)
            
CAST (System.DateCreated AS DBTYPE_WSTR)
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[資料類型對應](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



