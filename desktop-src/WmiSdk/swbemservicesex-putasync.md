---
description: 以非同步方式將物件儲存到命名空間。 成功時，這個方法會將 OnCompleted 事件傳送至指定為輸入參數的 SWbemSink 物件。
ms.assetid: 27da0c60-6dae-482d-a9bf-1aab016d3ae8
ms.tgt_platform: multiple
title: 'SWbemServicesEx. PutAsync 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 06f470ed6f8cbd497ba3d3a3a77c5a8b4e5748c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027072"
---
# <a name="swbemservicesexputasync-method"></a><span data-ttu-id="d6895-104">SWbemServicesEx. PutAsync 方法</span><span class="sxs-lookup"><span data-stu-id="d6895-104">SWbemServicesEx.PutAsync method</span></span>

<span data-ttu-id="d6895-105">[**SWbemServicesEx**](swbemservicesex.md)物件的 **PutAsync** 方法會以非同步方式將物件儲存到命名空間。</span><span class="sxs-lookup"><span data-stu-id="d6895-105">The **PutAsync** method of the [**SWbemServicesEx**](swbemservicesex.md) object saves an object asynchronously to a namespace.</span></span> <span data-ttu-id="d6895-106">成功時，這個方法會將 [**OnCompleted**](swbemsink-oncompleted.md) 事件傳送至指定為輸入參數的 [**SWbemSink**](swbemsink.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d6895-106">When successful, this method sends an [**OnCompleted**](swbemsink-oncompleted.md) event to the [**SWbemSink**](swbemsink.md) object that is specified as an input parameter.</span></span>

<span data-ttu-id="d6895-107">在非同步模式中呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="d6895-107">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="d6895-108">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="d6895-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="d6895-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="d6895-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d6895-110">語法</span><span class="sxs-lookup"><span data-stu-id="d6895-110">Syntax</span></span>


```VB
SWbemServicesEx.PutAsync( _
  ByVal objWbemSink, _
  ByVal ojbWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d6895-111">參數</span><span class="sxs-lookup"><span data-stu-id="d6895-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6895-112">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="d6895-112">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="d6895-113">必要。</span><span class="sxs-lookup"><span data-stu-id="d6895-113">Required.</span></span> <span data-ttu-id="d6895-114">以非同步方式接收物件的物件接收。</span><span class="sxs-lookup"><span data-stu-id="d6895-114">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="d6895-115">建立 [**SWbemSink**](swbemsink.md) 物件以接收物件。</span><span class="sxs-lookup"><span data-stu-id="d6895-115">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="d6895-116">*ojbWbemObject*</span><span class="sxs-lookup"><span data-stu-id="d6895-116">*ojbWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="d6895-117">必要。</span><span class="sxs-lookup"><span data-stu-id="d6895-117">Required.</span></span> <span data-ttu-id="d6895-118">要放入命名空間中的新物件。</span><span class="sxs-lookup"><span data-stu-id="d6895-118">The new object to be put in the namespace.</span></span> <span data-ttu-id="d6895-119">這可能是新建立的物件或修改過的物件。</span><span class="sxs-lookup"><span data-stu-id="d6895-119">This may be a newly created object or a modified object.</span></span>

</dd> <dt>

<span data-ttu-id="d6895-120">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="d6895-120">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6895-121">此參數會決定呼叫是建立或更新物件，以及呼叫是否立即傳回。</span><span class="sxs-lookup"><span data-stu-id="d6895-121">This parameter determines whether the call creates or updates the object and whether the call returns immediately.</span></span> <span data-ttu-id="d6895-122">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="d6895-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="d6895-123"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="d6895-123"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d6895-124">允許在沒有衍生類別且沒有類別的實例時，更新類別。</span><span class="sxs-lookup"><span data-stu-id="d6895-124">Allows a class to be updated when there are no derived classes and no instances for the class.</span></span> <span data-ttu-id="d6895-125">當變更僅限於不重要的辨識符號（例如， **描述** 辨識符號）時，它也可讓您在所有情況下進行更新。</span><span class="sxs-lookup"><span data-stu-id="d6895-125">It also allows updates in all cases when the change is only to unimportant qualifiers, for example, the **Description** qualifier.</span></span> <span data-ttu-id="d6895-126">這是此呼叫的預設行為，而且會用於與舊版 WMI 的相容性。</span><span class="sxs-lookup"><span data-stu-id="d6895-126">This is the default behavior for this call, and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="d6895-127">如果類別有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="d6895-127">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="d6895-128"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="d6895-128"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="d6895-129">即使有子類別且變更不會導致與子類別發生衝突，還是允許更新類別。</span><span class="sxs-lookup"><span data-stu-id="d6895-129">Allows updates of classes even when there are child classes and the change does not cause conflicts with the child classes.</span></span> <span data-ttu-id="d6895-130">將新屬性加入至先前未在任何子類別中提及的基類時，請使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="d6895-130">Use this flag when adding a new property to a base class that is not mentioned previously in any of the child classes.</span></span> <span data-ttu-id="d6895-131">如果類別有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="d6895-131">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="d6895-132"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40) ) </span><span class="sxs-lookup"><span data-stu-id="d6895-132"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="d6895-133">當有衝突的子類別存在時，此旗標會強制更新類別。</span><span class="sxs-lookup"><span data-stu-id="d6895-133">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="d6895-134">例如，當類別限定詞在子類別中定義時，此旗標會強制進行更新，而且基類會嘗試在與現有的限定詞衝突時，加入相同的限定詞。</span><span class="sxs-lookup"><span data-stu-id="d6895-134">For example, this flag forces an update when a class qualifier is defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="d6895-135">在強制模式中，在子類別中刪除衝突的辨識符號，即可解決此衝突。</span><span class="sxs-lookup"><span data-stu-id="d6895-135">In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="d6895-136">如果類別有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="d6895-136">If the class has instances, the update fails.</span></span>

<span data-ttu-id="d6895-137">使用強制模式來更新靜態類別，會導致刪除該類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="d6895-137">The use of the force mode to update a static class causes the deletion of all instances of that class.</span></span> <span data-ttu-id="d6895-138">提供者類別的強制更新不會刪除類別的實例。</span><span class="sxs-lookup"><span data-stu-id="d6895-138">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="d6895-139"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="d6895-139"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d6895-140">如果類別或實例不存在，則會加以建立，如果已經存在，則會予以覆寫。</span><span class="sxs-lookup"><span data-stu-id="d6895-140">Causes the class or instance to be created if it does not exist, or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="d6895-141"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="d6895-141"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="d6895-142">僅用於建立。</span><span class="sxs-lookup"><span data-stu-id="d6895-142">Used for creation only.</span></span> <span data-ttu-id="d6895-143">如果類別或實例已經存在，呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="d6895-143">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="d6895-144"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="d6895-144"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="d6895-145">導致此呼叫更新。</span><span class="sxs-lookup"><span data-stu-id="d6895-145">Causes this call to update.</span></span> <span data-ttu-id="d6895-146">類別或實例必須存在，呼叫才能成功。</span><span class="sxs-lookup"><span data-stu-id="d6895-146">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="d6895-147"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="d6895-147"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="d6895-148">導致呼叫立即返回。</span><span class="sxs-lookup"><span data-stu-id="d6895-148">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="d6895-149"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="d6895-149"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d6895-150">導致此呼叫封鎖，直到查詢完成為止。</span><span class="sxs-lookup"><span data-stu-id="d6895-150">Causes this call to block until the query is complete.</span></span> <span data-ttu-id="d6895-151">此旗標會在同步模式中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="d6895-151">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="d6895-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="d6895-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="d6895-153">導致 WMI 撰寫類別修訂資料和基類定義。</span><span class="sxs-lookup"><span data-stu-id="d6895-153">Causes WMI to write class amendment data and the base class definition.</span></span> <span data-ttu-id="d6895-154">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="d6895-154">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d6895-155">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="d6895-155">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6895-156">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="d6895-156">Typically, this is undefined.</span></span> <span data-ttu-id="d6895-157">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其專案代表服務要求的提供者可使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="d6895-157">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="d6895-158">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="d6895-158">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="d6895-159">*objWbemAsyncCoNtext* \[選\]</span><span class="sxs-lookup"><span data-stu-id="d6895-159">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6895-160">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，這個物件會傳回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="d6895-160">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="d6895-161">使用這個參數可使用相同的物件接收進行多個非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="d6895-161">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="d6895-162">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="d6895-162">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="d6895-163">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="d6895-163">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="d6895-164">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="d6895-164">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6895-165">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6895-165">Return value</span></span>

<span data-ttu-id="d6895-166">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d6895-166">This method does not return a value.</span></span> <span data-ttu-id="d6895-167">如果呼叫成功，所提供之物件接收的 [**OnObjectPut**](swbemsink-onobjectput.md) 事件會接收 [**SWbemObjectPath**](swbemobjectpath.md) 物件，其中包含已成功認可至 WMI 之實例或類別的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="d6895-167">If the call is successful, the [**OnObjectPut**](swbemsink-onobjectput.md) event of the supplied object sink receives an [**SWbemObjectPath**](swbemobjectpath.md) object, which contains the object path of the instance or class that is successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d6895-168">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d6895-168">Error codes</span></span>

<span data-ttu-id="d6895-169">**PutAsync** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d6895-169">After the completion of the **PutAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d6895-170">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="d6895-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d6895-171">目前的使用者沒有更新指定類別之實例的許可權。</span><span class="sxs-lookup"><span data-stu-id="d6895-171">Current user does not have the permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="d6895-172">**wbemErrAlreadyExists** -2147749913 (0x80041019) </span><span class="sxs-lookup"><span data-stu-id="d6895-172">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="d6895-173">指定了 **wbemChangeFlagCreateOnly** 旗標，但該實例已經存在。</span><span class="sxs-lookup"><span data-stu-id="d6895-173">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d6895-174">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="d6895-174">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d6895-175">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d6895-175">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d6895-176">**wbemErrIllegalNull** -2147749898 (0x8004100A) </span><span class="sxs-lookup"><span data-stu-id="d6895-176">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="d6895-177">針對不能為 Null 的屬性，指定了 Null 值。</span><span class="sxs-lookup"><span data-stu-id="d6895-177">A value of Null was specified for a property that cannot be Null.</span></span> <span data-ttu-id="d6895-178">這類屬性的範例之一，是由 **索引\*\*\*\*鍵**、索引或 **非 \_ Null** 的辨識符號標記。</span><span class="sxs-lookup"><span data-stu-id="d6895-178">An example of such a property is one marked by a **Key**, **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d6895-179">**wbemErrInvalidObject** -2147749908 (0x80041014) </span><span class="sxs-lookup"><span data-stu-id="d6895-179">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="d6895-180">所指定的執行個體無效。</span><span class="sxs-lookup"><span data-stu-id="d6895-180">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d6895-181">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="d6895-181">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d6895-182">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="d6895-182">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d6895-183">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="d6895-183">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="d6895-184">指定了 **wbemChangeFlagUpdateOnly** 旗標，但實例或類別不存在。</span><span class="sxs-lookup"><span data-stu-id="d6895-184">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="d6895-185">**wbemErrIncompleteClass** -2147749920 (0x80041020) </span><span class="sxs-lookup"><span data-stu-id="d6895-185">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="d6895-186">尚未設定類別的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="d6895-186">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="d6895-187">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="d6895-187">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d6895-188">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="d6895-188">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6895-189">備註</span><span class="sxs-lookup"><span data-stu-id="d6895-189">Remarks</span></span>

<span data-ttu-id="d6895-190">這個呼叫會立即傳回，而結果和狀態會透過傳遞給 *objWbemSink* 中指定之接收的事件傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="d6895-190">This call returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d6895-191">若要在每個物件抵達時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。</span><span class="sxs-lookup"><span data-stu-id="d6895-191">To handle each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="d6895-192">在所有物件抵達之後完成的任何處理，都是在 *objWbemSink* 的副程式中完成。[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="d6895-192">Any processing done after all the objects arrive is done in a subroutine for the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="d6895-193">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="d6895-193">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="d6895-194">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="d6895-194">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="d6895-195">若要消除風險，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="d6895-195">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6895-196">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6895-196">Requirements</span></span>



| <span data-ttu-id="d6895-197">需求</span><span class="sxs-lookup"><span data-stu-id="d6895-197">Requirement</span></span> | <span data-ttu-id="d6895-198">值</span><span class="sxs-lookup"><span data-stu-id="d6895-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6895-199">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6895-199">Minimum supported client</span></span><br/> | <span data-ttu-id="d6895-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6895-200">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6895-201">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6895-201">Minimum supported server</span></span><br/> | <span data-ttu-id="d6895-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6895-202">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6895-203">標頭</span><span class="sxs-lookup"><span data-stu-id="d6895-203">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6895-204"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="d6895-204"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6895-205">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d6895-205">Type library</span></span><br/>             | <dl> <span data-ttu-id="d6895-206"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d6895-206"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d6895-207">DLL</span><span class="sxs-lookup"><span data-stu-id="d6895-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6895-208"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6895-208"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d6895-209">CLSID</span><span class="sxs-lookup"><span data-stu-id="d6895-209">CLSID</span></span><br/>                    | <span data-ttu-id="d6895-210">CLSID \_ ISWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="d6895-210">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="d6895-211">IID</span><span class="sxs-lookup"><span data-stu-id="d6895-211">IID</span></span><br/>                      | <span data-ttu-id="d6895-212">IID \_ ISWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="d6895-212">IID\_ISWbemServicesEx</span></span><br/>                                                        |



 

