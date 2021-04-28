---
description: CDeferredCommand。 CDeferredCommand 函式-函數方法。
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: 'CDeferredCommand. CDeferredCommand (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.CDeferredCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a10d8bba48902ed2d6fd66da8483cea1ba9aacc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119786"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a><span data-ttu-id="35ba4-103">CDeferredCommand. CDeferredCommand 函數</span><span class="sxs-lookup"><span data-stu-id="35ba4-103">CDeferredCommand.CDeferredCommand constructor</span></span>

<span data-ttu-id="35ba4-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="35ba4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ba4-105">語法</span><span class="sxs-lookup"><span data-stu-id="35ba4-105">Syntax</span></span>


```C++
CDeferredCommand(
   CCmdQueue *pQ,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   LPUNKNOWN pUnkExecutor,
   REFTIME   time,
   GUID      *iid,
   long      dispidMethod,
   short     wFlags,
   long      cArgs,
   VARIANT   *pDispParams,
   VARIANT   *pvarResult,
   short     *puArgErr,
   BOOL      bStream
);
```



## <a name="parameters"></a><span data-ttu-id="35ba4-106">參數</span><span class="sxs-lookup"><span data-stu-id="35ba4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ba4-107">*Pq*</span><span class="sxs-lookup"><span data-stu-id="35ba4-107">*pQ*</span></span> 
</dt> <dd>

<span data-ttu-id="35ba4-108">公開 [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) 介面之物件的指標。</span><span class="sxs-lookup"><span data-stu-id="35ba4-108">Pointer to an object that exposes the [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) interface.</span></span>

</dd> <dt>

<span data-ttu-id="35ba4-109">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="35ba4-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="35ba4-110">用於匯總的外部 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="35ba4-110">Pointer to the outer **IUnknown** interface for aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="35ba4-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="35ba4-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="35ba4-112">傳回之 **HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="35ba4-112">Pointer to a returned **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="35ba4-113">*pUnkExecutor*</span><span class="sxs-lookup"><span data-stu-id="35ba4-113">*pUnkExecutor*</span></span> 
</dt> <dd>

<span data-ttu-id="35ba4-114">將執行此命令之物件的指標。</span><span class="sxs-lookup"><span data-stu-id="35ba4-114">Pointer to the object that will carry out this command.</span></span>

</dd> <dt>

<span data-ttu-id="35ba4-115">*time*</span><span class="sxs-lookup"><span data-stu-id="35ba4-115">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="35ba4-116">執行命令的時間。</span><span class="sxs-lookup"><span data-stu-id="35ba4-116">Time at which the command will be run.</span></span>

</dd> <dt>

<span data-ttu-id="35ba4-117">*Iid*</span><span class="sxs-lookup"><span data-stu-id="35ba4-117">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="35ba4-118">包含方法之介面 (**GUID**) 的全域唯一識別碼指標。</span><span class="sxs-lookup"><span data-stu-id="35ba4-118">Pointer to the globally unique identifier (**GUID**) of the interface that contains the method.</span></span>

</dd> <dt>

<span data-ttu-id="35ba4-119">*dispidMethod*</span><span class="sxs-lookup"><span data-stu-id="35ba4-119">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="35ba4-120">要呼叫的介面上的方法。</span><span class="sxs-lookup"><span data-stu-id="35ba4-120">Method on the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="35ba4-121">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="35ba4-121">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="35ba4-122">調用的內容。</span><span class="sxs-lookup"><span data-stu-id="35ba4-122">Context of the invocation.</span></span>

</dd> <dt>

<span data-ttu-id="35ba4-123">*cArgs*</span><span class="sxs-lookup"><span data-stu-id="35ba4-123">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="35ba4-124">傳遞的引數數目。</span><span class="sxs-lookup"><span data-stu-id="35ba4-124">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="35ba4-125">*pDispParams*</span><span class="sxs-lookup"><span data-stu-id="35ba4-125">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="35ba4-126">引數變異類型清單的指標。</span><span class="sxs-lookup"><span data-stu-id="35ba4-126">Pointer to a list of argument variant types.</span></span>

</dd> <dt>

<span data-ttu-id="35ba4-127">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="35ba4-127">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="35ba4-128">傳回之 variant 型別清單的指標（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="35ba4-128">Pointer to a returned variant type list, if any.</span></span>

</dd> <dt>

<span data-ttu-id="35ba4-129">*>puargerr*</span><span class="sxs-lookup"><span data-stu-id="35ba4-129">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="35ba4-130">包含錯誤之 *pDispParams* 參數清單中最後一個引數的指標。</span><span class="sxs-lookup"><span data-stu-id="35ba4-130">Pointer to the last argument in the *pDispParams* parameter list with an error.</span></span>

</dd> <dt>

<span data-ttu-id="35ba4-131">*bStream*</span><span class="sxs-lookup"><span data-stu-id="35ba4-131">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="35ba4-132">指出延後命令時間是否為數據流時間 (**TRUE**) 或呈現時間 (**FALSE**) 的值。</span><span class="sxs-lookup"><span data-stu-id="35ba4-132">Value indicating whether the deferred command time is in stream time (**TRUE**) or presentation time (**FALSE**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35ba4-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="35ba4-133">Requirements</span></span>



| <span data-ttu-id="35ba4-134">需求</span><span class="sxs-lookup"><span data-stu-id="35ba4-134">Requirement</span></span> | <span data-ttu-id="35ba4-135">值</span><span class="sxs-lookup"><span data-stu-id="35ba4-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ba4-136">標頭</span><span class="sxs-lookup"><span data-stu-id="35ba4-136">Header</span></span><br/>  | <dl> <span data-ttu-id="35ba4-137"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="35ba4-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="35ba4-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="35ba4-138">Library</span></span><br/> | <dl> <span data-ttu-id="35ba4-139"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="35ba4-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ba4-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35ba4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ba4-141">**CDeferredCommand 類別**</span><span class="sxs-lookup"><span data-stu-id="35ba4-141">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




