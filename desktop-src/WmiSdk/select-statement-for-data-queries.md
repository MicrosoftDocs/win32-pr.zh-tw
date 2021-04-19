---
description: 描述資料查詢的 SELECT 語句。
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: 資料查詢的 SELECT 語句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06905cfd9ef5e55022b3fc2275ed705a670a0ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982342"
---
# <a name="select-statement-for-data-queries"></a><span data-ttu-id="8bcc6-103">資料查詢的 SELECT 語句</span><span class="sxs-lookup"><span data-stu-id="8bcc6-103">SELECT Statement for Data Queries</span></span>

<span data-ttu-id="8bcc6-104">您可以使用各種 SELECT 語句來查詢資訊。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-104">You can use a variety of SELECT statements to query for information.</span></span> <span data-ttu-id="8bcc6-105">語句可以是基本語句，也可以更嚴格地縮減查詢所傳回的結果集。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-105">The statements can be basic statements or they can be more restrictive to narrow the result set that is returned from the query.</span></span>

<span data-ttu-id="8bcc6-106">下列範例是用來查詢資料的基本 SELECT 語句。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-106">The following example is a basic SELECT statement that is used to query for data.</span></span>


```sql
SELECT * FROM Class
```



<span data-ttu-id="8bcc6-107">這個語句會傳回指定之類別及其任何子類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-107">This statement returns instances of the specified class and any of its subclasses.</span></span> <span data-ttu-id="8bcc6-108">系統會包含類別的所有系統和使用者定義屬性。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-108">All of the system and user-defined properties for the classes are included.</span></span> <span data-ttu-id="8bcc6-109">如果系統屬性與特定查詢無關，則會包含 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-109">If a system property is not relevant for a particular query, it contains **NULL**.</span></span>

<span data-ttu-id="8bcc6-110">您可以使用數種技術來減少取出結果集所需的頻寬，如果查詢的執行結果太多，而且使用者只對屬性子集感興趣。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-110">You can use several techniques to reduce the bandwidth required to retrieve the result set, if the execution of the query results in too much overhead and the user is only interested in a subset of the properties.</span></span> <span data-ttu-id="8bcc6-111">首先，查詢可以將星號取代為所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-111">First, queries can replace the asterisk with the desired properties.</span></span>

<span data-ttu-id="8bcc6-112">下列範例示範如何查詢特定屬性。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-112">The following example shows how to query for specific properties.</span></span>


```sql
SELECT property_1, property_2, property_3 FROM class
```



<span data-ttu-id="8bcc6-113">結果集會包含所有系統屬性和指定的非系統屬性。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-113">The result set includes all system properties and the specified nonsystem properties.</span></span>

<span data-ttu-id="8bcc6-114">縮小查詢結果集範圍的另一個方法是使用 [**\_ \_ 類別**](wmi-system-properties.md)系統屬性。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-114">Another technique for narrowing the scope of a query's result set is to use the [**\_\_CLASS**](wmi-system-properties.md) system property.</span></span> <span data-ttu-id="8bcc6-115">依預設，查詢會傳回指定之類別及其子類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-115">Queries by default return all instances of the specified class and its subclasses.</span></span> <span data-ttu-id="8bcc6-116">您可以使用 **\_ \_ 類別** 系統屬性，只要求指定類別的實例，但不包括其子類別。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-116">You can use the **\_\_CLASS** system property to request only instances of the specified class, excluding its subclasses.</span></span>

<span data-ttu-id="8bcc6-117">下列範例示範如何在 WHERE 子句中使用 [**\_ \_ 類別**](wmi-system-properties.md)系統屬性。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-117">The following example shows how to use the [**\_\_CLASS**](wmi-system-properties.md) system property in a WHERE clause.</span></span>


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



<span data-ttu-id="8bcc6-118">您也可以使用 [**\_ \_ 類別**](wmi-system-properties.md)系統屬性，將結果集限制為特定子類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-118">You can also use the [**\_\_CLASS**](wmi-system-properties.md) system property to restrict the result set to instances of particular subclasses.</span></span>

<span data-ttu-id="8bcc6-119">下列範例顯示如何將結果集限制為特定子類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-119">The following example shows how to restrict the result set to instances of particular subclasses.</span></span>


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> <span data-ttu-id="8bcc6-120">如果您使用不正確內嵌物件路徑來建立查詢，則您的查詢不會傳回錯誤或任何結果。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-120">If you construct a query with an invalid path for an embedded object, your query does not return an error or any results.</span></span>

 

<span data-ttu-id="8bcc6-121">下列範例會傳回 **MainClass** 的實例，假設 **MainClass** 的實例存在，其包含屬性 **P \_ Uint32** 等於 "70011" 的内嵌物件 **EmbedObj** 。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-121">The following example returns an instance of **MainClass**, assuming that an instance of **MainClass** exists containing the embedded object **EmbedObj** with a property **P\_Uint32** that is equal to "70011".</span></span>


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



<span data-ttu-id="8bcc6-122">下列範例不會傳回任何結果，也不會傳回錯誤，假設 **MainClass** 實例中 **EmbedObj** 的内嵌物件沒有 **無效** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="8bcc6-122">The following example returns no results and does not return an error, assuming that the embedded object **EmbedObj** in the instance of **MainClass** does not have a property **INVALID**.</span></span>


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



