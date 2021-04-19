---
description: SWbemObject 的 AssociatorsAsync \_ 方法會取得與目前物件相關聯 (類別或實例) 的物件。 這些物件稱為端點。 這個方法會執行 WQL 查詢 ASSOCIATORS OF 所執行的相同功能。
ms.assetid: c71e11cd-39a5-40d8-b279-f5ee9ff3ae04
ms.tgt_platform: multiple
title: 'SWbemObject.AssociatorsAsync_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fe7a592327b6952308e44ac054fb94e21aa6d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974189"
---
# <a name="swbemobjectassociatorsasync_-method"></a><span data-ttu-id="a8460-105">SWbemObject. AssociatorsAsync \_ 方法</span><span class="sxs-lookup"><span data-stu-id="a8460-105">SWbemObject.AssociatorsAsync\_ method</span></span>

<span data-ttu-id="a8460-106">[**SWbemObject**](swbemobject.md)的 **AssociatorsAsync \_** 方法會取得與目前物件相關聯 (類別或實例) 的物件。</span><span class="sxs-lookup"><span data-stu-id="a8460-106">The **AssociatorsAsync\_** method of [**SWbemObject**](swbemobject.md) obtains objects (classes or instances) that are associated with the current object.</span></span> <span data-ttu-id="a8460-107">這些物件稱為端點。</span><span class="sxs-lookup"><span data-stu-id="a8460-107">These objects are called endpoints.</span></span> <span data-ttu-id="a8460-108">這個方法會執行 WQL 查詢 ASSOCIATORS OF 所執行的相同功能。</span><span class="sxs-lookup"><span data-stu-id="a8460-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="a8460-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="a8460-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8460-110">語法</span><span class="sxs-lookup"><span data-stu-id="a8460-110">Syntax</span></span>


```VB
SWbemObject.AssociatorsAsync_( _
  ByVal objWbemSink, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a8460-111">參數</span><span class="sxs-lookup"><span data-stu-id="a8460-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8460-112">*objWbemSink* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8460-112">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8460-113">必要。</span><span class="sxs-lookup"><span data-stu-id="a8460-113">Required.</span></span> <span data-ttu-id="a8460-114">以非同步方式接收物件作為回呼的物件接收。</span><span class="sxs-lookup"><span data-stu-id="a8460-114">Object sink that receives the objects asynchronously as a callback.</span></span>

</dd> <dt>

<span data-ttu-id="a8460-115">*strAssocClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a8460-115">*strAssocClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8460-116">包含關聯類別的字串。</span><span class="sxs-lookup"><span data-stu-id="a8460-116">String that contains an association class.</span></span> <span data-ttu-id="a8460-117">如果有指定，這個參數會指出傳回的端點必須透過指定的關聯類別或衍生自這個關聯類別的類別，與來源產生關聯。</span><span class="sxs-lookup"><span data-stu-id="a8460-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="a8460-118">*strResultClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a8460-118">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8460-119">包含類別名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="a8460-119">String that contains a class name.</span></span> <span data-ttu-id="a8460-120">如果有指定，這個參數會指出傳回的端點必須屬於或衍生自此參數中指定的類別。</span><span class="sxs-lookup"><span data-stu-id="a8460-120">If specified, this parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a8460-121">*strResultRole* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a8460-121">*strResultRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8460-122">包含屬性名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="a8460-122">String that contains a property name.</span></span> <span data-ttu-id="a8460-123">如果有指定，這個參數表示傳回的端點必須在其與來源物件的關聯中扮演特定的角色。</span><span class="sxs-lookup"><span data-stu-id="a8460-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="a8460-124">角色是由指定之屬性的名稱所定義 (必須是關聯) 的參考屬性。</span><span class="sxs-lookup"><span data-stu-id="a8460-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="a8460-125">*strRole* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a8460-125">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8460-126">包含屬性名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="a8460-126">String that contains a property name.</span></span> <span data-ttu-id="a8460-127">如果有指定，這個參數會指出傳回的端點必須參與來源物件的關聯，其中來源物件會扮演特定的角色。</span><span class="sxs-lookup"><span data-stu-id="a8460-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="a8460-128">角色是由指定之屬性的名稱所定義 (必須是關聯) 的參考屬性。</span><span class="sxs-lookup"><span data-stu-id="a8460-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="a8460-129">*bClassesOnly* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a8460-129">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8460-130">布林值，指出是否應該傳回類別名稱的清單，而不是類別的實際實例。</span><span class="sxs-lookup"><span data-stu-id="a8460-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="a8460-131">這些是端點實例所屬的類別。</span><span class="sxs-lookup"><span data-stu-id="a8460-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="a8460-132">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a8460-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a8460-133">*bSchemaOnly* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a8460-133">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8460-134">指出查詢是否適用于架構而非資料的布林值。</span><span class="sxs-lookup"><span data-stu-id="a8460-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="a8460-135">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a8460-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="a8460-136">如果叫用此方法的物件為類別，則只能設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="a8460-136">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="a8460-137">當設為 **TRUE** 時，傳回的端點集會代表與架構中的來源類別適當相關聯的類別。</span><span class="sxs-lookup"><span data-stu-id="a8460-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="a8460-138">*strRequiredAssocQualifier* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a8460-138">*strRequiredAssocQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8460-139">包含辨識符號名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="a8460-139">String that contains a qualifier name.</span></span> <span data-ttu-id="a8460-140">如果有指定，這個參數會指出傳回的端點必須透過包含指定限定詞的關聯類別，與來源物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="a8460-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="a8460-141">*strRequiredQualifier* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a8460-141">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8460-142">包含辨識符號名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="a8460-142">String that contains a qualifier name.</span></span> <span data-ttu-id="a8460-143">如果有指定，這個參數會指出傳回的端點必須包含指定的限定詞。</span><span class="sxs-lookup"><span data-stu-id="a8460-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="a8460-144">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a8460-144">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8460-145">指定作業其他旗標的整數。</span><span class="sxs-lookup"><span data-stu-id="a8460-145">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="a8460-146">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="a8460-146">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="a8460-147"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="a8460-147"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="a8460-148">導致非同步呼叫將狀態更新傳送至物件接收的 [**SWbemSink. OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="a8460-148">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="a8460-149"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="a8460-149"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="a8460-150">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="a8460-150">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="a8460-151"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="a8460-151"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="a8460-152">導致 WMI 傳回當地語系化的類別和屬性描述。</span><span class="sxs-lookup"><span data-stu-id="a8460-152">Causes WMI to return the localized class and property descriptions.</span></span> <span data-ttu-id="a8460-153">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="a8460-153">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a8460-154">*objwbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a8460-154">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8460-155">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="a8460-155">Typically, this is undefined.</span></span> <span data-ttu-id="a8460-156">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="a8460-156">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="a8460-157">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="a8460-157">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="a8460-158">*objWbemAsyncCoNtext* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a8460-158">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8460-159">這是一個 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，它會返回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="a8460-159">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="a8460-160">如果您要使用相同的物件接收進行多個非同步呼叫，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="a8460-160">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="a8460-161">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="a8460-161">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="a8460-162">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="a8460-162">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="a8460-163">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="a8460-163">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8460-164">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8460-164">Return value</span></span>

<span data-ttu-id="a8460-165">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a8460-165">This method does not return a value.</span></span> <span data-ttu-id="a8460-166">如果成功，接收就會收到每個實例的 [**OnObjectReady**](swbemsink-onobjectready.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="a8460-166">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="a8460-167">在最後一個實例之後，物件接收會收到 [**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="a8460-167">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a8460-168">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="a8460-168">Error codes</span></span>

<span data-ttu-id="a8460-169">完成 **AssociatorsAsync \_** 方法之後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a8460-169">After completion of the **AssociatorsAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a8460-170">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="a8460-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="a8460-171">目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="a8460-171">The current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="a8460-172">**wbemErrFailed** -2147449889 (0x7FFF7C21) </span><span class="sxs-lookup"><span data-stu-id="a8460-172">**wbemErrFailed** - 2147449889 (0x7FFF7C21)</span></span>
</dt> <dd>

<span data-ttu-id="a8460-173">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a8460-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a8460-174">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="a8460-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a8460-175">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="a8460-175">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a8460-176">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="a8460-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a8460-177">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="a8460-177">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8460-178">備註</span><span class="sxs-lookup"><span data-stu-id="a8460-178">Remarks</span></span>

<span data-ttu-id="a8460-179">此呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="a8460-179">This call returns immediately.</span></span> <span data-ttu-id="a8460-180">要求的物件和狀態會透過傳送至 *objWbemSink* 中指定之接收的呼叫傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="a8460-180">The requested objects and status are returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="a8460-181">若要在每個物件抵達時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。</span><span class="sxs-lookup"><span data-stu-id="a8460-181">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="a8460-182">傳回所有物件之後，您就可以在 *objWbemSink* 的執行中執行最終處理。[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="a8460-182">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="a8460-183">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="a8460-183">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="a8460-184">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="a8460-184">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="a8460-185">若要消除風險，請使用兩個同步通訊或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="a8460-185">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="a8460-186">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="a8460-186">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="a8460-187">如需有關 ASSOCIATORS OF 相關 WQL 查詢、來源實例和端點的詳細資訊，請參閱 [語句 associators of](associators-of-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="a8460-187">For more information about the ASSOCIATORS OF associated WQL queries, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8460-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8460-188">Requirements</span></span>



| <span data-ttu-id="a8460-189">需求</span><span class="sxs-lookup"><span data-stu-id="a8460-189">Requirement</span></span> | <span data-ttu-id="a8460-190">值</span><span class="sxs-lookup"><span data-stu-id="a8460-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8460-191">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8460-191">Minimum supported client</span></span><br/> | <span data-ttu-id="a8460-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8460-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8460-193">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8460-193">Minimum supported server</span></span><br/> | <span data-ttu-id="a8460-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8460-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8460-195">標頭</span><span class="sxs-lookup"><span data-stu-id="a8460-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8460-196"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8460-196"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8460-197">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a8460-197">Type library</span></span><br/>             | <dl> <span data-ttu-id="a8460-198"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a8460-198"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a8460-199">DLL</span><span class="sxs-lookup"><span data-stu-id="a8460-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8460-200"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8460-200"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a8460-201">CLSID</span><span class="sxs-lookup"><span data-stu-id="a8460-201">CLSID</span></span><br/>                    | <span data-ttu-id="a8460-202">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="a8460-202">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="a8460-203">IID</span><span class="sxs-lookup"><span data-stu-id="a8460-203">IID</span></span><br/>                      | <span data-ttu-id="a8460-204">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="a8460-204">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="a8460-205">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8460-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8460-206">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="a8460-206">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="a8460-207">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="a8460-207">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="a8460-208">**SWbemObject 參考\_**</span><span class="sxs-lookup"><span data-stu-id="a8460-208">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="a8460-209">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="a8460-209">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

