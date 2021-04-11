---
description: '\_SWbemObject 物件的 ExecMethod 方法會執行方法提供者所匯出的方法。'
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: 'SWbemObject.ExecMethod_ 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6b71d88a113e515d50ac01a23f070714fa467615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114868"
---
# <a name="swbemobjectexecmethod_-method"></a><span data-ttu-id="f9551-103">SWbemObject.ExecMethod \_ 方法</span><span class="sxs-lookup"><span data-stu-id="f9551-103">SWbemObject.ExecMethod\_ method</span></span>

<span data-ttu-id="f9551-104">[**SWbemObject**](swbemobject.md)物件的 **ExecMethod \_** 方法會執行方法提供者所匯出的方法。</span><span class="sxs-lookup"><span data-stu-id="f9551-104">The **ExecMethod\_** method of the [**SWbemObject**](swbemobject.md) object executes a method exported by a method provider.</span></span>

<span data-ttu-id="f9551-105">當轉送至適當提供者的方法執行時，這個方法會暫停。</span><span class="sxs-lookup"><span data-stu-id="f9551-105">This method pauses while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="f9551-106">然後會傳回信息和狀態。</span><span class="sxs-lookup"><span data-stu-id="f9551-106">The information and status are then returned.</span></span> <span data-ttu-id="f9551-107">提供者（而非 WMI）會執行方法。</span><span class="sxs-lookup"><span data-stu-id="f9551-107">The provider rather than WMI implements the method.</span></span>

<span data-ttu-id="f9551-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="f9551-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9551-109">語法</span><span class="sxs-lookup"><span data-stu-id="f9551-109">Syntax</span></span>


```VB
objOutParams = .ExecMethod_( _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f9551-110">參數</span><span class="sxs-lookup"><span data-stu-id="f9551-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9551-111">*strMethodName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f9551-111">*strMethodName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9551-112">必要。</span><span class="sxs-lookup"><span data-stu-id="f9551-112">Required.</span></span> <span data-ttu-id="f9551-113">物件之方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9551-113">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="f9551-114">*objwbemInParams* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="f9551-114">*objwbemInParams* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f9551-115">這是 [**SWbemObject**](swbemobject.md) 物件，其中包含所執行之方法的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="f9551-115">This is an [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="f9551-116">根據預設，這個參數是未定義的。</span><span class="sxs-lookup"><span data-stu-id="f9551-116">By default, this parameter is undefined.</span></span> <span data-ttu-id="f9551-117">如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="f9551-117">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9551-118">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="f9551-118">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f9551-119">如果已指定，則會保留，且必須設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="f9551-119">Reserved and must be set to 0 (zero) if specified.</span></span>

</dd> <dt>

<span data-ttu-id="f9551-120">*objwbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="f9551-120">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f9551-121">一般而言，它是未定義的。</span><span class="sxs-lookup"><span data-stu-id="f9551-121">Typically, it is undefined.</span></span> <span data-ttu-id="f9551-122">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="f9551-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="f9551-123">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="f9551-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9551-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="f9551-124">Return value</span></span>

<span data-ttu-id="f9551-125">如果這個方法成功， [**SWbemObject**](swbemobject.md) 物件會傳回。</span><span class="sxs-lookup"><span data-stu-id="f9551-125">If this method is successful, an [**SWbemObject**](swbemobject.md) object returns.</span></span> <span data-ttu-id="f9551-126">傳回的物件包含要執行之方法的 out 參數和傳回值。</span><span class="sxs-lookup"><span data-stu-id="f9551-126">The returned object contains the out parameters and return value for the method being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f9551-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f9551-127">Error codes</span></span>

<span data-ttu-id="f9551-128">**ExecMethod \_** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f9551-128">After the completion of the **ExecMethod\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f9551-129">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="f9551-129">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f9551-130">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f9551-130">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f9551-131">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="f9551-131">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="f9551-132">指定的類別無效。</span><span class="sxs-lookup"><span data-stu-id="f9551-132">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f9551-133">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="f9551-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f9551-134">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="f9551-134">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f9551-135">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="f9551-135">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="f9551-136">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="f9551-136">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f9551-137">**wbemErrInvalidMethod** -2147749934 (0x8004102E) </span><span class="sxs-lookup"><span data-stu-id="f9551-137">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="f9551-138">要求的方法無法使用。</span><span class="sxs-lookup"><span data-stu-id="f9551-138">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="f9551-139">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="f9551-139">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="f9551-140">目前的使用者未獲授權執行此方法。</span><span class="sxs-lookup"><span data-stu-id="f9551-140">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9551-141">備註</span><span class="sxs-lookup"><span data-stu-id="f9551-141">Remarks</span></span>

<span data-ttu-id="f9551-142">這個方法類似于 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)，但是它會直接在要執行其方法的物件上運作。</span><span class="sxs-lookup"><span data-stu-id="f9551-142">This method is similar to [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), but it operates directly on the object whose method is to be executed.</span></span> <span data-ttu-id="f9551-143">例如，下列程式碼範例會呼叫 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)中的 [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service)提供者方法，並使用 [直接存取](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="f9551-143">For example, the following code example calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) and uses [direct access](manipulating-class-and-instance-information.md).</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="f9551-144">此版本會呼叫 **SWbemObject.Exe\_ cMethod** 來執行 [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service)方法。</span><span class="sxs-lookup"><span data-stu-id="f9551-144">This version calls **SWbemObject.ExecMethod\_** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



<span data-ttu-id="f9551-145">在無法直接執行方法的情況下，使用 **SWbemObject.ExecMethod \_** 作為直接存取來執行 [*提供者方法*](gloss-p.md)的替代方法。</span><span class="sxs-lookup"><span data-stu-id="f9551-145">Use **SWbemObject.ExecMethod\_** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="f9551-146">例如，如果您的方法有 out 參數，則您會使用 **SWbemObject.ExecMethod \_** 搭配不支援輸出參數的指令碼語言。</span><span class="sxs-lookup"><span data-stu-id="f9551-146">For example, you would use **SWbemObject.ExecMethod\_** with a scripting language that does not support output parameters if your method has out parameters.</span></span> <span data-ttu-id="f9551-147">否則，叫用方法的建議方法是使用直接存取。</span><span class="sxs-lookup"><span data-stu-id="f9551-147">Otherwise, the recommended means of invoking a method is to use direct access.</span></span>

-   <span data-ttu-id="f9551-148">**SWbemObject.ExecMethod \_** 方法會假設 [**SWbemObject**](swbemobject.md)所代表的物件包含要執行的方法。</span><span class="sxs-lookup"><span data-stu-id="f9551-148">The **SWbemObject.ExecMethod\_** method assumes the object represented by [**SWbemObject**](swbemobject.md) contains the method to execute.</span></span> <span data-ttu-id="f9551-149">相較之下， [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) 需要物件路徑。</span><span class="sxs-lookup"><span data-stu-id="f9551-149">By contrast, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) requires an object path.</span></span> <span data-ttu-id="f9551-150">如果您已經取得要執行其方法的物件，請使用 **SWbemObject.ExecMethod \_** 。</span><span class="sxs-lookup"><span data-stu-id="f9551-150">Use **SWbemObject.ExecMethod\_** if you already have obtained the object whose method you want to execute.</span></span>

## <a name="examples"></a><span data-ttu-id="f9551-151">範例</span><span class="sxs-lookup"><span data-stu-id="f9551-151">Examples</span></span>

<span data-ttu-id="f9551-152">下列範例顯示 [**ExecMethod**](swbemservices-execmethod.md) 方法。腳本會建立 [**Win32 \_ 處理**](/windows/desktop/CIMWin32Prov/win32-process) 物件，代表執行 [記事本] 的進程。</span><span class="sxs-lookup"><span data-stu-id="f9551-152">The following example shows the [**ExecMethod**](swbemservices-execmethod.md) method.The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object representing a process running Notepad.</span></span> <span data-ttu-id="f9551-153">如需有關如何以非同步方式執行相同作業的腳本詳細資訊，請參閱 [**SWbemObject.ExecMethodAsync \_**](swbemobject-execmethodasync-.md)。</span><span class="sxs-lookup"><span data-stu-id="f9551-153">For more information about a script illustrating the same operations performed asynchronously, see [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md).</span></span> <span data-ttu-id="f9551-154">如需使用直接存取的範例，請參閱 [**在 Class Win32 \_ 進程中建立方法**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) 。</span><span class="sxs-lookup"><span data-stu-id="f9551-154">For an example using direct access, see [**Create Method in Class Win32\_Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) .</span></span> <span data-ttu-id="f9551-155">如需使用 [**SWbemServices**](swbemservices.md) 物件進行相同操作的範例，請參閱 **SWbemServices.ExecMethod**。</span><span class="sxs-lookup"><span data-stu-id="f9551-155">For an example of the same operation using an [**SWbemServices**](swbemservices.md) object, see **SWbemServices.ExecMethod**.</span></span>


```VB
' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a><span data-ttu-id="f9551-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9551-156">Requirements</span></span>



| <span data-ttu-id="f9551-157">需求</span><span class="sxs-lookup"><span data-stu-id="f9551-157">Requirement</span></span> | <span data-ttu-id="f9551-158">值</span><span class="sxs-lookup"><span data-stu-id="f9551-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9551-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9551-159">Minimum supported client</span></span><br/> | <span data-ttu-id="f9551-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9551-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9551-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9551-161">Minimum supported server</span></span><br/> | <span data-ttu-id="f9551-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9551-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9551-163">標頭</span><span class="sxs-lookup"><span data-stu-id="f9551-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9551-164"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="f9551-164"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9551-165">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f9551-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9551-166"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f9551-166"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f9551-167">DLL</span><span class="sxs-lookup"><span data-stu-id="f9551-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9551-168"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9551-168"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f9551-169">CLSID</span><span class="sxs-lookup"><span data-stu-id="f9551-169">CLSID</span></span><br/>                    | <span data-ttu-id="f9551-170">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="f9551-170">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="f9551-171">IID</span><span class="sxs-lookup"><span data-stu-id="f9551-171">IID</span></span><br/>                      | <span data-ttu-id="f9551-172">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="f9551-172">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="f9551-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9551-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9551-174">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="f9551-174">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="f9551-175">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="f9551-175">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="f9551-176">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="f9551-176">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> </dl>

 

