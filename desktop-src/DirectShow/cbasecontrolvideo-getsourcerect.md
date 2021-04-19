---
description: GetSourceRect 方法會抓取來源矩形。 這是內部方法。
ms.assetid: 51028b79-6aab-4abc-8ee8-2965bda9d191
title: 'CBaseControlVideo. GetSourceRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e57a5beda7b147e952ecbb26c96df5f7e372e6d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990182"
---
# <a name="cbasecontrolvideogetsourcerect-method"></a><span data-ttu-id="f0b10-104">CBaseControlVideo. GetSourceRect 方法</span><span class="sxs-lookup"><span data-stu-id="f0b10-104">CBaseControlVideo.GetSourceRect method</span></span>

<span data-ttu-id="f0b10-105">`GetSourceRect`方法會捕獲來源矩形。</span><span class="sxs-lookup"><span data-stu-id="f0b10-105">The `GetSourceRect` method retrieves the source rectangle.</span></span> <span data-ttu-id="f0b10-106">這是內部方法。</span><span class="sxs-lookup"><span data-stu-id="f0b10-106">This is an internal method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0b10-107">語法</span><span class="sxs-lookup"><span data-stu-id="f0b10-107">Syntax</span></span>


```C++
virtual HRESULT GetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="f0b10-108">參數</span><span class="sxs-lookup"><span data-stu-id="f0b10-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0b10-109">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="f0b10-109">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="f0b10-110">所抓取來源矩形的指標。</span><span class="sxs-lookup"><span data-stu-id="f0b10-110">Pointer to the retrieved source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0b10-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0b10-111">Return value</span></span>

<span data-ttu-id="f0b10-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="f0b10-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0b10-113">備註</span><span class="sxs-lookup"><span data-stu-id="f0b10-113">Remarks</span></span>

<span data-ttu-id="f0b10-114">必須在衍生類別中覆寫這個成員函式，以傳回影片轉譯器所持有的來源矩形。</span><span class="sxs-lookup"><span data-stu-id="f0b10-114">This member function must be overridden in the derived class to return the source rectangle held by the video renderer.</span></span> <span data-ttu-id="f0b10-115">它會從下列 [**CBaseControlVideo**](cbasecontrolvideo.md) 成員函式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="f0b10-115">It is called from the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="f0b10-116">**CBaseControlVideo::GetSourcePosition**</span><span class="sxs-lookup"><span data-stu-id="f0b10-116">**CBaseControlVideo::GetSourcePosition**</span></span>](cbasecontrolvideo-getsourceposition.md)
-   [<span data-ttu-id="f0b10-117">**CBaseControlVideo：:p 的 \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="f0b10-117">**CBaseControlVideo::put\_SourceLeft**</span></span>](cbasecontrolvideo-put-sourceleft.md)
-   [<span data-ttu-id="f0b10-118">**CBaseControlVideo：： get \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="f0b10-118">**CBaseControlVideo::get\_SourceLeft**</span></span>](cbasecontrolvideo-get-sourceleft.md)
-   [<span data-ttu-id="f0b10-119">**CBaseControlVideo：:p 的 \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="f0b10-119">**CBaseControlVideo::put\_SourceWidth**</span></span>](cbasecontrolvideo-put-sourcewidth.md)
-   [<span data-ttu-id="f0b10-120">**CBaseControlVideo：： get \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="f0b10-120">**CBaseControlVideo::get\_SourceWidth**</span></span>](cbasecontrolvideo-get-sourcewidth.md)
-   [<span data-ttu-id="f0b10-121">**CBaseControlVideo：:p 的 \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="f0b10-121">**CBaseControlVideo::put\_SourceTop**</span></span>](cbasecontrolvideo-put-sourcetop.md)
-   [<span data-ttu-id="f0b10-122">**CBaseControlVideo：： get \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="f0b10-122">**CBaseControlVideo::get\_SourceTop**</span></span>](cbasecontrolvideo-get-sourcetop.md)
-   [<span data-ttu-id="f0b10-123">**CBaseControlVideo：:p 的 \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="f0b10-123">**CBaseControlVideo::put\_SourceHeight**</span></span>](cbasecontrolvideo-put-sourceheight.md)
-   [<span data-ttu-id="f0b10-124">**CBaseControlVideo：： get \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="f0b10-124">**CBaseControlVideo::get\_SourceHeight**</span></span>](cbasecontrolvideo-get-sourceheight.md)

<span data-ttu-id="f0b10-125">下列範例示範如何在衍生類別中執行此函式。</span><span class="sxs-lookup"><span data-stu-id="f0b10-125">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return the current source rectangle
HRESULT CVideoText::GetSourceRect(RECT *pSourceRect)
{
    ASSERT(pSourceRect);
    m_pRenderer->m_DrawImage.GetSourceRect(pSourceRect);
    return NOERROR;
}
```



<span data-ttu-id="f0b10-126">在此範例中，CVideoText 是衍生自 [**CBaseControlVideo**](cbasecontrolvideo.md)的類別，m \_ pRenderer 會保存衍生自 [**CBaseVideoRenderer**](cbasevideorenderer.md)之類別的物件，而在 \_ 衍生類別中定義的 m DrawImage 資料成員則會保留 [**CDrawImage**](cdrawimage.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f0b10-126">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0b10-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0b10-127">Requirements</span></span>



| <span data-ttu-id="f0b10-128">需求</span><span class="sxs-lookup"><span data-stu-id="f0b10-128">Requirement</span></span> | <span data-ttu-id="f0b10-129">值</span><span class="sxs-lookup"><span data-stu-id="f0b10-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b10-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f0b10-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f0b10-131"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f0b10-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f0b10-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="f0b10-132">Library</span></span><br/> | <dl> <span data-ttu-id="f0b10-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f0b10-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0b10-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0b10-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0b10-135">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="f0b10-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




