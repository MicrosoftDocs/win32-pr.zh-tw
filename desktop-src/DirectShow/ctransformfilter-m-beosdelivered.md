---
description: 指出篩選是否已傳送資料流程結束通知的旗標。
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: 'CTransformFilter：： m_bEOSDelivered 成員 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24b87f9808c53b5f64f66031a8ee2a4e9449089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978447"
---
# <a name="ctransformfilterm_beosdelivered-member"></a><span data-ttu-id="00b9a-103">CTransformFilter：： m \_ bEOSDelivered 成員</span><span class="sxs-lookup"><span data-stu-id="00b9a-103">CTransformFilter::m\_bEOSDelivered member</span></span>

<span data-ttu-id="00b9a-104">指出篩選是否已傳送資料流程結束通知的旗標。</span><span class="sxs-lookup"><span data-stu-id="00b9a-104">Flag that indicates whether the filter has sent an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="00b9a-105">語法</span><span class="sxs-lookup"><span data-stu-id="00b9a-105">Syntax</span></span>


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a><span data-ttu-id="00b9a-106">備註</span><span class="sxs-lookup"><span data-stu-id="00b9a-106">Remarks</span></span>

<span data-ttu-id="00b9a-107">如果篩選在沒有輸入連接時暫停，則會傳送下游的結束資料流程通知，並將此旗標設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="00b9a-107">If the filter pauses when it does not have an input connection, it sends an end-of-stream notification downstream and sets this flag to **TRUE**.</span></span> <span data-ttu-id="00b9a-108">資料流程結束通知可確保下游篩選不會等候樣本。</span><span class="sxs-lookup"><span data-stu-id="00b9a-108">The end-of-stream notification ensures that the downstream filter does not wait for samples.</span></span> <span data-ttu-id="00b9a-109">請注意，篩選的 [**EndOfStream**](ctransformfilter-endofstream.md) 方法不會設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="00b9a-109">Note that the filter's [**EndOfStream**](ctransformfilter-endofstream.md) method does not set this flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="00b9a-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="00b9a-110">Requirements</span></span>



| <span data-ttu-id="00b9a-111">需求</span><span class="sxs-lookup"><span data-stu-id="00b9a-111">Requirement</span></span> | <span data-ttu-id="00b9a-112">值</span><span class="sxs-lookup"><span data-stu-id="00b9a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00b9a-113">標頭</span><span class="sxs-lookup"><span data-stu-id="00b9a-113">Header</span></span><br/>  | <dl> <span data-ttu-id="00b9a-114"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="00b9a-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="00b9a-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="00b9a-115">Library</span></span><br/> | <dl> <span data-ttu-id="00b9a-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="00b9a-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00b9a-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00b9a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00b9a-118">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="00b9a-118">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




