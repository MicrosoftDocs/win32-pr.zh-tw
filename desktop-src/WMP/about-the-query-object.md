---
title: 關於 Query 物件
description: 關於 Query 物件
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Windows Media Player，Query 物件
- Windows Media Player 物件模型、Query 物件
- 物件模型、查詢物件
- Windows Media Player ActiveX 控制項、Query 物件
- ActiveX 控制項、Query 物件
- Windows Media Player Mobile ActiveX 控制項、Query 物件
- Windows Media Player Mobile、Query 物件
- Query 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a26f60c38e053b91c7e56f5cbd7ccaf2ba0fe2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673395"
---
# <a name="about-the-query-object"></a><span data-ttu-id="7be94-111">關於 Query 物件</span><span class="sxs-lookup"><span data-stu-id="7be94-111">About the Query Object</span></span>

<span data-ttu-id="7be94-112">**查詢** 物件代表複合查詢。</span><span class="sxs-lookup"><span data-stu-id="7be94-112">The **Query** object represents a compound query.</span></span> <span data-ttu-id="7be94-113">您可以藉由呼叫 *mediaCollection* 來建立新的空白 **查詢** 物件。**createQuery**。</span><span class="sxs-lookup"><span data-stu-id="7be94-113">You create a new, empty **Query** object by calling *mediaCollection*.**createQuery**.</span></span> <span data-ttu-id="7be94-114">建立 **查詢** 物件之後，您可以呼叫 **addCondition** 將條件加入至複合查詢。</span><span class="sxs-lookup"><span data-stu-id="7be94-114">After you have created a **Query** object, you can call **addCondition** to add a condition to the compound query.</span></span> <span data-ttu-id="7be94-115">後續每次呼叫 **addCondition** 時，會使用和邏輯，將新的條件附加至現有的查詢。</span><span class="sxs-lookup"><span data-stu-id="7be94-115">Each subsequent call to **addCondition** appends a new condition to the existing query using AND logic.</span></span>

<span data-ttu-id="7be94-116">例如，假設您想要建立一個查詢，以代表所有數位媒體，其中 **WM/** 類型等於「爵士樂」且 **作者** 包含「Jim」。</span><span class="sxs-lookup"><span data-stu-id="7be94-116">For example, suppose you want to create a query that represents all digital media where **WM/Genre** equals "Jazz" and **Author** contains "Jim".</span></span> <span data-ttu-id="7be94-117">您可以使用下列 JScript 程式碼，建立複合查詢來表示這些條件：</span><span class="sxs-lookup"><span data-stu-id="7be94-117">You could create a compound query to represent these conditions by using the following JScript code:</span></span>


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



<span data-ttu-id="7be94-118">若要使用或邏輯將條件加入至複合查詢，您必須呼叫 **beginNextGroup**。</span><span class="sxs-lookup"><span data-stu-id="7be94-118">To add a condition to a compound query using OR logic, you must call **Query.beginNextGroup**.</span></span> <span data-ttu-id="7be94-119">這個方法會指出先前的條件群組已完成，而且下一次呼叫 **addCondition** 時，代表新條件群組的開始。</span><span class="sxs-lookup"><span data-stu-id="7be94-119">This method signals that the previous condition group is completed and that the next call to **addCondition** represents the start of a new condition group.</span></span>

<span data-ttu-id="7be94-120">例如，若要建立代表所有數位媒體的查詢，其中 **WM/** 類型等於「爵士樂」且 **作者** 包含 "Jim" 或 **作者** 包含 "Dave"，您可以使用下列範例程式碼：</span><span class="sxs-lookup"><span data-stu-id="7be94-120">For example, to create a query that represents all digital media where **WM/Genre** equals "Jazz" and **Author** contains "Jim" or **Author** contains "Dave", you could use the following example code:</span></span>


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");

// Start the next condition group. This group will be
// combined with the previous group using a logical OR operation.
Query.beginNextGroup();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Dave");
```



<span data-ttu-id="7be94-121">若要執行複合查詢，請呼叫 **MediaCollection. getPlaylistByQuery**。</span><span class="sxs-lookup"><span data-stu-id="7be94-121">To execute your compound query, call **MediaCollection.getPlaylistByQuery**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7be94-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="7be94-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7be94-123">**MediaCollection.getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="7be94-123">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="7be94-124">**指令碼語言的播放程式物件模型**</span><span class="sxs-lookup"><span data-stu-id="7be94-124">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="7be94-125">**Query 物件**</span><span class="sxs-lookup"><span data-stu-id="7be94-125">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 




