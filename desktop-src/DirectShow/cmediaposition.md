---
description: CMediaPosition 類別會處理 IMediaPosition 雙重介面的 IDispatch 方法。
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: 'CMediaPosition 類別 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60d06a08badf3302ef4ddb352d840842a2605600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984001"
---
# <a name="cmediaposition-class"></a><span data-ttu-id="2fd9c-103">CMediaPosition 類別</span><span class="sxs-lookup"><span data-stu-id="2fd9c-103">CMediaPosition class</span></span>

![cmediaposition 類別階層](images/cutil14.png)

<span data-ttu-id="2fd9c-105">**CMediaPosition** 類別會處理 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)雙重介面的 **IDispatch** 方法。</span><span class="sxs-lookup"><span data-stu-id="2fd9c-105">The **CMediaPosition** class handles the **IDispatch** methods of the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) dual interface.</span></span>

<span data-ttu-id="2fd9c-106">此類別會繼承 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 介面，但不會加以執行。</span><span class="sxs-lookup"><span data-stu-id="2fd9c-106">This class inherits the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface but does not implement it.</span></span> <span data-ttu-id="2fd9c-107">它會透過 [**CBaseDispatch**](cbasedispatch.md)類別和 DirectShow 類型程式庫來實行 **IDispatch** 。</span><span class="sxs-lookup"><span data-stu-id="2fd9c-107">It implements **IDispatch** through the [**CBaseDispatch**](cbasedispatch.md) class and the DirectShow type library.</span></span> <span data-ttu-id="2fd9c-108">請勿直接使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="2fd9c-108">Do not use this class directly.</span></span> <span data-ttu-id="2fd9c-109">相反地，請使用下列其中一個類別：</span><span class="sxs-lookup"><span data-stu-id="2fd9c-109">Instead, use one of the following classes:</span></span>

-   <span data-ttu-id="2fd9c-110">來源篩選器：使用 [**CSourceSeeking**](csourceseeking.md) 基類來執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="2fd9c-110">Source filters: Use the [**CSourceSeeking**](csourceseeking.md) base class to implement seeking.</span></span>
-   <span data-ttu-id="2fd9c-111">轉換篩選：使用 [**CPosPassThru**](cpospassthru.md) 類別傳遞上游的搜尋命令。</span><span class="sxs-lookup"><span data-stu-id="2fd9c-111">Transform filters: Use the [**CPosPassThru**](cpospassthru.md) class to pass seeking commands upstream.</span></span>
-   <span data-ttu-id="2fd9c-112">轉譯器：使用 [**CRendererPosPassThru**](crendererpospassthru.md) 類別傳遞上游的搜尋命令。</span><span class="sxs-lookup"><span data-stu-id="2fd9c-112">Renderers: Use the [**CRendererPosPassThru**](crendererpospassthru.md) class to pass seeking commands upstream.</span></span>



| <span data-ttu-id="2fd9c-113">公用方法</span><span class="sxs-lookup"><span data-stu-id="2fd9c-113">Public Methods</span></span>                                              | <span data-ttu-id="2fd9c-114">Description</span><span class="sxs-lookup"><span data-stu-id="2fd9c-114">Description</span></span>                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fd9c-115">**CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="2fd9c-115">**CMediaPosition**</span></span>](cmediaposition-cmediaposition.md)     | <span data-ttu-id="2fd9c-116">函式方法。</span><span class="sxs-lookup"><span data-stu-id="2fd9c-116">Constructor method.</span></span>                                                                                                 |
| <span data-ttu-id="2fd9c-117">IDispatch 方法</span><span class="sxs-lookup"><span data-stu-id="2fd9c-117">IDispatch Methods</span></span>                                           | <span data-ttu-id="2fd9c-118">Description</span><span class="sxs-lookup"><span data-stu-id="2fd9c-118">Description</span></span>                                                                                                         |
| [<span data-ttu-id="2fd9c-119">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="2fd9c-119">**GetIDsOfNames**</span></span>](cmediaposition-getidsofnames.md)       | <span data-ttu-id="2fd9c-120">將一組名稱對應至一組對應的 Dispid。</span><span class="sxs-lookup"><span data-stu-id="2fd9c-120">Maps a set of names to a corresponding set of DISPIDs.</span></span>                                                              |
| [<span data-ttu-id="2fd9c-121">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="2fd9c-121">**GetTypeInfo**</span></span>](cmediaposition-gettypeinfo.md)           | <span data-ttu-id="2fd9c-122">抓取物件的型別資訊，然後用來取得介面的型別資訊。</span><span class="sxs-lookup"><span data-stu-id="2fd9c-122">Retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span> |
| [<span data-ttu-id="2fd9c-123">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="2fd9c-123">**GetTypeInfoCount**</span></span>](cmediaposition-gettypeinfocount.md) | <span data-ttu-id="2fd9c-124">抓取物件提供的類型資訊介面數目。</span><span class="sxs-lookup"><span data-stu-id="2fd9c-124">Retrieves the number of type information interfaces the object provides.</span></span>                                            |
| [<span data-ttu-id="2fd9c-125">**調用**</span><span class="sxs-lookup"><span data-stu-id="2fd9c-125">**Invoke**</span></span>](cmediaposition-invoke.md)                     | <span data-ttu-id="2fd9c-126">提供物件所公開之屬性和方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="2fd9c-126">Provides access to properties and methods exposed by the object.</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="2fd9c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fd9c-127">Requirements</span></span>



| <span data-ttu-id="2fd9c-128">需求</span><span class="sxs-lookup"><span data-stu-id="2fd9c-128">Requirement</span></span> | <span data-ttu-id="2fd9c-129">值</span><span class="sxs-lookup"><span data-stu-id="2fd9c-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd9c-130">標頭</span><span class="sxs-lookup"><span data-stu-id="2fd9c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2fd9c-131"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2fd9c-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2fd9c-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="2fd9c-132">Library</span></span><br/> | <dl> <span data-ttu-id="2fd9c-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2fd9c-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fd9c-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fd9c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fd9c-135">DirectShow 基類</span><span class="sxs-lookup"><span data-stu-id="2fd9c-135">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




