---
description: Get \_ FramesDrawn 方法會抓取 m \_ cFramesDrawn 成員變數，以提供串流開始後所繪製的框架數。
ms.assetid: 486b5541-2952-47ce-944e-4efb8e5af9dd
title: 'CBaseVideoRenderer.get_FramesDrawn 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDrawn
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec8254e06429022bf657322e98ab317475c82f90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998759"
---
# <a name="cbasevideorendererget_framesdrawn-method"></a><span data-ttu-id="12d02-103">CBaseVideoRenderer. 取得 \_ FramesDrawn 方法</span><span class="sxs-lookup"><span data-stu-id="12d02-103">CBaseVideoRenderer.get\_FramesDrawn method</span></span>

<span data-ttu-id="12d02-104">方法會抓取 `get_FramesDrawn` **m \_ cFramesDrawn** 成員變數，以提供串流開始後所繪製的框架數。</span><span class="sxs-lookup"><span data-stu-id="12d02-104">The `get_FramesDrawn` method retrieves the **m\_cFramesDrawn** member variable, giving the number of frames drawn since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d02-105">語法</span><span class="sxs-lookup"><span data-stu-id="12d02-105">Syntax</span></span>


```C++
HRESULT get_FramesDrawn(
   int *pcFramesDrawn
);
```



## <a name="parameters"></a><span data-ttu-id="12d02-106">參數</span><span class="sxs-lookup"><span data-stu-id="12d02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12d02-107">*pcFramesDrawn*</span><span class="sxs-lookup"><span data-stu-id="12d02-107">*pcFramesDrawn*</span></span> 
</dt> <dd>

<span data-ttu-id="12d02-108">繪製的框架數目指標。</span><span class="sxs-lookup"><span data-stu-id="12d02-108">Pointer to the number of frames drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12d02-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="12d02-109">Return value</span></span>

<span data-ttu-id="12d02-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="12d02-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12d02-111">備註</span><span class="sxs-lookup"><span data-stu-id="12d02-111">Remarks</span></span>

<span data-ttu-id="12d02-112">此成員函式會實 [**IQualProp：： get \_ FramesDrawn**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) 方法。</span><span class="sxs-lookup"><span data-stu-id="12d02-112">This member function implements the [**IQualProp::get\_FramesDrawn**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="12d02-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="12d02-113">Requirements</span></span>



| <span data-ttu-id="12d02-114">需求</span><span class="sxs-lookup"><span data-stu-id="12d02-114">Requirement</span></span> | <span data-ttu-id="12d02-115">值</span><span class="sxs-lookup"><span data-stu-id="12d02-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12d02-116">標頭</span><span class="sxs-lookup"><span data-stu-id="12d02-116">Header</span></span><br/>  | <dl> <span data-ttu-id="12d02-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="12d02-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="12d02-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="12d02-118">Library</span></span><br/> | <dl> <span data-ttu-id="12d02-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="12d02-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12d02-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12d02-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d02-121">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="12d02-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




