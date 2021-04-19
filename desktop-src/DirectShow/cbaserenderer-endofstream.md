---
description: EndOfStream 方法會通知篩選輸入 pin 收到的資料流程結束通知。
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: 'CBaseRenderer. EndOfStream 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e12da02ffbce99b29d324c1166b3d4cdf2265c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983081"
---
# <a name="cbaserendererendofstream-method"></a><span data-ttu-id="2f466-103">CBaseRenderer. EndOfStream 方法</span><span class="sxs-lookup"><span data-stu-id="2f466-103">CBaseRenderer.EndOfStream method</span></span>

<span data-ttu-id="2f466-104">`EndOfStream`方法會通知篩選輸入 pin 收到的資料流程結束通知。</span><span class="sxs-lookup"><span data-stu-id="2f466-104">The `EndOfStream` method notifies the filter that the input pin received an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f466-105">語法</span><span class="sxs-lookup"><span data-stu-id="2f466-105">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="2f466-106">參數</span><span class="sxs-lookup"><span data-stu-id="2f466-106">Parameters</span></span>

<span data-ttu-id="2f466-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2f466-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f466-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f466-108">Return value</span></span>

<span data-ttu-id="2f466-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2f466-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f466-110">備註</span><span class="sxs-lookup"><span data-stu-id="2f466-110">Remarks</span></span>

<span data-ttu-id="2f466-111">篩選的輸入 pin 會在收到資料流程結束通知時呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="2f466-111">The filter's input pin calls this method when it receives an end-of-stream notification.</span></span>

<span data-ttu-id="2f466-112">這個方法會將 [**CBaseRenderer：： m \_ bEOS**](cbaserenderer-m-beos.md) 旗標設定為 **TRUE** ，並呼叫 [**CBaseRenderer：： SendEndOfStream**](cbaserenderer-sendendofstream.md) 方法來排定 [**EC \_ 完成**](ec-complete.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="2f466-112">This method sets the [**CBaseRenderer::m\_bEOS**](cbaserenderer-m-beos.md) flag to **TRUE** and calls the [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) method to schedule an [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="2f466-113">如果篩選已暫停且正在等候範例，這個方法會完成狀態轉換。</span><span class="sxs-lookup"><span data-stu-id="2f466-113">If the filter is paused and waiting for a sample, this method completes the state transition.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f466-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f466-114">Requirements</span></span>



| <span data-ttu-id="2f466-115">需求</span><span class="sxs-lookup"><span data-stu-id="2f466-115">Requirement</span></span> | <span data-ttu-id="2f466-116">值</span><span class="sxs-lookup"><span data-stu-id="2f466-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f466-117">標頭</span><span class="sxs-lookup"><span data-stu-id="2f466-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2f466-118"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2f466-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f466-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="2f466-119">Library</span></span><br/> | <dl> <span data-ttu-id="2f466-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2f466-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f466-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f466-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f466-122">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="2f466-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




