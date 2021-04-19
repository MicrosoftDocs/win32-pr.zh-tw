---
description: 值對應是連結至具有值和 ValueMap 限定詞之屬性的陣列。
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: ValueMap 和值限定詞
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df85342df9543e4d62b04482785ec31bb5bd3982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987257"
---
# <a name="valuemap-and-value-qualifiers"></a><span data-ttu-id="26aeb-103">ValueMap 和值限定詞</span><span class="sxs-lookup"><span data-stu-id="26aeb-103">ValueMap and Value Qualifiers</span></span>

<span data-ttu-id="26aeb-104">值對應是連結至具有 **值** 和 **ValueMap** 限定詞之屬性的陣列。</span><span class="sxs-lookup"><span data-stu-id="26aeb-104">A value map is an array linked to a property with the **Value** and **ValueMap** qualifiers.</span></span>

<span data-ttu-id="26aeb-105">屬性會作為陣列中的索引，並保留代表陣列中其中一個值的值。</span><span class="sxs-lookup"><span data-stu-id="26aeb-105">The property acts as an index into the array, holding a value that represents one of the values in the array.</span></span> <span data-ttu-id="26aeb-106">使用 MOF 程式碼，您可以有下列類型的值對應：</span><span class="sxs-lookup"><span data-stu-id="26aeb-106">Using MOF code, you can have the following types of value maps:</span></span>

-   <span data-ttu-id="26aeb-107">整數的陣列對應。</span><span class="sxs-lookup"><span data-stu-id="26aeb-107">Array mapping to an integer.</span></span>

    <span data-ttu-id="26aeb-108">您可以定義具有 **值** 限定詞的陣列，並將陣列直接連結至整數屬性，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="26aeb-108">You can define an array with the **Value** qualifier and link the array directly to an integer property, as shown in the following example:</span></span>

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    <span data-ttu-id="26aeb-109">在此範例中， **Status** 屬性值是以 **value** 定義之字串陣列中的索引。</span><span class="sxs-lookup"><span data-stu-id="26aeb-109">In this example, the **Status** property value is an index into the string array defined by **Value**.</span></span> <span data-ttu-id="26aeb-110">屬性只能採用對應至 **值** 陣列中序數位置的值減1。</span><span class="sxs-lookup"><span data-stu-id="26aeb-110">The property can only take on values that correspond to the ordinal positions in the **Value** array minus 1.</span></span> <span data-ttu-id="26aeb-111">例如，將 [ **狀態** ] 設定為 [1] 會對應至「錯誤」值。</span><span class="sxs-lookup"><span data-stu-id="26aeb-111">For example, setting **Status** to "1" maps to the "Error" value.</span></span> <span data-ttu-id="26aeb-112">索引屬性只能採用對應至 **值** 陣列中位置的值。</span><span class="sxs-lookup"><span data-stu-id="26aeb-112">The index property can take only values that correspond to positions in the **Value** array.</span></span> <span data-ttu-id="26aeb-113">例如，如果陣列有10個專案，則索引屬性可以是第0到第9個的故事，而不是30或177。</span><span class="sxs-lookup"><span data-stu-id="26aeb-113">For example, if the array has 10 entries, the index property can story 0 through 9, not 30 or 177.</span></span>

-   <span data-ttu-id="26aeb-114">對應至另一個對應至整數之陣列的陣列。</span><span class="sxs-lookup"><span data-stu-id="26aeb-114">Array mapping to another array mapping to an integer.</span></span>

    <span data-ttu-id="26aeb-115">如果您想要建立不使用序數系統計數的索引，請使用 **ValueMap** 辨識符號。</span><span class="sxs-lookup"><span data-stu-id="26aeb-115">If you wish to create an index that does not use an ordinal system of counting, use the **ValueMap** qualifier.</span></span> <span data-ttu-id="26aeb-116">**ValueMap** 辨識符號會設定另一個陣列來保存任意的索引編號系統，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="26aeb-116">The **ValueMap** qualifier sets up another array that holds an arbitrary index numbering system, as shown in the following example:</span></span>

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    <span data-ttu-id="26aeb-117">雖然您必須將 **ValueMap** 的值放在引號中，WMI 仍會將值視為整數。</span><span class="sxs-lookup"><span data-stu-id="26aeb-117">Although you must place the values of **ValueMap** in quotations, WMI considers the values integers.</span></span> <span data-ttu-id="26aeb-118">因此，在此範例中，您可以將 [ **狀態** ] 屬性設定為 [ **ValueMap** 集合： 1]、[3]、[99] 或 [0] 中的整數。</span><span class="sxs-lookup"><span data-stu-id="26aeb-118">Therefore, In this example you can set the **Status** property to an integer in the **ValueMap** set: 1, 3, 99, or 0.</span></span> <span data-ttu-id="26aeb-119">WMI 會將 **ValueMap** 字串陣列中序數位置的每個整數對應至 **值** 陣列中的對應位置。</span><span class="sxs-lookup"><span data-stu-id="26aeb-119">WMI maps each integer from an ordinal position in the **ValueMap** string array to a corresponding position in the **Value** array.</span></span> <span data-ttu-id="26aeb-120">例如，將 **狀態** 設定為0會對應到「未知」。</span><span class="sxs-lookup"><span data-stu-id="26aeb-120">For example, setting **Status** to 0 maps to "Unknown".</span></span>

-   <span data-ttu-id="26aeb-121">對應至另一個陣列對應至字串的陣列。</span><span class="sxs-lookup"><span data-stu-id="26aeb-121">Array mapping to another array mapping to a string.</span></span>

    <span data-ttu-id="26aeb-122">如果您不想要使用整數來編制陣列的索引，可以改為使用字串來保存陣列中的其中一個可能值。</span><span class="sxs-lookup"><span data-stu-id="26aeb-122">If you do not want to use an integer to index your array, you can instead use a string to hold one of the possible values in your array.</span></span> <span data-ttu-id="26aeb-123">若要這樣做，您必須定義同時包含字串的 **值** 和 **ValueMap** 陣列，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="26aeb-123">To do so, you must define both a **Value** and **ValueMap** array that both contain strings, as shown in the following example:</span></span>

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    <span data-ttu-id="26aeb-124">使用字串屬性時，屬性的實際可允許值為 **ValueMap** 陣列中的專案。</span><span class="sxs-lookup"><span data-stu-id="26aeb-124">With a string property, the actual allowable values of the property are the entries in the **ValueMap** array.</span></span> <span data-ttu-id="26aeb-125">例如，您可以將 **狀態** 設定為「確定」或「未知」。</span><span class="sxs-lookup"><span data-stu-id="26aeb-125">For example, you can set **Status** to "OK" or "Unknown".</span></span>

<span data-ttu-id="26aeb-126">應用程式是由應用程式以實用的方式利用對應。</span><span class="sxs-lookup"><span data-stu-id="26aeb-126">It is up to the application to take advantage of mappings in a useful way.</span></span> <span data-ttu-id="26aeb-127">由提供者來強制執行合法的值範圍。</span><span class="sxs-lookup"><span data-stu-id="26aeb-127">It is up to the provider to enforce a legal range of values.</span></span>

## <a name="remarks"></a><span data-ttu-id="26aeb-128">備註</span><span class="sxs-lookup"><span data-stu-id="26aeb-128">Remarks</span></span>

<span data-ttu-id="26aeb-129">在決定是否要使用 **ValueMap** / **值** 或 **點陣圖** / **BitValues** 限定詞時，判斷是否有任何指定的值可能會同時發生。</span><span class="sxs-lookup"><span data-stu-id="26aeb-129">In deciding whether to use the **ValueMap**/**Value** or **BitMap**/**BitValues** qualifiers, determine whether any of the values being indicated could occur concurrently.</span></span> <span data-ttu-id="26aeb-130">如果有多個並行值可以存在，您必須使用 **BitMap** / **BitValues**。</span><span class="sxs-lookup"><span data-stu-id="26aeb-130">If multiple concurrent values can exist, you must use **BitMap**/**BitValues**.</span></span> <span data-ttu-id="26aeb-131">如果所有值都是互斥的，您應該使用 **ValueMap** / **值** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="26aeb-131">If all the values are mutually exclusive, you should use the **ValueMap**/**Value** qualifiers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26aeb-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="26aeb-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26aeb-133">點陣圖和 BitValues</span><span class="sxs-lookup"><span data-stu-id="26aeb-133">BitMap and BitValues</span></span>](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



