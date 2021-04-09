---
description: SWbemObject 的 InstancesAsync \_ 方法會以非同步方式提供目前類別物件的實例。 這個方法會執行簡單的查詢。 更複雜的查詢可能需要使用 SWbemServices.ExecQuery。
ms.assetid: d10fcbbf-6110-4152-8201-db43dc7a3c14
ms.tgt_platform: multiple
title: 'SWbemObject.InstancesAsync_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.InstancesAsync_
- ISWbemObject.InstancesAsync_
- ISWbemObject.InstancesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 800e28184593e339f739fb52d488803666f552c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848622"
---
# <a name="swbemobjectinstancesasync_-method"></a><span data-ttu-id="0d4b9-105">SWbemObject. InstancesAsync \_ 方法</span><span class="sxs-lookup"><span data-stu-id="0d4b9-105">SWbemObject.InstancesAsync\_ method</span></span>

<span data-ttu-id="0d4b9-106">[**SWbemObject**](swbemobject.md)的 **InstancesAsync \_** 方法會以非同步方式提供目前類別物件的實例。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-106">The **InstancesAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously supplies the instances of the current class object.</span></span> <span data-ttu-id="0d4b9-107">這個方法會執行簡單的查詢。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-107">This method implements a simple query.</span></span> <span data-ttu-id="0d4b9-108">更複雜的查詢可能需要使用 [**SWbemServices.ExecQuery**](swbemservices-execquery.md)。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-108">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="0d4b9-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d4b9-110">語法</span><span class="sxs-lookup"><span data-stu-id="0d4b9-110">Syntax</span></span>


```VB
SWbemObject.InstancesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0d4b9-111">參數</span><span class="sxs-lookup"><span data-stu-id="0d4b9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d4b9-112">*objWbemSink* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d4b9-112">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4b9-113">傳回實例的物件接收。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-113">Object sink that returns the instances.</span></span>

</dd> <dt>

<span data-ttu-id="0d4b9-114">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="0d4b9-114">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4b9-115">判斷呼叫行為的整數。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-115">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="0d4b9-116">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-116">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="0d4b9-117"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="0d4b9-117"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="0d4b9-118">導致非同步呼叫將狀態更新傳送至物件接收的 [**SWbemSink. OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-118">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="0d4b9-119"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="0d4b9-119"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0d4b9-120">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-120">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="0d4b9-121"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="0d4b9-121"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="0d4b9-122">導致 WMI 傳回當地語系化的類別和屬性描述。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-122">Causes WMI to return the localized class and property descriptions.</span></span> <span data-ttu-id="0d4b9-123">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-123">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0d4b9-124">*objwbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="0d4b9-124">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4b9-125">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-125">Typically, this is undefined.</span></span> <span data-ttu-id="0d4b9-126">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-126">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="0d4b9-127">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-127">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="0d4b9-128">*objWbemAsyncCoNtext* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="0d4b9-128">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4b9-129">這是一個 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，它會返回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-129">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="0d4b9-130">如果您要使用相同的物件接收進行多個非同步呼叫，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-130">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="0d4b9-131">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-131">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="0d4b9-132">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-132">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="0d4b9-133">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-133">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d4b9-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d4b9-134">Return value</span></span>

<span data-ttu-id="0d4b9-135">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-135">This method does not return a value.</span></span> <span data-ttu-id="0d4b9-136">如果成功，接收就會收到每個實例的 [**OnObjectReady**](swbemsink-onobjectready.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-136">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="0d4b9-137">在最後一個實例之後，物件接收會收到 [**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-137">After the last instance, the object sink will receive an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0d4b9-138">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0d4b9-138">Error codes</span></span>

<span data-ttu-id="0d4b9-139">**InstancesAsync \_** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-139">After the completion of the **InstancesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="0d4b9-140">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="0d4b9-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="0d4b9-141">目前的使用者沒有許可權可查看指定之類別的實例。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-141">Current user does not have permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="0d4b9-142">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="0d4b9-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="0d4b9-143">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-143">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0d4b9-144">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="0d4b9-144">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="0d4b9-145">指定的類別無效。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-145">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0d4b9-146">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="0d4b9-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="0d4b9-147">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0d4b9-148">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="0d4b9-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="0d4b9-149">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d4b9-150">備註</span><span class="sxs-lookup"><span data-stu-id="0d4b9-150">Remarks</span></span>

<span data-ttu-id="0d4b9-151">此呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-151">This call returns immediately.</span></span> <span data-ttu-id="0d4b9-152">要求的物件和狀態會透過回呼傳遞給 *objWbemSink* 中指定的接收，傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-152">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="0d4b9-153">若要在每個物件抵達時進行處理，請建立 *objWbemSink*。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-153">To process each object when it arrives, create an *objWbemSink*.</span></span> <span data-ttu-id="0d4b9-154">[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-154">[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="0d4b9-155">傳回所有物件之後，您就可以在 *objWbemSink* 的執行中執行最終處理。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-155">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.</span></span> <span data-ttu-id="0d4b9-156">[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-156">[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="0d4b9-157">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-157">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="0d4b9-158">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-158">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="0d4b9-159">若要消除風險，請使用兩個同步通訊或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-159">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="0d4b9-160">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-160">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="0d4b9-161">**InstancesAsync \_** 方法只適用于類別物件。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-161">The **InstancesAsync\_** method only works for class objects.</span></span> <span data-ttu-id="0d4b9-162">傳回的集合不會有零 (0) 元素，這並不是錯誤。</span><span class="sxs-lookup"><span data-stu-id="0d4b9-162">It is not an error for the returned collection to have zero (0) elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d4b9-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d4b9-163">Requirements</span></span>



| <span data-ttu-id="0d4b9-164">需求</span><span class="sxs-lookup"><span data-stu-id="0d4b9-164">Requirement</span></span> | <span data-ttu-id="0d4b9-165">值</span><span class="sxs-lookup"><span data-stu-id="0d4b9-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4b9-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d4b9-166">Minimum supported client</span></span><br/> | <span data-ttu-id="0d4b9-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d4b9-167">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d4b9-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d4b9-168">Minimum supported server</span></span><br/> | <span data-ttu-id="0d4b9-169">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d4b9-169">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d4b9-170">標頭</span><span class="sxs-lookup"><span data-stu-id="0d4b9-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d4b9-171"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d4b9-171"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d4b9-172">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0d4b9-172">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d4b9-173"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0d4b9-173"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0d4b9-174">DLL</span><span class="sxs-lookup"><span data-stu-id="0d4b9-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d4b9-175"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d4b9-175"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d4b9-176">CLSID</span><span class="sxs-lookup"><span data-stu-id="0d4b9-176">CLSID</span></span><br/>                    | <span data-ttu-id="0d4b9-177">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="0d4b9-177">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="0d4b9-178">IID</span><span class="sxs-lookup"><span data-stu-id="0d4b9-178">IID</span></span><br/>                      | <span data-ttu-id="0d4b9-179">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="0d4b9-179">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="0d4b9-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d4b9-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d4b9-181">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="0d4b9-181">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="0d4b9-182">**Swbemobjectset 搭配使用**</span><span class="sxs-lookup"><span data-stu-id="0d4b9-182">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

