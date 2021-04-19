---
description: SWbemObject 的 ReferencesAsync \_ 方法會提供參考目前物件的所有關聯類別或實例的集合。 這個方法會執行查詢的 WQL 參考所執行的相同函數。
ms.assetid: 44989726-3f68-453b-b9f5-e76fb0fbb152
ms.tgt_platform: multiple
title: 'SWbemObject.ReferencesAsync_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: aa4b85475a0dc9f736254c8f207469a52897b7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978875"
---
# <a name="swbemobjectreferencesasync_-method"></a><span data-ttu-id="9cb7b-104">SWbemObject. ReferencesAsync \_ 方法</span><span class="sxs-lookup"><span data-stu-id="9cb7b-104">SWbemObject.ReferencesAsync\_ method</span></span>

<span data-ttu-id="9cb7b-105">[**SWbemObject**](swbemobject.md)的 **ReferencesAsync \_** 方法會提供參考目前物件的所有關聯類別或實例的集合。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-105">The **ReferencesAsync\_** method of [**SWbemObject**](swbemobject.md) supplies a collection of all association classes or instances that refer to the current object.</span></span> <span data-ttu-id="9cb7b-106">這個方法會執行查詢的 WQL [參考](references-of-statement.md) 所執行的相同函數。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-106">This method performs the same function that the WQL [REFERENCES OF](references-of-statement.md) query performs.</span></span>

<span data-ttu-id="9cb7b-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9cb7b-108">語法</span><span class="sxs-lookup"><span data-stu-id="9cb7b-108">Syntax</span></span>


```VB
SWbemObject.ReferencesAsync_( _
  ByVal objWbemSink, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9cb7b-109">參數</span><span class="sxs-lookup"><span data-stu-id="9cb7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cb7b-110">*objWbemSink* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9cb7b-110">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb7b-111">必要。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-111">Required.</span></span> <span data-ttu-id="9cb7b-112">以非同步方式接收物件的物件接收。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-112">Object sink that receives the objects asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="9cb7b-113">*strResultClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9cb7b-113">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb7b-114">包含類別名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-114">String that contains a class name.</span></span> <span data-ttu-id="9cb7b-115">如果有指定，這個參數會指出傳回的關聯物件必須屬於或衍生自這個參數中指定的類別。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-115">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9cb7b-116">*strRole* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9cb7b-116">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb7b-117">包含屬性名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-117">String that contains a property name.</span></span> <span data-ttu-id="9cb7b-118">如果有指定，這個參數表示所傳回的關聯物件必須限制為來源物件扮演特定角色的物件。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-118">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="9cb7b-119">指定之參考屬性的名稱會定義關聯的角色。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-119">The name of a specified reference property defines the role of an association.</span></span>

</dd> <dt>

<span data-ttu-id="9cb7b-120">*bClassesOnly* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9cb7b-120">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb7b-121">布林值，指出是否應該傳回類別名稱清單，而不是類別的實際實例。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-121">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="9cb7b-122">這些是關聯物件所屬的類別。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-122">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="9cb7b-123">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-123">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9cb7b-124">*bSchemaOnly* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9cb7b-124">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb7b-125">指出查詢是否適用于架構而非資料的布林值。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-125">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="9cb7b-126">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-126">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="9cb7b-127">如果叫用此方法的物件為類別，則只能設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-127">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="9cb7b-128">當設為 **TRUE** 時，傳回的端點集會代表與架構中的來源類別適當相關聯的類別。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-128">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="9cb7b-129">*strRequiredQualifier* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9cb7b-129">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb7b-130">包含辨識符號名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-130">String that contains a qualifier name.</span></span> <span data-ttu-id="9cb7b-131">如果有指定，這個參數會指出傳回的關聯物件必須包含指定的限定詞。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-131">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="9cb7b-132">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9cb7b-132">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb7b-133">指定作業其他旗標的整數。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-133">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="9cb7b-134">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-134">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="9cb7b-135"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="9cb7b-135"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="9cb7b-136">導致非同步呼叫將狀態更新傳送至物件接收的 [**SWbemSink. OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-136">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="9cb7b-137"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="9cb7b-137"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="9cb7b-138">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-138">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="9cb7b-139"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="9cb7b-139"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="9cb7b-140">造成 Windows Management Instrumentation (WMI) 以基類定義傳回類別修訂資料。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-140">Causes Windows Management Instrumentation (WMI) to return class amendment data with the base class definition.</span></span> <span data-ttu-id="9cb7b-141">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-141">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9cb7b-142">*objwbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9cb7b-142">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb7b-143">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-143">Typically, this is undefined.</span></span> <span data-ttu-id="9cb7b-144">否則，這會是 [SWbemNamedValueSet](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-144">Otherwise, this is an [SWbemNamedValueSet](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="9cb7b-145">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="9cb7b-146">*objWbemAsyncCoNtext* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9cb7b-146">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb7b-147">這是一個 [SWbemNamedValueSet](swbemnamedvalueset.md) 物件，它會返回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-147">This is an [SWbemNamedValueSet](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="9cb7b-148">如果您要使用相同的物件接收進行多個非同步呼叫，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="9cb7b-149">若要使用此參數，請建立 SWbemNamedValueSet 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-149">To use this parameter, create an SWbemNamedValueSet object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="9cb7b-150">這個 SWbemNamedValueSet 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-150">This SWbemNamedValueSet object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="9cb7b-151">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cb7b-152">傳回值</span><span class="sxs-lookup"><span data-stu-id="9cb7b-152">Return value</span></span>

<span data-ttu-id="9cb7b-153">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-153">This method does not return a value.</span></span> <span data-ttu-id="9cb7b-154">如果成功，接收就會收到每個實例的 [**OnObjectReady**](swbemsink-onobjectready.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-154">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="9cb7b-155">在最後一個實例之後，物件接收會收到 [**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-155">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9cb7b-156">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9cb7b-156">Error codes</span></span>

<span data-ttu-id="9cb7b-157">**ReferencesAsync \_** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-157">After the completion of the **ReferencesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="9cb7b-158">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="9cb7b-158">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="9cb7b-159">目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-159">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="9cb7b-160">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="9cb7b-160">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="9cb7b-161">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-161">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="9cb7b-162">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="9cb7b-162">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="9cb7b-163">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-163">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="9cb7b-164">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="9cb7b-164">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="9cb7b-165">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-165">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cb7b-166">備註</span><span class="sxs-lookup"><span data-stu-id="9cb7b-166">Remarks</span></span>

<span data-ttu-id="9cb7b-167">此呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-167">This call returns immediately.</span></span> <span data-ttu-id="9cb7b-168">要求的物件和狀態會透過回呼傳遞給 *objWbemSink* 中指定的接收，傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-168">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="9cb7b-169">若要在每個物件抵達時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-169">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="9cb7b-170">傳回所有物件之後，您就可以在 *objWbemSink* 的執行中執行最終處理。[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-170">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="9cb7b-171">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-171">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="9cb7b-172">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-172">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="9cb7b-173">若要消除風險，請使用兩個同步通訊或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-173">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="9cb7b-174">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-174">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="9cb7b-175">如需相關 WQL 查詢、來源實例和關聯物件之參考的詳細資訊，請參閱 [語句 associators of](associators-of-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="9cb7b-175">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cb7b-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="9cb7b-176">Requirements</span></span>



| <span data-ttu-id="9cb7b-177">需求</span><span class="sxs-lookup"><span data-stu-id="9cb7b-177">Requirement</span></span> | <span data-ttu-id="9cb7b-178">值</span><span class="sxs-lookup"><span data-stu-id="9cb7b-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cb7b-179">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9cb7b-179">Minimum supported client</span></span><br/> | <span data-ttu-id="9cb7b-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cb7b-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9cb7b-181">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9cb7b-181">Minimum supported server</span></span><br/> | <span data-ttu-id="9cb7b-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cb7b-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9cb7b-183">標頭</span><span class="sxs-lookup"><span data-stu-id="9cb7b-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cb7b-184"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="9cb7b-184"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9cb7b-185">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9cb7b-185">Type library</span></span><br/>             | <dl> <span data-ttu-id="9cb7b-186"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9cb7b-186"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9cb7b-187">DLL</span><span class="sxs-lookup"><span data-stu-id="9cb7b-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cb7b-188"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cb7b-188"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9cb7b-189">CLSID</span><span class="sxs-lookup"><span data-stu-id="9cb7b-189">CLSID</span></span><br/>                    | <span data-ttu-id="9cb7b-190">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="9cb7b-190">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="9cb7b-191">IID</span><span class="sxs-lookup"><span data-stu-id="9cb7b-191">IID</span></span><br/>                      | <span data-ttu-id="9cb7b-192">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="9cb7b-192">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="9cb7b-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9cb7b-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cb7b-194">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="9cb7b-194">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="9cb7b-195">**SWbemObject. Associators of\_**</span><span class="sxs-lookup"><span data-stu-id="9cb7b-195">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="9cb7b-196">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="9cb7b-196">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="9cb7b-197">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="9cb7b-197">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="9cb7b-198">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="9cb7b-198">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

