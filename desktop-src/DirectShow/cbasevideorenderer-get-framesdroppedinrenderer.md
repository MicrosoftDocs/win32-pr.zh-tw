---
description: Get FramesDroppedInRenderer 方法會抓取轉譯器 \_ 捨棄的框架數目。
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: 'CBaseVideoRenderer.get_FramesDroppedInRenderer 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef81678fce8d349c7c047b0453cc480d8673f8f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985753"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a><span data-ttu-id="cab5e-103">CBaseVideoRenderer. 取得 \_ FramesDroppedInRenderer 方法</span><span class="sxs-lookup"><span data-stu-id="cab5e-103">CBaseVideoRenderer.get\_FramesDroppedInRenderer method</span></span>

<span data-ttu-id="cab5e-104">方法會抓取轉譯器 `get_FramesDroppedInRenderer` 捨棄的框架數目。</span><span class="sxs-lookup"><span data-stu-id="cab5e-104">The `get_FramesDroppedInRenderer` method retrieves the number of frames dropped by the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cab5e-105">語法</span><span class="sxs-lookup"><span data-stu-id="cab5e-105">Syntax</span></span>


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a><span data-ttu-id="cab5e-106">參數</span><span class="sxs-lookup"><span data-stu-id="cab5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cab5e-107">*pcFramesDropped*</span><span class="sxs-lookup"><span data-stu-id="cab5e-107">*pcFramesDropped*</span></span> 
</dt> <dd>

<span data-ttu-id="cab5e-108">已卸載的框架數目指標。</span><span class="sxs-lookup"><span data-stu-id="cab5e-108">Pointer to the number of frames dropped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cab5e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="cab5e-109">Return value</span></span>

<span data-ttu-id="cab5e-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="cab5e-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cab5e-111">備註</span><span class="sxs-lookup"><span data-stu-id="cab5e-111">Remarks</span></span>

<span data-ttu-id="cab5e-112">此成員函式會實 [**IQualProp：： get \_ FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) 方法。</span><span class="sxs-lookup"><span data-stu-id="cab5e-112">This member function implements the [**IQualProp::get\_FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) method.</span></span> <span data-ttu-id="cab5e-113">這是屬性頁從排程器抓取資料的方式。</span><span class="sxs-lookup"><span data-stu-id="cab5e-113">This is how the property page retrieves the data from the scheduler.</span></span> <span data-ttu-id="cab5e-114">您也可以在不看到轉譯器的情況下，將框架卸載至上游。</span><span class="sxs-lookup"><span data-stu-id="cab5e-114">Frames can also be dropped upstream without the renderer even seeing them.</span></span>

## <a name="requirements"></a><span data-ttu-id="cab5e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="cab5e-115">Requirements</span></span>



| <span data-ttu-id="cab5e-116">需求</span><span class="sxs-lookup"><span data-stu-id="cab5e-116">Requirement</span></span> | <span data-ttu-id="cab5e-117">值</span><span class="sxs-lookup"><span data-stu-id="cab5e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cab5e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="cab5e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cab5e-119"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cab5e-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cab5e-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="cab5e-120">Library</span></span><br/> | <dl> <span data-ttu-id="cab5e-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cab5e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cab5e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cab5e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cab5e-123">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="cab5e-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




