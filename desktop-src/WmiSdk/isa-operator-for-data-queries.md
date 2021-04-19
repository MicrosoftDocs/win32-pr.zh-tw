---
description: 在資料查詢的 WHERE 子句中，使用 ISA 運算子來要求類別階層中的内嵌物件。
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: 資料查詢的 ISA 運算子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4c063c99f50a57c8b22a5bbe7040aa3fe96ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988893"
---
# <a name="isa-operator-for-data-queries"></a><span data-ttu-id="f3570-103">資料查詢的 ISA 運算子</span><span class="sxs-lookup"><span data-stu-id="f3570-103">ISA Operator for Data Queries</span></span>

<span data-ttu-id="f3570-104">在資料查詢的 WHERE 子句中，使用 ISA 運算子來要求類別階層中的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="f3570-104">Use the ISA operator in the WHERE clause of a data query to request embedded objects in a class hierarchy.</span></span>

<span data-ttu-id="f3570-105">下列範例顯示在類別階層中要求内嵌物件的語法。</span><span class="sxs-lookup"><span data-stu-id="f3570-105">The following example shows the syntax to request embedded objects in a class hierarchy.</span></span>


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



<span data-ttu-id="f3570-106">結果包含類別的實例，該 **類別** 具有在 **EmbeddedProp** 屬性中衍生自 **ParentClass** 的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="f3570-106">The result includes instances of **Class** having embedded objects that are derived from **ParentClass** in the **EmbeddedProp** property.</span></span> <span data-ttu-id="f3570-107">並非 **類別** 物件的每個實例都是衍生自 **ParentClass**，但結果會傳回衍生自 **ParentClass** 的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="f3570-107">Not every instance of the **Class** object is derived from **ParentClass**, but the result returns the embedded objects that are derived from **ParentClass**.</span></span>

<span data-ttu-id="f3570-108">例如，在下列查詢中， **ClassA** 會包含弱類型的 **EmbeddedObj** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f3570-108">For example, in the following query, **ClassA** includes the weakly typed **EmbeddedObj** property.</span></span> <span data-ttu-id="f3570-109">**ClassA** 類別有10個實例。</span><span class="sxs-lookup"><span data-stu-id="f3570-109">The **ClassA** class has ten instances.</span></span> <span data-ttu-id="f3570-110">其中五個實例的内嵌物件具有衍生自 **ClassZ** 的類型。</span><span class="sxs-lookup"><span data-stu-id="f3570-110">Five of those instances have embedded objects with a type derived from **ClassZ**.</span></span> <span data-ttu-id="f3570-111">其他五個具有其他類型的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="f3570-111">The other five have embedded objects of other types.</span></span>

<span data-ttu-id="f3570-112">下列範例顯示的查詢會傳回五個實例，其中包含衍生自 **ClassZ** 的物件。</span><span class="sxs-lookup"><span data-stu-id="f3570-112">The following example shows the query that returns the five instances, which include the objects that are derived from **ClassZ**.</span></span>


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



