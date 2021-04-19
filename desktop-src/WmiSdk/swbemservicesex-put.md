---
description: 傳回 SWbemObjectPath 物件，其中包含寫入資料的物件路徑。
ms.assetid: 1a9a718d-875d-4102-9d9d-3d10be162f58
ms.tgt_platform: multiple
title: 'SWbemServicesEx： Put 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.Put
- ISWbemServicesEx.Put
- ISWbemServicesEx.Put
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e495a38262e6b6f7dd8b67424b74db74c025be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974597"
---
# <a name="swbemservicesexput-method"></a><span data-ttu-id="110a1-103">SWbemServicesEx Put 方法</span><span class="sxs-lookup"><span data-stu-id="110a1-103">SWbemServicesEx.Put method</span></span>

<span data-ttu-id="110a1-104">[**SWbemServicesEx**](swbemservicesex.md)物件的 **Put** 方法會將物件儲存至系結至物件的命名空間，並傳回 [**SWbemObjectPath**](swbemobjectpath.md)物件，其中包含寫入資料的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="110a1-104">The **Put** method of the [**SWbemServicesEx**](swbemservicesex.md) object saves the object to the namespace bound to the object and returns an [**SWbemObjectPath**](swbemobjectpath.md) object that contains the path of the object to which the data was written.</span></span>

<span data-ttu-id="110a1-105">這個方法會在半同步模式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="110a1-105">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="110a1-106">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="110a1-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="110a1-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="110a1-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="110a1-108">語法</span><span class="sxs-lookup"><span data-stu-id="110a1-108">Syntax</span></span>


```VB
objObjectPath = .Put( _
  ByVal objWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="110a1-109">參數</span><span class="sxs-lookup"><span data-stu-id="110a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="110a1-110">*objWbemObject*</span><span class="sxs-lookup"><span data-stu-id="110a1-110">*objWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="110a1-111">必要。</span><span class="sxs-lookup"><span data-stu-id="110a1-111">Required.</span></span> <span data-ttu-id="110a1-112">要放入命名空間中的新物件。</span><span class="sxs-lookup"><span data-stu-id="110a1-112">The new object to be put in the namespace.</span></span> <span data-ttu-id="110a1-113">這可以是新建立的物件或修改過的物件。</span><span class="sxs-lookup"><span data-stu-id="110a1-113">This can be either a newly created object or a modified object.</span></span>

</dd> <dt>

<span data-ttu-id="110a1-114">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="110a1-114">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="110a1-115">此參數會判斷呼叫是否建立或更新物件，以及呼叫是否立即傳回。</span><span class="sxs-lookup"><span data-stu-id="110a1-115">This parameter determines if the call creates or updates the object and if the call returns immediately.</span></span> <span data-ttu-id="110a1-116">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="110a1-116">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="110a1-117"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="110a1-117"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="110a1-118">如果沒有衍生類別且沒有該類別的實例，則允許更新類別。</span><span class="sxs-lookup"><span data-stu-id="110a1-118">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="110a1-119">如果變更僅限於不 (重要的辨識符號（例如， **描述** 辨識符號) ），也可以在所有情況下進行更新。</span><span class="sxs-lookup"><span data-stu-id="110a1-119">It also allows updates in all cases if the change is only to unimportant qualifiers (for example, the **Description** qualifier).</span></span> <span data-ttu-id="110a1-120">這是此呼叫的預設行為，而且會用於與舊版 WMI 的相容性。</span><span class="sxs-lookup"><span data-stu-id="110a1-120">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="110a1-121">如果類別有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="110a1-121">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="110a1-122"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="110a1-122"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="110a1-123">即使在有子類別時，也允許更新類別，但變更不會造成與子類別的任何衝突。</span><span class="sxs-lookup"><span data-stu-id="110a1-123">Allows updates of classes even if there are child classes, when the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="110a1-124">將新屬性加入至先前未在任何子類別中提及的基類時，您可以使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="110a1-124">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="110a1-125">如果類別有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="110a1-125">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="110a1-126"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40) ) </span><span class="sxs-lookup"><span data-stu-id="110a1-126"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="110a1-127">當有衝突的子類別存在時，此旗標會強制更新類別。</span><span class="sxs-lookup"><span data-stu-id="110a1-127">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="110a1-128">例如，此旗標會在子類別中定義類別限定詞時強制進行更新，而且基類會嘗試在與現有限定詞衝突的情況下加入相同的限定詞。</span><span class="sxs-lookup"><span data-stu-id="110a1-128">For example, this flag forces an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="110a1-129">在強制模式中，在子類別中刪除衝突的辨識符號，即可解決此衝突。</span><span class="sxs-lookup"><span data-stu-id="110a1-129">In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="110a1-130">如果類別有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="110a1-130">If the class has instances, the update fails.</span></span>

<span data-ttu-id="110a1-131">使用強制模式來更新靜態類別，會導致刪除該類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="110a1-131">The use of the force mode to update a static class causes the deletion of all instances of that class.</span></span> <span data-ttu-id="110a1-132">提供者類別的強制更新不會刪除類別的實例。</span><span class="sxs-lookup"><span data-stu-id="110a1-132">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="110a1-133"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="110a1-133"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="110a1-134">如果類別或實例不存在，則會加以建立，如果已經存在，則會予以覆寫。</span><span class="sxs-lookup"><span data-stu-id="110a1-134">Causes the class or instance to be created if it does not exist, or overwritten if it already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="110a1-135"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="110a1-135"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="110a1-136">僅用於建立。</span><span class="sxs-lookup"><span data-stu-id="110a1-136">Used for creation only.</span></span> <span data-ttu-id="110a1-137">如果類別或實例已經存在，呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="110a1-137">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="110a1-138"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="110a1-138"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="110a1-139">導致此呼叫只進行更新。</span><span class="sxs-lookup"><span data-stu-id="110a1-139">Causes this call to only do an update.</span></span> <span data-ttu-id="110a1-140">類別或實例必須存在，呼叫才能成功。</span><span class="sxs-lookup"><span data-stu-id="110a1-140">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="110a1-141"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="110a1-141"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="110a1-142">導致呼叫立即返回。</span><span class="sxs-lookup"><span data-stu-id="110a1-142">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="110a1-143"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="110a1-143"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="110a1-144">導致此呼叫封鎖，直到作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="110a1-144">Causes this call to block until the operation has completed.</span></span> <span data-ttu-id="110a1-145">此旗標會在同步模式中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="110a1-145">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="110a1-146"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="110a1-146"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="110a1-147">導致 WMI 撰寫類別修訂資料和基類定義。</span><span class="sxs-lookup"><span data-stu-id="110a1-147">Causes WMI to write class amendment data as well as the base class definition.</span></span> <span data-ttu-id="110a1-148">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="110a1-148">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="110a1-149">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="110a1-149">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="110a1-150">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="110a1-150">Typically, this is undefined.</span></span> <span data-ttu-id="110a1-151">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其專案代表服務要求的提供者可使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="110a1-151">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="110a1-152">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="110a1-152">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="110a1-153">傳回值</span><span class="sxs-lookup"><span data-stu-id="110a1-153">Return value</span></span>

<span data-ttu-id="110a1-154">如果呼叫成功，則會傳回 [**SWbemObjectPath**](swbemobjectpath.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="110a1-154">If the call is successful, an [**SWbemObjectPath**](swbemobjectpath.md) object is returned.</span></span> <span data-ttu-id="110a1-155">此物件包含已成功認可至 WMI 之實例或類別的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="110a1-155">This object contains the object path of the instance or class that has been successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="110a1-156">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="110a1-156">Error codes</span></span>

<span data-ttu-id="110a1-157">完成 **Put** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="110a1-157">After the completion of the **Put** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="110a1-158">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="110a1-158">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="110a1-159">目前的使用者沒有操作的許可權。</span><span class="sxs-lookup"><span data-stu-id="110a1-159">Current user does not have the permission for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="110a1-160">**wbemErrAlreadyExists** -2147749913 (0x80041019) </span><span class="sxs-lookup"><span data-stu-id="110a1-160">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="110a1-161">指定了 **wbemChangeFlagCreateOnly** 旗標，但該實例已經存在。</span><span class="sxs-lookup"><span data-stu-id="110a1-161">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="110a1-162">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="110a1-162">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="110a1-163">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="110a1-163">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="110a1-164">**wbemErrIllegalNull** -2147749898 (0x8004100A) </span><span class="sxs-lookup"><span data-stu-id="110a1-164">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="110a1-165">針對不能為 **null** 的屬性，指定了 **null** 值。</span><span class="sxs-lookup"><span data-stu-id="110a1-165">A value of **NULL** was specified for a property that cannot be **NULL**.</span></span> <span data-ttu-id="110a1-166">這類屬性的範例之一，是由 **索引**[**鍵**](standard-qualifiers.md)、索引或 **非 \_ Null** 的辨識符號標記。</span><span class="sxs-lookup"><span data-stu-id="110a1-166">An example of such a property is one marked by a [**Key**](standard-qualifiers.md), **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="110a1-167">**wbemErrInvalidObject** -2147749908 (0x80041014) </span><span class="sxs-lookup"><span data-stu-id="110a1-167">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="110a1-168">指定的物件無效。</span><span class="sxs-lookup"><span data-stu-id="110a1-168">The specified object is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="110a1-169">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="110a1-169">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="110a1-170">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="110a1-170">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="110a1-171">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="110a1-171">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="110a1-172">指定了 **wbemChangeFlagUpdateOnly** 旗標，但實例或類別不存在。</span><span class="sxs-lookup"><span data-stu-id="110a1-172">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="110a1-173">**wbemErrIncompleteClass** -2147749920 (0x80041020) </span><span class="sxs-lookup"><span data-stu-id="110a1-173">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="110a1-174">尚未設定類別的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="110a1-174">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="110a1-175">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="110a1-175">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="110a1-176">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="110a1-176">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="110a1-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="110a1-177">Requirements</span></span>



| <span data-ttu-id="110a1-178">需求</span><span class="sxs-lookup"><span data-stu-id="110a1-178">Requirement</span></span> | <span data-ttu-id="110a1-179">值</span><span class="sxs-lookup"><span data-stu-id="110a1-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="110a1-180">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="110a1-180">Minimum supported client</span></span><br/> | <span data-ttu-id="110a1-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="110a1-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="110a1-182">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="110a1-182">Minimum supported server</span></span><br/> | <span data-ttu-id="110a1-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="110a1-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="110a1-184">標頭</span><span class="sxs-lookup"><span data-stu-id="110a1-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="110a1-185"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="110a1-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="110a1-186">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="110a1-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="110a1-187"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="110a1-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="110a1-188">DLL</span><span class="sxs-lookup"><span data-stu-id="110a1-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="110a1-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="110a1-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="110a1-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="110a1-190">CLSID</span></span><br/>                    | <span data-ttu-id="110a1-191">CLSID \_ ISWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="110a1-191">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="110a1-192">IID</span><span class="sxs-lookup"><span data-stu-id="110a1-192">IID</span></span><br/>                      | <span data-ttu-id="110a1-193">IID \_ ISWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="110a1-193">IID\_ISWbemServicesEx</span></span><br/>                                                        |



 

 




