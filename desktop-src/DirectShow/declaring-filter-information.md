---
description: 宣告篩選資訊
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: 宣告篩選資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8975217f1b7746b26dc5dd16ce9f4e7f694f44bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688383"
---
# <a name="declaring-filter-information"></a><span data-ttu-id="b366e-103">宣告篩選資訊</span><span class="sxs-lookup"><span data-stu-id="b366e-103">Declaring Filter Information</span></span>

<span data-ttu-id="b366e-104">第一個步驟是視需要宣告篩選資訊。</span><span class="sxs-lookup"><span data-stu-id="b366e-104">The first step is to declare the filter information, if needed.</span></span> <span data-ttu-id="b366e-105">DirectShow 定義了下列描述篩選、釘選和媒體類型的結構：</span><span class="sxs-lookup"><span data-stu-id="b366e-105">DirectShow defines the following structures for describing filters, pins, and media types:</span></span>



| <span data-ttu-id="b366e-106">結構</span><span class="sxs-lookup"><span data-stu-id="b366e-106">Structure</span></span>                                               | <span data-ttu-id="b366e-107">Description</span><span class="sxs-lookup"><span data-stu-id="b366e-107">Description</span></span>             |
|---------------------------------------------------------|-------------------------|
| [<span data-ttu-id="b366e-108">**AMOVIESETUP \_ 篩選**</span><span class="sxs-lookup"><span data-stu-id="b366e-108">**AMOVIESETUP\_FILTER**</span></span>](amoviesetup-filter.md)       | <span data-ttu-id="b366e-109">描述篩選。</span><span class="sxs-lookup"><span data-stu-id="b366e-109">Describes a filter.</span></span>     |
| [<span data-ttu-id="b366e-110">**AMOVIESETUP \_ 釘選**</span><span class="sxs-lookup"><span data-stu-id="b366e-110">**AMOVIESETUP\_PIN**</span></span>](amoviesetup-pin.md)             | <span data-ttu-id="b366e-111">描述 pin。</span><span class="sxs-lookup"><span data-stu-id="b366e-111">Describes a pin.</span></span>        |
| [<span data-ttu-id="b366e-112">**AMOVIESETUP \_ 媒體媒體**</span><span class="sxs-lookup"><span data-stu-id="b366e-112">**AMOVIESETUP\_MEDIATYPE**</span></span>](amoviesetup-mediatype.md) | <span data-ttu-id="b366e-113">描述媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b366e-113">Describes a media type.</span></span> |



 

<span data-ttu-id="b366e-114">這些結構是嵌套的。</span><span class="sxs-lookup"><span data-stu-id="b366e-114">These structures are nested.</span></span> <span data-ttu-id="b366e-115">**AMOVEIESETUP \_ 篩選** 結構有指向 **AMOVIESETUP \_ 釘** 選結構陣列的指標，其中每個結構都有指向 **AMOVEIESETUP \_ 媒體** 陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="b366e-115">The **AMOVEIESETUP\_FILTER** structure has a pointer to an array of **AMOVIESETUP\_PIN** structures, and each of these has a pointer to an array of **AMOVEIESETUP\_MEDIATYPE** structures.</span></span> <span data-ttu-id="b366e-116">這些結構會結合在一起，以提供足夠的資訊給 [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) 介面，以找出篩選。</span><span class="sxs-lookup"><span data-stu-id="b366e-116">Taken together, these structures provide enough information for the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface to locate a filter.</span></span> <span data-ttu-id="b366e-117">它們並不是篩選的完整描述。</span><span class="sxs-lookup"><span data-stu-id="b366e-117">They are not a complete description of a filter.</span></span> <span data-ttu-id="b366e-118">例如，如果篩選器會建立多個相同 pin 的實例，您應該只針對該 pin 宣告一個 [**AMOVIESETUP \_ 釘**](amoviesetup-pin.md) 選結構。</span><span class="sxs-lookup"><span data-stu-id="b366e-118">For example, if the filter creates multiple instances of the same pin, you should declare only one [**AMOVIESETUP\_PIN**](amoviesetup-pin.md) structure for that pin.</span></span> <span data-ttu-id="b366e-119">此外，不需要篩選以支援其所註冊的每個媒體類型組合;也不需要註冊每個支援的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b366e-119">Also, a filter is not required to support every combination of media types that it registers; nor is required to register every media type that it supports.</span></span>

<span data-ttu-id="b366e-120">將設定結構宣告為 DLL 內的全域變數。</span><span class="sxs-lookup"><span data-stu-id="b366e-120">Declare the set-up structures as global variables within your DLL.</span></span> <span data-ttu-id="b366e-121">下列範例顯示具有一個輸出圖釘的篩選準則：</span><span class="sxs-lookup"><span data-stu-id="b366e-121">The following example shows a filter with one output pin:</span></span>


```C++
static const WCHAR g_wszName[] = L"Some Filter";

AMOVIESETUP_MEDIATYPE sudMediaTypes[] = {
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB24 },
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB32 },
};

AMOVIESETUP_PIN sudOutputPin = {
    L"",            // Obsolete, not used.
    FALSE,          // Is this pin rendered?
    TRUE,           // Is it an output pin?
    FALSE,          // Can the filter create zero instances?
    FALSE,          // Does the filter create multiple instances?
    &GUID_NULL,     // Obsolete.
    NULL,           // Obsolete.
    2,              // Number of media types.
    sudMediaTypes   // Pointer to media types.
};

AMOVIESETUP_FILTER sudFilterReg = {
    &CLSID_SomeFilter,      // Filter CLSID.
    g_wszName,              // Filter name.
    MERIT_NORMAL,           // Merit.
    1,                      // Number of pin types.
    &sudOutputPin           // Pointer to pin information.
};
```



<span data-ttu-id="b366e-122">篩選名稱會宣告為靜態全域變數，因為它將會再次用於其他地方。</span><span class="sxs-lookup"><span data-stu-id="b366e-122">The filter name is declared as a static global variable, because it will be used again elsewhere.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b366e-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="b366e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b366e-124">如何註冊 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="b366e-124">How to Register DirectShow Filters</span></span>](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



