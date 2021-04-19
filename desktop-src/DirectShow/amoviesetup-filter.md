---
description: AMOVIESETUP \_ 篩選結構包含註冊篩選的資訊。
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: 'AMOVIESETUP_FILTER 結構 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMOVIESETUP_FILTER
api_type:
- HeaderDef
api_location:
- combase.h
ms.openlocfilehash: 55a225185733a822591d8f93c2eca3674d51a340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980175"
---
# <a name="amoviesetup_filter-structure"></a><span data-ttu-id="b292f-103">AMOVIESETUP \_ 篩選結構</span><span class="sxs-lookup"><span data-stu-id="b292f-103">AMOVIESETUP\_FILTER structure</span></span>

<span data-ttu-id="b292f-104">**AMOVIESETUP \_ 篩選** 結構包含註冊篩選的資訊。</span><span class="sxs-lookup"><span data-stu-id="b292f-104">The **AMOVIESETUP\_FILTER** structure contains information for registering a filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b292f-105">語法</span><span class="sxs-lookup"><span data-stu-id="b292f-105">Syntax</span></span>


```C++
typedef struct _AMOVIESETUP_FILTER {
  const  CLSID           *clsID;
  const  WCHAR           *strName;
  DWORD                  dwMerit;
  UINT                   nPins;
  const  AMOVIESETUP_PIN *lpPin;
} AMOVIESETUP_FILTER, *PAMOVIESETUP_FILTER, *FAR LPAMOVIESETUP_FILTER;
```



## <a name="members"></a><span data-ttu-id="b292f-106">成員</span><span class="sxs-lookup"><span data-stu-id="b292f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b292f-107">**Clsid**</span><span class="sxs-lookup"><span data-stu-id="b292f-107">**clsID**</span></span>
</dt> <dd>

<span data-ttu-id="b292f-108">篩選準則的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="b292f-108">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="b292f-109">**strName**</span><span class="sxs-lookup"><span data-stu-id="b292f-109">**strName**</span></span>
</dt> <dd>

<span data-ttu-id="b292f-110">篩選的名稱。</span><span class="sxs-lookup"><span data-stu-id="b292f-110">Name of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="b292f-111">**dwMerit**</span><span class="sxs-lookup"><span data-stu-id="b292f-111">**dwMerit**</span></span>
</dt> <dd>

<span data-ttu-id="b292f-112">篩選業績。</span><span class="sxs-lookup"><span data-stu-id="b292f-112">Filter merit.</span></span> <span data-ttu-id="b292f-113">在建立篩選圖形時，由 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 介面使用。</span><span class="sxs-lookup"><span data-stu-id="b292f-113">Used by the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface when constructing a filter graph.</span></span> <span data-ttu-id="b292f-114">如需相關值的清單，請參閱「 [業績](merit.md)」。</span><span class="sxs-lookup"><span data-stu-id="b292f-114">For a list of merit values, see [Merit](merit.md).</span></span>

</dd> <dt>

<span data-ttu-id="b292f-115">**nPins**</span><span class="sxs-lookup"><span data-stu-id="b292f-115">**nPins**</span></span>
</dt> <dd>

<span data-ttu-id="b292f-116">*LpPin* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="b292f-116">Number of elements in the *lpPin* array.</span></span> <span data-ttu-id="b292f-117">如果 *lpPin* 為 **Null**，請將此成員設定為零。</span><span class="sxs-lookup"><span data-stu-id="b292f-117">If *lpPin* is **NULL**, set this member to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b292f-118">**lpPin**</span><span class="sxs-lookup"><span data-stu-id="b292f-118">**lpPin**</span></span>
</dt> <dd>

<span data-ttu-id="b292f-119">[**AMOVIESETUP \_ 釘**](amoviesetup-pin.md)選結構陣列的指標，大小為 *nPins*。</span><span class="sxs-lookup"><span data-stu-id="b292f-119">Pointer to an array of [**AMOVIESETUP\_PIN**](amoviesetup-pin.md) structures, of size *nPins*.</span></span> <span data-ttu-id="b292f-120">這個陣列的每個成員都描述篩選上的釘選。</span><span class="sxs-lookup"><span data-stu-id="b292f-120">Each member of this array describes a pin on the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b292f-121">備註</span><span class="sxs-lookup"><span data-stu-id="b292f-121">Remarks</span></span>

<span data-ttu-id="b292f-122">如需使用此結構的詳細資訊，請參閱 [如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="b292f-122">For information about using this structure, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="b292f-123">此結構僅適用于在預設篩選準則分類 (CLSID LegacyAmFilterCategory) 中註冊的篩選準則 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b292f-123">Use this structure only for filters that are registered in the default filter category (CLSID\_LegacyAmFilterCategory).</span></span> <span data-ttu-id="b292f-124">若要在不同類別中註冊篩選準則，請使用 [**IFilterMapper2：： RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) 方法，如實 [DllRegisterServer](implementing-dllregisterserver.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="b292f-124">To register a filter in a different category, use the [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method, as described in [Implementing DllRegisterServer](implementing-dllregisterserver.md).</span></span>

> [!Note]  
> <span data-ttu-id="b292f-125">Combase 標頭檔隨附于 [DirectShow 基類](directshow-base-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="b292f-125">The header file combase.h is provided with the [DirectShow Base Classes](directshow-base-classes.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b292f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b292f-126">Requirements</span></span>



| <span data-ttu-id="b292f-127">需求</span><span class="sxs-lookup"><span data-stu-id="b292f-127">Requirement</span></span> | <span data-ttu-id="b292f-128">值</span><span class="sxs-lookup"><span data-stu-id="b292f-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b292f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="b292f-129">Header</span></span><br/> | <dl> <span data-ttu-id="b292f-130"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b292f-130"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b292f-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b292f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b292f-132">DirectShow 結構</span><span class="sxs-lookup"><span data-stu-id="b292f-132">DirectShow Structures</span></span>](directshow-structures.md)
</dt> </dl>

 

 




