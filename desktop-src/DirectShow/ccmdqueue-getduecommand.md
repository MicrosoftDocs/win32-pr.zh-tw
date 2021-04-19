---
description: GetDueCommand 方法會抓取指向下一個已到期命令的指標。
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: 'CCmdQueue. GetDueCommand 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a1297a3f0d514215270acf7e73b18cba46fca1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999094"
---
# <a name="ccmdqueuegetduecommand-method"></a><span data-ttu-id="23a4a-103">CCmdQueue. GetDueCommand 方法</span><span class="sxs-lookup"><span data-stu-id="23a4a-103">CCmdQueue.GetDueCommand method</span></span>

<span data-ttu-id="23a4a-104">`GetDueCommand`方法會抓取指向下一個命令的指標。</span><span class="sxs-lookup"><span data-stu-id="23a4a-104">The `GetDueCommand` method retrieves a pointer to the next command that is due.</span></span>

## <a name="syntax"></a><span data-ttu-id="23a4a-105">語法</span><span class="sxs-lookup"><span data-stu-id="23a4a-105">Syntax</span></span>


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="23a4a-106">參數</span><span class="sxs-lookup"><span data-stu-id="23a4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23a4a-107">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="23a4a-107">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="23a4a-108">延後命令指標的位址。</span><span class="sxs-lookup"><span data-stu-id="23a4a-108">Address of a pointer to the deferred command.</span></span>

</dd> <dt>

<span data-ttu-id="23a4a-109">*msTimeout*</span><span class="sxs-lookup"><span data-stu-id="23a4a-109">*msTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="23a4a-110">執行超時之前要等候的時間量。</span><span class="sxs-lookup"><span data-stu-id="23a4a-110">Amount of time to wait before carrying out the time-out.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23a4a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="23a4a-111">Return value</span></span>

<span data-ttu-id="23a4a-112">\_如果發生超時，則傳回 E ABORT。</span><span class="sxs-lookup"><span data-stu-id="23a4a-112">Returns E\_ABORT if a time-out occurs.</span></span> <span data-ttu-id="23a4a-113">\_如果成功，則傳回 [確定]，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="23a4a-113">Returns S\_OK if successful; otherwise, returns an error.</span></span> <span data-ttu-id="23a4a-114">傳回已使用 **IUnknown：： AddRef** 遞增的物件。</span><span class="sxs-lookup"><span data-stu-id="23a4a-114">Returns an object that has been incremented using **IUnknown::AddRef**.</span></span>

## <a name="remarks"></a><span data-ttu-id="23a4a-115">備註</span><span class="sxs-lookup"><span data-stu-id="23a4a-115">Remarks</span></span>

<span data-ttu-id="23a4a-116">此成員函式會封鎖，直到暫止的命令到期為止。</span><span class="sxs-lookup"><span data-stu-id="23a4a-116">This member function blocks until a pending command is due.</span></span> <span data-ttu-id="23a4a-117">成員函式會封鎖 *msTimeout* 參數中指定的時間量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="23a4a-117">The member function blocks for the amount of time, in milliseconds, specified in the *msTimeout* parameter.</span></span> <span data-ttu-id="23a4a-118">資料流程時間命令只會在 [**CCmdQueue：： Run**](ccmdqueue-run.md) 和 [**CCmdQueue：： EndRun**](ccmdqueue-endrun.md) 成員函式之間到期。</span><span class="sxs-lookup"><span data-stu-id="23a4a-118">Stream-time commands become due only between the [**CCmdQueue::Run**](ccmdqueue-run.md) and [**CCmdQueue::EndRun**](ccmdqueue-endrun.md) member functions.</span></span> <span data-ttu-id="23a4a-119">此命令會一直排入佇列，直到執行或取消為止。</span><span class="sxs-lookup"><span data-stu-id="23a4a-119">The command remains queued until run or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="23a4a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="23a4a-120">Requirements</span></span>



| <span data-ttu-id="23a4a-121">需求</span><span class="sxs-lookup"><span data-stu-id="23a4a-121">Requirement</span></span> | <span data-ttu-id="23a4a-122">值</span><span class="sxs-lookup"><span data-stu-id="23a4a-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23a4a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="23a4a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="23a4a-124"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="23a4a-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="23a4a-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="23a4a-125">Library</span></span><br/> | <dl> <span data-ttu-id="23a4a-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="23a4a-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23a4a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23a4a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23a4a-128">**CCmdQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="23a4a-128">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




