---
description: '\_SWbemObject 物件的 associators of 方法會傳回與目前物件相關聯)  (類別或實例的集合。'
ms.assetid: 79f01853-c649-4cbe-b2fa-cff38fb4b733
ms.tgt_platform: multiple
title: 'SWbemObject.Associators_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Associators_
- ISWbemObject.Associators_
- ISWbemObject.Associators_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1f9ff4536936661ece54b5bff29e500ce6e98d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944931"
---
# <a name="swbemobjectassociators_-method"></a><span data-ttu-id="409e8-103">SWbemObject. Associators of \_ 方法</span><span class="sxs-lookup"><span data-stu-id="409e8-103">SWbemObject.Associators\_ method</span></span>

<span data-ttu-id="409e8-104">[**SWbemObject**](swbemobject.md)物件的 **associators of \_** 方法會傳回與目前物件相關聯)  (類別或實例的集合。</span><span class="sxs-lookup"><span data-stu-id="409e8-104">The **Associators\_** method of the [**SWbemObject**](swbemobject.md) object returns a collection of objects (classes or instances) that are associated with the current object.</span></span> <span data-ttu-id="409e8-105">這些傳回的物件稱為端點。</span><span class="sxs-lookup"><span data-stu-id="409e8-105">These returned objects are called endpoints.</span></span> <span data-ttu-id="409e8-106">這個方法會執行 WQL 查詢 ASSOCIATORS OF 所執行的相同功能。</span><span class="sxs-lookup"><span data-stu-id="409e8-106">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="409e8-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="409e8-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="409e8-108">語法</span><span class="sxs-lookup"><span data-stu-id="409e8-108">Syntax</span></span>


```VB
objWbemObjectSet = .Associators_( _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="409e8-109">參數</span><span class="sxs-lookup"><span data-stu-id="409e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="409e8-110">*strAssocClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="409e8-110">*strAssocClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="409e8-111">包含關聯類別的字串。</span><span class="sxs-lookup"><span data-stu-id="409e8-111">String that contains an association class.</span></span> <span data-ttu-id="409e8-112">如果有指定，這個參數會指出傳回的端點必須透過指定的關聯類別或衍生自這個關聯類別的類別，與來源產生關聯。</span><span class="sxs-lookup"><span data-stu-id="409e8-112">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="409e8-113">*strResultClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="409e8-113">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="409e8-114">包含類別名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="409e8-114">String that contains a class name.</span></span> <span data-ttu-id="409e8-115">如果有指定，這個參數會指出傳回的端點必須屬於或衍生自此參數中指定的類別。</span><span class="sxs-lookup"><span data-stu-id="409e8-115">If specified, this parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="409e8-116">*strResultRole* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="409e8-116">*strResultRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="409e8-117">包含屬性名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="409e8-117">String that contains a property name.</span></span> <span data-ttu-id="409e8-118">如果有指定，這個參數表示傳回的端點必須在其與來源物件的關聯中扮演特定的角色。</span><span class="sxs-lookup"><span data-stu-id="409e8-118">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="409e8-119">角色是由指定之屬性的名稱所定義 (必須是關聯) 的參考屬性。</span><span class="sxs-lookup"><span data-stu-id="409e8-119">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="409e8-120">*strRole* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="409e8-120">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="409e8-121">包含屬性名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="409e8-121">String that contains a property name.</span></span> <span data-ttu-id="409e8-122">如果有指定，這個參數會指出傳回的端點必須參與來源物件的關聯，其中來源物件會扮演特定的角色。</span><span class="sxs-lookup"><span data-stu-id="409e8-122">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="409e8-123">角色是由指定之屬性的名稱所定義 (必須是關聯) 的參考屬性。</span><span class="sxs-lookup"><span data-stu-id="409e8-123">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="409e8-124">*bClassesOnly* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="409e8-124">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="409e8-125">布林值，指出是否應該傳回類別名稱的清單，而不是類別的實際實例。</span><span class="sxs-lookup"><span data-stu-id="409e8-125">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="409e8-126">這些是端點實例所屬的類別。</span><span class="sxs-lookup"><span data-stu-id="409e8-126">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="409e8-127">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="409e8-127">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="409e8-128">*bSchemaOnly* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="409e8-128">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="409e8-129">這是布林值，指出查詢是否適用于架構，而不是資料。</span><span class="sxs-lookup"><span data-stu-id="409e8-129">This is a Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="409e8-130">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="409e8-130">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="409e8-131">如果叫用此方法的物件為類別，則只能設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="409e8-131">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="409e8-132">當設為 **TRUE** 時，傳回的端點集會代表與架構中的來源類別適當相關聯的類別。</span><span class="sxs-lookup"><span data-stu-id="409e8-132">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="409e8-133">*strRequiredAssocQualifier* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="409e8-133">*strRequiredAssocQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="409e8-134">包含辨識符號名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="409e8-134">String that contains a qualifier name.</span></span> <span data-ttu-id="409e8-135">如果有指定，這個參數會指出傳回的端點必須透過包含指定限定詞的關聯類別，與來源物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="409e8-135">This parameter, if specified, indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="409e8-136">*strRequiredQualifier* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="409e8-136">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="409e8-137">包含辨識符號名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="409e8-137">String that contains a qualifier name.</span></span> <span data-ttu-id="409e8-138">如果有指定，這個參數表示傳回的端點必須包含指定的限定詞。</span><span class="sxs-lookup"><span data-stu-id="409e8-138">This parameter, if specified, indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="409e8-139">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="409e8-139">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="409e8-140">指定作業其他旗標的整數。</span><span class="sxs-lookup"><span data-stu-id="409e8-140">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="409e8-141">這個參數的預設值是 **wbemFlagReturnImmediately**，它會指示立即傳回呼叫，而不是等到查詢完成為止。</span><span class="sxs-lookup"><span data-stu-id="409e8-141">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="409e8-142">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="409e8-142">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="409e8-143"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="409e8-143"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="409e8-144">使順向列舉值傳回。</span><span class="sxs-lookup"><span data-stu-id="409e8-144">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="409e8-145">順向列舉值的速度通常會比傳統列舉值更快，且使用的記憶體較少，但不允許呼叫 [**SWbemObject。 \_**](swbemobject-clone-.md)</span><span class="sxs-lookup"><span data-stu-id="409e8-145">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="409e8-146"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="409e8-146"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="409e8-147">讓 WMI 保留列舉物件的指標，直到用戶端釋放列舉值為止。</span><span class="sxs-lookup"><span data-stu-id="409e8-147">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="409e8-148"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="409e8-148"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="409e8-149">導致呼叫立即返回。</span><span class="sxs-lookup"><span data-stu-id="409e8-149">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="409e8-150"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="409e8-150"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="409e8-151">導致此呼叫封鎖，直到查詢完成為止。</span><span class="sxs-lookup"><span data-stu-id="409e8-151">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="409e8-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="409e8-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="409e8-153">讓 WMI 以基類定義傳回類別修訂資料。</span><span class="sxs-lookup"><span data-stu-id="409e8-153">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="409e8-154">包含這個旗標可讓當地語系化的描述辨識符號文字可供類別、屬性和方法使用。</span><span class="sxs-lookup"><span data-stu-id="409e8-154">Including this flag makes the localized description qualifier text available for classes, properties and methods.</span></span> <span data-ttu-id="409e8-155">如需修改過的限定詞的詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="409e8-155">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="409e8-156">*objwbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="409e8-156">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="409e8-157">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="409e8-157">Typically, this is undefined.</span></span> <span data-ttu-id="409e8-158">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="409e8-158">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="409e8-159">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="409e8-159">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="409e8-160">傳回值</span><span class="sxs-lookup"><span data-stu-id="409e8-160">Return value</span></span>

<span data-ttu-id="409e8-161">如果呼叫成功，則會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="409e8-161">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="409e8-162">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="409e8-162">Error codes</span></span>

<span data-ttu-id="409e8-163">完成 **associators of \_** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="409e8-163">After completion of the **Associators\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="409e8-164">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="409e8-164">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="409e8-165">目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="409e8-165">The current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="409e8-166">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="409e8-166">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="409e8-167">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="409e8-167">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="409e8-168">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="409e8-168">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="409e8-169">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="409e8-169">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="409e8-170">**wbemErrOutOfMemory** -2147749894</span><span class="sxs-lookup"><span data-stu-id="409e8-170">**wbemErrOutOfMemory** - 2147749894</span></span>
</dt> <dd>

<span data-ttu-id="409e8-171">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="409e8-171">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="409e8-172">備註</span><span class="sxs-lookup"><span data-stu-id="409e8-172">Remarks</span></span>

<span data-ttu-id="409e8-173">如需有關 ASSOCIATORS OF 相關 WQL 查詢、來源實例和端點的詳細資訊，請參閱 [語句 associators of](associators-of-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="409e8-173">For more information about the ASSOCIATORS OF associated WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="409e8-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="409e8-174">Requirements</span></span>



| <span data-ttu-id="409e8-175">需求</span><span class="sxs-lookup"><span data-stu-id="409e8-175">Requirement</span></span> | <span data-ttu-id="409e8-176">值</span><span class="sxs-lookup"><span data-stu-id="409e8-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="409e8-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="409e8-177">Minimum supported client</span></span><br/> | <span data-ttu-id="409e8-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="409e8-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="409e8-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="409e8-179">Minimum supported server</span></span><br/> | <span data-ttu-id="409e8-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="409e8-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="409e8-181">標頭</span><span class="sxs-lookup"><span data-stu-id="409e8-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="409e8-182"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="409e8-182"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="409e8-183">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="409e8-183">Type library</span></span><br/>             | <dl> <span data-ttu-id="409e8-184"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="409e8-184"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="409e8-185">DLL</span><span class="sxs-lookup"><span data-stu-id="409e8-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="409e8-186"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="409e8-186"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="409e8-187">CLSID</span><span class="sxs-lookup"><span data-stu-id="409e8-187">CLSID</span></span><br/>                    | <span data-ttu-id="409e8-188">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="409e8-188">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="409e8-189">IID</span><span class="sxs-lookup"><span data-stu-id="409e8-189">IID</span></span><br/>                      | <span data-ttu-id="409e8-190">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="409e8-190">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="409e8-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="409e8-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="409e8-192">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="409e8-192">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="409e8-193">**SWbemObject 參考\_**</span><span class="sxs-lookup"><span data-stu-id="409e8-193">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="409e8-194">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="409e8-194">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="409e8-195">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="409e8-195">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




