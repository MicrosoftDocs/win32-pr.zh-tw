---
description: 這是連結至具有點陣圖和 BitValue 限定詞之屬性的整數。
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: 點陣圖和 BitValue 限定詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60dd6b4ad5866ddc79c960316757700bc5fbb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969312"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a><span data-ttu-id="10fee-103">點陣圖和 BitValue 限定詞</span><span class="sxs-lookup"><span data-stu-id="10fee-103">BitMap and BitValue Qualifiers</span></span>

<span data-ttu-id="10fee-104">點陣圖是連結至具有 **點陣圖** 和 **BitValue** 限定詞之屬性的整數。</span><span class="sxs-lookup"><span data-stu-id="10fee-104">A bitmap is an integer linked to a property with the **BitMap** and **BitValue** qualifiers.</span></span> <span data-ttu-id="10fee-105">屬性值的每個位都會作為 **BitValue** 清單中值陣列的索引。</span><span class="sxs-lookup"><span data-stu-id="10fee-105">Each bit of the property value acts as an index into the array of values in the **BitValue** list.</span></span> <span data-ttu-id="10fee-106">因為屬性值中的多個位可以同時為 "on"，所以您可以使用單一屬性值來指出多個並行值。</span><span class="sxs-lookup"><span data-stu-id="10fee-106">Because multiple bits in the property value can be "on" at the same time, it is possible to use a single property value to indicate multiple concurrent values.</span></span>

<span data-ttu-id="10fee-107">例如，下列 MOF 程式碼範例會建立具有 **點陣圖** 和 **BitValues** 限定詞的 [內容 **類型**] 屬性。</span><span class="sxs-lookup"><span data-stu-id="10fee-107">For example, the following MOF code example establishes the **FileType** property as having the **BitMap** and **BitValues** qualifiers.</span></span> <span data-ttu-id="10fee-108">它會進一步建立低序位位 (位0，) 對應至值「唯讀」。</span><span class="sxs-lookup"><span data-stu-id="10fee-108">It further establishes that the low-order bit (bit 0) corresponds to the value "Read Only".</span></span> <span data-ttu-id="10fee-109">下個位 (位 1) 對應至「隱藏」，依此類推。</span><span class="sxs-lookup"><span data-stu-id="10fee-109">The next bit (bit 1) corresponds to "Hidden", and so on.</span></span> <span data-ttu-id="10fee-110"> (並非所有的位都必須是很重要的。</span><span class="sxs-lookup"><span data-stu-id="10fee-110">(Not all bits must be significant.</span></span> <span data-ttu-id="10fee-111">在這八位系統中，這兩個高序位位（6和7）沒有任何意義。 ) </span><span class="sxs-lookup"><span data-stu-id="10fee-111">In this eight-bit system, the two high-order bits, 6 and 7, have no significance.)</span></span>

``` syntax
[BitMap("0","1","2","3","4","5"),
 BitValues("Read Only",
           "Hidden",
           "System",
           "Volume Label",
           "Subdirectory",
           "Archive")]
byte FileType;
```

<span data-ttu-id="10fee-112">如果 [內容 **類型** ] 屬性報告值 7 (bits 0000 0111) ，則檔案為「唯讀」、「系統」和「隱藏」。</span><span class="sxs-lookup"><span data-stu-id="10fee-112">If the **FileType** property reports the value 7 (bits 0000 0111), the file is "Read Only", "System", and "Hidden".</span></span> <span data-ttu-id="10fee-113">如果 [內容 **類型** ] 屬性報告值 18 (0x12，bits 0001 0010) ，它是隱藏的子目錄。</span><span class="sxs-lookup"><span data-stu-id="10fee-113">If the **FileType** property reports the value 18 (0x12, bits 0001 0010), it is a hidden subdirectory.</span></span>

<span data-ttu-id="10fee-114">使用 MOF 程式碼有兩種不同類型的點陣圖：</span><span class="sxs-lookup"><span data-stu-id="10fee-114">There are two different types of bitmaps using MOF code:</span></span>

-   <span data-ttu-id="10fee-115">以低序位位開頭的連續有效位數 (位 0) </span><span class="sxs-lookup"><span data-stu-id="10fee-115">Consecutive significant bits beginning with the low-order bit (bit 0)</span></span>

    <span data-ttu-id="10fee-116">您可以定義位值陣列，而不需要明確地指定有效位數（如果有效位數以低序位位開頭 (位) 0），並在不中斷 **BitValue** 陣列中的所有專案的情況下繼續進行。</span><span class="sxs-lookup"><span data-stu-id="10fee-116">You can define an array of bit values without explicitly specifying the significant bits if the significant bits begin with the low-order bit (bit 0) and progress upward without interruption through all items in the **BitValue** array.</span></span> <span data-ttu-id="10fee-117">下列 MOF 程式碼範例會執行與上一個範例相同的功能。</span><span class="sxs-lookup"><span data-stu-id="10fee-117">The following MOF code example performs the same function as the previous example.</span></span>

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   <span data-ttu-id="10fee-118">之前有點不重要的位</span><span class="sxs-lookup"><span data-stu-id="10fee-118">Significant bit preceded by a non-significant bit</span></span>

    <span data-ttu-id="10fee-119">如果低序位位沒有意義，或有效位的序列不連續，您必須同時指定 **BitMap** 和 **BitValues** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="10fee-119">If the low-order bit is insignificant, or the sequence of significant bits is not continuous, you must specify both the **BitMap** and **BitValues** qualifiers.</span></span> <span data-ttu-id="10fee-120">下列 MOF 程式碼範例會示範低序位位不重要的情況，以及有效位序列中的間隙。</span><span class="sxs-lookup"><span data-stu-id="10fee-120">The following MOF code example shows a situation in which the low-order bit is not significant and there is a gap in the sequence of significant bits.</span></span>

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    <span data-ttu-id="10fee-121">在此情況下，設定低序位位 (位 0) 沒有任何意義，而且會被忽略。</span><span class="sxs-lookup"><span data-stu-id="10fee-121">In this case, setting the low-order bit (bit 0) has no significance and is ignored.</span></span> <span data-ttu-id="10fee-122">但是，設定 bit 1 (0x2) 表示此電子郵件訊息已標示為待處理，設定位 4 (0x8) 指出當電子郵件訊息到達收件者的信箱時，傳送回條應傳送給寄件者，並設定位 5 (0x10) 指定當收件者開啟電子郵件訊息時，應將讀取回條傳送給傳送者。</span><span class="sxs-lookup"><span data-stu-id="10fee-122">However, setting bit 1 (0x2) indicates that this email message is flagged for follow up, setting bit 4 (0x8) indicates that a delivery receipt should be sent to the sender when the email message has arrived at the recipient's mailbox, and setting bit 5 (0x10) specifies that a read receipt should be sent to the sender when the email message is opened by the recipient.</span></span> <span data-ttu-id="10fee-123">將這三個有效位數全部設定 (0x1A) 指定電子郵件訊息的三個條件。</span><span class="sxs-lookup"><span data-stu-id="10fee-123">Setting all three significant bits (0x1A) specifies all three conditions for the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="10fee-124">備註</span><span class="sxs-lookup"><span data-stu-id="10fee-124">Remarks</span></span>

<span data-ttu-id="10fee-125">在決定是否要使用 **BitMap** / **BitValues** 或 **ValueMap** / **值** 限定詞時，請判斷是否有任何指定的值可能會同時發生。</span><span class="sxs-lookup"><span data-stu-id="10fee-125">In deciding whether to use the **BitMap**/**BitValues** or **ValueMap**/**Values** qualifiers, determine whether any of the values being indicated could occur concurrently.</span></span> <span data-ttu-id="10fee-126">如果有多個並行值可以存在，您必須使用 **BitMap** / **BitValues**。</span><span class="sxs-lookup"><span data-stu-id="10fee-126">If multiple concurrent values can exist, you must use **BitMap**/**BitValues**.</span></span> <span data-ttu-id="10fee-127">如果所有值都是互斥的，您應該使用 **ValueMap** / **值** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="10fee-127">If all the values are mutually exclusive, you should use the **ValueMap**/**Values** qualifiers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10fee-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="10fee-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10fee-129">ValueMap 和值限定詞</span><span class="sxs-lookup"><span data-stu-id="10fee-129">ValueMap and Value Qualifiers</span></span>](value-map.md)
</dt> </dl>

 

 



