---
description: 當非同步作業傳回物件時，會觸發 SWbemSink 物件的 OnObjectReady 事件。
ms.assetid: 14110ee7-a808-4786-b695-2ce54189d826
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents：： OnObjectReady 事件 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectReady
- ISWbemSinkEvents.OnObjectReady
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1fa803339e7007a030881c3d5b47d67f354b5661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114845"
---
# <a name="iswbemsinkeventsonobjectready-event"></a><span data-ttu-id="1a598-103">ISWbemSinkEvents：： OnObjectReady 事件</span><span class="sxs-lookup"><span data-stu-id="1a598-103">ISWbemSinkEvents::OnObjectReady event</span></span>

<span data-ttu-id="1a598-104">當非同步作業傳回物件時，會觸發 [**SWbemSink**](swbemsink.md)物件的 **OnObjectReady** 事件。</span><span class="sxs-lookup"><span data-stu-id="1a598-104">The **OnObjectReady** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous operation returns an object.</span></span> <span data-ttu-id="1a598-105">您可以使用此事件來處理非同步呼叫的物件，例如 [**SWbemObject \_ . InstancesAsync**](swbemobject-instancesasync-.md)或 [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)。</span><span class="sxs-lookup"><span data-stu-id="1a598-105">Use this event to process objects from asynchronous calls such as [**SWbemObject.InstancesAsync\_**](swbemobject-instancesasync-.md) or [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md).</span></span> <span data-ttu-id="1a598-106">**OnObjectReady** 會每次都傳回一個 [**SWbemObject**](swbemobject.md) ，直到列舉完成為止。</span><span class="sxs-lookup"><span data-stu-id="1a598-106">**OnObjectReady** returns one [**SWbemObject**](swbemobject.md) each time until the enumeration is complete.</span></span>

<span data-ttu-id="1a598-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="1a598-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1a598-108">語法</span><span class="sxs-lookup"><span data-stu-id="1a598-108">Syntax</span></span>


```VB
SWbemSink.OnObjectReady( _
  ByVal objWbemObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="1a598-109">參數</span><span class="sxs-lookup"><span data-stu-id="1a598-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a598-110">*objWbemObject*</span><span class="sxs-lookup"><span data-stu-id="1a598-110">*objWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="1a598-111">[**SWbemObject**](swbemobject.md)物件。</span><span class="sxs-lookup"><span data-stu-id="1a598-111">An [**SWbemObject**](swbemobject.md) object.</span></span> <span data-ttu-id="1a598-112">這與觸發這個事件之非同步呼叫的同步對等專案所傳回的內容類別似。</span><span class="sxs-lookup"><span data-stu-id="1a598-112">This is similar to what is returned by the synchronous equivalent of the asynchronous call that triggers this event.</span></span> <span data-ttu-id="1a598-113">例如，對 [**SWbemServices. GetAsync**](swbemservices-getasync.md)方法的呼叫會在 [**OnObjectReady**](swbemsink.md)物件之 **SWbemSink** 事件 *的 objWbemObject* 參數中傳回 **SWbemObject** ，該物件會以原始呼叫的 *objWbemObject* 參數形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="1a598-113">For example, a call to the [**SWbemServices.GetAsync**](swbemservices-getasync.md) method returns an **SWbemObject** in the *objWbemObject* parameter of the **OnObjectReady** event of the [**SWbemSink**](swbemsink.md) object, which is passed as the *objWbemObject* parameter of the original call.</span></span> <span data-ttu-id="1a598-114">您可以使用對 [**SWbemServices**](swbemservices-get.md)的對等同步呼叫來取得相同的 **SWbemObject** 物件。</span><span class="sxs-lookup"><span data-stu-id="1a598-114">The same **SWbemObject** object can be obtained by using an equivalent synchronous call to [**SWbemServices.Get**](swbemservices-get.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a598-115">*objWbemAsyncCoNtext*</span><span class="sxs-lookup"><span data-stu-id="1a598-115">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="1a598-116">傳遞至原始非同步呼叫的 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="1a598-116">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="1a598-117">使用這個參數來識別非同步呼叫的來源，此呼叫會在使用這個物件接收進行多個非同步呼叫時觸發這個事件。</span><span class="sxs-lookup"><span data-stu-id="1a598-117">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a598-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a598-118">Return value</span></span>

<span data-ttu-id="1a598-119">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1a598-119">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1a598-120">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1a598-120">Error codes</span></span>

<span data-ttu-id="1a598-121">**OnObjectReady** 事件完成之後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1a598-121">After the completion of the **OnObjectReady** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="1a598-122">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="1a598-122">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="1a598-123">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1a598-123">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="1a598-124">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="1a598-124">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="1a598-125">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="1a598-125">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1a598-126">**wbemErrTransportFailure** -2147749909 (0x80041015) </span><span class="sxs-lookup"><span data-stu-id="1a598-126">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="1a598-127">發生網路錯誤，導致無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="1a598-127">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a598-128">備註</span><span class="sxs-lookup"><span data-stu-id="1a598-128">Remarks</span></span>

<span data-ttu-id="1a598-129">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="1a598-129">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="1a598-130">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="1a598-130">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="1a598-131">若要消除風險，請使用半同步通訊或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="1a598-131">To eliminate the risks, use either semi-synchronous communication or synchronous communication.</span></span> <span data-ttu-id="1a598-132">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="1a598-132">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a598-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a598-133">Requirements</span></span>



| <span data-ttu-id="1a598-134">需求</span><span class="sxs-lookup"><span data-stu-id="1a598-134">Requirement</span></span> | <span data-ttu-id="1a598-135">值</span><span class="sxs-lookup"><span data-stu-id="1a598-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a598-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a598-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1a598-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a598-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1a598-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a598-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1a598-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a598-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1a598-140">標頭</span><span class="sxs-lookup"><span data-stu-id="1a598-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a598-141"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="1a598-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a598-142">Idl</span><span class="sxs-lookup"><span data-stu-id="1a598-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1a598-143"><dt>>wbemdisp.tlb .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1a598-143"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="1a598-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1a598-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a598-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a598-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1a598-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="1a598-146">CLSID</span></span><br/>                    | <span data-ttu-id="1a598-147">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="1a598-147">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="1a598-148">IID</span><span class="sxs-lookup"><span data-stu-id="1a598-148">IID</span></span><br/>                      | <span data-ttu-id="1a598-149">IID \_ ISWbemSinkEvents</span><span class="sxs-lookup"><span data-stu-id="1a598-149">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="1a598-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a598-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a598-151">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="1a598-151">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

