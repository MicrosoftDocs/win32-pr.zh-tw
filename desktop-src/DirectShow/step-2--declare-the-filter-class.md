---
description: 步驟 2：
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: 步驟 2： 宣告篩選類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ddfe28b7f31238089c331b319621787aef49f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975825"
---
# <a name="step-2-declare-the-filter-class"></a><span data-ttu-id="c1637-104">步驟 2：</span><span class="sxs-lookup"><span data-stu-id="c1637-104">Step 2.</span></span> <span data-ttu-id="c1637-105">宣告篩選類別</span><span class="sxs-lookup"><span data-stu-id="c1637-105">Declare the Filter Class</span></span>

<span data-ttu-id="c1637-106">這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟2。</span><span class="sxs-lookup"><span data-stu-id="c1637-106">This is step 2 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="c1637-107">從宣告繼承基類的 c + + 類別開始：</span><span class="sxs-lookup"><span data-stu-id="c1637-107">Start by declaring a C++ class that inherits the base class:</span></span>


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



<span data-ttu-id="c1637-108">每個篩選準則類別都有相關聯的釘選類別。</span><span class="sxs-lookup"><span data-stu-id="c1637-108">Each of the filter classes has associated pin classes.</span></span> <span data-ttu-id="c1637-109">視篩選準則的特定需求而定，您可能需要覆寫釘選類別。</span><span class="sxs-lookup"><span data-stu-id="c1637-109">Depending on the specific needs of your filter, you might need to override the pin classes.</span></span> <span data-ttu-id="c1637-110">在 **CTransformFilter** 的情況下，釘選將大部分的工作委派給篩選器，因此您可能不需要覆寫 pin。</span><span class="sxs-lookup"><span data-stu-id="c1637-110">In the case of **CTransformFilter**, the pins delegate most of their work to the filter, so you probably don't need to override the pins.</span></span>

<span data-ttu-id="c1637-111">您必須為篩選產生唯一的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="c1637-111">You must generate a unique CLSID for the filter.</span></span> <span data-ttu-id="c1637-112">您可以使用 Guidgen 或 Uuidgen.exe 公用程式;絕對不要複製現有的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c1637-112">You can use the Guidgen or Uuidgen utility; never copy an existing GUID.</span></span> <span data-ttu-id="c1637-113">有幾種方式可以宣告 CLSID。</span><span class="sxs-lookup"><span data-stu-id="c1637-113">There are several ways to declare a CLSID.</span></span> <span data-ttu-id="c1637-114">下列範例會使用 **定義 \_ GUID** 宏：</span><span class="sxs-lookup"><span data-stu-id="c1637-114">The following example uses the **DEFINE\_GUID** macro:</span></span>


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



<span data-ttu-id="c1637-115">接下來，撰寫篩選準則的函式方法：</span><span class="sxs-lookup"><span data-stu-id="c1637-115">Next, write a constructor method for the filter:</span></span>


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



<span data-ttu-id="c1637-116">請注意， [**CTransformFilter**](ctransformfilter-ctransformfilter.md) 函式的其中一個參數是稍早定義的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="c1637-116">Notice that one of the parameters to the [**CTransformFilter**](ctransformfilter-ctransformfilter.md) constructor is the CLSID defined earlier.</span></span>

<span data-ttu-id="c1637-117">下一 [步：步驟3。支援媒體類型的協商](step-3--support-media-type-negotiation.md)。</span><span class="sxs-lookup"><span data-stu-id="c1637-117">Next: [Step 3. Support Media Type Negotiation](step-3--support-media-type-negotiation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1637-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1637-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1637-119">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="c1637-119">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



