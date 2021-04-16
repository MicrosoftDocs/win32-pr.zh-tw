---
description: 刪除物件路徑中指定的類別或實例。 您只能刪除目前命名空間中的物件。
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.tgt_platform: multiple
title: 'SWbemServices 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Delete
- ISWbemServices.Delete
- ISWbemServices.Delete
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690dc595471baa5514d7f1ab84a8f6def16ee5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469308"
---
# <a name="swbemservicesdelete-method"></a><span data-ttu-id="f738c-104">SWbemServices 方法</span><span class="sxs-lookup"><span data-stu-id="f738c-104">SWbemServices.Delete method</span></span>

<span data-ttu-id="f738c-105">[**SWbemServices**](swbemservices.md)物件的 **Delete** 方法會刪除物件路徑中指定的類別或實例。</span><span class="sxs-lookup"><span data-stu-id="f738c-105">The **Delete** method of the [**SWbemServices**](swbemservices.md) object deletes the class or instance that is specified in the object path.</span></span> <span data-ttu-id="f738c-106">您只能刪除目前命名空間中的物件。</span><span class="sxs-lookup"><span data-stu-id="f738c-106">You can only delete objects in the current namespace.</span></span>

<span data-ttu-id="f738c-107">如果動態提供者提供類別或實例，除非提供者支援類別或實例的刪除，否則您無法刪除此物件。</span><span class="sxs-lookup"><span data-stu-id="f738c-107">If a dynamic provider supplies the class or instance, you cannot delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="f738c-108">這個方法是在同步模式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="f738c-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="f738c-109">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="f738c-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="f738c-110">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="f738c-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f738c-111">語法</span><span class="sxs-lookup"><span data-stu-id="f738c-111">Syntax</span></span>


```VB
SWbemServices.Delete( _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f738c-112">參數</span><span class="sxs-lookup"><span data-stu-id="f738c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f738c-113">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="f738c-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="f738c-114">必要。</span><span class="sxs-lookup"><span data-stu-id="f738c-114">Required.</span></span> <span data-ttu-id="f738c-115">字串，包含您要刪除之物件的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="f738c-115">String that contains the object path to the object that you want to delete.</span></span> <span data-ttu-id="f738c-116">如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="f738c-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="f738c-117">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="f738c-117">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f738c-118">保留的。</span><span class="sxs-lookup"><span data-stu-id="f738c-118">Reserved.</span></span> <span data-ttu-id="f738c-119">這個值必須為零。</span><span class="sxs-lookup"><span data-stu-id="f738c-119">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f738c-120">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="f738c-120">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f738c-121">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="f738c-121">Typically, this is undefined.</span></span> <span data-ttu-id="f738c-122">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其專案代表服務要求的提供者可使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="f738c-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="f738c-123">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="f738c-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f738c-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="f738c-124">Return value</span></span>

<span data-ttu-id="f738c-125">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f738c-125">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f738c-126">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f738c-126">Error codes</span></span>

<span data-ttu-id="f738c-127">完成 **刪除** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f738c-127">After the completion of the **Delete** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f738c-128">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="f738c-128">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="f738c-129">目前的內容沒有足夠的安全性許可權可刪除物件。</span><span class="sxs-lookup"><span data-stu-id="f738c-129">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="f738c-130">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="f738c-130">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f738c-131">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f738c-131">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f738c-132">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="f738c-132">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="f738c-133">指定的類別不存在。</span><span class="sxs-lookup"><span data-stu-id="f738c-133">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="f738c-134">**wbemErrInvalidOperation** -2147749910 (0x80041016) </span><span class="sxs-lookup"><span data-stu-id="f738c-134">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="f738c-135">無法刪除物件。</span><span class="sxs-lookup"><span data-stu-id="f738c-135">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="f738c-136">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="f738c-136">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="f738c-137">物件不存在。</span><span class="sxs-lookup"><span data-stu-id="f738c-137">Object does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="f738c-138">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="f738c-138">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="f738c-139">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="f738c-139">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f738c-140">備註</span><span class="sxs-lookup"><span data-stu-id="f738c-140">Remarks</span></span>

<span data-ttu-id="f738c-141">當物件的索引鍵屬性未指定值時，就可以使用 **SWbemServices** 方法，因為這個方法只需要物件路徑做為輸入。</span><span class="sxs-lookup"><span data-stu-id="f738c-141">The **SWbemServices.Delete** method can be used when the key property for the object is not given a value, because this method only requires an object path as input.</span></span> <span data-ttu-id="f738c-142">如果缺少索引鍵值， [**SWbemObject \_**](swbemobject-delete-.md)會失敗的情況下可以使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="f738c-142">This method can be used in situations where [**SWbemObject.Delete\_**](swbemobject-delete-.md) fails for lack of a key value.</span></span> <span data-ttu-id="f738c-143">如果透過 [**SWbemObject \_**](swbemobject-put-.md)將物件認可至 WMI，則會透過呼叫取得 [**SWbemObjectPath**](swbemobjectpath.md)物件。</span><span class="sxs-lookup"><span data-stu-id="f738c-143">If the object is committed to WMI through [**SWbemObject.Put\_**](swbemobject-put-.md), then an [**SWbemObjectPath**](swbemobjectpath.md) object was obtained through the call.</span></span>

## <a name="examples"></a><span data-ttu-id="f738c-144">範例</span><span class="sxs-lookup"><span data-stu-id="f738c-144">Examples</span></span>

<span data-ttu-id="f738c-145">下列範例會建立新的類別、加入非索引鍵的屬性、將新類別寫入存放庫，並顯示新類別物件的路徑。</span><span class="sxs-lookup"><span data-stu-id="f738c-145">The following example creates a new class, adds a property that is not a key, writes the new class to the repository, and displays the path of the new class object.</span></span> <span data-ttu-id="f738c-146">腳本接著會產生新類別的實例、寫入實例，並顯示路徑。</span><span class="sxs-lookup"><span data-stu-id="f738c-146">The script then spawns an instance of the new class, writes the instance, and displays the path.</span></span> <span data-ttu-id="f738c-147">請注意，腳本會藉由刪除類別，從存放庫中刪除類別和其實例。</span><span class="sxs-lookup"><span data-stu-id="f738c-147">Note that the script deletes both the class and its instances from the repository by deleting the class.</span></span> <span data-ttu-id="f738c-148">如需 WMI 類別和實例的詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md) 和 [通用訊息模型](common-information-model.md)。</span><span class="sxs-lookup"><span data-stu-id="f738c-148">For more information about WMI classes and instances, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Common Information Model](common-information-model.md).</span></span>


```VB
wbemCimtypeSint32 = 3
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' Integer property
objClass.Properties_.Add "iProperty", wbemCimtypeSint32  
objClass.Properties_("iProperty").Qualifiers_.Add "key", TRUE 

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.iProperty = 1000

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objSWbemService.Delete("NewClass")
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a><span data-ttu-id="f738c-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="f738c-149">Requirements</span></span>



| <span data-ttu-id="f738c-150">需求</span><span class="sxs-lookup"><span data-stu-id="f738c-150">Requirement</span></span> | <span data-ttu-id="f738c-151">值</span><span class="sxs-lookup"><span data-stu-id="f738c-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f738c-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f738c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="f738c-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f738c-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f738c-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f738c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="f738c-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f738c-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f738c-156">標頭</span><span class="sxs-lookup"><span data-stu-id="f738c-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="f738c-157"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="f738c-157"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f738c-158">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f738c-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="f738c-159"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f738c-159"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f738c-160">DLL</span><span class="sxs-lookup"><span data-stu-id="f738c-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f738c-161"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f738c-161"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f738c-162">CLSID</span><span class="sxs-lookup"><span data-stu-id="f738c-162">CLSID</span></span><br/>                    | <span data-ttu-id="f738c-163">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="f738c-163">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="f738c-164">IID</span><span class="sxs-lookup"><span data-stu-id="f738c-164">IID</span></span><br/>                      | <span data-ttu-id="f738c-165">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="f738c-165">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f738c-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f738c-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f738c-167">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="f738c-167">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="f738c-168">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="f738c-168">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> </dl>

 

 




