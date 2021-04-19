---
description: 傳回參考特定來源類別或實例的所有關聯類別或實例。
ms.assetid: 2ad66ea1-b8f0-4b6b-b68f-29496afbe4bf
ms.tgt_platform: multiple
title: 'SWbemServices. ReferencesToAsync 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 64a8b9b336a1e7aa6007b17d2e878f1ace5e6163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979760"
---
# <a name="swbemservicesreferencestoasync-method"></a><span data-ttu-id="8d2fa-103">SWbemServices. ReferencesToAsync 方法</span><span class="sxs-lookup"><span data-stu-id="8d2fa-103">SWbemServices.ReferencesToAsync method</span></span>

<span data-ttu-id="8d2fa-104">[**SWbemServices**](swbemservices.md)物件的 **ReferencesToAsync** 方法會傳回參考特定來源類別或實例的所有關聯類別或實例。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-104">The **ReferencesToAsync** method of the [**SWbemServices**](swbemservices.md) object returns all association classes or instances that refer to a specific source class or instance.</span></span> <span data-ttu-id="8d2fa-105">這個方法會執行 WQL 查詢 [參考](references-of-statement.md) 所執行的相同函數。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-105">This method performs the same function that the [REFERENCES OF](references-of-statement.md) WQL query performs.</span></span>

<span data-ttu-id="8d2fa-106">如需非同步模式的詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-106">For more information about the asynchronous mode, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="8d2fa-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d2fa-108">語法</span><span class="sxs-lookup"><span data-stu-id="8d2fa-108">Syntax</span></span>


```VB
SWbemServices.ReferencesToAsync( _
  ByVal ObjWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8d2fa-109">參數</span><span class="sxs-lookup"><span data-stu-id="8d2fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d2fa-110">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="8d2fa-110">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="8d2fa-111">必要。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-111">Required.</span></span> <span data-ttu-id="8d2fa-112">以非同步方式接收物件的物件接收。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-112">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="8d2fa-113">建立 [**SWbemSink**](swbemsink.md) 物件以接收物件。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-113">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="8d2fa-114">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="8d2fa-114">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="8d2fa-115">必要。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-115">Required.</span></span> <span data-ttu-id="8d2fa-116">字串，包含此方法之來源的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-116">String that contains the object path of the source for this method.</span></span> <span data-ttu-id="8d2fa-117">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-117">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d2fa-118">*strResultClass* \[選\]</span><span class="sxs-lookup"><span data-stu-id="8d2fa-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2fa-119">包含類別名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-119">String that contains a class name.</span></span> <span data-ttu-id="8d2fa-120">如果有指定，這個參數會指出傳回的關聯物件必須屬於或衍生自此參數中指定的類別。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-120">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class that is specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8d2fa-121">*strRole* \[選\]</span><span class="sxs-lookup"><span data-stu-id="8d2fa-121">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2fa-122">包含屬性名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-122">String that contains a property name.</span></span> <span data-ttu-id="8d2fa-123">如果有指定，這個參數表示所傳回的關聯物件必須限制為來源物件扮演特定角色的物件。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-123">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="8d2fa-124">角色是由關聯之指定參考屬性的名稱所定義。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-124">The role is defined by the name of a specified reference property of an association.</span></span>

</dd> <dt>

<span data-ttu-id="8d2fa-125">*bClassesOnly* \[選\]</span><span class="sxs-lookup"><span data-stu-id="8d2fa-125">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2fa-126">布林值，指出是否應該傳回類別名稱清單，而不是類別的實際實例。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-126">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="8d2fa-127">這些是關聯物件所屬的類別。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-127">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="8d2fa-128">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-128">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="8d2fa-129">*bSchemaOnly* \[選\]</span><span class="sxs-lookup"><span data-stu-id="8d2fa-129">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2fa-130">指出查詢是否適用于架構而非資料的布林值。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-130">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="8d2fa-131">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-131">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="8d2fa-132">如果 *strObjectPath* 參數指定類別的物件路徑，它只能設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-132">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="8d2fa-133">當設為 **TRUE** 時，傳回的端點集會代表與架構中的來源類別相關聯的類別。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-133">When set to **TRUE**, the set of returned endpoints represents classes that are associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="8d2fa-134">*strRequiredQualifier* \[選\]</span><span class="sxs-lookup"><span data-stu-id="8d2fa-134">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2fa-135">包含辨識符號名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-135">String that contains a qualifier name.</span></span> <span data-ttu-id="8d2fa-136">如果有指定，這個參數會指出傳回的關聯物件必須包含指定的限定詞。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-136">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="8d2fa-137">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="8d2fa-137">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2fa-138">指定運算其他旗標的整數。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-138">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="8d2fa-139">此參數的預設值為 **wbemFlagBidirectional**。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-139">The default for this parameter is **wbemFlagBidirectional**.</span></span> <span data-ttu-id="8d2fa-140">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-140">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="8d2fa-141"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="8d2fa-141"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="8d2fa-142">導致非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-142">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="8d2fa-143"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="8d2fa-143"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="8d2fa-144">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-144">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="8d2fa-145"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="8d2fa-145"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="8d2fa-146">造成 Windows Management Instrumentation (WMI) 傳回類別修訂資料以及基類定義。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-146">Causes Windows Management Instrumentation (WMI) to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="8d2fa-147">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-147">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8d2fa-148">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="8d2fa-148">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2fa-149">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-149">Typically, this is undefined.</span></span> <span data-ttu-id="8d2fa-150">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-150">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="8d2fa-151">支援或需要內容資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-151">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="8d2fa-152">*objWbemAsyncCoNtext* \[選\]</span><span class="sxs-lookup"><span data-stu-id="8d2fa-152">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2fa-153">這是一個 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，它會返回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-153">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="8d2fa-154">使用這個參數可使用相同的物件接收進行多個非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-154">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="8d2fa-155">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-155">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="8d2fa-156">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而且可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法來解壓縮呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-156">This **SWbemNamedValueSet** object is returned to the object sink, and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="8d2fa-157">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-157">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d2fa-158">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d2fa-158">Return value</span></span>

<span data-ttu-id="8d2fa-159">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-159">This method does not return a value.</span></span> <span data-ttu-id="8d2fa-160">如果成功，接收就會收到每個實例的 [**OnObjectReady**](swbemsink-onobjectready.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-160">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="8d2fa-161">在最後一個實例之後，物件接收會收到 [**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-161">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8d2fa-162">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="8d2fa-162">Error codes</span></span>

<span data-ttu-id="8d2fa-163">**ReferencesToAsync** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-163">After the completion of the **ReferencesToAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="8d2fa-164">具有零個元素的傳回集合不是錯誤。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-164">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="8d2fa-165">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="8d2fa-165">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="8d2fa-166">目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-166">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="8d2fa-167">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="8d2fa-167">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8d2fa-168">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-168">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="8d2fa-169">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="8d2fa-169">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="8d2fa-170">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-170">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="8d2fa-171">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="8d2fa-171">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="8d2fa-172">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-172">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d2fa-173">備註</span><span class="sxs-lookup"><span data-stu-id="8d2fa-173">Remarks</span></span>

<span data-ttu-id="8d2fa-174">此呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-174">This call returns immediately.</span></span> <span data-ttu-id="8d2fa-175">要求的物件和狀態會透過回呼傳遞給 *objWbemSink* 中指定的接收，傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-175">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="8d2fa-176">若要在每個物件返回時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-176">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="8d2fa-177">傳回所有物件之後，您就可以在 *objWbemSink* 的執行中執行最終處理。[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-177">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="8d2fa-178">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-178">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="8d2fa-179">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-179">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="8d2fa-180">若要消除風險，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="8d2fa-180">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d2fa-181">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d2fa-181">Requirements</span></span>



| <span data-ttu-id="8d2fa-182">需求</span><span class="sxs-lookup"><span data-stu-id="8d2fa-182">Requirement</span></span> | <span data-ttu-id="8d2fa-183">值</span><span class="sxs-lookup"><span data-stu-id="8d2fa-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d2fa-184">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d2fa-184">Minimum supported client</span></span><br/> | <span data-ttu-id="8d2fa-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d2fa-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d2fa-186">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d2fa-186">Minimum supported server</span></span><br/> | <span data-ttu-id="8d2fa-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d2fa-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d2fa-188">標頭</span><span class="sxs-lookup"><span data-stu-id="8d2fa-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d2fa-189"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d2fa-189"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d2fa-190">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8d2fa-190">Type library</span></span><br/>             | <dl> <span data-ttu-id="8d2fa-191"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8d2fa-191"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8d2fa-192">DLL</span><span class="sxs-lookup"><span data-stu-id="8d2fa-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d2fa-193"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d2fa-193"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8d2fa-194">CLSID</span><span class="sxs-lookup"><span data-stu-id="8d2fa-194">CLSID</span></span><br/>                    | <span data-ttu-id="8d2fa-195">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="8d2fa-195">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="8d2fa-196">IID</span><span class="sxs-lookup"><span data-stu-id="8d2fa-196">IID</span></span><br/>                      | <span data-ttu-id="8d2fa-197">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="8d2fa-197">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="8d2fa-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d2fa-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d2fa-199">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="8d2fa-199">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="8d2fa-200">**SWbemObject. Associators of\_**</span><span class="sxs-lookup"><span data-stu-id="8d2fa-200">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="8d2fa-201">**SWbemObject 參考\_**</span><span class="sxs-lookup"><span data-stu-id="8d2fa-201">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="8d2fa-202">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="8d2fa-202">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

