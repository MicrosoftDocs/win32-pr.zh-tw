---
description: Seek 方法會設定資料流程的開始和停止位置。
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: 'CPullPin： Seek 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Seek
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f1a82ec549b5ceb888acc194a7abc2cd3eace47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990748"
---
# <a name="cpullpinseek-method"></a><span data-ttu-id="9680f-103">CPullPin. Seek 方法</span><span class="sxs-lookup"><span data-stu-id="9680f-103">CPullPin.Seek method</span></span>

<span data-ttu-id="9680f-104">`Seek`方法會設定資料流程的開始和停止位置。</span><span class="sxs-lookup"><span data-stu-id="9680f-104">The `Seek` method sets the start and stop positions of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="9680f-105">語法</span><span class="sxs-lookup"><span data-stu-id="9680f-105">Syntax</span></span>


```C++
HRESULT Seek(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop
);
```



## <a name="parameters"></a><span data-ttu-id="9680f-106">參數</span><span class="sxs-lookup"><span data-stu-id="9680f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9680f-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="9680f-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="9680f-108">指定開始位置，以位元組乘以10000000。</span><span class="sxs-lookup"><span data-stu-id="9680f-108">Specifies the start position, in bytes multiplied by 10,000,000.</span></span>

</dd> <dt>

<span data-ttu-id="9680f-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="9680f-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="9680f-110">指定停止位置，以位元組乘以10000000。</span><span class="sxs-lookup"><span data-stu-id="9680f-110">Specifies the stop position, in bytes multiplied by 10,000,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9680f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9680f-111">Return value</span></span>

<span data-ttu-id="9680f-112">\_如果方法成功，則傳回 S OK，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9680f-112">Returns S\_OK if the method succeeds, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9680f-113">備註</span><span class="sxs-lookup"><span data-stu-id="9680f-113">Remarks</span></span>

<span data-ttu-id="9680f-114">如果背景工作執行緒正在執行，方法會暫停執行緒、排清篩選圖形，然後繼續執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="9680f-114">If the worker thread is running, the method pauses the thread, flushes the filter graph, and resumes the thread.</span></span> <span data-ttu-id="9680f-115">執行緒會從新的開始位置開始提取資料。</span><span class="sxs-lookup"><span data-stu-id="9680f-115">The thread begins pulling data from the new start position.</span></span> <span data-ttu-id="9680f-116">否則，每當啟動執行緒時，新的位置值就會生效。</span><span class="sxs-lookup"><span data-stu-id="9680f-116">Otherwise, the new position values become effective whenever the thread is started.</span></span>

<span data-ttu-id="9680f-117">位置是相對於原始來源的起點。</span><span class="sxs-lookup"><span data-stu-id="9680f-117">Positions are relative to the start of the original source.</span></span> <span data-ttu-id="9680f-118">將所需的位元組位移乘以在基類庫中定義為10000000的常數單位。</span><span class="sxs-lookup"><span data-stu-id="9680f-118">Multiply the desired byte offsets by the constant UNITS, which is defined in the base class library as 10,000,000.</span></span>

<span data-ttu-id="9680f-119">當 pin 首次連接時，[停止] 和 [開始] 位置會預設為數據流的開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="9680f-119">When the pin first connects, the stop and start positions default to the beginning and end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="9680f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="9680f-120">Requirements</span></span>



| <span data-ttu-id="9680f-121">需求</span><span class="sxs-lookup"><span data-stu-id="9680f-121">Requirement</span></span> | <span data-ttu-id="9680f-122">值</span><span class="sxs-lookup"><span data-stu-id="9680f-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9680f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9680f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9680f-124"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="9680f-124"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="9680f-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="9680f-125">Library</span></span><br/> | <dl> <span data-ttu-id="9680f-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9680f-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9680f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9680f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9680f-128">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="9680f-128">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




