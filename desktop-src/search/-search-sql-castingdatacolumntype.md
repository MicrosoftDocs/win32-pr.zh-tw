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
# <a name="casting-the-data-type-of-a-column"></a><span data-ttu-id="47366-103">轉換資料行的資料類型</span><span class="sxs-lookup"><span data-stu-id="47366-103">Casting the Data Type of a Column</span></span>

<span data-ttu-id="47366-104">有時您可能需要將從檔中解壓縮的字串資料轉換成另一種資料類型，以便進行適當的比較。</span><span class="sxs-lookup"><span data-stu-id="47366-104">At times you may need to cast string data extracted from documents as another data type, so that an appropriate comparison can be made.</span></span> <span data-ttu-id="47366-105">使用下列語法，將識別碼或常值轉換為另一個資料類型：</span><span class="sxs-lookup"><span data-stu-id="47366-105">Cast an identifier or literal as another data type using the following syntax:</span></span>


```
CAST (<identifier> | <literal> AS <datatype>)
```



<span data-ttu-id="47366-106">例如：</span><span class="sxs-lookup"><span data-stu-id="47366-106">For example:</span></span>


```
CAST ('10000' AS DBTYPE_I4)
            
CAST (System.DateCreated AS DBTYPE_WSTR)
```



## <a name="related-topics"></a><span data-ttu-id="47366-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="47366-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47366-108">資料類型對應</span><span class="sxs-lookup"><span data-stu-id="47366-108">Data Type Mappings</span></span>](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



