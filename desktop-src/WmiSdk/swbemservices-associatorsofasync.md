---
description: SWbemServices. AssociatorsOfAsync 方法-傳回 (類別或實例的集合，) 名為與指定物件相關聯的端點。
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: 'SWbemServices. AssociatorsOfAsync 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4b16eed97c891b4b4f5bd283496868d99f9e0fbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103666"
---
# <a name="swbemservicesassociatorsofasync-method"></a><span data-ttu-id="970ee-103">SWbemServices. AssociatorsOfAsync 方法</span><span class="sxs-lookup"><span data-stu-id="970ee-103">SWbemServices.AssociatorsOfAsync method</span></span>

<span data-ttu-id="970ee-104">[**SWbemServices**](swbemservices.md)物件的 **AssociatorsOfAsync** 方法會傳回物件的集合， (類別或實例) 稱為與指定物件相關聯的端點。</span><span class="sxs-lookup"><span data-stu-id="970ee-104">The **AssociatorsOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="970ee-105">**AssociatorsOfAsync** 的呼叫會立即傳回，而結果和狀態會透過傳遞至 *objWbemSink* 中指定之接收的事件傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="970ee-105">The call to **AssociatorsOfAsync** returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="970ee-106">若要處理每個傳回的物件，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="970ee-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event handler.</span></span>

<span data-ttu-id="970ee-107">所有物件都抵達之後，就會在 *objWbemSink* 中進行處理。[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="970ee-107">After all the objects arrive, processing is done in the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span> <span data-ttu-id="970ee-108">這個方法會執行 WQL 查詢 ASSOCIATORS OF 所執行的相同功能。</span><span class="sxs-lookup"><span data-stu-id="970ee-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span> <span data-ttu-id="970ee-109">如需建立接收的詳細資訊，請參閱 [接收 WMI 事件](receiving-a-wmi-event.md)。</span><span class="sxs-lookup"><span data-stu-id="970ee-109">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="970ee-110">在非同步模式中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="970ee-110">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="970ee-111">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="970ee-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="970ee-112">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="970ee-112">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="970ee-113">語法</span><span class="sxs-lookup"><span data-stu-id="970ee-113">Syntax</span></span>


```VB
SWbemServices.AssociatorsOfAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="970ee-114">參數</span><span class="sxs-lookup"><span data-stu-id="970ee-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="970ee-115">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="970ee-115">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="970ee-116">必要。</span><span class="sxs-lookup"><span data-stu-id="970ee-116">Required.</span></span> <span data-ttu-id="970ee-117">以非同步方式接收物件的物件接收。</span><span class="sxs-lookup"><span data-stu-id="970ee-117">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="970ee-118">建立 [**SWbemSink**](swbemsink.md) 物件以接收物件。</span><span class="sxs-lookup"><span data-stu-id="970ee-118">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="970ee-119">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="970ee-119">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="970ee-120">必要。</span><span class="sxs-lookup"><span data-stu-id="970ee-120">Required.</span></span> <span data-ttu-id="970ee-121">字串，包含來源類別或實例的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="970ee-121">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="970ee-122">如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="970ee-122">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="970ee-123">*strAssocClass* \[選\]</span><span class="sxs-lookup"><span data-stu-id="970ee-123">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="970ee-124">包含關聯類別的字串。</span><span class="sxs-lookup"><span data-stu-id="970ee-124">String that contains an association class.</span></span> <span data-ttu-id="970ee-125">指定時，這個參數會指出傳回的端點必須透過指定的關聯類別或衍生自這個關聯類別的類別，與來源產生關聯。</span><span class="sxs-lookup"><span data-stu-id="970ee-125">When specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="970ee-126">*strResultClass* \[選\]</span><span class="sxs-lookup"><span data-stu-id="970ee-126">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="970ee-127">包含類別名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="970ee-127">String that contains a class name.</span></span> <span data-ttu-id="970ee-128">如果有指定，此選擇性參數表示傳回的端點必須屬於或衍生自此參數中指定的類別。</span><span class="sxs-lookup"><span data-stu-id="970ee-128">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="970ee-129">*strResultRole* \[選\]</span><span class="sxs-lookup"><span data-stu-id="970ee-129">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="970ee-130">包含屬性名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="970ee-130">String that contains a property name.</span></span> <span data-ttu-id="970ee-131">如果有指定，這個參數表示傳回的端點必須在其與來源物件的關聯中扮演特定的角色。</span><span class="sxs-lookup"><span data-stu-id="970ee-131">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="970ee-132">角色是由指定之屬性的名稱所定義 (必須是關聯) 的參考屬性。</span><span class="sxs-lookup"><span data-stu-id="970ee-132">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="970ee-133">*strRole* \[選\]</span><span class="sxs-lookup"><span data-stu-id="970ee-133">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="970ee-134">包含屬性名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="970ee-134">String that contains a property name.</span></span> <span data-ttu-id="970ee-135">如果有指定，這個參數會指出傳回的端點必須參與來源物件的關聯，其中來源物件會扮演特定的角色。</span><span class="sxs-lookup"><span data-stu-id="970ee-135">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="970ee-136">角色是由指定之屬性的名稱所定義 (必須是關聯) 的參考屬性。</span><span class="sxs-lookup"><span data-stu-id="970ee-136">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="970ee-137">*bClassesOnly* \[選\]</span><span class="sxs-lookup"><span data-stu-id="970ee-137">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="970ee-138">布林值，指出是否應該傳回類別名稱的清單，而不是類別的實際實例。</span><span class="sxs-lookup"><span data-stu-id="970ee-138">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="970ee-139">這些是端點實例所屬的類別。</span><span class="sxs-lookup"><span data-stu-id="970ee-139">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="970ee-140">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="970ee-140">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="970ee-141">*bSchemaOnly* \[選\]</span><span class="sxs-lookup"><span data-stu-id="970ee-141">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="970ee-142">指出查詢是否適用于架構而非資料的布林值。</span><span class="sxs-lookup"><span data-stu-id="970ee-142">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="970ee-143">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="970ee-143">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="970ee-144">如果 *strObjectPath* 參數指定類別的物件路徑，它只能設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="970ee-144">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="970ee-145">當設為 **TRUE** 時，傳回的端點集會代表與架構中的來源類別適當相關聯的類別。</span><span class="sxs-lookup"><span data-stu-id="970ee-145">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="970ee-146">*strRequiredAssocQualifier* \[選\]</span><span class="sxs-lookup"><span data-stu-id="970ee-146">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="970ee-147">包含辨識符號名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="970ee-147">String that contains a qualifier name.</span></span> <span data-ttu-id="970ee-148">如果有指定，這個參數會指出傳回的端點必須透過包含指定限定詞的關聯類別，與來源物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="970ee-148">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="970ee-149">*strRequiredQualifier* \[選\]</span><span class="sxs-lookup"><span data-stu-id="970ee-149">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="970ee-150">包含辨識符號名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="970ee-150">String that contains a qualifier name.</span></span> <span data-ttu-id="970ee-151">如果有指定，這個參數會指出傳回的端點必須包含指定的限定詞。</span><span class="sxs-lookup"><span data-stu-id="970ee-151">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="970ee-152">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="970ee-152">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="970ee-153">指定作業其他旗標的整數。</span><span class="sxs-lookup"><span data-stu-id="970ee-153">Integer that specifies the additional flags to the operation.</span></span> <span data-ttu-id="970ee-154">此參數的預設值為 **wbemFlagDontSendStatus**。</span><span class="sxs-lookup"><span data-stu-id="970ee-154">The default for this parameter is **wbemFlagDontSendStatus**.</span></span> <span data-ttu-id="970ee-155">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="970ee-155">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="970ee-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="970ee-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="970ee-157">導致非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="970ee-157">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="970ee-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="970ee-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="970ee-159">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="970ee-159">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="970ee-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="970ee-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="970ee-161">導致 WMI 傳回類別修訂資料以及基類定義。</span><span class="sxs-lookup"><span data-stu-id="970ee-161">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="970ee-162">如需修改過的限定詞的詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="970ee-162">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="970ee-163">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="970ee-163">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="970ee-164">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="970ee-164">Typically, this is undefined.</span></span> <span data-ttu-id="970ee-165">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="970ee-165">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="970ee-166">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="970ee-166">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="970ee-167">*objWbemAsyncCoNtext* \[選\]</span><span class="sxs-lookup"><span data-stu-id="970ee-167">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="970ee-168">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，這個物件會傳回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="970ee-168">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="970ee-169">如果您要使用相同的物件接收進行多個非同步呼叫，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="970ee-169">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="970ee-170">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="970ee-170">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="970ee-171">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="970ee-171">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="970ee-172">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="970ee-172">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="970ee-173">傳回值</span><span class="sxs-lookup"><span data-stu-id="970ee-173">Return value</span></span>

<span data-ttu-id="970ee-174">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="970ee-174">This method does not return a value.</span></span> <span data-ttu-id="970ee-175">如果成功，接收就會收到每個實例的 [**OnObjectReady**](swbemsink-onobjectready.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="970ee-175">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="970ee-176">在最後一個實例之後，物件接收會收到 [**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="970ee-176">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="970ee-177">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="970ee-177">Error codes</span></span>

<span data-ttu-id="970ee-178">**AssociatorsOfAsync** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="970ee-178">After the completion of the **AssociatorsOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="970ee-179">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="970ee-179">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="970ee-180">目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="970ee-180">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="970ee-181">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="970ee-181">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="970ee-182">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="970ee-182">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="970ee-183">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="970ee-183">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="970ee-184">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="970ee-184">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="970ee-185">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="970ee-185">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="970ee-186">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="970ee-186">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="970ee-187">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="970ee-187">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="970ee-188">找不到要求的專案。</span><span class="sxs-lookup"><span data-stu-id="970ee-188">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="970ee-189">備註</span><span class="sxs-lookup"><span data-stu-id="970ee-189">Remarks</span></span>

<span data-ttu-id="970ee-190">此呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="970ee-190">This call returns immediately.</span></span> <span data-ttu-id="970ee-191">要求的物件和狀態會透過回呼傳遞給 *objWbemSink* 中指定的接收，傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="970ee-191">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="970ee-192">若要在每個物件返回時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。</span><span class="sxs-lookup"><span data-stu-id="970ee-192">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="970ee-193">傳回所有物件之後，您就可以在 *objWbemSink* 的執行中執行最終處理。[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="970ee-193">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="970ee-194">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="970ee-194">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="970ee-195">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="970ee-195">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="970ee-196">若要消除風險，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="970ee-196">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="970ee-197">在腳本中使用 *objWbemAsyncCoNtext* 參數來驗證呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="970ee-197">Use the *objWbemAsyncContext* parameter in scripts to verify the source of a call.</span></span>

## <a name="requirements"></a><span data-ttu-id="970ee-198">規格需求</span><span class="sxs-lookup"><span data-stu-id="970ee-198">Requirements</span></span>



| <span data-ttu-id="970ee-199">需求</span><span class="sxs-lookup"><span data-stu-id="970ee-199">Requirement</span></span> | <span data-ttu-id="970ee-200">值</span><span class="sxs-lookup"><span data-stu-id="970ee-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="970ee-201">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="970ee-201">Minimum supported client</span></span><br/> | <span data-ttu-id="970ee-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="970ee-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="970ee-203">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="970ee-203">Minimum supported server</span></span><br/> | <span data-ttu-id="970ee-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="970ee-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="970ee-205">標頭</span><span class="sxs-lookup"><span data-stu-id="970ee-205">Header</span></span><br/>                   | <dl> <span data-ttu-id="970ee-206"><dt>>Wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="970ee-206"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="970ee-207">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="970ee-207">Type library</span></span><br/>             | <dl> <span data-ttu-id="970ee-208"><dt>>Wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="970ee-208"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="970ee-209">DLL</span><span class="sxs-lookup"><span data-stu-id="970ee-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="970ee-210"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="970ee-210"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="970ee-211">CLSID</span><span class="sxs-lookup"><span data-stu-id="970ee-211">CLSID</span></span><br/>                    | <span data-ttu-id="970ee-212">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="970ee-212">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="970ee-213">IID</span><span class="sxs-lookup"><span data-stu-id="970ee-213">IID</span></span><br/>                      | <span data-ttu-id="970ee-214">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="970ee-214">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="970ee-215">另請參閱</span><span class="sxs-lookup"><span data-stu-id="970ee-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="970ee-216">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="970ee-216">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="970ee-217">**SWbemObject. Associators of\_**</span><span class="sxs-lookup"><span data-stu-id="970ee-217">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="970ee-218">**SWbemObject. AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="970ee-218">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="970ee-219">**SWbemObject 參考\_**</span><span class="sxs-lookup"><span data-stu-id="970ee-219">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="970ee-220">**SWbemObject. ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="970ee-220">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)
</dt> <dt>

[<span data-ttu-id="970ee-221">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="970ee-221">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="970ee-222">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="970ee-222">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

