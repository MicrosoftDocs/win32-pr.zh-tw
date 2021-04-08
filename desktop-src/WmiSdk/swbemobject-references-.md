---
description: '\_SWbemObject 物件的 References 方法會傳回參考目前物件的所有關聯類別或實例的集合。'
ms.assetid: ba02da47-0bb2-40e1-af50-1c42b4be2abd
ms.tgt_platform: multiple
title: 'SWbemObject.References_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.References_
- ISWbemObject.References_
- ISWbemObject.References_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3349ff104a5f0730ee99735a230d265fffd1333f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852471"
---
# <a name="swbemobjectreferences_-method"></a><span data-ttu-id="eb65a-103">SWbemObject. References \_ 方法</span><span class="sxs-lookup"><span data-stu-id="eb65a-103">SWbemObject.References\_ method</span></span>

<span data-ttu-id="eb65a-104">[**SWbemObject**](swbemobject.md)物件的 **References \_** 方法會傳回參考目前物件的所有關聯類別或實例的集合。</span><span class="sxs-lookup"><span data-stu-id="eb65a-104">The **References\_** method of the [**SWbemObject**](swbemobject.md) object returns a collection of all association classes or instances that refer to the current object.</span></span>

<span data-ttu-id="eb65a-105">這個方法會執行與 WQL 查詢 [參考](references-of-statement.md) 相同的功能。</span><span class="sxs-lookup"><span data-stu-id="eb65a-105">This method performs the same function as the [REFERENCES OF](references-of-statement.md) WQL query.</span></span>

<span data-ttu-id="eb65a-106">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="eb65a-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb65a-107">語法</span><span class="sxs-lookup"><span data-stu-id="eb65a-107">Syntax</span></span>


```VB
objWbemObjectSet = .References_( _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="eb65a-108">參數</span><span class="sxs-lookup"><span data-stu-id="eb65a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb65a-109">*strResultClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="eb65a-109">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb65a-110">包含類別名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="eb65a-110">String that contains a class name.</span></span> <span data-ttu-id="eb65a-111">如果有指定，這個參數會指出傳回的關聯物件必須屬於或衍生自這個參數中指定的類別。</span><span class="sxs-lookup"><span data-stu-id="eb65a-111">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="eb65a-112">*strRole* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="eb65a-112">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb65a-113">包含屬性名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="eb65a-113">String that contains a property name.</span></span> <span data-ttu-id="eb65a-114">如果有指定，這個參數表示所傳回的關聯物件必須限制為來源物件扮演特定角色的物件。</span><span class="sxs-lookup"><span data-stu-id="eb65a-114">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="eb65a-115">角色是由指定之屬性的名稱所定義 (必須是關聯) 的參考屬性。</span><span class="sxs-lookup"><span data-stu-id="eb65a-115">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="eb65a-116">*bClassesOnly* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="eb65a-116">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb65a-117">布林值，指出是否應該傳回類別名稱清單，而不是類別的實際實例。</span><span class="sxs-lookup"><span data-stu-id="eb65a-117">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="eb65a-118">這些是關聯物件所屬的類別。</span><span class="sxs-lookup"><span data-stu-id="eb65a-118">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="eb65a-119">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="eb65a-119">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="eb65a-120">*bSchemaOnly* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="eb65a-120">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb65a-121">指出查詢是否適用于架構而非資料的布林值。</span><span class="sxs-lookup"><span data-stu-id="eb65a-121">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="eb65a-122">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="eb65a-122">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="eb65a-123">如果叫用此方法的物件為類別，則只能設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="eb65a-123">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="eb65a-124">當設為 **TRUE** 時，傳回的端點集會代表與架構中的來源類別適當相關聯的類別。</span><span class="sxs-lookup"><span data-stu-id="eb65a-124">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="eb65a-125">*strRequiredQualifier* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="eb65a-125">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb65a-126">包含辨識符號名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="eb65a-126">String that contains a qualifier name.</span></span> <span data-ttu-id="eb65a-127">如果有指定，這個參數會指出傳回的關聯物件必須包含指定的限定詞。</span><span class="sxs-lookup"><span data-stu-id="eb65a-127">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="eb65a-128">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="eb65a-128">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb65a-129">指定作業其他旗標的整數。</span><span class="sxs-lookup"><span data-stu-id="eb65a-129">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="eb65a-130">這個參數的預設值是 **wbemFlagReturnImmediately**，它會指示立即傳回呼叫，而不是等到查詢完成為止。</span><span class="sxs-lookup"><span data-stu-id="eb65a-130">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="eb65a-131">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="eb65a-131">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="eb65a-132"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="eb65a-132"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="eb65a-133">使順向列舉值傳回。</span><span class="sxs-lookup"><span data-stu-id="eb65a-133">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="eb65a-134">順向列舉值的速度通常會比傳統列舉值更快，且使用的記憶體較少，但不允許呼叫 [**SWbemObject。 \_**](swbemobject-clone-.md)</span><span class="sxs-lookup"><span data-stu-id="eb65a-134">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="eb65a-135"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="eb65a-135"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="eb65a-136">造成 Windows Management Instrumentation (WMI) 保留列舉物件的指標，直到用戶端釋放列舉值為止。</span><span class="sxs-lookup"><span data-stu-id="eb65a-136">Causes Windows Management Instrumentation (WMI) to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="eb65a-137"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="eb65a-137"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="eb65a-138">導致呼叫立即返回。</span><span class="sxs-lookup"><span data-stu-id="eb65a-138">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="eb65a-139"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="eb65a-139"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="eb65a-140">導致此呼叫封鎖，直到查詢完成為止。</span><span class="sxs-lookup"><span data-stu-id="eb65a-140">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="eb65a-141"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="eb65a-141"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="eb65a-142">讓 WMI 以基類定義傳回類別修訂資料。</span><span class="sxs-lookup"><span data-stu-id="eb65a-142">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="eb65a-143">如需修改過的限定詞的詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="eb65a-143">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="eb65a-144">*objwbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="eb65a-144">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb65a-145">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="eb65a-145">Typically, this is undefined.</span></span> <span data-ttu-id="eb65a-146">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="eb65a-146">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="eb65a-147">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="eb65a-147">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb65a-148">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb65a-148">Return value</span></span>

<span data-ttu-id="eb65a-149">如果呼叫成功，則會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="eb65a-149">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eb65a-150">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="eb65a-150">Error codes</span></span>

<span data-ttu-id="eb65a-151">在完成 **References \_** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="eb65a-151">After the completion of the **References\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="eb65a-152">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="eb65a-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="eb65a-153">目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="eb65a-153">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="eb65a-154">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="eb65a-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="eb65a-155">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb65a-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="eb65a-156">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="eb65a-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="eb65a-157">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="eb65a-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="eb65a-158">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="eb65a-158">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="eb65a-159">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="eb65a-159">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb65a-160">備註</span><span class="sxs-lookup"><span data-stu-id="eb65a-160">Remarks</span></span>

<span data-ttu-id="eb65a-161">如需相關 WQL 查詢、來源實例和關聯物件之參考的詳細資訊，請參閱 [語句 associators of](associators-of-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="eb65a-161">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb65a-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb65a-162">Requirements</span></span>



| <span data-ttu-id="eb65a-163">需求</span><span class="sxs-lookup"><span data-stu-id="eb65a-163">Requirement</span></span> | <span data-ttu-id="eb65a-164">值</span><span class="sxs-lookup"><span data-stu-id="eb65a-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb65a-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb65a-165">Minimum supported client</span></span><br/> | <span data-ttu-id="eb65a-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb65a-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb65a-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb65a-167">Minimum supported server</span></span><br/> | <span data-ttu-id="eb65a-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb65a-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb65a-169">標頭</span><span class="sxs-lookup"><span data-stu-id="eb65a-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb65a-170"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="eb65a-170"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb65a-171">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="eb65a-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb65a-172"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eb65a-172"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eb65a-173">DLL</span><span class="sxs-lookup"><span data-stu-id="eb65a-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb65a-174"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb65a-174"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb65a-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="eb65a-175">CLSID</span></span><br/>                    | <span data-ttu-id="eb65a-176">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="eb65a-176">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="eb65a-177">IID</span><span class="sxs-lookup"><span data-stu-id="eb65a-177">IID</span></span><br/>                      | <span data-ttu-id="eb65a-178">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="eb65a-178">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="eb65a-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb65a-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb65a-180">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="eb65a-180">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="eb65a-181">**SWbemObject. Associators of\_**</span><span class="sxs-lookup"><span data-stu-id="eb65a-181">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="eb65a-182">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="eb65a-182">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="eb65a-183">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="eb65a-183">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




