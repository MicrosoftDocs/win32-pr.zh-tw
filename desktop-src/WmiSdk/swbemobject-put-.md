---
description: SWbemObject 的 Put \_ 方法會建立或更新實例或類別物件，以 Windows Management Instrumentation (WMI) 。 在修改 SWbemObject 中的任何屬性或方法之後，您可以使用這個方法，而您的變更會寫入至 WMI。
ms.assetid: c636ff95-9f3e-4ba9-adf3-30b981be02a4
ms.tgt_platform: multiple
title: 'SWbemObject.Put_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Put_
- ISWbemObject.Put_
- ISWbemObject.Put_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9f5ca9b79c9def8f209da37e0ef1cfddefa0dbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976812"
---
# <a name="swbemobjectput_-method"></a><span data-ttu-id="2f19f-104">SWbemObject Put \_ 方法</span><span class="sxs-lookup"><span data-stu-id="2f19f-104">SWbemObject.Put\_ method</span></span>

<span data-ttu-id="2f19f-105">[**SWbemObject**](swbemobject.md)的 **Put \_** 方法會建立或更新實例或類別物件，以 Windows Management Instrumentation (WMI) 。</span><span class="sxs-lookup"><span data-stu-id="2f19f-105">The **Put\_** method of [**SWbemObject**](swbemobject.md) creates or updates an instance or a class object to Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="2f19f-106">在修改 **SWbemObject** 中的任何屬性或方法之後，您可以使用這個方法，而您的變更會寫入至 WMI。</span><span class="sxs-lookup"><span data-stu-id="2f19f-106">You can use this method after you modify any properties or methods in an **SWbemObject**, and your changes are written to WMI.</span></span>

<span data-ttu-id="2f19f-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="2f19f-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f19f-108">語法</span><span class="sxs-lookup"><span data-stu-id="2f19f-108">Syntax</span></span>


```VB
objObjectPath = .Put_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2f19f-109">參數</span><span class="sxs-lookup"><span data-stu-id="2f19f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f19f-110">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2f19f-110">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2f19f-111">此參數會判斷呼叫是否建立或更新類別或實例，以及呼叫是否立即傳回。</span><span class="sxs-lookup"><span data-stu-id="2f19f-111">This parameter determines if the call creates or updates the class or instance and if the call returns immediately.</span></span> <span data-ttu-id="2f19f-112">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="2f19f-112">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="2f19f-113"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="2f19f-113"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>\*\*\*\*wbemChangeFlagUpdateCompatible\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2f19f-114">如果沒有衍生類別且沒有該類別的實例，則允許更新類別。</span><span class="sxs-lookup"><span data-stu-id="2f19f-114">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="2f19f-115">如果變更只是不重要的辨識符號，也可以在所有情況下進行更新，例如 (的 **描述** 辨識符號) 。</span><span class="sxs-lookup"><span data-stu-id="2f19f-115">It also allows updates in all cases if the change is just to unimportant qualifiers (for example, the **Description** qualifier).</span></span> <span data-ttu-id="2f19f-116">這是此呼叫的預設行為，而且會用於與舊版 WMI 的相容性。</span><span class="sxs-lookup"><span data-stu-id="2f19f-116">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="2f19f-117">如果類別具有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="2f19f-117">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="2f19f-118"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode \* \* \* (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="2f19f-118"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>\*\*\*\*wbemChangeFlagUpdateSafeMode\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="2f19f-119">即使在變更不會造成與子類別的任何衝突時，仍可更新類別，即使有子類別也一樣。</span><span class="sxs-lookup"><span data-stu-id="2f19f-119">Allows updates of classes even if there are child classes if the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="2f19f-120">將新屬性加入至先前未在任何子類別中提及的基類時，您可以使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="2f19f-120">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="2f19f-121">如果類別具有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="2f19f-121">If the class has instances the update fails.</span></span> <span data-ttu-id="2f19f-122">如果類別具有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="2f19f-122">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="2f19f-123"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode \* \* \* (64 (0x40) ) </span><span class="sxs-lookup"><span data-stu-id="2f19f-123"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>\*\*\*\*WbemChangeFlagUpdateForceMode\*\*\*\* (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="2f19f-124">當有衝突的子類別存在時，此旗標會強制更新類別。</span><span class="sxs-lookup"><span data-stu-id="2f19f-124">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="2f19f-125">例如，此旗標會在子類別中定義類別限定詞時強制進行更新，而且基類會嘗試加入相同的辨識符號，並與現有的辨識符號發生衝突。</span><span class="sxs-lookup"><span data-stu-id="2f19f-125">For example, this flag will force an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier and in conflict with the existing one.</span></span> <span data-ttu-id="2f19f-126">在強制模式中，此衝突的解決方式是在子類別中刪除衝突的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="2f19f-126">In force mode this conflict would be resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="2f19f-127">如果類別具有實例，則更新將會失敗。</span><span class="sxs-lookup"><span data-stu-id="2f19f-127">If the class has instances the update will fail.</span></span>

<span data-ttu-id="2f19f-128">使用強制模式來更新靜態類別，會導致刪除該類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="2f19f-128">Using force mode to update a static class results in the deletion of all instances of that class.</span></span> <span data-ttu-id="2f19f-129">提供者類別的強制更新不會刪除類別的實例。</span><span class="sxs-lookup"><span data-stu-id="2f19f-129">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="2f19f-130"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="2f19f-130"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>\*\*\*\*wbemChangeFlagCreateOrUpdate\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2f19f-131">如果類別或實例已經存在，則會建立或覆寫。</span><span class="sxs-lookup"><span data-stu-id="2f19f-131">Causes the class or instance to be created if it does not exist or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="2f19f-132"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly \* \* \* (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="2f19f-132"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>\*\*\*\*wbemChangeFlagCreateOnly\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="2f19f-133">僅用於建立。</span><span class="sxs-lookup"><span data-stu-id="2f19f-133">Used for creation only.</span></span> <span data-ttu-id="2f19f-134">如果類別或實例已經存在，呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="2f19f-134">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="2f19f-135"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly \* \* \* (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="2f19f-135"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>\*\*\*\*wbemChangeFlagUpdateOnly\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="2f19f-136">導致此呼叫更新。</span><span class="sxs-lookup"><span data-stu-id="2f19f-136">Causes this call to update.</span></span> <span data-ttu-id="2f19f-137">類別或實例必須存在，呼叫才能成功。</span><span class="sxs-lookup"><span data-stu-id="2f19f-137">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="2f19f-138"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="2f19f-138"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="2f19f-139">導致呼叫立即返回。</span><span class="sxs-lookup"><span data-stu-id="2f19f-139">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="2f19f-140"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="2f19f-140"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2f19f-141">導致此呼叫封鎖，直到查詢完成為止。</span><span class="sxs-lookup"><span data-stu-id="2f19f-141">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="2f19f-142"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="2f19f-142"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="2f19f-143">導致 WMI 撰寫類別修訂資料和基類定義。</span><span class="sxs-lookup"><span data-stu-id="2f19f-143">Causes WMI to write class amendment data as well as the base class definition.</span></span> <span data-ttu-id="2f19f-144">如需修改過的限定詞的詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="2f19f-144">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2f19f-145">*objwbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2f19f-145">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2f19f-146">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="2f19f-146">Typically, this is undefined.</span></span> <span data-ttu-id="2f19f-147">否則，這會是 [**SWbemObjectPath**](swbemobjectpath.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="2f19f-147">Otherwise, this is an [**SWbemObjectPath**](swbemobjectpath.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="2f19f-148">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="2f19f-148">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f19f-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f19f-149">Return value</span></span>

<span data-ttu-id="2f19f-150">如果呼叫成功，則會傳回 [**SWbemObjectPath**](swbemobjectpath.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="2f19f-150">If the call is successful, an [**SWbemObjectPath**](swbemobjectpath.md) object is returned.</span></span> <span data-ttu-id="2f19f-151">此物件包含已成功認可至 WMI 之實例或類別的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="2f19f-151">This object contains the object path of the instance or class that has been successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2f19f-152">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2f19f-152">Error codes</span></span>

<span data-ttu-id="2f19f-153">完成 **Put \_** 方法之後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2f19f-153">After the completion of the **Put\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="2f19f-154">**wbemErrAccessDenied** -2147749891</span><span class="sxs-lookup"><span data-stu-id="2f19f-154">**wbemErrAccessDenied** - 2147749891</span></span>
</dt> <dd>

<span data-ttu-id="2f19f-155">目前的使用者沒有更新指定類別之實例的許可權。</span><span class="sxs-lookup"><span data-stu-id="2f19f-155">Current user does not have permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="2f19f-156">**wbemErrAlreadyExists** -2147749913 (0x80041019) </span><span class="sxs-lookup"><span data-stu-id="2f19f-156">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="2f19f-157">指定了 **wbemChangeFlagCreateOnly** 旗標，但該實例已經存在。</span><span class="sxs-lookup"><span data-stu-id="2f19f-157">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2f19f-158">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="2f19f-158">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2f19f-159">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2f19f-159">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="2f19f-160">**wbemErrIllegalNull** -2147749898 (0x8004100A) </span><span class="sxs-lookup"><span data-stu-id="2f19f-160">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="2f19f-161">未針對不是 **任何** 專案的屬性指定 **任何** 值。</span><span class="sxs-lookup"><span data-stu-id="2f19f-161">A value of **Nothing** was specified for a property that may not be **Nothing**.</span></span> <span data-ttu-id="2f19f-162">這類屬性的範例之一，是由索引 **鍵、** **索引** 或 **非 \_ Null** 的辨識符號標記。</span><span class="sxs-lookup"><span data-stu-id="2f19f-162">An example of such a property is one marked by a **Key,** **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="2f19f-163">**wbemErrInvalidObject** -2147749908 (0x80041014) </span><span class="sxs-lookup"><span data-stu-id="2f19f-163">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="2f19f-164">所指定的執行個體無效。</span><span class="sxs-lookup"><span data-stu-id="2f19f-164">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2f19f-165">**wbemErrInvalidParameter** -0x80041008</span><span class="sxs-lookup"><span data-stu-id="2f19f-165">**wbemErrInvalidParameter** - 0x80041008</span></span>
</dt> <dd>

<span data-ttu-id="2f19f-166">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="2f19f-166">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2f19f-167">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="2f19f-167">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="2f19f-168">指定了 **wbemChangeFlagUpdateOnly** 旗標，但實例或類別不存在。</span><span class="sxs-lookup"><span data-stu-id="2f19f-168">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="2f19f-169">**wbemErrIncompleteClass** -2147749920 (0x80041020) </span><span class="sxs-lookup"><span data-stu-id="2f19f-169">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="2f19f-170">尚未設定類別的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="2f19f-170">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="2f19f-171">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="2f19f-171">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="2f19f-172">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="2f19f-172">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f19f-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f19f-173">Requirements</span></span>



| <span data-ttu-id="2f19f-174">需求</span><span class="sxs-lookup"><span data-stu-id="2f19f-174">Requirement</span></span> | <span data-ttu-id="2f19f-175">值</span><span class="sxs-lookup"><span data-stu-id="2f19f-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f19f-176">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f19f-176">Minimum supported client</span></span><br/> | <span data-ttu-id="2f19f-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f19f-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f19f-178">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f19f-178">Minimum supported server</span></span><br/> | <span data-ttu-id="2f19f-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f19f-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f19f-180">標頭</span><span class="sxs-lookup"><span data-stu-id="2f19f-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f19f-181"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f19f-181"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f19f-182">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2f19f-182">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f19f-183"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2f19f-183"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2f19f-184">DLL</span><span class="sxs-lookup"><span data-stu-id="2f19f-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f19f-185"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f19f-185"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2f19f-186">CLSID</span><span class="sxs-lookup"><span data-stu-id="2f19f-186">CLSID</span></span><br/>                    | <span data-ttu-id="2f19f-187">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="2f19f-187">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="2f19f-188">IID</span><span class="sxs-lookup"><span data-stu-id="2f19f-188">IID</span></span><br/>                      | <span data-ttu-id="2f19f-189">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="2f19f-189">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="2f19f-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f19f-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f19f-191">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="2f19f-191">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="2f19f-192">**SWbemObjectPath 類別**</span><span class="sxs-lookup"><span data-stu-id="2f19f-192">**SWbemObjectPath.Class**</span></span>](swbemobjectpath-class.md)
</dt> <dt>

[<span data-ttu-id="2f19f-193">**Swbempropertyset**</span><span class="sxs-lookup"><span data-stu-id="2f19f-193">**SWbemProperty**</span></span>](swbemproperty.md)
</dt> <dt>

[<span data-ttu-id="2f19f-194">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="2f19f-194">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

