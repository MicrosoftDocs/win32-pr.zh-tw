---
description: 非同步呼叫完成時，會觸發 SWbemSink 物件的 OnCompleted 事件。 此事件表示用戶端應用程式、非同步作業的結果，並提供非同步呼叫失敗時的錯誤資訊。
ms.assetid: 2723185d-5b8b-4cc7-ada3-51c3275272a9
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents：： OnCompleted 事件 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnCompleted
- ISWbemSinkEvents.OnCompleted
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 16cb0362b5c1b1d432d72bb959103adbb7315069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114849"
---
# <a name="iswbemsinkeventsoncompleted-event"></a><span data-ttu-id="3e5e9-104">ISWbemSinkEvents：： OnCompleted 事件</span><span class="sxs-lookup"><span data-stu-id="3e5e9-104">ISWbemSinkEvents::OnCompleted event</span></span>

<span data-ttu-id="3e5e9-105">非同步呼叫完成時，會觸發 [**SWbemSink**](swbemsink.md)物件的 **OnCompleted** 事件。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-105">The **OnCompleted** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous call is complete.</span></span> <span data-ttu-id="3e5e9-106">此事件表示用戶端應用程式、非同步作業的結果，並提供非同步呼叫失敗時的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-106">This event indicates to the client application, the result of an asynchronous operation, and provides error information when the asynchronous call fails.</span></span>

<span data-ttu-id="3e5e9-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e5e9-108">語法</span><span class="sxs-lookup"><span data-stu-id="3e5e9-108">Syntax</span></span>


```VB
SWbemSink.OnCompleted( _
  ByVal iHResult, _
  ByVal objWbemErrorObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="3e5e9-109">參數</span><span class="sxs-lookup"><span data-stu-id="3e5e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e5e9-110">*iHResult*</span><span class="sxs-lookup"><span data-stu-id="3e5e9-110">*iHResult*</span></span> 
</dt> <dd>

<span data-ttu-id="3e5e9-111">已完成之非同步方法的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-111">The HRESULT of the completed asynchronous method.</span></span> <span data-ttu-id="3e5e9-112">HRESULT 與針對 WMI 方法呼叫的對等 [COM API](com-api-for-wmi.md) 所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-112">The HRESULT is the same as the value that is returned from an equivalent [COM API for WMI](com-api-for-wmi.md) method call.</span></span> <span data-ttu-id="3e5e9-113">檢查此值以判斷非同步呼叫是否成功。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-113">Check this value to determine whether or not the asynchronous call is successful.</span></span> <span data-ttu-id="3e5e9-114">如果非同步呼叫成功，則此參數會包含 WBEM \_ S \_ ， \_ (0) 不會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-114">If the asynchronous call is successful, this parameter contains WBEM\_S\_NO\_ERROR (0).</span></span> <span data-ttu-id="3e5e9-115">如果非同步呼叫失敗，此參數會包含錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-115">If the asynchronous call fails, this parameter contains an error code.</span></span>

</dd> <dt>

<span data-ttu-id="3e5e9-116">*objWbemErrorObject*</span><span class="sxs-lookup"><span data-stu-id="3e5e9-116">*objWbemErrorObject*</span></span> 
</dt> <dd>

<span data-ttu-id="3e5e9-117">當非同步方法失敗時，包含 [**SWbemLastError**](swbemlasterror.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-117">Contains an [**SWbemLastError**](swbemlasterror.md) object when the asynchronous method fails.</span></span>

</dd> <dt>

<span data-ttu-id="3e5e9-118">*objWbemAsyncCoNtext*</span><span class="sxs-lookup"><span data-stu-id="3e5e9-118">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="3e5e9-119">這是傳遞至原始非同步呼叫的 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-119">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="3e5e9-120">使用這個參數來識別非同步呼叫的來源，此呼叫會在使用這個物件接收進行多個非同步呼叫時觸發這個事件。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-120">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e5e9-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e5e9-121">Return value</span></span>

<span data-ttu-id="3e5e9-122">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-122">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e5e9-123">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3e5e9-123">Error codes</span></span>

<span data-ttu-id="3e5e9-124">完成 **OnCompleted** 事件之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-124">After completion of the **OnCompleted** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="3e5e9-125">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="3e5e9-125">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="3e5e9-126">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-126">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="3e5e9-127">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="3e5e9-127">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="3e5e9-128">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-128">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3e5e9-129">**wbemErrTransportFailure** -2147749909 (0x80041015) </span><span class="sxs-lookup"><span data-stu-id="3e5e9-129">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="3e5e9-130">發生網路錯誤，導致無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-130">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e5e9-131">備註</span><span class="sxs-lookup"><span data-stu-id="3e5e9-131">Remarks</span></span>

<span data-ttu-id="3e5e9-132">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-132">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="3e5e9-133">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-133">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="3e5e9-134">若要消除風險，請使用最半同步或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-134">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="3e5e9-135">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="3e5e9-135">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e5e9-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e5e9-136">Requirements</span></span>



| <span data-ttu-id="3e5e9-137">需求</span><span class="sxs-lookup"><span data-stu-id="3e5e9-137">Requirement</span></span> | <span data-ttu-id="3e5e9-138">值</span><span class="sxs-lookup"><span data-stu-id="3e5e9-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5e9-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e5e9-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3e5e9-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e5e9-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e5e9-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e5e9-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3e5e9-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e5e9-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e5e9-143">標頭</span><span class="sxs-lookup"><span data-stu-id="3e5e9-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e5e9-144"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e5e9-144"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e5e9-145">Idl</span><span class="sxs-lookup"><span data-stu-id="3e5e9-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3e5e9-146"><dt>>wbemdisp.tlb .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3e5e9-146"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="3e5e9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="3e5e9-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e5e9-148"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e5e9-148"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3e5e9-149">CLSID</span><span class="sxs-lookup"><span data-stu-id="3e5e9-149">CLSID</span></span><br/>                    | <span data-ttu-id="3e5e9-150">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="3e5e9-150">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="3e5e9-151">IID</span><span class="sxs-lookup"><span data-stu-id="3e5e9-151">IID</span></span><br/>                      | <span data-ttu-id="3e5e9-152">IID \_ ISWbemSinkEvents</span><span class="sxs-lookup"><span data-stu-id="3e5e9-152">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



 

