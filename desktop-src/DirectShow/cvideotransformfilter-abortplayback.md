---
description: AbortPlayback 方法是用來發出串流錯誤的信號。 它會將 EC \_ ERRORABORT 事件傳送至篩選圖形管理員，並傳送下游的結束資料流程通知。
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: 'CVideoTransformFilter. AbortPlayback 方法 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 952987dec315408920e92d79003480a01640d14e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981877"
---
# <a name="cvideotransformfilterabortplayback-method"></a><span data-ttu-id="8eddd-104">CVideoTransformFilter. AbortPlayback 方法</span><span class="sxs-lookup"><span data-stu-id="8eddd-104">CVideoTransformFilter.AbortPlayback method</span></span>

<span data-ttu-id="8eddd-105">`AbortPlayback`方法是用來發出串流錯誤的信號。</span><span class="sxs-lookup"><span data-stu-id="8eddd-105">The `AbortPlayback` method is used to signal a streaming error.</span></span> <span data-ttu-id="8eddd-106">它會將 [**EC \_ ERRORABORT**](ec-errorabort.md) 事件傳送至篩選圖形管理員，並傳送下游的結束資料流程通知。</span><span class="sxs-lookup"><span data-stu-id="8eddd-106">It sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the Filter Graph Manager, and sends an end-of-stream notification downstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eddd-107">語法</span><span class="sxs-lookup"><span data-stu-id="8eddd-107">Syntax</span></span>


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="8eddd-108">參數</span><span class="sxs-lookup"><span data-stu-id="8eddd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eddd-109">*小時*</span><span class="sxs-lookup"><span data-stu-id="8eddd-109">*hr*</span></span> 
</dt> <dd>

<span data-ttu-id="8eddd-110">失敗之作業的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="8eddd-110">**HRESULT** value of the operation that failed.</span></span> <span data-ttu-id="8eddd-111">這個值是用來做為 EC ERRORABORT 事件的第一個事件參數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8eddd-111">This value is used as the first event parameter for the EC\_ERRORABORT event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eddd-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8eddd-112">Return value</span></span>

<span data-ttu-id="8eddd-113">傳回 *hr* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="8eddd-113">Returns the value of the *hr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eddd-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8eddd-114">Requirements</span></span>



| <span data-ttu-id="8eddd-115">需求</span><span class="sxs-lookup"><span data-stu-id="8eddd-115">Requirement</span></span> | <span data-ttu-id="8eddd-116">值</span><span class="sxs-lookup"><span data-stu-id="8eddd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eddd-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8eddd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8eddd-118"><dt>Vtrans (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8eddd-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8eddd-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="8eddd-119">Library</span></span><br/> | <dl> <span data-ttu-id="8eddd-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8eddd-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eddd-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8eddd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eddd-122">**CVideoTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="8eddd-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




