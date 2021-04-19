---
description: GetCommandDueFor 方法會抓取在指定時間排程的延後命令。
ms.assetid: f8a2f9ae-f359-4429-aca5-021b6fe2aa93
title: 'CCmdQueue. GetCommandDueFor 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetCommandDueFor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48a01436a68a5b98d08880c1516bbf4576d10be2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992385"
---
# <a name="ccmdqueuegetcommandduefor-method"></a><span data-ttu-id="a9c5d-103">CCmdQueue. GetCommandDueFor 方法</span><span class="sxs-lookup"><span data-stu-id="a9c5d-103">CCmdQueue.GetCommandDueFor method</span></span>

<span data-ttu-id="a9c5d-104">`GetCommandDueFor`方法會抓取在指定時間排程的延後命令。</span><span class="sxs-lookup"><span data-stu-id="a9c5d-104">The `GetCommandDueFor` method retrieves a deferred command that is scheduled at a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c5d-105">語法</span><span class="sxs-lookup"><span data-stu-id="a9c5d-105">Syntax</span></span>


```C++
virtual HRESULT GetCommandDueFor(
   REFERENCE_TIME   tStream,
   CDeferredCommand **ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="a9c5d-106">參數</span><span class="sxs-lookup"><span data-stu-id="a9c5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9c5d-107">*tStream*</span><span class="sxs-lookup"><span data-stu-id="a9c5d-107">*tStream*</span></span> 
</dt> <dd>

<span data-ttu-id="a9c5d-108">排定命令的時間。</span><span class="sxs-lookup"><span data-stu-id="a9c5d-108">Time for which the command is scheduled.</span></span>

</dd> <dt>

<span data-ttu-id="a9c5d-109">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="a9c5d-109">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="a9c5d-110">要在 *tStream* 參數中指定的時間執行之延後命令指標的位址。</span><span class="sxs-lookup"><span data-stu-id="a9c5d-110">Address of a pointer to the deferred command to be carried out at the time specified in the *tStream* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9c5d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9c5d-111">Return value</span></span>

<span data-ttu-id="a9c5d-112">\_ \_ 如果沒有任何命令，則會傳回 VFW E \_ ; 否則會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="a9c5d-112">Returns VFW\_E\_NOT\_FOUND if no commands are due; otherwise, returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9c5d-113">備註</span><span class="sxs-lookup"><span data-stu-id="a9c5d-113">Remarks</span></span>

<span data-ttu-id="a9c5d-114">此成員函式會接受資料流程時間，並傳回該時間排程的延遲命令。</span><span class="sxs-lookup"><span data-stu-id="a9c5d-114">This member function takes a stream time and returns the deferred command scheduled at that time.</span></span> <span data-ttu-id="a9c5d-115">執行命令佇列時，會計算實際的資料流程時間位移。</span><span class="sxs-lookup"><span data-stu-id="a9c5d-115">The actual stream-time offset is calculated when the command queue is run.</span></span> <span data-ttu-id="a9c5d-116">命令會保持佇列，直到執行或取消為止。</span><span class="sxs-lookup"><span data-stu-id="a9c5d-116">Commands remain queued until run or canceled.</span></span> <span data-ttu-id="a9c5d-117">此成員函式不會封鎖。</span><span class="sxs-lookup"><span data-stu-id="a9c5d-117">This member function will not block.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9c5d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9c5d-118">Requirements</span></span>



| <span data-ttu-id="a9c5d-119">需求</span><span class="sxs-lookup"><span data-stu-id="a9c5d-119">Requirement</span></span> | <span data-ttu-id="a9c5d-120">值</span><span class="sxs-lookup"><span data-stu-id="a9c5d-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c5d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="a9c5d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a9c5d-122"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a9c5d-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a9c5d-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="a9c5d-123">Library</span></span><br/> | <dl> <span data-ttu-id="a9c5d-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a9c5d-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9c5d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9c5d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9c5d-126">**CCmdQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="a9c5d-126">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




