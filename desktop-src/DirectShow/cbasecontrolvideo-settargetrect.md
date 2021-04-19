---
description: SetTargetRect 方法會將目前的目標矩形設定 (純虛擬) 。 這是在目的地矩形變更時所呼叫的內部成員函式。
ms.assetid: 9e48989d-5995-4f9d-82b2-01229473c3e8
title: 'CBaseControlVideo. SetTargetRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3868e7d8df93940829fb96c7152a55048a5cae82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980200"
---
# <a name="cbasecontrolvideosettargetrect-method"></a><span data-ttu-id="e3895-104">CBaseControlVideo. SetTargetRect 方法</span><span class="sxs-lookup"><span data-stu-id="e3895-104">CBaseControlVideo.SetTargetRect method</span></span>

<span data-ttu-id="e3895-105">`SetTargetRect`方法會將目前的目標矩形設定 (純虛擬) 。</span><span class="sxs-lookup"><span data-stu-id="e3895-105">The `SetTargetRect` method sets the current target rectangle (pure virtual).</span></span> <span data-ttu-id="e3895-106">這是在目的地矩形變更時所呼叫的內部成員函式。</span><span class="sxs-lookup"><span data-stu-id="e3895-106">This is an internal member function that gets called when the destination rectangle changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3895-107">語法</span><span class="sxs-lookup"><span data-stu-id="e3895-107">Syntax</span></span>


```C++
virtual HRESULT SetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="e3895-108">參數</span><span class="sxs-lookup"><span data-stu-id="e3895-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3895-109">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="e3895-109">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="e3895-110">目的地矩形的指標。</span><span class="sxs-lookup"><span data-stu-id="e3895-110">Pointer to the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3895-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3895-111">Return value</span></span>

<span data-ttu-id="e3895-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e3895-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3895-113">備註</span><span class="sxs-lookup"><span data-stu-id="e3895-113">Remarks</span></span>

<span data-ttu-id="e3895-114">衍生類別應該覆寫此參數，以瞭解目的地矩形變更的時間。</span><span class="sxs-lookup"><span data-stu-id="e3895-114">Derived classes should override this to know when the destination rectangle changes.</span></span> <span data-ttu-id="e3895-115">它是從下列成員函式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="e3895-115">It is called from the following member functions.</span></span>

-   [<span data-ttu-id="e3895-116">**CBaseControlVideo::SetDestinationPosition**</span><span class="sxs-lookup"><span data-stu-id="e3895-116">**CBaseControlVideo::SetDestinationPosition**</span></span>](cbasecontrolvideo-setdestinationposition.md)
-   [<span data-ttu-id="e3895-117">**CBaseControlVideo：:p 的 \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="e3895-117">**CBaseControlVideo::put\_DestinationLeft**</span></span>](cbasecontrolvideo-put-destinationleft.md)
-   [<span data-ttu-id="e3895-118">**CBaseControlVideo：:p 的 \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="e3895-118">**CBaseControlVideo::put\_DestinationWidth**</span></span>](cbasecontrolvideo-put-destinationwidth.md)
-   [<span data-ttu-id="e3895-119">**CBaseControlVideo：:p 的 \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="e3895-119">**CBaseControlVideo::put\_DestinationTop**</span></span>](cbasecontrolvideo-put-destinationtop.md)
-   [<span data-ttu-id="e3895-120">**CBaseControlVideo：:p 的 \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="e3895-120">**CBaseControlVideo::put\_DestinationHeight**</span></span>](cbasecontrolvideo-put-destinationheight.md)

<span data-ttu-id="e3895-121">下列範例示範如何在衍生類別中執行此函式。</span><span class="sxs-lookup"><span data-stu-id="e3895-121">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
    return NOERROR;
}
```



<span data-ttu-id="e3895-122">在此範例中，CVideoText 是衍生自 [**CBaseControlVideo**](cbasecontrolvideo.md)的類別，m \_ pRenderer 會保存衍生自 [**CBaseVideoRenderer**](cbasevideorenderer.md)之類別的物件，而在 \_ 衍生類別中定義的 m DrawImage 資料成員則會保留 [**CDrawImage**](cdrawimage.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e3895-122">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3895-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3895-123">Requirements</span></span>



| <span data-ttu-id="e3895-124">需求</span><span class="sxs-lookup"><span data-stu-id="e3895-124">Requirement</span></span> | <span data-ttu-id="e3895-125">值</span><span class="sxs-lookup"><span data-stu-id="e3895-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3895-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e3895-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e3895-127"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e3895-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e3895-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="e3895-128">Library</span></span><br/> | <dl> <span data-ttu-id="e3895-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e3895-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3895-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3895-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3895-131">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="e3895-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




