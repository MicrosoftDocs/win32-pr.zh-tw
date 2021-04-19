---
description: SetSink 方法會設定將接收品質訊息的 IQualityControl 物件。
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: 'CBaseVideoRenderer. SetSink 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9658ab4a1099e7baaef0a3e1a0ae3c0d495e89e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977626"
---
# <a name="cbasevideorenderersetsink-method"></a><span data-ttu-id="cbe98-103">CBaseVideoRenderer. SetSink 方法</span><span class="sxs-lookup"><span data-stu-id="cbe98-103">CBaseVideoRenderer.SetSink method</span></span>

<span data-ttu-id="cbe98-104">`SetSink`方法會設定將接收品質訊息的 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)物件。</span><span class="sxs-lookup"><span data-stu-id="cbe98-104">The `SetSink` method sets the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) object that will receive quality messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbe98-105">語法</span><span class="sxs-lookup"><span data-stu-id="cbe98-105">Syntax</span></span>


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a><span data-ttu-id="cbe98-106">參數</span><span class="sxs-lookup"><span data-stu-id="cbe98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbe98-107">*piqc*</span><span class="sxs-lookup"><span data-stu-id="cbe98-107">*piqc*</span></span> 
</dt> <dd>

<span data-ttu-id="cbe98-108">應傳送通知之 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="cbe98-108">Pointer to the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) object to which the notifications should be sent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbe98-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="cbe98-109">Return value</span></span>

<span data-ttu-id="cbe98-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="cbe98-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbe98-111">備註</span><span class="sxs-lookup"><span data-stu-id="cbe98-111">Remarks</span></span>

<span data-ttu-id="cbe98-112">此成員函式會在影片轉譯器上 [**執行 IQualityControl：： SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) 方法。</span><span class="sxs-lookup"><span data-stu-id="cbe98-112">This member function implements the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method on the video renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbe98-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbe98-113">Requirements</span></span>



| <span data-ttu-id="cbe98-114">需求</span><span class="sxs-lookup"><span data-stu-id="cbe98-114">Requirement</span></span> | <span data-ttu-id="cbe98-115">值</span><span class="sxs-lookup"><span data-stu-id="cbe98-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe98-116">標頭</span><span class="sxs-lookup"><span data-stu-id="cbe98-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cbe98-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cbe98-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cbe98-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="cbe98-118">Library</span></span><br/> | <dl> <span data-ttu-id="cbe98-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cbe98-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbe98-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cbe98-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe98-121">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="cbe98-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




