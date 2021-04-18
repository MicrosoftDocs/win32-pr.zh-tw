---
description: SetSourceRect 方法會將目前的來源影片矩形設定 (純虛擬) 。 這是來源矩形變更時所呼叫的內部成員函式。
ms.assetid: 13bb594b-b154-40a2-ad00-f1e86781074d
title: 'CBaseControlVideo. SetSourceRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e3be6cc3819e1452fd196d4906377204a6e90bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996462"
---
# <a name="cbasecontrolvideosetsourcerect-method"></a><span data-ttu-id="40e7c-104">CBaseControlVideo. SetSourceRect 方法</span><span class="sxs-lookup"><span data-stu-id="40e7c-104">CBaseControlVideo.SetSourceRect method</span></span>

<span data-ttu-id="40e7c-105">`SetSourceRect`方法會將目前的來源影片矩形設定 (純虛擬) 。</span><span class="sxs-lookup"><span data-stu-id="40e7c-105">The `SetSourceRect` method sets the current source video rectangle (pure virtual).</span></span> <span data-ttu-id="40e7c-106">這是來源矩形變更時所呼叫的內部成員函式。</span><span class="sxs-lookup"><span data-stu-id="40e7c-106">This is an internal member function that gets called when the source rectangle changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="40e7c-107">語法</span><span class="sxs-lookup"><span data-stu-id="40e7c-107">Syntax</span></span>


```C++
virtual HRESULT SetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="40e7c-108">參數</span><span class="sxs-lookup"><span data-stu-id="40e7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40e7c-109">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="40e7c-109">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="40e7c-110">來源矩形的指標。</span><span class="sxs-lookup"><span data-stu-id="40e7c-110">Pointer to the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40e7c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="40e7c-111">Return value</span></span>

<span data-ttu-id="40e7c-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="40e7c-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40e7c-113">備註</span><span class="sxs-lookup"><span data-stu-id="40e7c-113">Remarks</span></span>

<span data-ttu-id="40e7c-114">衍生類別應該覆寫這個成員函式，以得知來源矩形何時變更。</span><span class="sxs-lookup"><span data-stu-id="40e7c-114">Derived classes should override this member function to know when the source rectangle changes.</span></span> <span data-ttu-id="40e7c-115">它是從下列成員函式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="40e7c-115">It is called from the following member functions.</span></span>

-   [<span data-ttu-id="40e7c-116">**CBaseControlVideo::SetSourcePosition**</span><span class="sxs-lookup"><span data-stu-id="40e7c-116">**CBaseControlVideo::SetSourcePosition**</span></span>](cbasecontrolvideo-setsourceposition.md)
-   [<span data-ttu-id="40e7c-117">**CBaseControlVideo：:p 的 \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="40e7c-117">**CBaseControlVideo::put\_SourceLeft**</span></span>](cbasecontrolvideo-put-sourceleft.md)
-   [<span data-ttu-id="40e7c-118">**CBaseControlVideo：:p 的 \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="40e7c-118">**CBaseControlVideo::put\_SourceWidth**</span></span>](cbasecontrolvideo-put-sourcewidth.md)
-   [<span data-ttu-id="40e7c-119">**CBaseControlVideo：:p 的 \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="40e7c-119">**CBaseControlVideo::put\_SourceTop**</span></span>](cbasecontrolvideo-put-sourcetop.md)
-   [<span data-ttu-id="40e7c-120">**CBaseControlVideo：:p 的 \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="40e7c-120">**CBaseControlVideo::put\_SourceHeight**</span></span>](cbasecontrolvideo-put-sourceheight.md)

<span data-ttu-id="40e7c-121">下列範例示範如何在衍生類別中執行此函式。</span><span class="sxs-lookup"><span data-stu-id="40e7c-121">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
HRESULT CVideoText::SetSourceRect(RECT *pSourceRect)
{
    m_pRenderer->m_DrawImage.SetSourceRect(pSourceRect);
    return NOERROR;
}
```



<span data-ttu-id="40e7c-122">在此範例中，CVideoText 是衍生自 [**CBaseControlVideo**](cbasecontrolvideo.md)的類別，m \_ pRenderer 會保存衍生自 [**CBaseVideoRenderer**](cbasevideorenderer.md)之類別的物件，而在 \_ 衍生類別中定義的 m DrawImage 資料成員則會保留 [**CDrawImage**](cdrawimage.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="40e7c-122">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="40e7c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="40e7c-123">Requirements</span></span>



| <span data-ttu-id="40e7c-124">需求</span><span class="sxs-lookup"><span data-stu-id="40e7c-124">Requirement</span></span> | <span data-ttu-id="40e7c-125">值</span><span class="sxs-lookup"><span data-stu-id="40e7c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40e7c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="40e7c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="40e7c-127"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="40e7c-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="40e7c-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="40e7c-128">Library</span></span><br/> | <dl> <span data-ttu-id="40e7c-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="40e7c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40e7c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40e7c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40e7c-131">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="40e7c-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




