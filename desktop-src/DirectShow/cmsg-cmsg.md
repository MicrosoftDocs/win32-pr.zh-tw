---
description: 結構 CMsg 物件。
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: 'CMsg. CMsg (Msgthrd. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg.CMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b26a9572b51d4a476b70c3dd7ddae8c896a4d648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000832"
---
# <a name="cmsgcmsg-constructor"></a><span data-ttu-id="9da1b-103">CMsg. CMsg 函數</span><span class="sxs-lookup"><span data-stu-id="9da1b-103">CMsg.CMsg constructor</span></span>

<span data-ttu-id="9da1b-104">結構 [**CMsg**](cmsg.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="9da1b-104">Constructs a [**CMsg**](cmsg.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9da1b-105">語法</span><span class="sxs-lookup"><span data-stu-id="9da1b-105">Syntax</span></span>


```C++
CMsg(
   UINT     u,
   DWORD    dw,
   LPVOID   lp,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a><span data-ttu-id="9da1b-106">參數</span><span class="sxs-lookup"><span data-stu-id="9da1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9da1b-107">*u*</span><span class="sxs-lookup"><span data-stu-id="9da1b-107">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="9da1b-108">要求碼，由執行緒類別的用戶端所定義，並由覆寫的背景工作執行緒函數理解。</span><span class="sxs-lookup"><span data-stu-id="9da1b-108">Request code, defined by the client of the thread class and understood by the overridden worker thread function.</span></span>

</dd> <dt>

<span data-ttu-id="9da1b-109">*dw*</span><span class="sxs-lookup"><span data-stu-id="9da1b-109">*dw*</span></span> 
</dt> <dd>

<span data-ttu-id="9da1b-110">要求碼的旗標參數。</span><span class="sxs-lookup"><span data-stu-id="9da1b-110">Flag parameter to the request code.</span></span>

</dd> <dt>

<span data-ttu-id="9da1b-111">*lp*</span><span class="sxs-lookup"><span data-stu-id="9da1b-111">*lp*</span></span> 
</dt> <dd>

<span data-ttu-id="9da1b-112">背景工作執行緒所需的資料指標，作為參數或傳回值。</span><span class="sxs-lookup"><span data-stu-id="9da1b-112">Pointer to data required by the worker thread as parameter or return values.</span></span> <span data-ttu-id="9da1b-113">此資料不應以堆疊為基礎，因為它會在完成佇列作業之後被參考一段時間。</span><span class="sxs-lookup"><span data-stu-id="9da1b-113">This data should not be stack-based, as it will be referenced some time after completing the queuing operation.</span></span>

</dd> <dt>

<span data-ttu-id="9da1b-114">*pEvent*</span><span class="sxs-lookup"><span data-stu-id="9da1b-114">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="9da1b-115">背景工作執行緒可以指示的事件物件指標，表示作業已完成。</span><span class="sxs-lookup"><span data-stu-id="9da1b-115">Pointer to the event object that a worker thread can signal to indicate the completion of the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9da1b-116">備註</span><span class="sxs-lookup"><span data-stu-id="9da1b-116">Remarks</span></span>

<span data-ttu-id="9da1b-117">此成員函式包含 [**CMsgThread**](cmsgthread.md) worker 執行緒的要求，以採取動作。</span><span class="sxs-lookup"><span data-stu-id="9da1b-117">This member function contains a request for a [**CMsgThread**](cmsgthread.md) worker thread to act on.</span></span> <span data-ttu-id="9da1b-118">處理此訊息時，會將所有參數傳遞至背景工作執行緒函式作為參數。</span><span class="sxs-lookup"><span data-stu-id="9da1b-118">All the parameters are passed to the worker thread function as parameters when this message gets processed.</span></span> <span data-ttu-id="9da1b-119">參數的意義是由呼叫工作者執行緒的用戶端函數以及提供工作者執行緒執行函式的衍生類別所定義。</span><span class="sxs-lookup"><span data-stu-id="9da1b-119">The meanings of the parameters are defined by the client function that calls the worker thread and the derived class that supplies the worker thread's execution function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9da1b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="9da1b-120">Requirements</span></span>



| <span data-ttu-id="9da1b-121">需求</span><span class="sxs-lookup"><span data-stu-id="9da1b-121">Requirement</span></span> | <span data-ttu-id="9da1b-122">值</span><span class="sxs-lookup"><span data-stu-id="9da1b-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9da1b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9da1b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9da1b-124"><dt>Msgthrd (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9da1b-124"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9da1b-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="9da1b-125">Library</span></span><br/> | <dl> <span data-ttu-id="9da1b-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9da1b-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




