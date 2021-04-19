---
description: 衍生類別覆寫的純虛擬方法。
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: 'CBaseControlVideo. GetStaticImage 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetStaticImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13b0515e20202373954050b6fa18f10a20a76a6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001583"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a><span data-ttu-id="976af-103">CBaseControlVideo. GetStaticImage 方法</span><span class="sxs-lookup"><span data-stu-id="976af-103">CBaseControlVideo.GetStaticImage method</span></span>

<span data-ttu-id="976af-104">衍生類別覆寫的純虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="976af-104">Pure virtual method that derived classes override.</span></span>

## <a name="syntax"></a><span data-ttu-id="976af-105">語法</span><span class="sxs-lookup"><span data-stu-id="976af-105">Syntax</span></span>


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="976af-106">參數</span><span class="sxs-lookup"><span data-stu-id="976af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="976af-107">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="976af-107">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="976af-108">輸出緩衝區大小的指標。</span><span class="sxs-lookup"><span data-stu-id="976af-108">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="976af-109">*pDIBImage*</span><span class="sxs-lookup"><span data-stu-id="976af-109">*pDIBImage*</span></span> 
</dt> <dd>

<span data-ttu-id="976af-110">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="976af-110">Pointer to the output buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="976af-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="976af-111">Return value</span></span>

<span data-ttu-id="976af-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="976af-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="976af-113">備註</span><span class="sxs-lookup"><span data-stu-id="976af-113">Remarks</span></span>

<span data-ttu-id="976af-114">透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面，應用程式可以要求在記憶體緩衝區中取得目前映射的複本， (某些轉譯器可能會在 \_) 不支援時，將電子 >notimpl 傳給它。</span><span class="sxs-lookup"><span data-stu-id="976af-114">Through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface, an application can request that it be given a copy of the current image in a memory buffer (some renderers can return E\_NOTIMPL to this if they do not support it).</span></span> <span data-ttu-id="976af-115">衍生類別會決定如何取出影像。</span><span class="sxs-lookup"><span data-stu-id="976af-115">The derived class determines how to retrieve the image.</span></span> <span data-ttu-id="976af-116">當應用程式呼叫 **CBaseControlVideo：： GetStaticImage** 時，它會呼叫此純虛擬方法，衍生類別應該覆寫此方法來執行它。</span><span class="sxs-lookup"><span data-stu-id="976af-116">When the application calls **CBaseControlVideo::GetStaticImage**, it calls this pure virtual method that the derived class should override to implement it.</span></span> <span data-ttu-id="976af-117">這也是由 [**CBaseControlVideo：： GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) 成員函式所呼叫。</span><span class="sxs-lookup"><span data-stu-id="976af-117">This is also called by the [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) member function.</span></span>

<span data-ttu-id="976af-118">類別會提供 helper 成員函式 [**CBaseControlVideo：： CopyImage**](cbasecontrolvideo-copyimage.md)，其可提供包含影像的範例，而且成員函式會根據目前的來源矩形) ，將它的相關區段 (複製到應用程式所提供的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="976af-118">The class provides a helper member function, [**CBaseControlVideo::CopyImage**](cbasecontrolvideo-copyimage.md), that can be given a sample that contains an image, and the member function will copy the relevant section of it (based on the current source rectangle) into the output buffer supplied by the application.</span></span>

<span data-ttu-id="976af-119">下列範例示範如何在衍生類別中執行這個成員函式。</span><span class="sxs-lookup"><span data-stu-id="976af-119">The following example demonstrates an implementation of this member function in a derived class.</span></span> <span data-ttu-id="976af-120">在此範例中，m \_ pRenderer 會保存衍生自 [**CBaseVideoRenderer**](cbasevideorenderer.md)之類別的物件。</span><span class="sxs-lookup"><span data-stu-id="976af-120">In this example, m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md).</span></span>


```C++
// Return a copy of the current image in the video renderer
HRESULT CVideoText::GetStaticImage(long *pBufferSize,long *pDIBImage)
{
    // Get any sample the renderer may be holding.

    IMediaSample *pMediaSample = m_pRenderer->GetCurrentSample();
    if (pMediaSample == NULL) {
        return E_UNEXPECTED;
    }

    // Call the base class helper method to do the work.

    HRESULT hr = CopyImage(pMediaSample,       // Buffer containing image
                      &m_pRenderer->m_mtIn,    // Type representing bitmap
                      pBufferSize,             // Size of buffer for DIB
                     (BYTE*) pDIBImage);       // Data buffer for output

    pMediaSample->Release();
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="976af-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="976af-121">Requirements</span></span>



| <span data-ttu-id="976af-122">需求</span><span class="sxs-lookup"><span data-stu-id="976af-122">Requirement</span></span> | <span data-ttu-id="976af-123">值</span><span class="sxs-lookup"><span data-stu-id="976af-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="976af-124">標頭</span><span class="sxs-lookup"><span data-stu-id="976af-124">Header</span></span><br/>  | <dl> <span data-ttu-id="976af-125"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="976af-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="976af-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="976af-126">Library</span></span><br/> | <dl> <span data-ttu-id="976af-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="976af-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="976af-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="976af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="976af-129">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="976af-129">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




