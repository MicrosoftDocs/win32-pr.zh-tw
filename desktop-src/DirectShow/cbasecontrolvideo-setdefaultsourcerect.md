---
description: SetDefaultSourceRect 方法會將預設的來源影片矩形設定 (純虛擬) 。 這是內部成員函式，會在來源矩形重設時呼叫。
ms.assetid: d0dae0a9-8763-485e-b9d3-80076a3f2f35
title: 'CBaseControlVideo. SetDefaultSourceRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82fe2001a42ca75fff4f3172c8ce05da18881d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989880"
---
# <a name="cbasecontrolvideosetdefaultsourcerect-method"></a><span data-ttu-id="0a669-104">CBaseControlVideo. SetDefaultSourceRect 方法</span><span class="sxs-lookup"><span data-stu-id="0a669-104">CBaseControlVideo.SetDefaultSourceRect method</span></span>

<span data-ttu-id="0a669-105">`SetDefaultSourceRect`方法會將預設的來源影片矩形設定 (純虛擬) 。</span><span class="sxs-lookup"><span data-stu-id="0a669-105">The `SetDefaultSourceRect` method sets the default source video rectangle (pure virtual).</span></span> <span data-ttu-id="0a669-106">這是內部成員函式，會在來源矩形重設時呼叫。</span><span class="sxs-lookup"><span data-stu-id="0a669-106">This in an internal member function that gets called when the source rectangle is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a669-107">語法</span><span class="sxs-lookup"><span data-stu-id="0a669-107">Syntax</span></span>


```C++
virtual HRESULT SetDefaultSourceRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="0a669-108">參數</span><span class="sxs-lookup"><span data-stu-id="0a669-108">Parameters</span></span>

<span data-ttu-id="0a669-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0a669-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a669-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a669-110">Return value</span></span>

<span data-ttu-id="0a669-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0a669-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a669-112">備註</span><span class="sxs-lookup"><span data-stu-id="0a669-112">Remarks</span></span>

<span data-ttu-id="0a669-113">衍生類別應該覆寫此值，以重設來源矩形。</span><span class="sxs-lookup"><span data-stu-id="0a669-113">Derived classes should override this to reset the source rectangle.</span></span> <span data-ttu-id="0a669-114">它是從 [**CBaseControlVideo：： SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md)呼叫。</span><span class="sxs-lookup"><span data-stu-id="0a669-114">It is called from [**CBaseControlVideo::SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md).</span></span>

<span data-ttu-id="0a669-115">下列範例示範如何在衍生類別中執行此函式。</span><span class="sxs-lookup"><span data-stu-id="0a669-115">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// This is called when you reset the default source rectangle.
HRESULT CVideoText::SetDefaultSourceRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT SourceRect = {0,0,pHeader->biWidth,pHeader->biHeight};
    m_pRenderer->m_DrawImage.SetSourceRect(&SourceRect);
    return NOERROR;
}
```



<span data-ttu-id="0a669-116">在此範例中，CVideoText 是衍生自 [**CBaseControlVideo**](cbasecontrolvideo.md)的類別，m \_ pRenderer 會保存衍生自 [**CBaseVideoRenderer**](cbasevideorenderer.md)之類別的物件，而在 \_ 衍生類別中定義的 m DrawImage 資料成員則會保留 [**CDrawImage**](cdrawimage.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="0a669-116">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="0a669-117">M \_ mtIn 資料成員（也定義于衍生類別中）會保存具有輸入釘選媒體類型的 [**CMediaType**](cmediatype.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="0a669-117">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a669-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a669-118">Requirements</span></span>



| <span data-ttu-id="0a669-119">需求</span><span class="sxs-lookup"><span data-stu-id="0a669-119">Requirement</span></span> | <span data-ttu-id="0a669-120">值</span><span class="sxs-lookup"><span data-stu-id="0a669-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a669-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0a669-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0a669-122"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0a669-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0a669-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="0a669-123">Library</span></span><br/> | <dl> <span data-ttu-id="0a669-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0a669-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a669-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a669-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a669-126">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="0a669-126">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




