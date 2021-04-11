---
description: 傳回參考特定來源類別或實例的所有關聯類別或實例的集合。
ms.assetid: 33425b1c-13f5-4c3d-8f8a-2922f3e95264
ms.tgt_platform: multiple
title: 'SWbemServices. ReferencesTo 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73addea189815d1594d0963fbdd6e20c562b3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115797"
---
# <a name="swbemservicesreferencesto-method"></a><span data-ttu-id="0b477-103">SWbemServices. ReferencesTo 方法</span><span class="sxs-lookup"><span data-stu-id="0b477-103">SWbemServices.ReferencesTo method</span></span>

<span data-ttu-id="0b477-104">[**SWbemServices**](swbemservices.md)物件的 **ReferencesTo** 方法會傳回參考特定來源類別或實例之所有關聯類別或實例的集合。</span><span class="sxs-lookup"><span data-stu-id="0b477-104">The **ReferencesTo** method of the [**SWbemServices**](swbemservices.md) object returns a collection of all association classes or instances that refer to a specific source class or instance.</span></span> <span data-ttu-id="0b477-105">這個方法會執行 WQL 查詢 [參考](references-of-statement.md) 所執行的相同函數。</span><span class="sxs-lookup"><span data-stu-id="0b477-105">This method performs the same function that the [REFERENCES OF](references-of-statement.md) WQL query performs.</span></span>

<span data-ttu-id="0b477-106">這個方法會在半同步模式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="0b477-106">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="0b477-107">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="0b477-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="0b477-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="0b477-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b477-109">語法</span><span class="sxs-lookup"><span data-stu-id="0b477-109">Syntax</span></span>


```VB
objWbemObjectSet = .ReferencesTo( _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0b477-110">參數</span><span class="sxs-lookup"><span data-stu-id="0b477-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b477-111">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="0b477-111">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="0b477-112">必要。</span><span class="sxs-lookup"><span data-stu-id="0b477-112">Required.</span></span> <span data-ttu-id="0b477-113">字串，包含此方法之來源的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="0b477-113">String that contains the object path of the source for this method.</span></span> <span data-ttu-id="0b477-114">如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="0b477-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b477-115">*strResultClass* \[選\]</span><span class="sxs-lookup"><span data-stu-id="0b477-115">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b477-116">包含類別名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="0b477-116">String that contains a class name.</span></span> <span data-ttu-id="0b477-117">如果有指定，這個參數會指出傳回的關聯物件必須屬於或衍生自此參數中指定的類別。</span><span class="sxs-lookup"><span data-stu-id="0b477-117">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class that is specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0b477-118">*strRole* \[選\]</span><span class="sxs-lookup"><span data-stu-id="0b477-118">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b477-119">包含屬性名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="0b477-119">String that contains a property name.</span></span> <span data-ttu-id="0b477-120">如果有指定，這個參數表示所傳回的關聯物件必須限制為來源物件扮演特定角色的物件。</span><span class="sxs-lookup"><span data-stu-id="0b477-120">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="0b477-121">角色是由指定之屬性的名稱所定義 (必須是關聯) 的參考屬性。</span><span class="sxs-lookup"><span data-stu-id="0b477-121">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="0b477-122">*bClassesOnly* \[選\]</span><span class="sxs-lookup"><span data-stu-id="0b477-122">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b477-123">布林值，指出是否應該傳回類別名稱清單，而不是類別的實際實例。</span><span class="sxs-lookup"><span data-stu-id="0b477-123">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="0b477-124">這些是關聯物件所屬的類別。</span><span class="sxs-lookup"><span data-stu-id="0b477-124">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="0b477-125">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0b477-125">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0b477-126">*bSchemaOnly* \[選\]</span><span class="sxs-lookup"><span data-stu-id="0b477-126">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b477-127">指出查詢是否適用于架構而非資料的布林值。</span><span class="sxs-lookup"><span data-stu-id="0b477-127">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="0b477-128">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0b477-128">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="0b477-129">如果 *strObjectPath* 參數指定類別的物件路徑，它只能設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="0b477-129">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="0b477-130">當設為 **TRUE** 時，傳回的端點集會代表與架構中的來源類別適當相關聯的類別。</span><span class="sxs-lookup"><span data-stu-id="0b477-130">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="0b477-131">*strRequiredQualifier* \[選\]</span><span class="sxs-lookup"><span data-stu-id="0b477-131">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b477-132">包含辨識符號名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="0b477-132">String that contains a qualifier name.</span></span> <span data-ttu-id="0b477-133">如果有指定，這個參數會指出傳回的關聯物件必須包含指定的限定詞。</span><span class="sxs-lookup"><span data-stu-id="0b477-133">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="0b477-134">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="0b477-134">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b477-135">指定運算其他旗標的整數。</span><span class="sxs-lookup"><span data-stu-id="0b477-135">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="0b477-136">這個參數的預設值是 **wbemFlagReturnImmediately**，它會指示立即傳回呼叫，而不是等到查詢完成為止。</span><span class="sxs-lookup"><span data-stu-id="0b477-136">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="0b477-137">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="0b477-137">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="0b477-138"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="0b477-138"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="0b477-139">使順向列舉值傳回。</span><span class="sxs-lookup"><span data-stu-id="0b477-139">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="0b477-140">順向列舉值的速度通常會比傳統列舉值更快，且使用的記憶體較少，但不允許呼叫 [**SWbemObject。 \_**](swbemobject-clone-.md)</span><span class="sxs-lookup"><span data-stu-id="0b477-140">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="0b477-141"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="0b477-141"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0b477-142">造成 Windows Management Instrumentation (WMI) 保留列舉物件的指標，直到用戶端釋放列舉值為止。</span><span class="sxs-lookup"><span data-stu-id="0b477-142">Causes Windows Management Instrumentation (WMI) to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="0b477-143"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="0b477-143"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="0b477-144">導致呼叫立即返回。</span><span class="sxs-lookup"><span data-stu-id="0b477-144">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="0b477-145"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="0b477-145"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0b477-146">導致此呼叫封鎖，直到查詢完成為止。</span><span class="sxs-lookup"><span data-stu-id="0b477-146">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="0b477-147">此旗標會在同步模式中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="0b477-147">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="0b477-148"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="0b477-148"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="0b477-149">導致 WMI 傳回類別修訂資料以及基類定義。</span><span class="sxs-lookup"><span data-stu-id="0b477-149">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="0b477-150">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="0b477-150">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0b477-151">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="0b477-151">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b477-152">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="0b477-152">Typically, this is undefined.</span></span> <span data-ttu-id="0b477-153">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="0b477-153">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="0b477-154">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="0b477-154">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b477-155">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b477-155">Return value</span></span>

<span data-ttu-id="0b477-156">如果方法成功，則方法會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="0b477-156">If the method is successful, the method returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0b477-157">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0b477-157">Error codes</span></span>

<span data-ttu-id="0b477-158">**ReferencesTo** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0b477-158">After the completion of the **ReferencesTo** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="0b477-159">具有零個元素的傳回集合不是錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b477-159">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="0b477-160">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="0b477-160">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="0b477-161">目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="0b477-161">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="0b477-162">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="0b477-162">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="0b477-163">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b477-163">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="0b477-164">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="0b477-164">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="0b477-165">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="0b477-165">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="0b477-166">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="0b477-166">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="0b477-167">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="0b477-167">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0b477-168">**wbemFlagUseAmendedQualifiers** -131072 (0x20000) </span><span class="sxs-lookup"><span data-stu-id="0b477-168">**wbemFlagUseAmendedQualifiers** - 131072 (0x20000)</span></span>
</dt> <dd>

<span data-ttu-id="0b477-169">讓 WMI 以基類定義傳回類別修訂資料。</span><span class="sxs-lookup"><span data-stu-id="0b477-169">Causes WMI to return class amendment data with the base class definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b477-170">備註</span><span class="sxs-lookup"><span data-stu-id="0b477-170">Remarks</span></span>

<span data-ttu-id="0b477-171">如需相關 WQL 查詢、來源實例和關聯物件之參考的詳細資訊，請參閱 [語句 associators of](associators-of-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="0b477-171">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b477-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b477-172">Requirements</span></span>



| <span data-ttu-id="0b477-173">需求</span><span class="sxs-lookup"><span data-stu-id="0b477-173">Requirement</span></span> | <span data-ttu-id="0b477-174">值</span><span class="sxs-lookup"><span data-stu-id="0b477-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b477-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b477-175">Minimum supported client</span></span><br/> | <span data-ttu-id="0b477-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b477-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b477-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b477-177">Minimum supported server</span></span><br/> | <span data-ttu-id="0b477-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b477-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b477-179">標頭</span><span class="sxs-lookup"><span data-stu-id="0b477-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b477-180"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="0b477-180"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b477-181">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0b477-181">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b477-182"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0b477-182"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0b477-183">DLL</span><span class="sxs-lookup"><span data-stu-id="0b477-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b477-184"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b477-184"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0b477-185">CLSID</span><span class="sxs-lookup"><span data-stu-id="0b477-185">CLSID</span></span><br/>                    | <span data-ttu-id="0b477-186">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="0b477-186">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="0b477-187">IID</span><span class="sxs-lookup"><span data-stu-id="0b477-187">IID</span></span><br/>                      | <span data-ttu-id="0b477-188">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="0b477-188">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="0b477-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b477-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b477-190">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="0b477-190">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="0b477-191">**SWbemObject. Associators of\_**</span><span class="sxs-lookup"><span data-stu-id="0b477-191">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="0b477-192">**SWbemObject 參考\_**</span><span class="sxs-lookup"><span data-stu-id="0b477-192">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="0b477-193">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="0b477-193">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> </dl>

 

 




