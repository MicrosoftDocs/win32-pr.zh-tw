---
description: 執行方法提供者所匯出的方法。
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: " (>wbemdisp.tlb 的 SWbemServices.ExecMethodAsync 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898912efae276fc0404576e162468e06e1b95a68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986833"
---
# <a name="swbemservicesexecmethodasync-method"></a><span data-ttu-id="bf2ae-103">SWbemServices.ExecMethodAsync 方法</span><span class="sxs-lookup"><span data-stu-id="bf2ae-103">SWbemServices.ExecMethodAsync method</span></span>

<span data-ttu-id="bf2ae-104">[**SWbemServices**](swbemservices.md)物件的 **ExecMethodAsync** 方法會執行方法提供者所匯出的方法。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-104">The **ExecMethodAsync** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="bf2ae-105">呼叫會立即傳回至用戶端，而輸入參數會轉送至方法執行所在的適當提供者。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-105">The call immediately returns to the client while the inbound parameters are forwarded to the appropriate provider where the method executes.</span></span> <span data-ttu-id="bf2ae-106">資訊和狀態會透過傳遞給 *objWbemSink* 中指定之接收的事件傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-106">Information and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="bf2ae-107">提供者（而不是 Windows Management Instrumentation (WMI) ）會執行方法。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-107">The provider, rather than Windows Management Instrumentation (WMI), implements the method.</span></span>

<span data-ttu-id="bf2ae-108">在非同步模式中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="bf2ae-109">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="bf2ae-110">如需此語法的詳細資訊與說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-110">For more information and an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2ae-111">語法</span><span class="sxs-lookup"><span data-stu-id="bf2ae-111">Syntax</span></span>


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="bf2ae-112">參數</span><span class="sxs-lookup"><span data-stu-id="bf2ae-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf2ae-113">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="bf2ae-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="bf2ae-114">必要。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-114">Required.</span></span> <span data-ttu-id="bf2ae-115">建立 [**SWbemSink**](swbemsink.md) 物件以接收物件。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-115">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span> <span data-ttu-id="bf2ae-116">接收方法呼叫結果的物件接收。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-116">Object sink that receives the result of the method call.</span></span> <span data-ttu-id="bf2ae-117">輸出參數會傳送到所提供之物件接收的 [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-117">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="bf2ae-118">呼叫機制的結果會傳送到所提供之物件接收的 [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-118">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="bf2ae-119">請注意， **SWbemSink OnCompleted** 不會收到 WMI 方法的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-119">Be aware that **SWbemSink.OnCompleted** does not receive the return code of the WMI method.</span></span> <span data-ttu-id="bf2ae-120">但是，它會接收實際呼叫傳回機制的傳回碼，而且只適用于驗證呼叫是否發生，或是基於機械原因而失敗。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-120">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span> <span data-ttu-id="bf2ae-121">從 WMI 方法傳回的結果碼會在提供給 **SWbemSink** 的輸出參數物件中傳回。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-121">The result code that is returned from the WMI method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="bf2ae-122">如果傳回任何錯誤碼，則不會使用提供的 [**IWbemObjectSink**](iwbemobjectsink.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-122">If any error code is returned, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="bf2ae-123">如果呼叫成功，則會呼叫使用者的 **IWbemObjectSink** 執行以指出作業的結果。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-123">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bf2ae-124">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="bf2ae-124">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="bf2ae-125">必要。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-125">Required.</span></span> <span data-ttu-id="bf2ae-126">字串，包含執行方法之物件的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-126">A string that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="bf2ae-127">如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-127">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf2ae-128">*strMethodName*</span><span class="sxs-lookup"><span data-stu-id="bf2ae-128">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="bf2ae-129">必要。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-129">Required.</span></span> <span data-ttu-id="bf2ae-130">要執行的方法名稱。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-130">The name of the method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="bf2ae-131">*objWbemInParams* \[選\]</span><span class="sxs-lookup"><span data-stu-id="bf2ae-131">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2ae-132">[**SWbemObject**](swbemobject.md)物件，其中包含所執行之方法的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-132">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method that is executed.</span></span> <span data-ttu-id="bf2ae-133">根據預設，這個參數是未定義的。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-133">By default, this parameter is undefined.</span></span> <span data-ttu-id="bf2ae-134">如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-134">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf2ae-135">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="bf2ae-135">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2ae-136">判斷呼叫行為的整數。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-136">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="bf2ae-137">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-137">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="bf2ae-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="bf2ae-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="bf2ae-139">導致非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-139">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="bf2ae-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="bf2ae-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="bf2ae-141">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-141">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bf2ae-142">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="bf2ae-142">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2ae-143">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-143">Typically, this is undefined.</span></span> <span data-ttu-id="bf2ae-144">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-144">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="bf2ae-145">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="bf2ae-146">*objWbemAsyncCoNtext* \[選\]</span><span class="sxs-lookup"><span data-stu-id="bf2ae-146">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2ae-147">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，這個物件會返回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-147">A [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="bf2ae-148">如果您要使用相同的物件接收進行多個非同步呼叫，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="bf2ae-149">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-149">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="bf2ae-150">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-150">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="bf2ae-151">如需詳細資訊，請參閱 [使用 VBScript 進行非同步呼叫](making-an-asynchronous-call-with-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-151">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf2ae-152">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf2ae-152">Return value</span></span>

<span data-ttu-id="bf2ae-153">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-153">This method does not return a value.</span></span> <span data-ttu-id="bf2ae-154">如果呼叫成功，則會將 [**OutParameters**](swbemmethod-outparameters.md) 物件（也就是 [**SWbemObject**](swbemobject.md) ）提供給 *objWbemSink* 中指定的接收。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-154">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) is supplied to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="bf2ae-155">傳回的 **OutParameters** 物件包含所執行之方法的輸出參數和傳回值。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-155">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span> <span data-ttu-id="bf2ae-156">如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-156">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="bf2ae-157">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bf2ae-157">Error codes</span></span>

<span data-ttu-id="bf2ae-158">**ExecMethodAsync** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單所列的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-158">After the completion of the **ExecMethodAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes listed in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="bf2ae-159">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="bf2ae-159">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="bf2ae-160">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-160">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="bf2ae-161">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="bf2ae-161">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="bf2ae-162">指定的類別無效。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-162">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="bf2ae-163">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="bf2ae-163">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="bf2ae-164">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-164">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="bf2ae-165">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="bf2ae-165">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="bf2ae-166">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-166">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bf2ae-167">**wbemErrInvalidMethod** -2147749934 (0x8004102E) </span><span class="sxs-lookup"><span data-stu-id="bf2ae-167">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="bf2ae-168">要求的方法無法使用。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-168">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="bf2ae-169">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="bf2ae-169">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="bf2ae-170">目前的使用者未獲授權執行此方法。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-170">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf2ae-171">備註</span><span class="sxs-lookup"><span data-stu-id="bf2ae-171">Remarks</span></span>

<span data-ttu-id="bf2ae-172">如果執行的方法具有輸入參數，則 *objWbemInParam* 參數中的 [**InParameters**](swbemmethod-inparameters.md)物件必須與「[建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)」主題中的描述相同。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-172">If the method executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object in the *objWbemInParam* parameter must be the same as the description in the [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md) topics.</span></span>

<span data-ttu-id="bf2ae-173">當您無法直接執行方法時，請使用 **SWbemServices.ExecMethodAsync** 做為直接存取來執行 [*提供者方法*](gloss-p.md) 的替代方法。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-173">Use **SWbemServices.ExecMethodAsync** as an alternative to direct access for executing a [*provider method*](gloss-p.md) when it is not possible to execute a method directly.</span></span> <span data-ttu-id="bf2ae-174">例如，將它用於不支援輸出參數的指令碼語言，也就是您的方法有 OUT 參數。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-174">For example, use it with a scripting language that does not support output parameters, that is, if your method has OUT parameters.</span></span> <span data-ttu-id="bf2ae-175">否則，建議您使用直接存取來叫用方法。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-175">Otherwise, it is recommended that you use direct access to invoke a method.</span></span> <span data-ttu-id="bf2ae-176">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-176">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="bf2ae-177">**SWbemServices.Exe的 cMethodAsync** 方法需要物件路徑。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-177">The **SWbemServices.ExecMethodAsync** method requires an object path.</span></span> <span data-ttu-id="bf2ae-178">如果腳本已經包含 [**SWbemObject**](swbemobject.md) 物件，您可以呼叫 [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md)。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-178">If the script already contains an [**SWbemObject**](swbemobject.md) object, you can call [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>

<span data-ttu-id="bf2ae-179">此呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-179">This call returns immediately.</span></span> <span data-ttu-id="bf2ae-180">狀態資訊會透過傳回到呼叫的呼叫，傳回到呼叫端（在 *objWbemSink* 中指定的接收）。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-180">The status information is returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="bf2ae-181">若要在呼叫完成時繼續處理，請執行 *objWbemSink* 的副程式。[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-181">To continue processing when the call is completed, implement a subroutine for the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="bf2ae-182">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-182">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="bf2ae-183">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-183">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="bf2ae-184">如需如何消除風險的詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-184">For more information about how to eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="bf2ae-185">使用 *objWbemAsyncCoNtext* 參數來驗證呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-185">Use the *objWbemAsyncContext* parameter to verify the source of a call.</span></span>

## <a name="examples"></a><span data-ttu-id="bf2ae-186">範例</span><span class="sxs-lookup"><span data-stu-id="bf2ae-186">Examples</span></span>

<span data-ttu-id="bf2ae-187">下列程式碼範例顯示 **ExecMethodAsync** 方法。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-187">The following code example shows the **ExecMethodAsync** method.</span></span> <span data-ttu-id="bf2ae-188">腳本會建立 [**Win32 \_ 處理**](/windows/desktop/CIMWin32Prov/win32-process) 物件，該物件代表正在執行 [記事本] 的進程。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-188">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="bf2ae-189">它會顯示 [**InParameters**](swbemmethod-inparameters.md) 物件的設定，以及如何從 [**OutParameters**](swbemmethod-outparameters.md) 物件取得結果。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-189">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="bf2ae-190">如需顯示同步執行相同作業的腳本，請參閱 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-190">For a script that shows the same operations performed synchronously, see [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="bf2ae-191">如需使用直接存取的範例，請參閱 [在 Class Win32 \_ 進程中建立方法](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-191">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="bf2ae-192">如需使用 [**SWbemObject**](swbemobject.md)進行相同操作的範例，請參閱 [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md)。</span><span class="sxs-lookup"><span data-stu-id="bf2ae-192">For an example of the same operation using [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
        "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
        & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="bf2ae-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf2ae-193">Requirements</span></span>



| <span data-ttu-id="bf2ae-194">需求</span><span class="sxs-lookup"><span data-stu-id="bf2ae-194">Requirement</span></span> | <span data-ttu-id="bf2ae-195">值</span><span class="sxs-lookup"><span data-stu-id="bf2ae-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2ae-196">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf2ae-196">Minimum supported client</span></span><br/> | <span data-ttu-id="bf2ae-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf2ae-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf2ae-198">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf2ae-198">Minimum supported server</span></span><br/> | <span data-ttu-id="bf2ae-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf2ae-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf2ae-200">標頭</span><span class="sxs-lookup"><span data-stu-id="bf2ae-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf2ae-201"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf2ae-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf2ae-202">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bf2ae-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf2ae-203"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bf2ae-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bf2ae-204">DLL</span><span class="sxs-lookup"><span data-stu-id="bf2ae-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf2ae-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf2ae-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf2ae-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="bf2ae-206">CLSID</span></span><br/>                    | <span data-ttu-id="bf2ae-207">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="bf2ae-207">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="bf2ae-208">IID</span><span class="sxs-lookup"><span data-stu-id="bf2ae-208">IID</span></span><br/>                      | <span data-ttu-id="bf2ae-209">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="bf2ae-209">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="bf2ae-210">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf2ae-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2ae-211">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="bf2ae-211">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="bf2ae-212">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="bf2ae-212">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="bf2ae-213">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="bf2ae-213">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="bf2ae-214">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="bf2ae-214">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="bf2ae-215">呼叫提供者方法</span><span class="sxs-lookup"><span data-stu-id="bf2ae-215">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="bf2ae-216">操作類別和實例資訊</span><span class="sxs-lookup"><span data-stu-id="bf2ae-216">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

