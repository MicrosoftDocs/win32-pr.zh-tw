---
description: SWbemServices.ExecMethod 方法-執行方法提供者所匯出的方法。
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: " (>wbemdisp.tlb 的 SWbemServices.ExecMethod 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethod
- ISWbemServices.ExecMethod
- ISWbemServices.ExecMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 452c42c37e8dcb9f2b37b660b1f8899e587b5579
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103636"
---
# <a name="swbemservicesexecmethod-method"></a><span data-ttu-id="37306-103">SWbemServices.ExecMethod 方法</span><span class="sxs-lookup"><span data-stu-id="37306-103">SWbemServices.ExecMethod method</span></span>

<span data-ttu-id="37306-104">[**SWbemServices**](swbemservices.md)物件的 **ExecMethod** 方法會執行方法提供者所匯出的方法。</span><span class="sxs-lookup"><span data-stu-id="37306-104">The **ExecMethod** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="37306-105">當轉送至適當提供者的方法執行時，這個方法會封鎖。</span><span class="sxs-lookup"><span data-stu-id="37306-105">This method blocks while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="37306-106">然後會傳回信息和狀態。</span><span class="sxs-lookup"><span data-stu-id="37306-106">The information and status are then returned.</span></span> <span data-ttu-id="37306-107">提供者（而非 WMI）會執行方法。</span><span class="sxs-lookup"><span data-stu-id="37306-107">The provider, rather than WMI, implements the method.</span></span>

<span data-ttu-id="37306-108">這個方法是在同步模式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="37306-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="37306-109">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="37306-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="37306-110">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="37306-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="37306-111">語法</span><span class="sxs-lookup"><span data-stu-id="37306-111">Syntax</span></span>


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="37306-112">參數</span><span class="sxs-lookup"><span data-stu-id="37306-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37306-113">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="37306-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="37306-114">必要。</span><span class="sxs-lookup"><span data-stu-id="37306-114">Required.</span></span> <span data-ttu-id="37306-115">字串，包含執行方法之物件的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="37306-115">String that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="37306-116">如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="37306-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="37306-117">*strMethodName*</span><span class="sxs-lookup"><span data-stu-id="37306-117">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="37306-118">必要。</span><span class="sxs-lookup"><span data-stu-id="37306-118">Required.</span></span> <span data-ttu-id="37306-119">物件之方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="37306-119">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="37306-120">*objWbemInParams* \[選\]</span><span class="sxs-lookup"><span data-stu-id="37306-120">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37306-121">[**SWbemObject**](swbemobject.md)物件，其中包含所要執行之方法的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="37306-121">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="37306-122">根據預設，這個參數是未定義的。</span><span class="sxs-lookup"><span data-stu-id="37306-122">By default, this parameter is undefined.</span></span> <span data-ttu-id="37306-123">如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="37306-123">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="37306-124">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="37306-124">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37306-125">保留的。</span><span class="sxs-lookup"><span data-stu-id="37306-125">Reserved.</span></span> <span data-ttu-id="37306-126">這個值必須為零。</span><span class="sxs-lookup"><span data-stu-id="37306-126">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="37306-127">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="37306-127">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37306-128">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="37306-128">Typically, this is undefined.</span></span> <span data-ttu-id="37306-129">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="37306-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="37306-130">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="37306-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37306-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="37306-131">Return value</span></span>

<span data-ttu-id="37306-132">如果方法成功，則會傳回 [**SWbemObject**](swbemobject.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="37306-132">If the method is successful, an [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="37306-133">傳回的物件包含要執行之方法的 out 參數和傳回值。</span><span class="sxs-lookup"><span data-stu-id="37306-133">The returned object contains the out parameters and return value for the method that is being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="37306-134">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="37306-134">Error codes</span></span>

<span data-ttu-id="37306-135">**ExecMethod** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="37306-135">After the completion of the **ExecMethod** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="37306-136">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="37306-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="37306-137">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="37306-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="37306-138">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="37306-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="37306-139">指定的類別無效。</span><span class="sxs-lookup"><span data-stu-id="37306-139">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="37306-140">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="37306-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="37306-141">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="37306-141">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="37306-142">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="37306-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="37306-143">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="37306-143">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="37306-144">**wbemErrInvalidMethod** -2147749934 (0x8004102E) </span><span class="sxs-lookup"><span data-stu-id="37306-144">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="37306-145">要求的方法無法使用。</span><span class="sxs-lookup"><span data-stu-id="37306-145">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="37306-146">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="37306-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="37306-147">目前的使用者未獲授權執行此方法。</span><span class="sxs-lookup"><span data-stu-id="37306-147">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37306-148">備註</span><span class="sxs-lookup"><span data-stu-id="37306-148">Remarks</span></span>

<span data-ttu-id="37306-149">在無法直接執行方法的情況下，使用 **SWbemServices.ExecMethod** 作為直接存取來執行 [*提供者方法*](gloss-p.md) 的替代方法。</span><span class="sxs-lookup"><span data-stu-id="37306-149">Use **SWbemServices.ExecMethod** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="37306-150">**ExecMethod** 方法可讓您取得輸出參數（如果提供者提供的話），以及不支援輸出參數的指令碼語言。</span><span class="sxs-lookup"><span data-stu-id="37306-150">The **ExecMethod** method allows you to obtain output parameters, if the provider supplies them, with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="37306-151">否則，叫用方法的建議方法是使用直接存取。</span><span class="sxs-lookup"><span data-stu-id="37306-151">Otherwise, the recommended means of invoking a method is to use direct access.</span></span> <span data-ttu-id="37306-152">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="37306-152">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="37306-153">例如，下列程式碼範例會呼叫 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)中的 [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service)提供者方法，以使用直接存取。</span><span class="sxs-lookup"><span data-stu-id="37306-153">For example, the following code example that calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) uses direct access.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="37306-154">這個範例會呼叫 **SWbemServices.ExecMethod** 來執行 [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) 方法。</span><span class="sxs-lookup"><span data-stu-id="37306-154">This example calls **SWbemServices.ExecMethod** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="37306-155">請注意，物件路徑是必要的，因為 **SWbemServices.ExecMethod** 不會在物件上運作，不同于 [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md)。</span><span class="sxs-lookup"><span data-stu-id="37306-155">Note that an object path is required because **SWbemServices.ExecMethod** is not operating on the object already, unlike [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



<span data-ttu-id="37306-156">**SWbemServices.Exe的 cMethod** 方法需要物件路徑。</span><span class="sxs-lookup"><span data-stu-id="37306-156">The **SWbemServices.ExecMethod** method requires an object path.</span></span> <span data-ttu-id="37306-157">如果腳本已保存 [**SWbemObject**](swbemobject.md) 物件，請使用 [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="37306-157">If the script already holds an [**SWbemObject**](swbemobject.md) object, use the [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="37306-158">範例</span><span class="sxs-lookup"><span data-stu-id="37306-158">Examples</span></span>

<span data-ttu-id="37306-159">下列範例顯示 **ExecMethod** 方法。</span><span class="sxs-lookup"><span data-stu-id="37306-159">The following example shows the **ExecMethod** method.</span></span> <span data-ttu-id="37306-160">腳本會建立 [**Win32 \_ 處理**](/windows/desktop/CIMWin32Prov/win32-process) 物件，該物件代表正在執行 [記事本] 的進程。</span><span class="sxs-lookup"><span data-stu-id="37306-160">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="37306-161">它會顯示 [**InParameters**](swbemmethod-inparameters.md) 物件的設定，以及如何從 [**OutParameters**](swbemmethod-outparameters.md) 物件取得結果。</span><span class="sxs-lookup"><span data-stu-id="37306-161">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="37306-162">如需顯示以非同步方式執行相同作業的腳本，請參閱 [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)。</span><span class="sxs-lookup"><span data-stu-id="37306-162">For a script that shows the same operations performed asynchronously, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span> <span data-ttu-id="37306-163">如需使用直接存取的範例，請參閱 [在 Class Win32 \_ 進程中建立方法](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)。</span><span class="sxs-lookup"><span data-stu-id="37306-163">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="37306-164">如需使用 [**SWbemObject**](swbemobject.md)進行相同操作的範例，請參閱 [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md)。</span><span class="sxs-lookup"><span data-stu-id="37306-164">For an example of the same operation using an [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            & " but had error " _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a><span data-ttu-id="37306-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="37306-165">Requirements</span></span>



| <span data-ttu-id="37306-166">需求</span><span class="sxs-lookup"><span data-stu-id="37306-166">Requirement</span></span> | <span data-ttu-id="37306-167">值</span><span class="sxs-lookup"><span data-stu-id="37306-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37306-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37306-168">Minimum supported client</span></span><br/> | <span data-ttu-id="37306-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37306-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="37306-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37306-170">Minimum supported server</span></span><br/> | <span data-ttu-id="37306-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37306-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37306-172">標頭</span><span class="sxs-lookup"><span data-stu-id="37306-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="37306-173"><dt>>Wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="37306-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="37306-174">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="37306-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="37306-175"><dt>>Wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="37306-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="37306-176">DLL</span><span class="sxs-lookup"><span data-stu-id="37306-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37306-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37306-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="37306-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="37306-178">CLSID</span></span><br/>                    | <span data-ttu-id="37306-179">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="37306-179">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="37306-180">IID</span><span class="sxs-lookup"><span data-stu-id="37306-180">IID</span></span><br/>                      | <span data-ttu-id="37306-181">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="37306-181">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="37306-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37306-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37306-183">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="37306-183">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="37306-184">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="37306-184">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="37306-185">呼叫提供者方法</span><span class="sxs-lookup"><span data-stu-id="37306-185">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="37306-186">操作類別和實例資訊</span><span class="sxs-lookup"><span data-stu-id="37306-186">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

