---
description: Run 方法會切換至執行模式，以便執行由資料流程時間延遲的命令。
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: 'CCmdQueue： Run 方法 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 424914e53a12ff0f43e8b7e2a3345c28d84437d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993955"
---
# <a name="ccmdqueuerun-method"></a><span data-ttu-id="9150d-103">CCmdQueue 方法</span><span class="sxs-lookup"><span data-stu-id="9150d-103">CCmdQueue.Run method</span></span>

<span data-ttu-id="9150d-104">`Run`方法會切換至執行模式，以便執行由資料流程時間延遲的命令。</span><span class="sxs-lookup"><span data-stu-id="9150d-104">The `Run` method switches to running mode so that commands that are deferred by the stream time can be run.</span></span>

## <a name="syntax"></a><span data-ttu-id="9150d-105">語法</span><span class="sxs-lookup"><span data-stu-id="9150d-105">Syntax</span></span>


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a><span data-ttu-id="9150d-106">參數</span><span class="sxs-lookup"><span data-stu-id="9150d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9150d-107">*tStreamTimeOffset*</span><span class="sxs-lookup"><span data-stu-id="9150d-107">*tStreamTimeOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="9150d-108">位移時間。</span><span class="sxs-lookup"><span data-stu-id="9150d-108">Offset time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9150d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="9150d-109">Return value</span></span>

<span data-ttu-id="9150d-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="9150d-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9150d-111">備註</span><span class="sxs-lookup"><span data-stu-id="9150d-111">Remarks</span></span>

<span data-ttu-id="9150d-112">在執行模式中，已知資料流程時間與呈現時間的對應。</span><span class="sxs-lookup"><span data-stu-id="9150d-112">During running mode, stream-time-to-presentation-time mapping is known.</span></span>

## <a name="requirements"></a><span data-ttu-id="9150d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9150d-113">Requirements</span></span>



| <span data-ttu-id="9150d-114">需求</span><span class="sxs-lookup"><span data-stu-id="9150d-114">Requirement</span></span> | <span data-ttu-id="9150d-115">值</span><span class="sxs-lookup"><span data-stu-id="9150d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9150d-116">標頭</span><span class="sxs-lookup"><span data-stu-id="9150d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9150d-117"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9150d-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9150d-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="9150d-118">Library</span></span><br/> | <dl> <span data-ttu-id="9150d-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9150d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9150d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9150d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9150d-121">**CCmdQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="9150d-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




