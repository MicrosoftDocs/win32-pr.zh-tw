---
description: DisplaySampleTimes 方法會在影片影像上方繪製媒體範例的時間戳記。
ms.assetid: 3741dc74-5311-4cb1-9e6b-4a8bf6113477
title: 'CDrawImage. DisplaySampleTimes 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DisplaySampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9988aaedf9a1c01c83412cdbe9e00533556c9b15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995520"
---
# <a name="cdrawimagedisplaysampletimes-method"></a><span data-ttu-id="88d3a-103">CDrawImage. DisplaySampleTimes 方法</span><span class="sxs-lookup"><span data-stu-id="88d3a-103">CDrawImage.DisplaySampleTimes method</span></span>

<span data-ttu-id="88d3a-104">`DisplaySampleTimes`方法會在影片影像上方繪製媒體範例的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="88d3a-104">The `DisplaySampleTimes` method draws the time stamps of a media sample on top of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="88d3a-105">語法</span><span class="sxs-lookup"><span data-stu-id="88d3a-105">Syntax</span></span>


```C++
void DisplaySampleTimes(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="88d3a-106">參數</span><span class="sxs-lookup"><span data-stu-id="88d3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88d3a-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="88d3a-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="88d3a-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="88d3a-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88d3a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="88d3a-109">Return value</span></span>

<span data-ttu-id="88d3a-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="88d3a-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88d3a-111">備註</span><span class="sxs-lookup"><span data-stu-id="88d3a-111">Remarks</span></span>

<span data-ttu-id="88d3a-112">這個方法只會在 debug 組建中呼叫。</span><span class="sxs-lookup"><span data-stu-id="88d3a-112">This method is called only in debug builds.</span></span>

## <a name="requirements"></a><span data-ttu-id="88d3a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="88d3a-113">Requirements</span></span>



| <span data-ttu-id="88d3a-114">需求</span><span class="sxs-lookup"><span data-stu-id="88d3a-114">Requirement</span></span> | <span data-ttu-id="88d3a-115">值</span><span class="sxs-lookup"><span data-stu-id="88d3a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88d3a-116">標頭</span><span class="sxs-lookup"><span data-stu-id="88d3a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="88d3a-117"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="88d3a-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="88d3a-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="88d3a-118">Library</span></span><br/> | <dl> <span data-ttu-id="88d3a-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="88d3a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88d3a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88d3a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88d3a-121">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="88d3a-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




