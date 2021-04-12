---
description: SWbemObject 的 SubclassesAsync \_ 方法會以非同步方式提供目前物件的子類別，該物件必須是類別。
ms.assetid: 14d4a609-3aa4-49bd-bea4-6a71bc24d9dd
ms.tgt_platform: multiple
title: 'SWbemObject.SubclassesAsync_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6e922953e9f25aae2e47ea572678790b1228a581
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195043"
---
# <a name="swbemobjectsubclassesasync_-method"></a><span data-ttu-id="4ff89-103">SWbemObject. SubclassesAsync \_ 方法</span><span class="sxs-lookup"><span data-stu-id="4ff89-103">SWbemObject.SubclassesAsync\_ method</span></span>

<span data-ttu-id="4ff89-104">[**SWbemObject**](swbemobject.md)的 **SubclassesAsync \_** 方法會以非同步方式提供目前物件的子類別，該物件必須是類別。</span><span class="sxs-lookup"><span data-stu-id="4ff89-104">The **SubclassesAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously supplies the subclasses of the current object, which must be a class.</span></span>

<span data-ttu-id="4ff89-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="4ff89-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ff89-106">語法</span><span class="sxs-lookup"><span data-stu-id="4ff89-106">Syntax</span></span>


```VB
SWbemObject.SubclassesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4ff89-107">參數</span><span class="sxs-lookup"><span data-stu-id="4ff89-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ff89-108">*objWbemSink* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ff89-108">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ff89-109">必要。</span><span class="sxs-lookup"><span data-stu-id="4ff89-109">Required.</span></span> <span data-ttu-id="4ff89-110">以非同步方式接收物件的物件接收。</span><span class="sxs-lookup"><span data-stu-id="4ff89-110">Object sink that receives the objects asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="4ff89-111">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4ff89-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ff89-112">決定呼叫列舉的詳細程度。</span><span class="sxs-lookup"><span data-stu-id="4ff89-112">Determines how detailed the call enumerates.</span></span> <span data-ttu-id="4ff89-113">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="4ff89-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="4ff89-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="4ff89-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="4ff89-115">強制遞迴列舉至所有衍生自指定父類別的子類別。</span><span class="sxs-lookup"><span data-stu-id="4ff89-115">Forces recursive enumeration into all subclasses derived from the specified parent class.</span></span> <span data-ttu-id="4ff89-116">父類別本身不會在列舉中傳回。</span><span class="sxs-lookup"><span data-stu-id="4ff89-116">The parent class itself is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="4ff89-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="4ff89-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="4ff89-118">此參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="4ff89-118">Default for this parameter.</span></span> <span data-ttu-id="4ff89-119">它會強制列舉只包含指定之父類別的直屬子類別。</span><span class="sxs-lookup"><span data-stu-id="4ff89-119">It forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="4ff89-120"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="4ff89-120"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="4ff89-121">導致非同步呼叫將狀態更新傳送至物件接收的 [**SWbemSink. OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="4ff89-121">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="4ff89-122"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="4ff89-122"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="4ff89-123">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="4ff89-123">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="4ff89-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="4ff89-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="4ff89-125">讓 WMI 以基類定義傳回類別修訂資料。</span><span class="sxs-lookup"><span data-stu-id="4ff89-125">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="4ff89-126">如需修改過的限定詞的詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="4ff89-126">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4ff89-127">*objWbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4ff89-127">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ff89-128">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="4ff89-128">Typically, this is undefined.</span></span> <span data-ttu-id="4ff89-129">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="4ff89-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="4ff89-130">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="4ff89-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="4ff89-131">*objWbemAsyncCoNtext* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4ff89-131">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ff89-132">這是一個 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，它會返回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="4ff89-132">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="4ff89-133">當您使用相同的物件接收進行多個非同步呼叫時，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="4ff89-133">Use this parameter when you make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="4ff89-134">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="4ff89-134">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="4ff89-135">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而且可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法來解壓縮呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="4ff89-135">This **SWbemNamedValueSet** object is returned to the object sink, and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="4ff89-136">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="4ff89-136">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ff89-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ff89-137">Return value</span></span>

<span data-ttu-id="4ff89-138">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4ff89-138">This method does not return a value.</span></span> <span data-ttu-id="4ff89-139">如果成功，接收就會收到每個實例的 [**OnObjectReady**](swbemsink-onobjectready.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="4ff89-139">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event for each instance.</span></span> <span data-ttu-id="4ff89-140">在最後一個實例之後，物件接收會收到 [**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="4ff89-140">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4ff89-141">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="4ff89-141">Error codes</span></span>

<span data-ttu-id="4ff89-142">**SubclassesAsync \_** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4ff89-142">After the completion of the **SubclassesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="4ff89-143">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="4ff89-143">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="4ff89-144">目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="4ff89-144">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="4ff89-145">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="4ff89-145">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="4ff89-146">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4ff89-146">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="4ff89-147">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="4ff89-147">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="4ff89-148">指定的類別不存在。</span><span class="sxs-lookup"><span data-stu-id="4ff89-148">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="4ff89-149">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="4ff89-149">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="4ff89-150">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="4ff89-150">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="4ff89-151">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="4ff89-151">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="4ff89-152">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="4ff89-152">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ff89-153">備註</span><span class="sxs-lookup"><span data-stu-id="4ff89-153">Remarks</span></span>

<span data-ttu-id="4ff89-154">此呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="4ff89-154">This call returns immediately.</span></span> <span data-ttu-id="4ff89-155">要求的物件和狀態會透過回呼傳遞給 *objWbemSink* 中指定的接收，傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="4ff89-155">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="4ff89-156">若要在每個物件抵達時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。</span><span class="sxs-lookup"><span data-stu-id="4ff89-156">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="4ff89-157">傳回所有物件之後，您就可以在 *objWbemSink* 的執行中執行最終處理。[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="4ff89-157">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="4ff89-158">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="4ff89-158">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="4ff89-159">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="4ff89-159">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="4ff89-160">若要消除風險，請使用兩個同步通訊或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="4ff89-160">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="4ff89-161">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="4ff89-161">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="4ff89-162">建議腳本使用 *objWbemAsyncCoNtext* 參數來驗證呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="4ff89-162">It is recommended that scripts verify the source of the call by using an *objWbemAsyncContext* parameter.</span></span>

<span data-ttu-id="4ff89-163">如果沒有目前物件的子類別，則傳回的集合不會有零個元素的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4ff89-163">It is not an error for the returned collection to have zero elements if there are no subclasses of the current object.</span></span> <span data-ttu-id="4ff89-164">**SubclassesAsync \_** 方法只適用于類別物件。</span><span class="sxs-lookup"><span data-stu-id="4ff89-164">The **SubclassesAsync\_** method only works for class objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ff89-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ff89-165">Requirements</span></span>



| <span data-ttu-id="4ff89-166">需求</span><span class="sxs-lookup"><span data-stu-id="4ff89-166">Requirement</span></span> | <span data-ttu-id="4ff89-167">值</span><span class="sxs-lookup"><span data-stu-id="4ff89-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ff89-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ff89-168">Minimum supported client</span></span><br/> | <span data-ttu-id="4ff89-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ff89-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4ff89-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ff89-170">Minimum supported server</span></span><br/> | <span data-ttu-id="4ff89-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ff89-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ff89-172">標頭</span><span class="sxs-lookup"><span data-stu-id="4ff89-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ff89-173"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ff89-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ff89-174">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4ff89-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="4ff89-175"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4ff89-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4ff89-176">DLL</span><span class="sxs-lookup"><span data-stu-id="4ff89-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ff89-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ff89-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4ff89-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="4ff89-178">CLSID</span></span><br/>                    | <span data-ttu-id="4ff89-179">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="4ff89-179">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="4ff89-180">IID</span><span class="sxs-lookup"><span data-stu-id="4ff89-180">IID</span></span><br/>                      | <span data-ttu-id="4ff89-181">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="4ff89-181">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="4ff89-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ff89-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ff89-183">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="4ff89-183">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="4ff89-184">**Swbemobjectset 搭配使用**</span><span class="sxs-lookup"><span data-stu-id="4ff89-184">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> <dt>

[<span data-ttu-id="4ff89-185">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="4ff89-185">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> </dl>

 

