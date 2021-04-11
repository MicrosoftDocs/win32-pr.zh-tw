---
description: SWbemObject 的 PutAsync 方法會以 \_ 非同步方式建立或更新實例或類別物件，以 Windows Management Instrumentation (WMI) 。
ms.assetid: ff738412-fcca-4e4a-a178-0d1d391ec99b
ms.tgt_platform: multiple
title: 'SWbemObject.PutAsync_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.PutAsync_
- ISWbemObject.PutAsync_
- ISWbemObject.PutAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3530c3883763773f53bec81aeee8b0d199170133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195048"
---
# <a name="swbemobjectputasync_-method"></a><span data-ttu-id="c20da-103">SWbemObject. PutAsync \_ 方法</span><span class="sxs-lookup"><span data-stu-id="c20da-103">SWbemObject.PutAsync\_ method</span></span>

<span data-ttu-id="c20da-104">[**SWbemObject**](swbemobject.md)的 **PutAsync \_** 方法會以非同步方式建立或更新實例或類別物件，以 Windows Management Instrumentation (WMI) 。</span><span class="sxs-lookup"><span data-stu-id="c20da-104">The **PutAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously creates or updates an instance or class object to Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="c20da-105">在修改 **SWbemObject** 中的任何屬性或方法之後，您可以使用這個方法，而您的變更會寫入至 WMI。</span><span class="sxs-lookup"><span data-stu-id="c20da-105">You can use this method after you modify any properties or methods in **SWbemObject**, and your changes are written to WMI.</span></span>

<span data-ttu-id="c20da-106">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="c20da-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c20da-107">語法</span><span class="sxs-lookup"><span data-stu-id="c20da-107">Syntax</span></span>


```VB
SWbemObject.PutAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c20da-108">參數</span><span class="sxs-lookup"><span data-stu-id="c20da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c20da-109">*objWbemSink* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c20da-109">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20da-110">必要。</span><span class="sxs-lookup"><span data-stu-id="c20da-110">Required.</span></span> <span data-ttu-id="c20da-111">以非同步方式接收 **put** 運算結果的物件接收。</span><span class="sxs-lookup"><span data-stu-id="c20da-111">Object sink that asynchronously receives the result of the **put** operation.</span></span>

</dd> <dt>

<span data-ttu-id="c20da-112">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c20da-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c20da-113">判斷呼叫是否建立或更新類別或實例，以及呼叫是否立即傳回。</span><span class="sxs-lookup"><span data-stu-id="c20da-113">Determines if the call creates or updates the class or instance and if the call returns immediately.</span></span> <span data-ttu-id="c20da-114">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="c20da-114">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="c20da-115"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="c20da-115"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>\*\*\*\*wbemChangeFlagUpdateCompatible\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c20da-116">如果沒有衍生類別且沒有該類別的實例，則允許更新類別。</span><span class="sxs-lookup"><span data-stu-id="c20da-116">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="c20da-117">如果變更僅限於不重要的辨識符號 (（例如 **描述** 辨識符號) ），它也可讓您在所有情況下進行更新。</span><span class="sxs-lookup"><span data-stu-id="c20da-117">It also allows updates in all cases if the change is just to unimportant qualifiers (for example the **Description** qualifier).</span></span> <span data-ttu-id="c20da-118">這是此呼叫的預設行為，而且會用於與舊版 WMI 的相容性。</span><span class="sxs-lookup"><span data-stu-id="c20da-118">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="c20da-119">如果類別具有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="c20da-119">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="c20da-120"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode \* \* \* (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="c20da-120"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>\*\*\*\*wbemChangeFlagUpdateSafeMode\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="c20da-121">即使有子類別，也允許更新類別，如果變更不會導致與子類別發生衝突。</span><span class="sxs-lookup"><span data-stu-id="c20da-121">Allows updates of classes, even if there are child classes, if the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="c20da-122">將新屬性加入至先前未在任何子類別中提及的基類時，您可以使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="c20da-122">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="c20da-123">如果類別具有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="c20da-123">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="c20da-124"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode \* \* \* (64 (0x40) ) </span><span class="sxs-lookup"><span data-stu-id="c20da-124"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>\*\*\*\*WbemChangeFlagUpdateForceMode\*\*\*\* (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="c20da-125">存在衝突的子類別時，強制更新類別。</span><span class="sxs-lookup"><span data-stu-id="c20da-125">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="c20da-126">例如，此旗標會在子類別中定義類別限定詞時強制進行更新，而且基類會嘗試在與現有限定詞衝突的情況下加入相同的限定詞。</span><span class="sxs-lookup"><span data-stu-id="c20da-126">For example, this flag forces an update if a class qualifier was defined in a child class, and the base class attempts to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="c20da-127">在強制模式中，此衝突的解決方式是在子類別中刪除衝突的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="c20da-127">In force mode this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="c20da-128">如果類別具有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="c20da-128">If the class has instances the update fails.</span></span>

<span data-ttu-id="c20da-129">使用強制模式來更新靜態類別，會導致刪除該類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="c20da-129">Using force mode to update a static class results in the deletion of all instances of that class.</span></span> <span data-ttu-id="c20da-130">提供者類別的強制更新不會刪除類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c20da-130">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="c20da-131"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="c20da-131"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>\*\*\*\*wbemChangeFlagCreateOrUpdate\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c20da-132">如果類別或實例已經存在，則會建立或覆寫。</span><span class="sxs-lookup"><span data-stu-id="c20da-132">Causes the class or instance to be created if it does not exist or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="c20da-133"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly \* \* \* (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="c20da-133"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>\*\*\*\*wbemChangeFlagCreateOnly\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="c20da-134">僅用於建立。</span><span class="sxs-lookup"><span data-stu-id="c20da-134">Used for creation only.</span></span> <span data-ttu-id="c20da-135">如果類別或實例已經存在，呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="c20da-135">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="c20da-136"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly \* \* \* (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="c20da-136"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>\*\*\*\*wbemChangeFlagUpdateOnly\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="c20da-137">導致此呼叫更新。</span><span class="sxs-lookup"><span data-stu-id="c20da-137">Causes this call to update.</span></span> <span data-ttu-id="c20da-138">類別或實例必須存在，呼叫才能成功。</span><span class="sxs-lookup"><span data-stu-id="c20da-138">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="c20da-139"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="c20da-139"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="c20da-140">導致呼叫立即返回。</span><span class="sxs-lookup"><span data-stu-id="c20da-140">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="c20da-141"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="c20da-141"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c20da-142">導致此呼叫封鎖，直到查詢完成為止。</span><span class="sxs-lookup"><span data-stu-id="c20da-142">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="c20da-143"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="c20da-143"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="c20da-144">導致非同步呼叫將狀態更新傳送至物件接收的 [**SWbemSink. OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="c20da-144">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="c20da-145"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="c20da-145"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c20da-146">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="c20da-146">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="c20da-147"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="c20da-147"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="c20da-148">導致 WMI 撰寫類別修訂資料和基類定義。</span><span class="sxs-lookup"><span data-stu-id="c20da-148">Causes WMI to write class amendment data along with the base class definition.</span></span> <span data-ttu-id="c20da-149">如需修改過的限定詞的詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="c20da-149">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c20da-150">*objWbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c20da-150">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c20da-151">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="c20da-151">Typically, this is undefined.</span></span> <span data-ttu-id="c20da-152">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="c20da-152">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="c20da-153">支援或需要這項資訊的提供者，必須記載可辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="c20da-153">A provider that supports or requires this information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c20da-154">*objWbemAsyncCoNtext* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c20da-154">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c20da-155">這是一個 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，它會返回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="c20da-155">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="c20da-156">如果您要使用相同的物件接收進行多個非同步呼叫，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="c20da-156">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="c20da-157">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="c20da-157">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="c20da-158">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="c20da-158">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="c20da-159">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="c20da-159">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c20da-160">傳回值</span><span class="sxs-lookup"><span data-stu-id="c20da-160">Return value</span></span>

<span data-ttu-id="c20da-161">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c20da-161">This method does not return a value.</span></span> <span data-ttu-id="c20da-162">如果呼叫成功，所提供之物件接收的 [**OnObjectPut**](swbemsink-onobjectput.md) 事件會接收 [**SWbemObjectPath**](swbemobjectpath.md) 物件，其中包含已成功認可至 WMI 之實例或類別的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="c20da-162">If the call is successful, the [**OnObjectPut**](swbemsink-onobjectput.md) event of the supplied object sink receives an [**SWbemObjectPath**](swbemobjectpath.md) object, containing the object path of the instance or class that is successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c20da-163">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c20da-163">Error codes</span></span>

<span data-ttu-id="c20da-164">**PutAsync \_** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c20da-164">After the completion of the **PutAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c20da-165">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="c20da-165">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="c20da-166">目前的使用者沒有更新指定類別之實例的許可權。</span><span class="sxs-lookup"><span data-stu-id="c20da-166">Current user does not have permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="c20da-167">**wbemErrAlreadyExists** -2147749913 (0x80041019) </span><span class="sxs-lookup"><span data-stu-id="c20da-167">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="c20da-168">指定了 **wbemChangeFlagCreateOnly** 旗標，但該實例已經存在。</span><span class="sxs-lookup"><span data-stu-id="c20da-168">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c20da-169">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="c20da-169">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c20da-170">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c20da-170">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="c20da-171">**wbemErrIllegalNull** -2147749898 (0x8004100A) </span><span class="sxs-lookup"><span data-stu-id="c20da-171">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="c20da-172">未針對不是 **任何** 專案的屬性指定 **任何** 值。</span><span class="sxs-lookup"><span data-stu-id="c20da-172">A value of **Nothing** was specified for a property that may not be **Nothing**.</span></span> <span data-ttu-id="c20da-173">這類屬性的範例之一，是由 **索引\*\*\*\*鍵**、索引或 **非 \_ Null** 限定詞標記的屬性。</span><span class="sxs-lookup"><span data-stu-id="c20da-173">An example of such a property is one that is marked by a **Key**, **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="c20da-174">**wbemErrInvalidObject** -2147749908 (0x80041014) </span><span class="sxs-lookup"><span data-stu-id="c20da-174">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="c20da-175">所指定的執行個體無效。</span><span class="sxs-lookup"><span data-stu-id="c20da-175">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c20da-176">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="c20da-176">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c20da-177">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="c20da-177">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c20da-178">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="c20da-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="c20da-179">指定了 **wbemChangeFlagUpdateOnly** 旗標，但實例或類別不存在。</span><span class="sxs-lookup"><span data-stu-id="c20da-179">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="c20da-180">**wbemErrIncompleteClass** -2147749920 (0x80041020) </span><span class="sxs-lookup"><span data-stu-id="c20da-180">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="c20da-181">尚未設定類別的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="c20da-181">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="c20da-182">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="c20da-182">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="c20da-183">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="c20da-183">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c20da-184">備註</span><span class="sxs-lookup"><span data-stu-id="c20da-184">Remarks</span></span>

<span data-ttu-id="c20da-185">這個呼叫會立即傳回，而 **put** 作業的結果會透過回呼傳遞給 *objWbemSink* 中指定的接收來傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="c20da-185">This call returns immediately, and the result of the **put** operation is returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="c20da-186">執行 *objWbemSink*。</span><span class="sxs-lookup"><span data-stu-id="c20da-186">Implement the *objWbemSink*.</span></span> <span data-ttu-id="c20da-187">[**OnObjectPut**](swbemsink-onobjectput.md) 方法，取得寫入 WMI 儲存機制之實例或類別的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="c20da-187">[**OnObjectPut**](swbemsink-onobjectput.md) method to obtain the object path of the instance or class that is written to the WMI repository.</span></span> <span data-ttu-id="c20da-188">如需接收方法的詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="c20da-188">For more information about sink methods, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="c20da-189">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="c20da-189">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="c20da-190">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="c20da-190">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="c20da-191">若要消除風險，請使用最半同步或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="c20da-191">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="c20da-192">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="c20da-192">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c20da-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="c20da-193">Requirements</span></span>



| <span data-ttu-id="c20da-194">需求</span><span class="sxs-lookup"><span data-stu-id="c20da-194">Requirement</span></span> | <span data-ttu-id="c20da-195">值</span><span class="sxs-lookup"><span data-stu-id="c20da-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c20da-196">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c20da-196">Minimum supported client</span></span><br/> | <span data-ttu-id="c20da-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c20da-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c20da-198">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c20da-198">Minimum supported server</span></span><br/> | <span data-ttu-id="c20da-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c20da-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c20da-200">標頭</span><span class="sxs-lookup"><span data-stu-id="c20da-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="c20da-201"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="c20da-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c20da-202">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c20da-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="c20da-203"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c20da-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c20da-204">DLL</span><span class="sxs-lookup"><span data-stu-id="c20da-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c20da-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c20da-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c20da-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="c20da-206">CLSID</span></span><br/>                    | <span data-ttu-id="c20da-207">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="c20da-207">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="c20da-208">IID</span><span class="sxs-lookup"><span data-stu-id="c20da-208">IID</span></span><br/>                      | <span data-ttu-id="c20da-209">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="c20da-209">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="c20da-210">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c20da-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c20da-211">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="c20da-211">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="c20da-212">**SWbemObjectPath 類別**</span><span class="sxs-lookup"><span data-stu-id="c20da-212">**SWbemObjectPath.Class**</span></span>](swbemobjectpath-class.md)
</dt> <dt>

[<span data-ttu-id="c20da-213">**Swbempropertyset**</span><span class="sxs-lookup"><span data-stu-id="c20da-213">**SWbemProperty**</span></span>](swbemproperty.md)
</dt> <dt>

[<span data-ttu-id="c20da-214">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="c20da-214">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

