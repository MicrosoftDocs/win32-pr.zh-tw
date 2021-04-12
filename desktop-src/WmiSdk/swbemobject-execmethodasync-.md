---
description: SWbemObject 的 ExecMethodAsync \_ 方法會以非同步方式執行方法提供者所匯出的方法。
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: 'SWbemObject.ExecMethodAsync_ 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8af1b7c10eed427423afea8b40a1df5bc237f99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194913"
---
# <a name="swbemobjectexecmethodasync_-method"></a><span data-ttu-id="09dc0-103">SWbemObject.ExecMethodAsync \_ 方法</span><span class="sxs-lookup"><span data-stu-id="09dc0-103">SWbemObject.ExecMethodAsync\_ method</span></span>

<span data-ttu-id="09dc0-104">[**SWbemObject**](swbemobject.md)的 **ExecMethodAsync \_** 方法會以非同步方式執行方法提供者所匯出的方法。</span><span class="sxs-lookup"><span data-stu-id="09dc0-104">The **ExecMethodAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously executes a method that a method provider exports.</span></span> <span data-ttu-id="09dc0-105">這個方法類似于 [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)，但會直接在要執行之方法的物件上運作。</span><span class="sxs-lookup"><span data-stu-id="09dc0-105">This method is similar to [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), but operates directly on the object of the method to be executed.</span></span> <span data-ttu-id="09dc0-106">Windows Management Instrumentation (WMI) 不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="09dc0-106">Windows Management Instrumentation (WMI) does not implement this method.</span></span> <span data-ttu-id="09dc0-107">提供者會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="09dc0-107">The provider implements this method.</span></span>

<span data-ttu-id="09dc0-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="09dc0-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="09dc0-109">語法</span><span class="sxs-lookup"><span data-stu-id="09dc0-109">Syntax</span></span>


```VB
objOutParams = .ExecMethodAsync_( _
  ByVal objWbemSink, _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="09dc0-110">參數</span><span class="sxs-lookup"><span data-stu-id="09dc0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09dc0-111">*objWbemSink* \[在\]</span><span class="sxs-lookup"><span data-stu-id="09dc0-111">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09dc0-112">必要。</span><span class="sxs-lookup"><span data-stu-id="09dc0-112">Required.</span></span> <span data-ttu-id="09dc0-113">這是接收方法呼叫結果的物件接收。</span><span class="sxs-lookup"><span data-stu-id="09dc0-113">This is the object sink that receives the results of the method call.</span></span> <span data-ttu-id="09dc0-114">輸出參數會傳送到所提供之物件接收的 [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="09dc0-114">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="09dc0-115">呼叫機制的結果會傳送到所提供之物件接收的 [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="09dc0-115">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="09dc0-116">請注意， **SWbemSink OnCompleted** 不會收到方法的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="09dc0-116">Notice that **SWbemSink.OnCompleted** does not receive the return code of the method.</span></span> <span data-ttu-id="09dc0-117">但是，它會接收實際呼叫傳回機制的傳回碼，而且只適用于驗證發生的呼叫，或是基於機械原因而失敗。</span><span class="sxs-lookup"><span data-stu-id="09dc0-117">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred, or that it failed for mechanical reasons.</span></span> <span data-ttu-id="09dc0-118">從方法傳回的結果碼會在提供給 **SWbemSink** 的輸出參數物件中傳回。</span><span class="sxs-lookup"><span data-stu-id="09dc0-118">The result code returned from the method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="09dc0-119">如果有任何錯誤碼傳回，則不會使用提供的 [**IWbemObjectSink**](iwbemobjectsink.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="09dc0-119">If any error code returns, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="09dc0-120">如果呼叫成功，則會呼叫使用者的 **IWbemObjectSink** 執行以指出作業的結果。</span><span class="sxs-lookup"><span data-stu-id="09dc0-120">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="09dc0-121">*strMethodName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="09dc0-121">*strMethodName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09dc0-122">必要。</span><span class="sxs-lookup"><span data-stu-id="09dc0-122">Required.</span></span> <span data-ttu-id="09dc0-123">這是物件的方法名稱。</span><span class="sxs-lookup"><span data-stu-id="09dc0-123">This is the name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="09dc0-124">*objwbemInParams* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="09dc0-124">*objwbemInParams* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="09dc0-125">這是 [**SWbemObject**](swbemobject.md) 物件，其中包含所執行之方法的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="09dc0-125">This is an [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="09dc0-126">根據預設，這個參數是未定義的。</span><span class="sxs-lookup"><span data-stu-id="09dc0-126">By default, this parameter is undefined.</span></span> <span data-ttu-id="09dc0-127">如需詳細資訊，請參閱 [建立 InParameters 物件](constructing-inparameters-objects.md) 和 [剖析 OutParameters 物件](parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="09dc0-127">For more information, see [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="09dc0-128">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="09dc0-128">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="09dc0-129">判斷呼叫行為的整數。</span><span class="sxs-lookup"><span data-stu-id="09dc0-129">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="09dc0-130">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="09dc0-130">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="09dc0-131"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="09dc0-131"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="09dc0-132">導致非同步呼叫將狀態更新傳送至物件接收的 [**SWbemSink. OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="09dc0-132">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="09dc0-133"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="09dc0-133"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="09dc0-134">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="09dc0-134">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="09dc0-135">*objwbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="09dc0-135">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="09dc0-136">一般而言，它是未定義的。</span><span class="sxs-lookup"><span data-stu-id="09dc0-136">Typically, it is undefined.</span></span> <span data-ttu-id="09dc0-137">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="09dc0-137">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="09dc0-138">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="09dc0-138">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="09dc0-139">*objWbemAsyncCoNtext* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="09dc0-139">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="09dc0-140">這是一個 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，它會返回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="09dc0-140">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="09dc0-141">如果您要使用相同的物件接收進行多個非同步呼叫，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="09dc0-141">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="09dc0-142">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="09dc0-142">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="09dc0-143">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="09dc0-143">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="09dc0-144">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="09dc0-144">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09dc0-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="09dc0-145">Return value</span></span>

<span data-ttu-id="09dc0-146">這個方法沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="09dc0-146">This method has no return values.</span></span> <span data-ttu-id="09dc0-147">如果呼叫成功，則會將 [**OutParameters**](swbemmethod-outparameters.md) 物件（也是 [**SWbemObject**](swbemobject.md) 物件）提供給 *objWbemSink* 中指定的接收。</span><span class="sxs-lookup"><span data-stu-id="09dc0-147">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) object, is supplied to the sink specified in *objWbemSink*.</span></span> <span data-ttu-id="09dc0-148">傳回的 **OutParameters** 物件包含所執行之方法的輸出參數和傳回值。</span><span class="sxs-lookup"><span data-stu-id="09dc0-148">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="09dc0-149">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="09dc0-149">Error codes</span></span>

<span data-ttu-id="09dc0-150">完成 **ExecMethodAsync \_** 方法之後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="09dc0-150">After completion of the **ExecMethodAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="09dc0-151">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="09dc0-151">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="09dc0-152">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="09dc0-152">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="09dc0-153">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="09dc0-153">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="09dc0-154">指定的類別無效。</span><span class="sxs-lookup"><span data-stu-id="09dc0-154">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="09dc0-155">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="09dc0-155">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="09dc0-156">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="09dc0-156">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="09dc0-157">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="09dc0-157">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="09dc0-158">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="09dc0-158">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="09dc0-159">**wbemErrInvalidMethod** -2147749934 (0x8004102E) </span><span class="sxs-lookup"><span data-stu-id="09dc0-159">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="09dc0-160">要求的方法無法使用。</span><span class="sxs-lookup"><span data-stu-id="09dc0-160">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="09dc0-161">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="09dc0-161">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="09dc0-162">目前的使用者未獲授權執行此方法。</span><span class="sxs-lookup"><span data-stu-id="09dc0-162">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09dc0-163">備註</span><span class="sxs-lookup"><span data-stu-id="09dc0-163">Remarks</span></span>

<span data-ttu-id="09dc0-164">當您無法直接執行方法時，請使用 **SWbemObject.ExecMethodAsync \_** 方法做為直接存取執行 [*提供者方法*](gloss-p.md)的替代方法。</span><span class="sxs-lookup"><span data-stu-id="09dc0-164">Use the **SWbemObject.ExecMethodAsync\_** method as an alternative to direct access for executing a [*provider method*](gloss-p.md) when you cannot execute a method directly.</span></span> <span data-ttu-id="09dc0-165">例如，如果您的方法有 out 參數，請使用 **SWbemObject.ExecMethodAsync \_** 方法搭配不支援輸出參數的指令碼語言。</span><span class="sxs-lookup"><span data-stu-id="09dc0-165">For example, if your method has out parameters, use the **SWbemObject.ExecMethodAsync\_** method with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="09dc0-166">否則，建議您使用直接存取來叫用方法。</span><span class="sxs-lookup"><span data-stu-id="09dc0-166">Otherwise, it is recommended that you invoke a method using direct access.</span></span> <span data-ttu-id="09dc0-167">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="09dc0-167">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="09dc0-168">此呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="09dc0-168">This call returns immediately.</span></span> <span data-ttu-id="09dc0-169">要求的物件和狀態會透過回呼傳遞給 *objWbemSink* 中指定的接收，傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="09dc0-169">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="09dc0-170">若要在每個物件抵達時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。</span><span class="sxs-lookup"><span data-stu-id="09dc0-170">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="09dc0-171">傳回所有物件之後，您就可以在 *objWbemSink* 的執行中執行最終處理。[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="09dc0-171">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="09dc0-172">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="09dc0-172">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="09dc0-173">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="09dc0-173">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="09dc0-174">若要消除風險，請使用兩個同步通訊或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="09dc0-174">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="09dc0-175">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="09dc0-175">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="09dc0-176">如果正在執行的方法具有輸入參數，則 [**InParameters**](swbemmethod-inparameters.md) 物件和 *objWbemInParam* 參數必須依照 [建立 InParameters 物件](constructing-inparameters-objects.md) 和 [剖析 OutParameters 物件](parsing-outparameters-objects.md)中所述的方式來進行結構化。</span><span class="sxs-lookup"><span data-stu-id="09dc0-176">If the method being executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object and *objWbemInParam* parameter must be constructed as described in [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="09dc0-177">**SWbemObject.ExecMethodAsync \_** 方法會假設 [**SWbemObject**](swbemobject.md)所代表的物件包含要執行的方法。</span><span class="sxs-lookup"><span data-stu-id="09dc0-177">The **SWbemObject.ExecMethodAsync\_** method assumes the object represented by [**SWbemObject**](swbemobject.md) contains the method to execute.</span></span> <span data-ttu-id="09dc0-178">[**SWbemServices.Exe的 cMethodAsync**](swbemservices-execmethodasync.md)方法需要物件路徑。</span><span class="sxs-lookup"><span data-stu-id="09dc0-178">The [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) method requires an object path.</span></span>

## <a name="examples"></a><span data-ttu-id="09dc0-179">範例</span><span class="sxs-lookup"><span data-stu-id="09dc0-179">Examples</span></span>

<span data-ttu-id="09dc0-180">下列範例顯示 [**ExecMethodAsync**](swbemservices-execmethodasync.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="09dc0-180">The following example shows the [**ExecMethodAsync**](swbemservices-execmethodasync.md) method.</span></span> <span data-ttu-id="09dc0-181">腳本會建立 [**Win32 \_ 處理**](/windows/desktop/CIMWin32Prov/win32-process) 物件，該物件代表正在執行 [記事本] 的進程。</span><span class="sxs-lookup"><span data-stu-id="09dc0-181">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="09dc0-182">它會顯示 [**InParameters**](swbemmethod-inparameters.md) 物件的設定，以及如何從 [**OutParameters**](swbemmethod-outparameters.md) 物件取得結果。</span><span class="sxs-lookup"><span data-stu-id="09dc0-182">It shows setting up of [**InParameters**](swbemmethod-inparameters.md) object, and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span>

<span data-ttu-id="09dc0-183">如需顯示同步執行相同作業的腳本，請參閱 [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md)。</span><span class="sxs-lookup"><span data-stu-id="09dc0-183">For a script that shows the same operations performed synchronously, see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span> <span data-ttu-id="09dc0-184">如需使用直接存取的範例，請參閱 [**在 Class Win32 \_ 進程中建立方法**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)。</span><span class="sxs-lookup"><span data-stu-id="09dc0-184">For an example using direct access, see [**Create Method in Class Win32\_Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="09dc0-185">如需使用 [**SWbemServices**](swbemservices.md) 物件進行相同操作的範例，請參閱 [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)。</span><span class="sxs-lookup"><span data-stu-id="09dc0-185">For an example of the same operation using an [**SWbemServices**](swbemservices.md) object, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span>


```VB
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
    "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
    & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="09dc0-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="09dc0-186">Requirements</span></span>



| <span data-ttu-id="09dc0-187">需求</span><span class="sxs-lookup"><span data-stu-id="09dc0-187">Requirement</span></span> | <span data-ttu-id="09dc0-188">值</span><span class="sxs-lookup"><span data-stu-id="09dc0-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09dc0-189">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09dc0-189">Minimum supported client</span></span><br/> | <span data-ttu-id="09dc0-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09dc0-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="09dc0-191">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09dc0-191">Minimum supported server</span></span><br/> | <span data-ttu-id="09dc0-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09dc0-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="09dc0-193">標頭</span><span class="sxs-lookup"><span data-stu-id="09dc0-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="09dc0-194"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="09dc0-194"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="09dc0-195">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="09dc0-195">Type library</span></span><br/>             | <dl> <span data-ttu-id="09dc0-196"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="09dc0-196"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="09dc0-197">DLL</span><span class="sxs-lookup"><span data-stu-id="09dc0-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09dc0-198"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09dc0-198"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="09dc0-199">CLSID</span><span class="sxs-lookup"><span data-stu-id="09dc0-199">CLSID</span></span><br/>                    | <span data-ttu-id="09dc0-200">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="09dc0-200">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="09dc0-201">IID</span><span class="sxs-lookup"><span data-stu-id="09dc0-201">IID</span></span><br/>                      | <span data-ttu-id="09dc0-202">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="09dc0-202">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="09dc0-203">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09dc0-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09dc0-204">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="09dc0-204">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="09dc0-205">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="09dc0-205">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

