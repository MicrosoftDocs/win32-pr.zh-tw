---
title: 類型指標
description: 實際屬性會遵循屬性識別碼/位移配對屬性集值的表格。 每個屬性都會儲存為 DWORD，後面接著資料類型值。
ms.assetid: 8523458b-8b1b-4e9f-8f96-d7601e57675c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8383a860f07e908b72a7b25091f3cc2e280e4407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023837"
---
# <a name="type-indicators"></a><span data-ttu-id="f1c10-104">類型指標</span><span class="sxs-lookup"><span data-stu-id="f1c10-104">Type Indicators</span></span>

<span data-ttu-id="f1c10-105">實際屬性會遵循屬性識別碼/位移配對屬性集值的表格。</span><span class="sxs-lookup"><span data-stu-id="f1c10-105">The actual properties follow the table of Property Identifiers/Offset Pairs property set values.</span></span> <span data-ttu-id="f1c10-106">每個屬性都會儲存為 **DWORD**，後面接著資料類型值。</span><span class="sxs-lookup"><span data-stu-id="f1c10-106">Each property is stored as a **DWORD**, followed by the data type value.</span></span>

<span data-ttu-id="f1c10-107">類型指標和其相關聯的值會在 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構中描述。</span><span class="sxs-lookup"><span data-stu-id="f1c10-107">Type indicators and their associated values are described in the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="f1c10-108">所有類型/值組都必須從32位界限開始。</span><span class="sxs-lookup"><span data-stu-id="f1c10-108">All Type/Value pairs must begin on a 32-bit boundary.</span></span> <span data-ttu-id="f1c10-109">因此，值之後可能會有 null 位元組，以在32位界限上對齊後續的配對。</span><span class="sxs-lookup"><span data-stu-id="f1c10-109">Thus, values may be followed with null bytes to align the subsequent pair on a 32-bit boundary.</span></span>

<span data-ttu-id="f1c10-110">下列範例程式碼會根據指定的位元組計數，計算在32位界限上對齊所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="f1c10-110">The following example code calculates how many bytes are required to align on a 32-bit boundary, given a count of bytes.</span></span>


```C++
cbAdd = (((cbCurrent + 3) >> 2) << 2) - cbCurrent ;
```



<span data-ttu-id="f1c10-111">在值的向量內，每次重複小於32位的簡單純量值，都必須符合其自然對齊，而不是32位的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="f1c10-111">Within a vector of values, each repetition of a simple scalar value smaller than 32 bits must align with its natural alignment rather than with a 32-bit alignment.</span></span> <span data-ttu-id="f1c10-112">在實務上，這僅適用于型 **別 \_ VT UI1**、 **vt \_ UI2**、 **vt \_ I2** 和 **vt \_ BOOL** (，其中有一個位元組或雙位元組的自然對齊) 。</span><span class="sxs-lookup"><span data-stu-id="f1c10-112">In practice, this is only significant for types **VT\_UI1**, **VT\_UI2**, **VT\_I2**, and **VT\_BOOL** (which have one-byte or two-byte natural alignment).</span></span> <span data-ttu-id="f1c10-113">所有其他類型都有四個位元組的自然對齊。</span><span class="sxs-lookup"><span data-stu-id="f1c10-113">All other types have four-byte natural alignment.</span></span> <span data-ttu-id="f1c10-114">某些類型（例如 **VT \_ R8**）實際上有8個位元組的自然對齊，但是會儲存為具有四位元組對齊的方式。</span><span class="sxs-lookup"><span data-stu-id="f1c10-114">Some types, for example, **VT\_R8**, actually have 8-byte natural alignment, but are stored as if they have four-byte alignment.</span></span>

<span data-ttu-id="f1c10-115">型別指標 **vt \_** 的 \| **vt \_ 向量** 的屬性值包含：</span><span class="sxs-lookup"><span data-stu-id="f1c10-115">A property value with type indicator **VT\_I2** \| **VT\_VECTOR** would include:</span></span>

-   <span data-ttu-id="f1c10-116">**DWORD** 元素計數。</span><span class="sxs-lookup"><span data-stu-id="f1c10-116">A **DWORD** element count.</span></span>
-   <span data-ttu-id="f1c10-117">封裝的雙位元組整數，其之間沒有 null 填補的序列。</span><span class="sxs-lookup"><span data-stu-id="f1c10-117">A sequence of packed two-byte integers with no null padding between them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1c10-118">任何儲存為 vector property 元素一部分的32位元數目或屬性類型，也必須對齊32位。</span><span class="sxs-lookup"><span data-stu-id="f1c10-118">Any 32-bit counts or property types that are stored as a part of a vector property element must also be 32-bit aligned.</span></span>

 

<span data-ttu-id="f1c10-119">類型識別碼 **VT \_ LPSTR** \| **vt \_ 向量** 的屬性值包含：</span><span class="sxs-lookup"><span data-stu-id="f1c10-119">A property value of type identifier **VT\_LPSTR** \| **VT\_VECTOR** would include:</span></span>

-   <span data-ttu-id="f1c10-120">Dword **元素計數** (**dword** *cElems*) 。</span><span class="sxs-lookup"><span data-stu-id="f1c10-120">A **DWORD** element count (**DWORD** *cElems*).</span></span>
-   <span data-ttu-id="f1c10-121">字串序列 (**char** *rgch \[ \]*) ，每個字串前面都加上長度計數 **DWORD** ，而且後面可能接著 null 填補以舍入至32位界限。</span><span class="sxs-lookup"><span data-stu-id="f1c10-121">A sequence of strings (**char** *rgch\[\]*), each preceded by a length-count **DWORD** and possibly followed by null padding to round to a 32-bit boundary.</span></span>

 

 