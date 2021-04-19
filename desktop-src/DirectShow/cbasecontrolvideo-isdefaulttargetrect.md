---
description: IsDefaultTargetRect 方法會判斷轉譯器是否使用預設的目標矩形 (純虛擬) 。
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: 'CBaseControlVideo. IsDefaultTargetRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e267cc65345d18800beccbc80ac7952c89d781d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995523"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a><span data-ttu-id="e6af8-103">CBaseControlVideo. IsDefaultTargetRect 方法</span><span class="sxs-lookup"><span data-stu-id="e6af8-103">CBaseControlVideo.IsDefaultTargetRect method</span></span>

<span data-ttu-id="e6af8-104">`IsDefaultTargetRect`方法會判斷轉譯器是否使用預設的目標矩形 (純虛擬) 。</span><span class="sxs-lookup"><span data-stu-id="e6af8-104">The `IsDefaultTargetRect` method determines if the renderer is using the default target rectangle (pure virtual).</span></span>

## <a name="syntax"></a><span data-ttu-id="e6af8-105">語法</span><span class="sxs-lookup"><span data-stu-id="e6af8-105">Syntax</span></span>


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="e6af8-106">參數</span><span class="sxs-lookup"><span data-stu-id="e6af8-106">Parameters</span></span>

<span data-ttu-id="e6af8-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e6af8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6af8-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6af8-108">Return value</span></span>

<span data-ttu-id="e6af8-109">如果轉譯器 \_ 使用預設目標，則傳回 [確定]，否則傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="e6af8-109">Returns S\_OK if the renderer is using the default target; otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6af8-110">備註</span><span class="sxs-lookup"><span data-stu-id="e6af8-110">Remarks</span></span>

<span data-ttu-id="e6af8-111">此成員函式必須在衍生類別中執行。</span><span class="sxs-lookup"><span data-stu-id="e6af8-111">This member function must be implemented in the derived class.</span></span> <span data-ttu-id="e6af8-112">它是由 [**CBaseControlVideo：： IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) 成員函式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="e6af8-112">It is called by the [**CBaseControlVideo::IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) member function.</span></span>

<span data-ttu-id="e6af8-113">下列範例示範如何在衍生類別中執行此函式。</span><span class="sxs-lookup"><span data-stu-id="e6af8-113">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return S_OK if using the default target; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultTargetRect()
{
    RECT TargetRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetTargetRect(&TargetRect);

    // Check the destination that matches the initial client area.

    if (TargetRect.left != 0 || TargetRect.top != 0 ||
            TargetRect.right != m_Size.cx ||
                TargetRect.bottom != m_Size.cy) {
                    return S_FALSE;
    }
    return S_OK;
}
```



<span data-ttu-id="e6af8-114">在此範例中，CVideoText 是衍生自 [**CBaseControlVideo**](cbasecontrolvideo.md)的類別，m \_ pRenderer 會保存衍生自 [**CBaseVideoRenderer**](cbasevideorenderer.md)之類別的物件，而在 \_ 衍生類別中定義的 m DrawImage 資料成員則會保留 [**CDrawImage**](cdrawimage.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e6af8-114">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="e6af8-115">M \_ mtIn 資料成員（也定義于衍生類別中）會保存具有輸入釘選媒體類型的 [**CMediaType**](cmediatype.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e6af8-115">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6af8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6af8-116">Requirements</span></span>



| <span data-ttu-id="e6af8-117">需求</span><span class="sxs-lookup"><span data-stu-id="e6af8-117">Requirement</span></span> | <span data-ttu-id="e6af8-118">值</span><span class="sxs-lookup"><span data-stu-id="e6af8-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6af8-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e6af8-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e6af8-120"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e6af8-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6af8-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="e6af8-121">Library</span></span><br/> | <dl> <span data-ttu-id="e6af8-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e6af8-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6af8-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6af8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6af8-124">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="e6af8-124">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




