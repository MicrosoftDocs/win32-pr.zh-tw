---
description: 新方法會初始化要執行的命令，並傳回新的 CDeferredCommand 物件。
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: 'CCmdQueue： New 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.New
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 58c3aee63005010b9ed7366cfb63a69fcc7348b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992782"
---
# <a name="ccmdqueuenew-method"></a><span data-ttu-id="3d010-103">CCmdQueue 新方法</span><span class="sxs-lookup"><span data-stu-id="3d010-103">CCmdQueue.New method</span></span>

<span data-ttu-id="3d010-104">`New`方法會初始化要執行的命令，並傳回新的 [**CDeferredCommand**](cdeferredcommand.md)物件。</span><span class="sxs-lookup"><span data-stu-id="3d010-104">The `New` method initializes a command to be run and returns a new [**CDeferredCommand**](cdeferredcommand.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d010-105">語法</span><span class="sxs-lookup"><span data-stu-id="3d010-105">Syntax</span></span>


```C++
virtual HRESULT New(
   CDeferredCommand **ppCmd,
   LPUNKNOWN        pUnk,
   REFTIME          time,
   GUID             *iid,
   long             dispidMethod,
   short            wFlags,
   long             cArgs,
   VARIANT          *pDispParams,
   VARIANT          *pvarResult,
   short            *puArgErr,
   BOOL             bStream
);
```



## <a name="parameters"></a><span data-ttu-id="3d010-106">參數</span><span class="sxs-lookup"><span data-stu-id="3d010-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d010-107">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="3d010-107">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="3d010-108">[**CDeferredCommand**](cdeferredcommand.md)物件的指標位址，應用程式可以透過此物件取消命令、為其設定新的呈現時間，或取得估計資訊。</span><span class="sxs-lookup"><span data-stu-id="3d010-108">Address of a pointer to a [**CDeferredCommand**](cdeferredcommand.md) object by which an application can cancel the command, set a new presentation time for it, or retrieve estimate information.</span></span>

</dd> <dt>

<span data-ttu-id="3d010-109">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="3d010-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="3d010-110">將執行命令之物件的指標。</span><span class="sxs-lookup"><span data-stu-id="3d010-110">Pointer to the object that will run the command.</span></span>

</dd> <dt>

<span data-ttu-id="3d010-111">*time*</span><span class="sxs-lookup"><span data-stu-id="3d010-111">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="3d010-112">執行佇列命令或命令的時間。</span><span class="sxs-lookup"><span data-stu-id="3d010-112">Time at which to run the queued command or commands.</span></span>

</dd> <dt>

<span data-ttu-id="3d010-113">*Iid*</span><span class="sxs-lookup"><span data-stu-id="3d010-113">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="3d010-114">要呼叫之介面 (**GUID**) 的全域唯一識別碼指標。</span><span class="sxs-lookup"><span data-stu-id="3d010-114">Pointer to the globally unique identifier (**GUID**) of the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="3d010-115">*dispidMethod*</span><span class="sxs-lookup"><span data-stu-id="3d010-115">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="3d010-116">要呼叫的介面上的方法。</span><span class="sxs-lookup"><span data-stu-id="3d010-116">Method on the interface to be called.</span></span>

</dd> <dt>

<span data-ttu-id="3d010-117">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="3d010-117">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="3d010-118">描述呼叫之內容的旗標。</span><span class="sxs-lookup"><span data-stu-id="3d010-118">Flags describing the context of the call.</span></span> <span data-ttu-id="3d010-119">此參數支援與 **IDispatch：： Invoke** 方法相同的旗標。</span><span class="sxs-lookup"><span data-stu-id="3d010-119">This parameter supports the same flags as the **IDispatch::Invoke** method.</span></span>

</dd> <dt>

<span data-ttu-id="3d010-120">*cArgs*</span><span class="sxs-lookup"><span data-stu-id="3d010-120">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="3d010-121">傳遞的引數數目。</span><span class="sxs-lookup"><span data-stu-id="3d010-121">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="3d010-122">*pDispParams*</span><span class="sxs-lookup"><span data-stu-id="3d010-122">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="3d010-123">與分派參數相關聯之 variant 類型清單的指標。</span><span class="sxs-lookup"><span data-stu-id="3d010-123">Pointer to the list of variant types associated with the dispatch parameters.</span></span>

</dd> <dt>

<span data-ttu-id="3d010-124">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="3d010-124">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="3d010-125">要傳回結果的清單（如果有的話）的指標。</span><span class="sxs-lookup"><span data-stu-id="3d010-125">Pointer to the list where results, if any, are to be returned.</span></span>

</dd> <dt>

<span data-ttu-id="3d010-126">*>puargerr*</span><span class="sxs-lookup"><span data-stu-id="3d010-126">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="3d010-127">最後發生錯誤之 *pDispParams* 參數清單中索引的指標。</span><span class="sxs-lookup"><span data-stu-id="3d010-127">Pointer to the index within the *pDispParams* parameter list where the last error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3d010-128">*bStream*</span><span class="sxs-lookup"><span data-stu-id="3d010-128">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="3d010-129">值，指出 *time* 參數是否為數據流時間值 (**TRUE**) 或表示時間值 (**FALSE**) 。</span><span class="sxs-lookup"><span data-stu-id="3d010-129">Value indicating whether the *time* parameter is a stream-time value (**TRUE**) or a presentation-time value (**FALSE**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d010-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d010-130">Return value</span></span>

<span data-ttu-id="3d010-131">\_如果成功，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="3d010-131">Returns S\_OK if successful.</span></span> <span data-ttu-id="3d010-132">\_如果 *ppCmd* 從建立新的 [**CDeferredCommand**](cdeferredcommand.md)物件，其值為 **Null**，則傳回 E OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="3d010-132">Returns E\_OUTOFMEMORY if *ppCmd* returns from creating the new [**CDeferredCommand**](cdeferredcommand.md) object with a value of **NULL**.</span></span> <span data-ttu-id="3d010-133">否則，會傳回 **HRESULT** ，表示嘗試建立新的 **CDeferredCommand** 物件時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="3d010-133">Otherwise, returns an **HRESULT** that indicates an error from attempting to create a new **CDeferredCommand** object.</span></span> <span data-ttu-id="3d010-134">如果發生錯誤，則不會將任何物件排入佇列。</span><span class="sxs-lookup"><span data-stu-id="3d010-134">If there is an error, no object has been queued.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d010-135">備註</span><span class="sxs-lookup"><span data-stu-id="3d010-135">Remarks</span></span>

<span data-ttu-id="3d010-136">新的 [**CDeferredCommand**](cdeferredcommand.md) 物件將會以參數進行初始化，並在結構化期間新增至佇列。</span><span class="sxs-lookup"><span data-stu-id="3d010-136">The new [**CDeferredCommand**](cdeferredcommand.md) object will be initialized with the parameters and will be added to the queue during construction.</span></span> <span data-ttu-id="3d010-137">這個方法類似于 **IDispatch：： Invoke** 方法。</span><span class="sxs-lookup"><span data-stu-id="3d010-137">This method is similar to the **IDispatch::Invoke** method.</span></span>

<span data-ttu-id="3d010-138">*WFlags* 參數的值包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="3d010-138">Values for the *wFlags* parameter include the following:</span></span>



| <span data-ttu-id="3d010-139">值</span><span class="sxs-lookup"><span data-stu-id="3d010-139">Value</span></span>                    | <span data-ttu-id="3d010-140">描述</span><span class="sxs-lookup"><span data-stu-id="3d010-140">Description</span></span>                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d010-141">分派 \_ 方法</span><span class="sxs-lookup"><span data-stu-id="3d010-141">DISPATCH\_METHOD</span></span>         | <span data-ttu-id="3d010-142">成員正在以方法的形式執行。</span><span class="sxs-lookup"><span data-stu-id="3d010-142">The member is being run as a method.</span></span> <span data-ttu-id="3d010-143">如果屬性具有相同的名稱，則可以設定此和分派 \_ PROPERTYGET 旗標。</span><span class="sxs-lookup"><span data-stu-id="3d010-143">If a property has the same name, both this and the DISPATCH\_PROPERTYGET flag can be set.</span></span>                                       |
| <span data-ttu-id="3d010-144">分派 \_ PROPERTYGET</span><span class="sxs-lookup"><span data-stu-id="3d010-144">DISPATCH\_PROPERTYGET</span></span>    | <span data-ttu-id="3d010-145">正在將成員取出為屬性或資料成員。</span><span class="sxs-lookup"><span data-stu-id="3d010-145">The member is being retrieved as a property or data member.</span></span>                                                                                                          |
| <span data-ttu-id="3d010-146">分派 \_ PROPERTYPUT</span><span class="sxs-lookup"><span data-stu-id="3d010-146">DISPATCH\_PROPERTYPUT</span></span>    | <span data-ttu-id="3d010-147">成員正變更為屬性或資料成員。</span><span class="sxs-lookup"><span data-stu-id="3d010-147">The member is being changed as a property or data member.</span></span>                                                                                                            |
| <span data-ttu-id="3d010-148">分派 \_ PROPERTYPUTREF</span><span class="sxs-lookup"><span data-stu-id="3d010-148">DISPATCH\_PROPERTYPUTREF</span></span> | <span data-ttu-id="3d010-149">成員正在透過參考指派進行變更，而不是值指派。</span><span class="sxs-lookup"><span data-stu-id="3d010-149">The member is being changed via a reference assignment, rather than a value assignment.</span></span> <span data-ttu-id="3d010-150">只有當屬性接受物件的參考時，此值才有效。</span><span class="sxs-lookup"><span data-stu-id="3d010-150">This value is valid only when the property accepts a reference to an object.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="3d010-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d010-151">Requirements</span></span>



| <span data-ttu-id="3d010-152">需求</span><span class="sxs-lookup"><span data-stu-id="3d010-152">Requirement</span></span> | <span data-ttu-id="3d010-153">值</span><span class="sxs-lookup"><span data-stu-id="3d010-153">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d010-154">標頭</span><span class="sxs-lookup"><span data-stu-id="3d010-154">Header</span></span><br/>  | <dl> <span data-ttu-id="3d010-155"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3d010-155"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3d010-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="3d010-156">Library</span></span><br/> | <dl> <span data-ttu-id="3d010-157"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3d010-157"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d010-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d010-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d010-159">**CCmdQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="3d010-159">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




