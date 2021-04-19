---
description: OnRenderEnd 方法會在轉譯時間因中斷而異的情況下執行平滑處理。
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: 'CBaseVideoRenderer. OnRenderEnd 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f37b4d03f77090f4cac40a218fd3ac27c0c349d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989255"
---
# <a name="cbasevideorendereronrenderend-method"></a><span data-ttu-id="7eeaf-103">CBaseVideoRenderer. OnRenderEnd 方法</span><span class="sxs-lookup"><span data-stu-id="7eeaf-103">CBaseVideoRenderer.OnRenderEnd method</span></span>

<span data-ttu-id="7eeaf-104">當轉譯 `OnRenderEnd` 時間因中斷而改變時，方法會執行平滑處理。</span><span class="sxs-lookup"><span data-stu-id="7eeaf-104">The `OnRenderEnd` method performs smoothing for cases where the rendering time varies due to interruptions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eeaf-105">語法</span><span class="sxs-lookup"><span data-stu-id="7eeaf-105">Syntax</span></span>


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="7eeaf-106">參數</span><span class="sxs-lookup"><span data-stu-id="7eeaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eeaf-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="7eeaf-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="7eeaf-108">媒體範例的指標。</span><span class="sxs-lookup"><span data-stu-id="7eeaf-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eeaf-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7eeaf-109">Return value</span></span>

<span data-ttu-id="7eeaf-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7eeaf-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7eeaf-111">備註</span><span class="sxs-lookup"><span data-stu-id="7eeaf-111">Remarks</span></span>

<span data-ttu-id="7eeaf-112">在繪製影像之後，就應該呼叫這個成員函式。</span><span class="sxs-lookup"><span data-stu-id="7eeaf-112">This member function should be called just after drawing an image.</span></span>

<span data-ttu-id="7eeaf-113">此成員函式會覆寫 [**CBaseRenderer：： OnRenderEnd**](cbaserenderer-onrenderend.md)。</span><span class="sxs-lookup"><span data-stu-id="7eeaf-113">This member function overrides [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7eeaf-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7eeaf-114">Requirements</span></span>



| <span data-ttu-id="7eeaf-115">需求</span><span class="sxs-lookup"><span data-stu-id="7eeaf-115">Requirement</span></span> | <span data-ttu-id="7eeaf-116">值</span><span class="sxs-lookup"><span data-stu-id="7eeaf-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eeaf-117">標頭</span><span class="sxs-lookup"><span data-stu-id="7eeaf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7eeaf-118"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7eeaf-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7eeaf-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="7eeaf-119">Library</span></span><br/> | <dl> <span data-ttu-id="7eeaf-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7eeaf-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eeaf-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7eeaf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eeaf-122">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="7eeaf-122">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




