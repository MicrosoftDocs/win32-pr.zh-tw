---
description: SWbemServices. AssociatorsOf 方法-傳回 (類別或實例的集合，) 名為與指定物件相關聯的端點。
ms.assetid: a78e6701-6779-4a02-b811-23b2da4f4167
ms.tgt_platform: multiple
title: 'SWbemServices. AssociatorsOf 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 95dc8e16939c345b6f885980dd2f1194f180ac5e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103686"
---
# <a name="swbemservicesassociatorsof-method"></a><span data-ttu-id="b5be4-103">SWbemServices. AssociatorsOf 方法</span><span class="sxs-lookup"><span data-stu-id="b5be4-103">SWbemServices.AssociatorsOf method</span></span>

<span data-ttu-id="b5be4-104">[**SWbemServices**](swbemservices.md)物件的 **AssociatorsOf** 方法會傳回物件的集合， (類別或實例) 稱為與指定物件相關聯的端點。</span><span class="sxs-lookup"><span data-stu-id="b5be4-104">The **AssociatorsOf** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="b5be4-105">這個方法會執行 WQL 查詢 ASSOCIATORS OF 所執行的相同功能。</span><span class="sxs-lookup"><span data-stu-id="b5be4-105">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="b5be4-106">依預設，會在 [半同步模式] 中呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="b5be4-106">This method is called in the semisynchronous mode by default.</span></span> <span data-ttu-id="b5be4-107">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="b5be4-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="b5be4-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="b5be4-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b5be4-109">語法</span><span class="sxs-lookup"><span data-stu-id="b5be4-109">Syntax</span></span>


```VB
objWbemObjectSet = .AssociatorsOf( _
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
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b5be4-110">參數</span><span class="sxs-lookup"><span data-stu-id="b5be4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5be4-111">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="b5be4-111">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="b5be4-112">必要。</span><span class="sxs-lookup"><span data-stu-id="b5be4-112">Required.</span></span> <span data-ttu-id="b5be4-113">字串，包含來源類別或實例的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="b5be4-113">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="b5be4-114">如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="b5be4-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5be4-115">*strAssocClass* \[選\]</span><span class="sxs-lookup"><span data-stu-id="b5be4-115">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-116">包含關聯類別的字串。</span><span class="sxs-lookup"><span data-stu-id="b5be4-116">String that contains an association class.</span></span> <span data-ttu-id="b5be4-117">如果有指定，這個參數表示傳回的端點必須透過指定的關聯類別或衍生自這個關聯類別的類別，與來源產生關聯。</span><span class="sxs-lookup"><span data-stu-id="b5be4-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class that is derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="b5be4-118">*strResultClass* \[選\]</span><span class="sxs-lookup"><span data-stu-id="b5be4-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-119">包含類別名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="b5be4-119">String that contains a class name.</span></span> <span data-ttu-id="b5be4-120">如果有指定，此選擇性參數表示傳回的端點必須屬於或衍生自此參數中指定的類別。</span><span class="sxs-lookup"><span data-stu-id="b5be4-120">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b5be4-121">*strResultRole* \[選\]</span><span class="sxs-lookup"><span data-stu-id="b5be4-121">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-122">包含屬性名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="b5be4-122">String that contains a property name.</span></span> <span data-ttu-id="b5be4-123">如果有指定，這個參數表示傳回的端點必須在其與來源物件的關聯中扮演特定的角色。</span><span class="sxs-lookup"><span data-stu-id="b5be4-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="b5be4-124">角色是由指定之屬性的名稱所定義 (必須是關聯) 的參考屬性。</span><span class="sxs-lookup"><span data-stu-id="b5be4-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="b5be4-125">*strRole* \[選\]</span><span class="sxs-lookup"><span data-stu-id="b5be4-125">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-126">包含屬性名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="b5be4-126">String that contains a property name.</span></span> <span data-ttu-id="b5be4-127">如果有指定，這個參數會指出傳回的端點必須參與來源物件的關聯，其中來源物件會扮演特定的角色。</span><span class="sxs-lookup"><span data-stu-id="b5be4-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="b5be4-128">角色是由指定之屬性的名稱所定義 (必須是關聯) 的參考屬性。</span><span class="sxs-lookup"><span data-stu-id="b5be4-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="b5be4-129">*bClassesOnly* \[選\]</span><span class="sxs-lookup"><span data-stu-id="b5be4-129">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-130">布林值，指出是否應該傳回類別名稱的清單，而不是類別的實際實例。</span><span class="sxs-lookup"><span data-stu-id="b5be4-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="b5be4-131">這些是端點實例所屬的類別。</span><span class="sxs-lookup"><span data-stu-id="b5be4-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="b5be4-132">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b5be4-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b5be4-133">*bSchemaOnly* \[選\]</span><span class="sxs-lookup"><span data-stu-id="b5be4-133">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-134">指出查詢是否適用于架構而非資料的布林值。</span><span class="sxs-lookup"><span data-stu-id="b5be4-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="b5be4-135">此參數的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b5be4-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="b5be4-136">如果 *strObjectPath* 參數指定類別的物件路徑，它只能設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="b5be4-136">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="b5be4-137">當設為 **TRUE** 時，傳回的端點集會代表與架構中的來源類別適當相關聯的類別。</span><span class="sxs-lookup"><span data-stu-id="b5be4-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="b5be4-138">*strRequiredAssocQualifier* \[選\]</span><span class="sxs-lookup"><span data-stu-id="b5be4-138">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-139">包含辨識符號名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="b5be4-139">String that contains a qualifier name.</span></span> <span data-ttu-id="b5be4-140">如果有指定，這個參數會指出傳回的端點必須透過包含指定限定詞的關聯類別，與來源物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="b5be4-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b5be4-141">*strRequiredQualifier* \[選\]</span><span class="sxs-lookup"><span data-stu-id="b5be4-141">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-142">包含辨識符號名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="b5be4-142">String that contains a qualifier name.</span></span> <span data-ttu-id="b5be4-143">如果有指定，這個參數會指出傳回的端點必須包含指定的限定詞。</span><span class="sxs-lookup"><span data-stu-id="b5be4-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b5be4-144">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="b5be4-144">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-145">指定運算其他旗標的整數。</span><span class="sxs-lookup"><span data-stu-id="b5be4-145">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="b5be4-146">這個參數的預設值是 **wbemFlagReturnImmediately**，它會以半同步模式呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="b5be4-146">The default value for this parameter is **wbemFlagReturnImmediately**, which calls the method in the semisynchronous mode.</span></span> <span data-ttu-id="b5be4-147">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="b5be4-147">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="b5be4-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="b5be4-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="b5be4-149">使順向列舉值傳回。</span><span class="sxs-lookup"><span data-stu-id="b5be4-149">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="b5be4-150">順向列舉值的速度通常會比傳統列舉值更快，且使用的記憶體較少，但不允許呼叫 [**SWbemObject。 \_**](swbemobject-clone-.md)</span><span class="sxs-lookup"><span data-stu-id="b5be4-150">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="b5be4-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="b5be4-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b5be4-152">讓 WMI 保留列舉物件的指標，直到用戶端釋放列舉值為止。</span><span class="sxs-lookup"><span data-stu-id="b5be4-152">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="b5be4-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="b5be4-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="b5be4-154">導致呼叫立即返回。</span><span class="sxs-lookup"><span data-stu-id="b5be4-154">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="b5be4-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="b5be4-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b5be4-156">導致此呼叫封鎖，直到查詢完成為止。</span><span class="sxs-lookup"><span data-stu-id="b5be4-156">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="b5be4-157">此旗標會以同步模式呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="b5be4-157">This flag calls the method in synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="b5be4-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="b5be4-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b5be4-159">導致 WMI 傳回類別修訂資料以及基類定義。</span><span class="sxs-lookup"><span data-stu-id="b5be4-159">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="b5be4-160">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="b5be4-160">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b5be4-161">*objwbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="b5be4-161">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-162">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="b5be4-162">Typically, this is undefined.</span></span> <span data-ttu-id="b5be4-163">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="b5be4-163">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="b5be4-164">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="b5be4-164">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5be4-165">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5be4-165">Return value</span></span>

<span data-ttu-id="b5be4-166">如果呼叫成功，則會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b5be4-166">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b5be4-167">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b5be4-167">Error codes</span></span>

<span data-ttu-id="b5be4-168">**AssociatorsOf** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b5be4-168">After the completion of the **AssociatorsOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="b5be4-169">具有零個元素的傳回集合不是錯誤。</span><span class="sxs-lookup"><span data-stu-id="b5be4-169">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="b5be4-170">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="b5be4-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-171">目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="b5be4-171">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="b5be4-172">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="b5be4-172">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-173">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b5be4-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b5be4-174">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="b5be4-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-175">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="b5be4-175">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="b5be4-176">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="b5be4-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-177">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="b5be4-177">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b5be4-178">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="b5be4-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="b5be4-179">找不到要求的專案。</span><span class="sxs-lookup"><span data-stu-id="b5be4-179">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5be4-180">備註</span><span class="sxs-lookup"><span data-stu-id="b5be4-180">Remarks</span></span>

<span data-ttu-id="b5be4-181">方法會透過一或多個關聯類別，取得與指定之資源相關聯之 managed 資源的實例。</span><span class="sxs-lookup"><span data-stu-id="b5be4-181">The method retrieves the instances of managed resources that are associated with a specified resource through one or more association classes.</span></span> <span data-ttu-id="b5be4-182">您會提供原始端點的物件路徑，而 AssociatorsOf 會傳回相對端點的 managed 資源。</span><span class="sxs-lookup"><span data-stu-id="b5be4-182">You provide the object path for the originating endpoint, and AssociatorsOf returns the managed resources at the opposite endpoint.</span></span> <span data-ttu-id="b5be4-183">AssociatorsOf 方法會執行 WQL 查詢 ASSOCIATORS OF 所執行的相同功能。</span><span class="sxs-lookup"><span data-stu-id="b5be4-183">The AssociatorsOf method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="b5be4-184">如需 WQL 查詢、來源實例和端點 ASSOCIATORS OF 的詳細資訊，請參閱 [語句 associators of](associators-of-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="b5be4-184">For more information about the ASSOCIATORS OF WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5be4-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5be4-185">Requirements</span></span>



| <span data-ttu-id="b5be4-186">需求</span><span class="sxs-lookup"><span data-stu-id="b5be4-186">Requirement</span></span> | <span data-ttu-id="b5be4-187">值</span><span class="sxs-lookup"><span data-stu-id="b5be4-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5be4-188">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5be4-188">Minimum supported client</span></span><br/> | <span data-ttu-id="b5be4-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5be4-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5be4-190">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5be4-190">Minimum supported server</span></span><br/> | <span data-ttu-id="b5be4-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5be4-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5be4-192">標頭</span><span class="sxs-lookup"><span data-stu-id="b5be4-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5be4-193"><dt>>Wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="b5be4-193"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5be4-194">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b5be4-194">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5be4-195"><dt>>Wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b5be4-195"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b5be4-196">DLL</span><span class="sxs-lookup"><span data-stu-id="b5be4-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5be4-197"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5be4-197"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b5be4-198">CLSID</span><span class="sxs-lookup"><span data-stu-id="b5be4-198">CLSID</span></span><br/>                    | <span data-ttu-id="b5be4-199">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="b5be4-199">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="b5be4-200">IID</span><span class="sxs-lookup"><span data-stu-id="b5be4-200">IID</span></span><br/>                      | <span data-ttu-id="b5be4-201">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="b5be4-201">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b5be4-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5be4-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5be4-203">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="b5be4-203">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="b5be4-204">**SWbemObject. Associators of\_**</span><span class="sxs-lookup"><span data-stu-id="b5be4-204">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="b5be4-205">**SWbemObject. AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="b5be4-205">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="b5be4-206">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="b5be4-206">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="b5be4-207">**SWbemObject 參考\_**</span><span class="sxs-lookup"><span data-stu-id="b5be4-207">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="b5be4-208">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="b5be4-208">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




