---
description: '\_SWbemObject 物件的 Delete 方法會刪除目前的類別或目前的實例。'
ms.assetid: bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb
ms.tgt_platform: multiple
title: 'SWbemObject.Delete_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Delete_
- ISWbemObject.Delete_
- ISWbemObject.Delete_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d994c8a9b9e0af9d4bd884c89cd67280513c9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027073"
---
# <a name="swbemobjectdelete_-method"></a><span data-ttu-id="8a270-103">SWbemObject \_ 方法</span><span class="sxs-lookup"><span data-stu-id="8a270-103">SWbemObject.Delete\_ method</span></span>

<span data-ttu-id="8a270-104">[**SWbemObject**](swbemobject.md)物件的 **Delete \_** 方法會刪除目前的類別或目前的實例。</span><span class="sxs-lookup"><span data-stu-id="8a270-104">The **Delete\_** method of the [**SWbemObject**](swbemobject.md) object deletes either the current class or the current instance.</span></span> <span data-ttu-id="8a270-105">如果動態提供者提供了類別或實例，除非提供者支援類別或實例的刪除，否則有時候無法刪除此物件。</span><span class="sxs-lookup"><span data-stu-id="8a270-105">If a dynamic provider supplies the class or instance, it is sometimes not possible to delete this object unless the provider supports class or instance deletion.</span></span> <span data-ttu-id="8a270-106">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="8a270-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a270-107">語法</span><span class="sxs-lookup"><span data-stu-id="8a270-107">Syntax</span></span>


```VB
SWbemObject.Delete_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8a270-108">參數</span><span class="sxs-lookup"><span data-stu-id="8a270-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a270-109">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="8a270-109">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a270-110">如果有指定，就會保留，且必須為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="8a270-110">Reserved and must be 0 (zero) if specified.</span></span>

</dd> <dt>

<span data-ttu-id="8a270-111">*objwbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="8a270-111">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a270-112">此參數通常是未定義的。</span><span class="sxs-lookup"><span data-stu-id="8a270-112">This parameter is typically undefined.</span></span> <span data-ttu-id="8a270-113">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="8a270-113">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="8a270-114">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="8a270-114">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a270-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a270-115">Return value</span></span>

<span data-ttu-id="8a270-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8a270-116">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8a270-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="8a270-117">Error codes</span></span>

<span data-ttu-id="8a270-118">完成 **刪除 \_** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8a270-118">After completion of the **Delete\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="8a270-119">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="8a270-119">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="8a270-120">目前的內容沒有足夠的安全性許可權可刪除物件。</span><span class="sxs-lookup"><span data-stu-id="8a270-120">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="8a270-121">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="8a270-121">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8a270-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8a270-122">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="8a270-123">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="8a270-123">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="8a270-124">指定的類別不存在。</span><span class="sxs-lookup"><span data-stu-id="8a270-124">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="8a270-125">**wbemErrInvalidOperation** -2147749910 (0x80041016) </span><span class="sxs-lookup"><span data-stu-id="8a270-125">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="8a270-126">無法刪除物件。</span><span class="sxs-lookup"><span data-stu-id="8a270-126">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="8a270-127">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="8a270-127">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="8a270-128">物件不存在。</span><span class="sxs-lookup"><span data-stu-id="8a270-128">Object did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="8a270-129">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="8a270-129">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="8a270-130">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="8a270-130">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a270-131">備註</span><span class="sxs-lookup"><span data-stu-id="8a270-131">Remarks</span></span>

<span data-ttu-id="8a270-132">如果建立了 [**SWbemObject**](swbemobject.md)的新實例，但未提供索引鍵屬性的值， **Delete \_** 方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="8a270-132">The **Delete\_** method fails if a new instance of [**SWbemObject**](swbemobject.md) is created, but no value is supplied for the key property.</span></span> <span data-ttu-id="8a270-133">Windows Management Instrumentation (WMI) 會自動產生全域唯一識別碼 (GUID) 值，但 **SWbemObject \_** 不接受 guid 值。</span><span class="sxs-lookup"><span data-stu-id="8a270-133">Windows Management Instrumentation (WMI) generates a globally unique identifier (GUID) value automatically, but a GUID value is not accepted by **SWbemObject.Delete\_**.</span></span> <span data-ttu-id="8a270-134">在此情況下， [**SWbemServices**](swbemservices-delete.md)會使用物件路徑運作。</span><span class="sxs-lookup"><span data-stu-id="8a270-134">In this case, [**SWbemServices.Delete**](swbemservices-delete.md), which uses the object path works.</span></span> <span data-ttu-id="8a270-135">請注意，在將物件認可至 WMI 之後， [**SWbemObject \_ . Put**](swbemobject-put-.md)方法會傳回 [**SWbemObjectPath**](swbemobjectpath.md)物件。</span><span class="sxs-lookup"><span data-stu-id="8a270-135">Note that an [**SWbemObjectPath**](swbemobjectpath.md) object is returned by the [**SWbemObject.Put\_**](swbemobject-put-.md) method after an object is committed to WMI.</span></span>

## <a name="examples"></a><span data-ttu-id="8a270-136">範例</span><span class="sxs-lookup"><span data-stu-id="8a270-136">Examples</span></span>

<span data-ttu-id="8a270-137">下列範例會建立新的類別。加入索引鍵屬性;將新類別寫入至存放庫;並顯示新類別物件的路徑。</span><span class="sxs-lookup"><span data-stu-id="8a270-137">The following example creates a new class; adds a key property; writes the new class to the repository; and displays the path of the new class object.</span></span> <span data-ttu-id="8a270-138">腳本接著會產生新類別的實例;寫入它;並顯示路徑。</span><span class="sxs-lookup"><span data-stu-id="8a270-138">The script then spawns an instance of the new class; writes it; and displays the path.</span></span> <span data-ttu-id="8a270-139">請注意，腳本只會刪除類別，從儲存機制刪除類別及其實例。</span><span class="sxs-lookup"><span data-stu-id="8a270-139">Note that the script deletes both the class and its instances from the repository by simply deleting the class.</span></span>


```VB
On Error Resume Next
wbemCimtypeString = 8             ' String datatype
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString 
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.Add "key", TRUE

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objClass.Delete_()
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a><span data-ttu-id="8a270-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a270-140">Requirements</span></span>



| <span data-ttu-id="8a270-141">需求</span><span class="sxs-lookup"><span data-stu-id="8a270-141">Requirement</span></span> | <span data-ttu-id="8a270-142">值</span><span class="sxs-lookup"><span data-stu-id="8a270-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a270-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a270-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8a270-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a270-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a270-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a270-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8a270-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a270-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a270-147">標頭</span><span class="sxs-lookup"><span data-stu-id="8a270-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a270-148"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="8a270-148"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a270-149">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8a270-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a270-150"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8a270-150"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8a270-151">DLL</span><span class="sxs-lookup"><span data-stu-id="8a270-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a270-152"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a270-152"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a270-153">CLSID</span><span class="sxs-lookup"><span data-stu-id="8a270-153">CLSID</span></span><br/>                    | <span data-ttu-id="8a270-154">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="8a270-154">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="8a270-155">IID</span><span class="sxs-lookup"><span data-stu-id="8a270-155">IID</span></span><br/>                      | <span data-ttu-id="8a270-156">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="8a270-156">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




