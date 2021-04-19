---
description: GetMediaPositionInterface 方法會抓取篩選器的 IMediaPosition 和 IMediaSeeking 介面指標。
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: 'CBaseRenderer. GetMediaPositionInterface 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetMediaPositionInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d41d777b88f0e18ae1510c32b7e89024ea7bdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995211"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a><span data-ttu-id="0f120-103">CBaseRenderer. GetMediaPositionInterface 方法</span><span class="sxs-lookup"><span data-stu-id="0f120-103">CBaseRenderer.GetMediaPositionInterface method</span></span>

<span data-ttu-id="0f120-104">方法會抓取 `GetMediaPositionInterface` 篩選器的 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 和 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="0f120-104">The `GetMediaPositionInterface` method retrieves the filter's [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface pointers.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f120-105">語法</span><span class="sxs-lookup"><span data-stu-id="0f120-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="0f120-106">參數</span><span class="sxs-lookup"><span data-stu-id="0f120-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f120-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="0f120-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="0f120-108">介面的參考識別碼。</span><span class="sxs-lookup"><span data-stu-id="0f120-108">Reference identifier of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="0f120-109">*Ppv*</span><span class="sxs-lookup"><span data-stu-id="0f120-109">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="0f120-110">接收介面指標之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="0f120-110">Address of a variable that receives the interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f120-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f120-111">Return value</span></span>

<span data-ttu-id="0f120-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0f120-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0f120-113">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="0f120-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0f120-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0f120-114">Return code</span></span>                                                                                   | <span data-ttu-id="0f120-115">Description</span><span class="sxs-lookup"><span data-stu-id="0f120-115">Description</span></span>                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="0f120-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0f120-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0f120-117">成功。</span><span class="sxs-lookup"><span data-stu-id="0f120-117">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="0f120-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0f120-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0f120-119">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="0f120-119">Insufficient memory.</span></span><br/>     |
| <dl> <span data-ttu-id="0f120-120"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="0f120-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="0f120-121">不支援的介面。</span><span class="sxs-lookup"><span data-stu-id="0f120-121">Interface not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f120-122">備註</span><span class="sxs-lookup"><span data-stu-id="0f120-122">Remarks</span></span>

<span data-ttu-id="0f120-123">篩選準則會將所有搜尋命令委派給 [**CRendererPosPassThru**](crendererpospassthru.md) 物件，並將它們傳遞至上游。</span><span class="sxs-lookup"><span data-stu-id="0f120-123">The filter delegates all seeking commands to a [**CRendererPosPassThru**](crendererpospassthru.md) object, which passes them upstream.</span></span> <span data-ttu-id="0f120-124">這個方法會建立 **CRendererPosPassThru** 物件（如果尚不存在），並針對要求的介面進行查詢。</span><span class="sxs-lookup"><span data-stu-id="0f120-124">This method creates the **CRendererPosPassThru** object, if it does not yet exist, and queries it for the requested interface.</span></span>

<span data-ttu-id="0f120-125">[**CBaseRenderer：： m \_ pPosition**](cbaserenderer-m-pposition.md)成員變數會將指標儲存至 **CRendererPosPassThru** 物件。</span><span class="sxs-lookup"><span data-stu-id="0f120-125">The [**CBaseRenderer::m\_pPosition**](cbaserenderer-m-pposition.md) member variable stores a pointer to the **CRendererPosPassThru** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f120-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f120-126">Requirements</span></span>



| <span data-ttu-id="0f120-127">需求</span><span class="sxs-lookup"><span data-stu-id="0f120-127">Requirement</span></span> | <span data-ttu-id="0f120-128">值</span><span class="sxs-lookup"><span data-stu-id="0f120-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f120-129">標頭</span><span class="sxs-lookup"><span data-stu-id="0f120-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0f120-130"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0f120-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f120-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="0f120-131">Library</span></span><br/> | <dl> <span data-ttu-id="0f120-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0f120-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f120-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f120-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f120-134">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="0f120-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




