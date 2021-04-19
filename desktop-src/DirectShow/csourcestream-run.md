---
description: Run 方法會通知串流執行緒執行。
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: 'CSourceStream： Run 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39093654677ab4828f8a1d5a01a8cf7deaf42507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994856"
---
# <a name="csourcestreamrun-method"></a><span data-ttu-id="1adc8-103">CSourceStream 方法</span><span class="sxs-lookup"><span data-stu-id="1adc8-103">CSourceStream.Run method</span></span>

<span data-ttu-id="1adc8-104">`Run`方法會通知串流執行緒執行。</span><span class="sxs-lookup"><span data-stu-id="1adc8-104">The `Run` method signals the streaming thread to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="1adc8-105">語法</span><span class="sxs-lookup"><span data-stu-id="1adc8-105">Syntax</span></span>


```C++
HRESULT Run();
```



## <a name="parameters"></a><span data-ttu-id="1adc8-106">參數</span><span class="sxs-lookup"><span data-stu-id="1adc8-106">Parameters</span></span>

<span data-ttu-id="1adc8-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1adc8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1adc8-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="1adc8-108">Return value</span></span>

<span data-ttu-id="1adc8-109">傳回 \_ [OK] 或 [E 未 \_ 預期]。</span><span class="sxs-lookup"><span data-stu-id="1adc8-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="1adc8-110">備註</span><span class="sxs-lookup"><span data-stu-id="1adc8-110">Remarks</span></span>

<span data-ttu-id="1adc8-111">在基類中，此方法的效果與 [**CSourceStream：:P ause**](csourcestream-pause.md) 要求相同，且不會使用。</span><span class="sxs-lookup"><span data-stu-id="1adc8-111">In the base class, this method has the same effect as the [**CSourceStream::Pause**](csourcestream-pause.md) request, and is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="1adc8-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="1adc8-112">Requirements</span></span>



| <span data-ttu-id="1adc8-113">需求</span><span class="sxs-lookup"><span data-stu-id="1adc8-113">Requirement</span></span> | <span data-ttu-id="1adc8-114">值</span><span class="sxs-lookup"><span data-stu-id="1adc8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1adc8-115">標頭</span><span class="sxs-lookup"><span data-stu-id="1adc8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="1adc8-116"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="1adc8-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1adc8-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="1adc8-117">Library</span></span><br/> | <dl> <span data-ttu-id="1adc8-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1adc8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1adc8-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1adc8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1adc8-120">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="1adc8-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




