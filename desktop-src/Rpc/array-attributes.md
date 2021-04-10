---
title: 陣列屬性
description: C 語言中的陣列和指標之間有接近的關聯性。
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed669a2a81528afa84b41a1be25a0c84f70fbe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682891"
---
# <a name="array-attributes"></a><span data-ttu-id="13101-103">陣列屬性</span><span class="sxs-lookup"><span data-stu-id="13101-103">Array Attributes</span></span>

<span data-ttu-id="13101-104">C 語言中的陣列和指標之間有接近的關聯性。</span><span class="sxs-lookup"><span data-stu-id="13101-104">There is a close relationship between arrays and pointers in the C language.</span></span> <span data-ttu-id="13101-105">以參數形式傳遞至函式時，會將陣列名稱稱視為陣列第一個元素的指標，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="13101-105">When passed as a parameter to a function, an array name is treated as a pointer to the first element of the array, as shown in the following example:</span></span>


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



<span data-ttu-id="13101-106">在本機呼叫中，您可以使用指標參數來建立3到記憶體的內容，並檢查其他位址的內容：</span><span class="sxs-lookup"><span data-stu-id="13101-106">In a local call, you can use the pointer parameter to march through memory and examine the contents of other addresses:</span></span>


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



<span data-ttu-id="13101-107">當用戶端將指標傳遞至遠端程式時，用戶端存根會將指標和其指向的資料都傳送出去。</span><span class="sxs-lookup"><span data-stu-id="13101-107">When a client passes a pointer to a remote procedure, the client stub transmits both the pointer and the data it points to.</span></span> <span data-ttu-id="13101-108">除非指標受限於其對應的資料，否則所有用戶端的記憶體都必須在每次遠端呼叫時傳輸。</span><span class="sxs-lookup"><span data-stu-id="13101-108">Unless the pointer is restricted to its corresponding data, all the client's memory must be transmitted with every remote call.</span></span> <span data-ttu-id="13101-109">藉由在介面定義中強制強型別，MIDL 會將用戶端存根處理限制為對應至指定之指標的資料。</span><span class="sxs-lookup"><span data-stu-id="13101-109">By enforcing strong typing in the interface definition, MIDL limits client-stub processing to the data that corresponds to the specified pointer.</span></span>

<span data-ttu-id="13101-110">陣列的大小和傳送至遠端電腦的陣列元素範圍可以是常數或變數。</span><span class="sxs-lookup"><span data-stu-id="13101-110">The size of the array and the range of array elements transmitted to the remote computer can be constant or variable.</span></span> <span data-ttu-id="13101-111">當這些值是變數，因此在執行時間決定時，您必須使用 IDL 檔案中的屬性來指定要傳輸的陣列元素數目。</span><span class="sxs-lookup"><span data-stu-id="13101-111">When these values are variable, and thus determined at run time, you must use attributes in the IDL file to specify how many array elements to transmit.</span></span> <span data-ttu-id="13101-112">下列 MIDL 屬性支援陣列界限。</span><span class="sxs-lookup"><span data-stu-id="13101-112">The following MIDL attributes support array bounds.</span></span>



| <span data-ttu-id="13101-113">屬性</span><span class="sxs-lookup"><span data-stu-id="13101-113">Attribute</span></span>                             | <span data-ttu-id="13101-114">描述</span><span class="sxs-lookup"><span data-stu-id="13101-114">Description</span></span>                                             | <span data-ttu-id="13101-115">預設</span><span class="sxs-lookup"><span data-stu-id="13101-115">Default</span></span> |
|---------------------------------------|---------------------------------------------------------|---------|
| <span data-ttu-id="13101-116">\[[**第一個 \_ 是**](/windows/desktop/Midl/first-is)\]</span><span class="sxs-lookup"><span data-stu-id="13101-116">\[ [**first\_is**](/windows/desktop/Midl/first-is)\]</span></span>   | <span data-ttu-id="13101-117">已傳送之第一個陣列元素的索引。</span><span class="sxs-lookup"><span data-stu-id="13101-117">Index of the first array element transmitted.</span></span>           | <span data-ttu-id="13101-118">0</span><span class="sxs-lookup"><span data-stu-id="13101-118">0</span></span>       |
| <span data-ttu-id="13101-119">\[[ **last \_**](/windows/desktop/Midl/last-is)\]</span><span class="sxs-lookup"><span data-stu-id="13101-119">\[ [**last\_is**](/windows/desktop/Midl/last-is)\]</span></span>     | <span data-ttu-id="13101-120">最後傳送的陣列元素索引。</span><span class="sxs-lookup"><span data-stu-id="13101-120">Index of the last array element transmitted.</span></span>            | \-      |
| <span data-ttu-id="13101-121">\[[**長度 \_ 為**](/windows/desktop/Midl/length-is)\]</span><span class="sxs-lookup"><span data-stu-id="13101-121">\[ [**length\_is**](/windows/desktop/Midl/length-is)\]</span></span> | <span data-ttu-id="13101-122">已傳送的陣列元素總數。</span><span class="sxs-lookup"><span data-stu-id="13101-122">Total number of array elements transmitted.</span></span>             | \-      |
| <span data-ttu-id="13101-123">\[[**最大值 \_ 為**](/windows/desktop/Midl/max-is)\]</span><span class="sxs-lookup"><span data-stu-id="13101-123">\[ [**max\_is**](/windows/desktop/Midl/max-is)\]</span></span>       | <span data-ttu-id="13101-124">最大有效陣列索引值。</span><span class="sxs-lookup"><span data-stu-id="13101-124">Highest valid array index value.</span></span>                        | \-      |
| <span data-ttu-id="13101-125">\[[**最小值 \_ 為**](/windows/desktop/Midl/min-is)\]</span><span class="sxs-lookup"><span data-stu-id="13101-125">\[ [**min\_is**](/windows/desktop/Midl/min-is)\]</span></span>       | <span data-ttu-id="13101-126">最低有效陣列索引值。</span><span class="sxs-lookup"><span data-stu-id="13101-126">Lowest valid array index value.</span></span>                         | <span data-ttu-id="13101-127">0</span><span class="sxs-lookup"><span data-stu-id="13101-127">0</span></span>       |
| <span data-ttu-id="13101-128">\[[**大小 \_ 為**](/windows/desktop/Midl/size-is)\]</span><span class="sxs-lookup"><span data-stu-id="13101-128">\[ [**size\_is**](/windows/desktop/Midl/size-is)\]</span></span>     | <span data-ttu-id="13101-129">配置給陣列的陣列元素總數。</span><span class="sxs-lookup"><span data-stu-id="13101-129">Total number of array elements allocated for the array.</span></span> | \-      |



 

> [!Note]  
> <span data-ttu-id="13101-130">**最小值 \_ 是** 不會在 RPC 中執行的屬性。</span><span class="sxs-lookup"><span data-stu-id="13101-130">The **min\_is** attribute is not implemented in RPC.</span></span> <span data-ttu-id="13101-131">最小陣列索引一律會被視為零。</span><span class="sxs-lookup"><span data-stu-id="13101-131">The minimum array index is always treated as zero.</span></span>

 

 

 