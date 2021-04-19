---
description: GetTargetRect 方法會捕獲目的地矩形。 這是內部 helper 成員函式。
ms.assetid: bf9d95c9-eee8-46b8-bdee-a7d16777ed83
title: 'CBaseControlVideo. GetTargetRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d59a12e134edf37c8ab0a63f46f77923b112605d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982602"
---
# <a name="cbasecontrolvideogettargetrect-method"></a><span data-ttu-id="517be-104">CBaseControlVideo. GetTargetRect 方法</span><span class="sxs-lookup"><span data-stu-id="517be-104">CBaseControlVideo.GetTargetRect method</span></span>

<span data-ttu-id="517be-105">方法會抓取 `GetTargetRect` 目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="517be-105">The `GetTargetRect` method retrieves the destination rectangle.</span></span> <span data-ttu-id="517be-106">這是內部 helper 成員函式。</span><span class="sxs-lookup"><span data-stu-id="517be-106">This is an internal helper member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="517be-107">語法</span><span class="sxs-lookup"><span data-stu-id="517be-107">Syntax</span></span>


```C++
virtual HRESULT GetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="517be-108">參數</span><span class="sxs-lookup"><span data-stu-id="517be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="517be-109">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="517be-109">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="517be-110">目的地矩形的指標。</span><span class="sxs-lookup"><span data-stu-id="517be-110">Pointer to the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="517be-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="517be-111">Return value</span></span>

<span data-ttu-id="517be-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="517be-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="517be-113">備註</span><span class="sxs-lookup"><span data-stu-id="517be-113">Remarks</span></span>

<span data-ttu-id="517be-114">必須在衍生類別中覆寫這個成員函式，以傳回影片轉譯器所持有的目標矩形。</span><span class="sxs-lookup"><span data-stu-id="517be-114">This member function must be overridden in the derived class to return the target rectangle held by the video renderer.</span></span> <span data-ttu-id="517be-115">它會從下列 [**CBaseControlVideo**](cbasecontrolvideo.md) 成員函式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="517be-115">It is called from the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="517be-116">**CBaseControlVideo::GetDestinationPosition**</span><span class="sxs-lookup"><span data-stu-id="517be-116">**CBaseControlVideo::GetDestinationPosition**</span></span>](cbasecontrolvideo-getdestinationposition.md)
-   [<span data-ttu-id="517be-117">**CBaseControlVideo：:p 的 \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="517be-117">**CBaseControlVideo::put\_DestinationLeft**</span></span>](cbasecontrolvideo-put-destinationleft.md)
-   [<span data-ttu-id="517be-118">**CBaseControlVideo：： get \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="517be-118">**CBaseControlVideo::get\_DestinationLeft**</span></span>](cbasecontrolvideo-get-destinationleft.md)
-   [<span data-ttu-id="517be-119">**CBaseControlVideo：:p 的 \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="517be-119">**CBaseControlVideo::put\_DestinationWidth**</span></span>](cbasecontrolvideo-put-destinationwidth.md)
-   [<span data-ttu-id="517be-120">**CBaseControlVideo：： get \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="517be-120">**CBaseControlVideo::get\_DestinationWidth**</span></span>](cbasecontrolvideo-get-destinationwidth.md)
-   [<span data-ttu-id="517be-121">**CBaseControlVideo：:p 的 \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="517be-121">**CBaseControlVideo::put\_DestinationTop**</span></span>](cbasecontrolvideo-put-destinationtop.md)
-   [<span data-ttu-id="517be-122">**CBaseControlVideo：： get \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="517be-122">**CBaseControlVideo::get\_DestinationTop**</span></span>](cbasecontrolvideo-get-destinationtop.md)
-   [<span data-ttu-id="517be-123">**CBaseControlVideo：:p 的 \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="517be-123">**CBaseControlVideo::put\_DestinationHeight**</span></span>](cbasecontrolvideo-put-destinationheight.md)
-   [<span data-ttu-id="517be-124">**CBaseControlVideo：： get \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="517be-124">**CBaseControlVideo::get\_DestinationHeight**</span></span>](cbasecontrolvideo-get-destinationheight.md)

<span data-ttu-id="517be-125">下列範例示範如何在衍生類別中執行此函式。</span><span class="sxs-lookup"><span data-stu-id="517be-125">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return the current destination rectangle.
HRESULT CVideoText::GetTargetRect(RECT *pTargetRect)
{
    ASSERT(pTargetRect);
    m_pRenderer->m_DrawImage.GetTargetRect(pTargetRect);
    return NOERROR;
}
```



<span data-ttu-id="517be-126">在此範例中，CVideoText 是衍生自 [**CBaseControlVideo**](cbasecontrolvideo.md)的類別，m \_ pRenderer 會保存衍生自 [**CBaseVideoRenderer**](cbasevideorenderer.md)之類別的物件，而在 \_ 衍生類別中定義的 m DrawImage 資料成員則會保留 [**CDrawImage**](cdrawimage.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="517be-126">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="517be-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="517be-127">Requirements</span></span>



| <span data-ttu-id="517be-128">需求</span><span class="sxs-lookup"><span data-stu-id="517be-128">Requirement</span></span> | <span data-ttu-id="517be-129">值</span><span class="sxs-lookup"><span data-stu-id="517be-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="517be-130">標頭</span><span class="sxs-lookup"><span data-stu-id="517be-130">Header</span></span><br/>  | <dl> <span data-ttu-id="517be-131"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="517be-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="517be-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="517be-132">Library</span></span><br/> | <dl> <span data-ttu-id="517be-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="517be-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="517be-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="517be-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="517be-135">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="517be-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




