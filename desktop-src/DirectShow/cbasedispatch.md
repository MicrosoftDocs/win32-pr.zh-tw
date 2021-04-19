---
description: CBaseDispatch 類別是在 DirectShow 篩選器中實作為 IDispatch 介面的基類。
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: 'CBaseDispatch 類別 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d115412b2b668f640834d5a3fa3b134f7a8d9c01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995936"
---
# <a name="cbasedispatch-class"></a><span data-ttu-id="1c04b-103">CBaseDispatch 類別</span><span class="sxs-lookup"><span data-stu-id="1c04b-103">CBaseDispatch class</span></span>

![cbasedispatch 類別階層](images/cutil01.png)

<span data-ttu-id="1c04b-105">**CBaseDispatch** 類別是在 DirectShow 篩選器中實作為 **IDispatch** 介面的基類。</span><span class="sxs-lookup"><span data-stu-id="1c04b-105">The **CBaseDispatch** class is a base class for implementing the **IDispatch** interface in a DirectShow filter.</span></span>

<span data-ttu-id="1c04b-106">此類別僅限於支援 DirectShow 類型程式庫（QuartzTypeLib）所匯出的自動化相容介面。</span><span class="sxs-lookup"><span data-stu-id="1c04b-106">This class is limited to supporting the Automation-compatible interfaces exported by the DirectShow type library, QuartzTypeLib.</span></span> <span data-ttu-id="1c04b-107">例如， [**CMediaControl**](cmediacontrol.md) 和 [**CMediaPosition**](cmediaposition.md) 類別會使用 **CBaseDispatch** 分別執行 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 和 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)。</span><span class="sxs-lookup"><span data-stu-id="1c04b-107">For example, the [**CMediaControl**](cmediacontrol.md) and [**CMediaPosition**](cmediaposition.md) classes use **CBaseDispatch** to implement [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), respectively.</span></span> <span data-ttu-id="1c04b-108">由於這項限制，因此可能沒有理由直接在您自己的篩選器中使用 **CBaseDispatch** 。</span><span class="sxs-lookup"><span data-stu-id="1c04b-108">Because of this limitation, there is probably no reason to use **CBaseDispatch** directly in your own filters.</span></span>

<span data-ttu-id="1c04b-109">若要使用此類別，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="1c04b-109">To use this class, do the following:</span></span>

-   <span data-ttu-id="1c04b-110">宣告支援 **IDispatch** 的新類別。</span><span class="sxs-lookup"><span data-stu-id="1c04b-110">Declare a new class that supports **IDispatch**.</span></span>
-   <span data-ttu-id="1c04b-111">為您的新類別提供 **CBaseDispatch** 型別的私用成員變數。</span><span class="sxs-lookup"><span data-stu-id="1c04b-111">Give your new class a private member variable of type **CBaseDispatch**.</span></span>
-   <span data-ttu-id="1c04b-112">執行 **IDispatch** 方法。</span><span class="sxs-lookup"><span data-stu-id="1c04b-112">Implement the **IDispatch** methods.</span></span>
-   <span data-ttu-id="1c04b-113">在您的 **IDispatch** 方法中，呼叫 **CBaseDispatch** 方法。</span><span class="sxs-lookup"><span data-stu-id="1c04b-113">In your **IDispatch** methods, call the **CBaseDispatch** methods.</span></span>

<span data-ttu-id="1c04b-114">如需詳細資訊，請參閱 Ctlutil 中所宣告的任何範例類別的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="1c04b-114">For more details, refer to the source code for any of the sample classes declared in Ctlutil.h.</span></span>



| <span data-ttu-id="1c04b-115">公用方法</span><span class="sxs-lookup"><span data-stu-id="1c04b-115">Public Methods</span></span>                                             | <span data-ttu-id="1c04b-116">Description</span><span class="sxs-lookup"><span data-stu-id="1c04b-116">Description</span></span>                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c04b-117">**CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="1c04b-117">**CBaseDispatch**</span></span>](cbasedispatch-cbasedispatch.md)       | <span data-ttu-id="1c04b-118">函式方法。</span><span class="sxs-lookup"><span data-stu-id="1c04b-118">Constructor method.</span></span>                                                                                                 |
| [<span data-ttu-id="1c04b-119">**~ CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="1c04b-119">**~CBaseDispatch**</span></span>](cbasedispatch--cbasedispatch.md)     | <span data-ttu-id="1c04b-120">函式方法。</span><span class="sxs-lookup"><span data-stu-id="1c04b-120">Destructor method.</span></span>                                                                                                  |
| [<span data-ttu-id="1c04b-121">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="1c04b-121">**GetIDsOfNames**</span></span>](cbasedispatch-getidsofnames.md)       | <span data-ttu-id="1c04b-122">將一組名稱對應至一組對應的 Dispid。</span><span class="sxs-lookup"><span data-stu-id="1c04b-122">Maps a set of names to a corresponding set of DISPIDs.</span></span>                                                              |
| [<span data-ttu-id="1c04b-123">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="1c04b-123">**GetTypeInfo**</span></span>](cbasedispatch-gettypeinfo.md)           | <span data-ttu-id="1c04b-124">抓取物件的型別資訊，然後用來取得介面的型別資訊。</span><span class="sxs-lookup"><span data-stu-id="1c04b-124">Retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span> |
| [<span data-ttu-id="1c04b-125">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="1c04b-125">**GetTypeInfoCount**</span></span>](cbasedispatch-gettypeinfocount.md) | <span data-ttu-id="1c04b-126">抓取物件提供的類型資訊介面數目。</span><span class="sxs-lookup"><span data-stu-id="1c04b-126">Retrieves the number of type information interfaces the object provides.</span></span>                                            |



 

## <a name="requirements"></a><span data-ttu-id="1c04b-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c04b-127">Requirements</span></span>



| <span data-ttu-id="1c04b-128">需求</span><span class="sxs-lookup"><span data-stu-id="1c04b-128">Requirement</span></span> | <span data-ttu-id="1c04b-129">值</span><span class="sxs-lookup"><span data-stu-id="1c04b-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c04b-130">標頭</span><span class="sxs-lookup"><span data-stu-id="1c04b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="1c04b-131"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1c04b-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c04b-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="1c04b-132">Library</span></span><br/> | <dl> <span data-ttu-id="1c04b-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1c04b-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c04b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c04b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c04b-135">DirectShow 基類</span><span class="sxs-lookup"><span data-stu-id="1c04b-135">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




