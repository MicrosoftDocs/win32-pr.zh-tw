---
description: SET 語句會指定查詢的 PROPERTYNAME 和 RANKMETHOD 選項。
ms.assetid: 14b833a5-5e6a-4f1a-b15e-3b32d7e0df37
title: SET 語句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55124f75c1462dbd377ff0de02a55596fbd3ab71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112413"
---
# <a name="set-statement"></a><span data-ttu-id="36929-103">SET 語句</span><span class="sxs-lookup"><span data-stu-id="36929-103">SET Statement</span></span>

<span data-ttu-id="36929-104">SET 語句會指定查詢的 PROPERTYNAME 和 RANKMETHOD 選項。</span><span class="sxs-lookup"><span data-stu-id="36929-104">The SET statement specifies PROPERTYNAME and RANKMETHOD options for the query.</span></span>

## <a name="propertyname"></a><span data-ttu-id="36929-105">PROPERTYNAME</span><span class="sxs-lookup"><span data-stu-id="36929-105">PROPERTYNAME</span></span>

<span data-ttu-id="36929-106">您可以使用下列語法，將屬性與查詢的易記別名建立關聯：</span><span class="sxs-lookup"><span data-stu-id="36929-106">You can associate a property with a friendly alias for the query by using the following syntax:</span></span>


```
SET PROPERTYNAME <guid_format> 
PROPID <property_id> | <property_name> 
AS <column_alias> [<type_clause>] 
```



## <a name="rankmethod"></a><span data-ttu-id="36929-107">RANKMETHOD</span><span class="sxs-lookup"><span data-stu-id="36929-107">RANKMETHOD</span></span>

<span data-ttu-id="36929-108">您可以使用下列語法，針對具有 ISABOUT 詞彙的查詢指定 rank 方法：</span><span class="sxs-lookup"><span data-stu-id="36929-108">You can specify the rank method for queries with the ISABOUT term by using the following syntax:</span></span>


```
SET RANKMETHOD <rankmethod>      
```



<span data-ttu-id="36929-109">可以使用 SET 語句來指定的 RANKMETHOD 方法為 JACCARD 係數、骰子係數和內部乘積。</span><span class="sxs-lookup"><span data-stu-id="36929-109">The RANKMETHOD methods that can be specified by using the SET statement are JACCARD COEFFICIENT, DICE COEFFICIENT, and INNER PRODUCT.</span></span>

 

 



