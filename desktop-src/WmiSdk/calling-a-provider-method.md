---
description: 提供者方法是由 Windows Management Instrumentation (WMI) 提供者所執行的方法。
ms.assetid: 9c692bc7-246b-4619-a371-cc9e0e2d5a6e
ms.tgt_platform: multiple
title: 呼叫提供者方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ed8d05a1105c15f06b3df5f47006c5dafcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991894"
---
# <a name="calling-a-provider-method"></a><span data-ttu-id="9ac2b-103">呼叫提供者方法</span><span class="sxs-lookup"><span data-stu-id="9ac2b-103">Calling a Provider Method</span></span>

<span data-ttu-id="9ac2b-104">提供者方法是由 Windows Management Instrumentation (WMI) 提供者所執行的方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-104">A provider method is a method that is implemented by a Windows Management Instrumentation (WMI) provider.</span></span> <span data-ttu-id="9ac2b-105">在提供者所定義的類別中找到方法，以代表軟體或硬體的資料。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-105">The method is found in a class defined by a provider to represent data from software or hardware.</span></span> <span data-ttu-id="9ac2b-106">例如， [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 類別具有可啟動、停止、繼續、暫停及變更服務的方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-106">For example, the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class has methods to start, stop, resume, pause, and change services.</span></span>

<span data-ttu-id="9ac2b-107">提供者方法不應與下列類型的方法混淆：</span><span class="sxs-lookup"><span data-stu-id="9ac2b-107">Provider methods should not be confused with the following types of methods:</span></span>

-   <span data-ttu-id="9ac2b-108">[WMI 系統類別](wmi-system-classes.md)上的方法，例如 [**\_ \_ SystemSecurity**](--systemsecurity.md)上的 [**GetSD**](--systemsecurity-getsd.md)方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-108">Methods on [WMI system classes](wmi-system-classes.md), such as the [**GetSD**](--systemsecurity-getsd.md) method on [**\_\_SystemSecurity**](--systemsecurity.md).</span></span>
-   <span data-ttu-id="9ac2b-109">[適用于 WMI 的腳本 API](scripting-api-for-wmi.md)中物件的方法，例如 [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-109">Methods on objects in the [Scripting API for WMI](scripting-api-for-wmi.md), such as [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span>
-   <span data-ttu-id="9ac2b-110">[適用于 WMI 的 COM API](com-api-for-wmi.md)中的方法，例如 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-110">Methods in the [COM API for WMI](com-api-for-wmi.md), such as [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

## <a name="calling-a-provider-method-using-scripting"></a><span data-ttu-id="9ac2b-111">使用腳本呼叫提供者方法</span><span class="sxs-lookup"><span data-stu-id="9ac2b-111">Calling a Provider Method Using Scripting</span></span>

<span data-ttu-id="9ac2b-112">任何自動化語言（例如 VBScript、PowerShell 或 Perl）都可以呼叫 WMI 方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-112">Any automation language, such as VBScript, PowerShell, or Perl, can call a WMI method.</span></span> <span data-ttu-id="9ac2b-113">某些語言可以使用 [直接存取](/windows)，但其他語言必須使用 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) 來間接執行提供者方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-113">Some languages can use [direct access](/windows), but others must use [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) to execute the provider method indirectly.</span></span>

<span id="direct_access"></span><span id="DIRECT_ACCESS"></span>

<span data-ttu-id="9ac2b-114">下列程式描述如何使用腳本 API 和直接存取來呼叫提供者方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-114">The following procedure describes how to call a provider method using the Scripting API and using direct access.</span></span>

<span data-ttu-id="9ac2b-115">**使用腳本 API 和直接存取來呼叫提供者方法**</span><span class="sxs-lookup"><span data-stu-id="9ac2b-115">**To call a provider method using the Scripting API and direct access**</span></span>

1.  <span data-ttu-id="9ac2b-116">將此方法用於 VBScript 或 PowerShell。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-116">Use this approach for VBScript or PowerShell.</span></span>
2.  <span data-ttu-id="9ac2b-117">判斷您想要執行的方法是否已執行。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-117">Determine if the method you want to execute is implemented.</span></span>

    <span data-ttu-id="9ac2b-118">某些類別有定義了提供者不支援的方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-118">Some classes have methods defined that are not supported by a provider.</span></span> <span data-ttu-id="9ac2b-119">如果未執行方法，則無法執行。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-119">If a method is not implemented, you cannot execute it.</span></span> <span data-ttu-id="9ac2b-120">您可以藉由檢查方法是否具有已 [**執行**](standard-wmi-qualifiers.md) 的辨識符號來判斷是否已執行方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-120">You can determine if a method is implemented by checking if the method has the [**Implemented**](standard-wmi-qualifiers.md) qualifier.</span></span> <span data-ttu-id="9ac2b-121">如需詳細資訊，請參閱 [Wmi 限定詞](wmi-qualifiers.md) 和 [存取 wmi 辨識符號](accessing-a-qualifier.md)。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-121">For more information, see [WMI Qualifiers](wmi-qualifiers.md) and [Accessing a WMI Qualifier](accessing-a-qualifier.md).</span></span> <span data-ttu-id="9ac2b-122">您也可以藉由執行不受支援的 Wbemtest.exe 公用程式（可在任何已安裝 WMI 的作業系統上取得）來判斷提供者類別方法是否具有所設定的已 **執行** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-122">You can also determine if a provider class method has the **Implemented** qualifier set by running the unsupported Wbemtest.exe utility, available on any operating system with WMI installed.</span></span>

3.  <span data-ttu-id="9ac2b-123">判斷您想要執行的方法是 [*靜態方法*](gloss-s.md) 或非靜態方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-123">Determine if the method you want to execute is a [*static method*](gloss-s.md) or a nonstatic method.</span></span>

    <span data-ttu-id="9ac2b-124">靜態方法只適用于 WMI 類別，而不會套用至類別的特定實例。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-124">Static methods apply only to WMI classes and not to specific instances of a class.</span></span> <span data-ttu-id="9ac2b-125">例如， [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)類別的 [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)方法是靜態方法，因為使用它來建立新的進程，而不使用這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-125">For example, the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class is a static method because use it to create a new process without an instance of this class.</span></span> <span data-ttu-id="9ac2b-126">非靜態方法只適用于類別的實例。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-126">Nonstatic methods apply only to instances of a class.</span></span> <span data-ttu-id="9ac2b-127">例如， **Win32 \_ 進程** 類別的 [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process)方法是非靜態方法，因為如果該進程的實例存在，則終止進程會有意義。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-127">For example, the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method of the **Win32\_Process** class is a nonstatic method because it only makes sense to terminate a process if an instance of that process exists.</span></span> <span data-ttu-id="9ac2b-128">您可以藉由檢查 [**靜態**](standard-wmi-qualifiers.md) 限定詞是否與方法相關聯，判斷方法是否為靜態。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-128">You can determine if a method is static by checking if the [**Static**](standard-wmi-qualifiers.md) qualifier is associated with the method.</span></span>

4.  <span data-ttu-id="9ac2b-129">取出類別或實例，其中包含您想要執行的方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-129">Retrieve the class or instance that contains the method you want to execute.</span></span>

    <span data-ttu-id="9ac2b-130">如需詳細資訊，請參閱抓取 [WMI 類別或實例資料](retrieving-class-or-instance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-130">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

5.  <span data-ttu-id="9ac2b-131">設定方法可能需要的任何安全性設定。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-131">Set up any security settings that the method may require.</span></span>

    <span data-ttu-id="9ac2b-132">您通常可以藉由檢查方法之 [**許可權**](swbemsecurity-privileges.md) 辨識符號中的值，來判斷方法所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-132">You can often determine the privileges that a method requires by examining the values in the [**Privileges**](swbemsecurity-privileges.md) qualifier of the method.</span></span> <span data-ttu-id="9ac2b-133">例如， [**Win32 \_ 作業系統**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) class [**Shutdown**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) 方法需要您設定 "SeShutdownPrivilege" 許可權。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-133">For example, the [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) class [**Shutdown**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) method requires you to set the "SeShutdownPrivilege" privilege.</span></span> <span data-ttu-id="9ac2b-134">如需詳細資訊，請參閱 [執行特殊許可權作業](executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-134">For more information, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

6.  <span data-ttu-id="9ac2b-135">呼叫方法並檢查傳回值，以判斷方法是否成功。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-135">Call the method and examine the return value to determine if the method was successful.</span></span>

<span data-ttu-id="9ac2b-136">下列程式碼範例會建立「記事本」處理常式，並使用直接存取來取得處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-136">The following code example creates a Notepad process and gets the process ID using direct access.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_Process")

Error = objWMIService.Create("notepad.exe", null, _
    null, intProcessID)
If Error = 0 Then
    Wscript.Echo "Notepad was started with a process ID of " _
       & intProcessID & "."
Else
    Wscript.Echo "Notepad could not be started due to error " _
       & Error & "."
End If  
```


```PowerShell

try
{ 
    $myProcess = ([wmiclass]&quot;win32_process&quot;).create(&quot;notepad.exe&quot;, $null, $null) 
}
catch 
{
    &quot;Notepad could not be started due to the following error:&quot; 
    $error[0]
    return 
}
#else
&quot;Notepad was started with a process ID of &quot; + $myProcess.ProcessID
```





<span id="indirect_access"></span><span id="INDIRECT_ACCESS"></span>

<span data-ttu-id="9ac2b-137">下列程式描述如何使用腳本 API 和 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)來呼叫提供者方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-137">The following procedure describes how to call a provider method using the Scripting API and the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>

<span data-ttu-id="9ac2b-138">**使用腳本 API 和 SWbemServices.ExecMethod 來呼叫提供者方法**</span><span class="sxs-lookup"><span data-stu-id="9ac2b-138">**To call a provider method using the Scripting API and SWbemServices.ExecMethod**</span></span>

1.  <span data-ttu-id="9ac2b-139">取出 WMI 類別定義來執行靜態方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-139">Retrieve the WMI class definition to execute a static method.</span></span> <span data-ttu-id="9ac2b-140">取出 WMI 類別實例，以執行非靜態方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-140">Retrieve the WMI class instance to execute a nonstatic method.</span></span>
2.  <span data-ttu-id="9ac2b-141">使用 [**swbemobjectset 搭配使用. Item**](swbemobjectset-item.md)方法，從您的類別或實例的 [**\_ SWbemObject 方法**](swbemobject-methods-.md)集合中取出要執行的方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-141">Retrieve the method to execute from the [**SWbemObject.Methods\_**](swbemobject-methods-.md) collection of your class or instance by using the [**SWbemObjectSet.Item**](swbemobjectset-item.md) method.</span></span>
3.  <span data-ttu-id="9ac2b-142">取得方法的 [**InParameters**](swbemmethod-inparameters.md) 物件，並依照 [建立 InParameters 物件](constructing-inparameters-objects.md)中所述的方式設定參數。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-142">Obtain an [**InParameters**](swbemmethod-inparameters.md) object for the method and set up the parameters as described in [Constructing InParameters Objects](constructing-inparameters-objects.md).</span></span>
4.  <span data-ttu-id="9ac2b-143">呼叫 **SWbemServices.ExecMethod** 方法來執行，並將傳回值指派給 [**SWbemObject**](swbemobject.md) 物件，以儲存輸出參數。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-143">Call the **SWbemServices.ExecMethod** method to execute and assign the return value to an [**SWbemObject**](swbemobject.md) object to store the output parameters.</span></span>
5.  <span data-ttu-id="9ac2b-144">檢查 output parameters 物件中的值，以確認方法是否正確執行。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-144">Check the values in the output parameters object to verify that the method executed correctly.</span></span>

<span data-ttu-id="9ac2b-145">下列 VBScript 程式碼範例會透過呼叫 [**SWBemServices.ExecMethod**](swbemservices-execmethod.md)，以間接方法執行與先前腳本相同的作業。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-145">The following VBScript code example performs the same operation as the previous script by the indirect approach through calling [**SWBemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")

Set objProcess = objWMIService.Get("Win32_Process")

' Obtain an InParameters object specific to 
'   the Win32_Process.Create method.
Set objInParam = _
    objProcess.Methods_("Create").inParameters.SpawnInstance_()

' Add the input parameters. 
objInParam.Properties_.item("CommandLine") = "Notepad"
objInParam.Properties_.item("CurrentDirectory") = NULL
objInParam.Properties_.item("ProcessStartupInformation") = NULL


Set objOutParams = objProcess.ExecMethod_("Create", objInParam) 
If Error = 0 Then
    Wscript.Echo "Notepad was started with a process ID of " _
       & objOutParams.ProcessId 
Else
    Wscript.Echo "Notepad could not be started due to error " & _
       objOutParams.ReturnValue
End If
```




<span data-ttu-id="9ac2b-146">下列程式說明如何使用 c + + 呼叫提供者方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-146">The following procedure describes how to call a provider method using C++.</span></span>

<span data-ttu-id="9ac2b-147">**使用 c + + 呼叫提供者方法**</span><span class="sxs-lookup"><span data-stu-id="9ac2b-147">**To call a provider method using C++**</span></span>

1.  <span data-ttu-id="9ac2b-148">連接到 WMI。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-148">Connect to WMI.</span></span>

    <span data-ttu-id="9ac2b-149">若要在 WMI 中呼叫方法，您必須先擁有與 WMI 命名空間的工作連接。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-149">To call a method in WMI, first you must have a working connection to a WMI namespace.</span></span> <span data-ttu-id="9ac2b-150">如需詳細資訊，請參閱 [使用 c + + 建立 Wmi 應用程式](creating-a-wmi-application-using-c-.md) ，以及 [初始化 wmi 應用程式的 COM](initializing-com-for-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-150">For more information, see [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md) and [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="9ac2b-151">下列範例示範如何連接至 WMI。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-151">The following example shows how to connect to WMI.</span></span> <span data-ttu-id="9ac2b-152">如需 WMI 提供者呼叫中安全性問題的詳細資訊，請參閱 [維護 Wmi 安全性](maintaining-wmi-security.md)。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-152">For more information about security issues in WMI provider calls, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

```C++
    HRESULT hr = CoInitialize(0);
        hr  =  CoInitializeSecurity(
                NULL, 
                -1, 
                NULL, 
                NULL,
                RPC_C_AUTHN_LEVEL_DEFAULT, 
                RPC_C_IMP_LEVEL_IMPERSONATE, 
                NULL, 
                EOAC_NONE, 
                NULL); 
        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
                CLSCTX_INPROC_SERVER,
                IID_IWbemLocator, (LPVOID *) &pLocator);
        hr = pLocator->ConnectServer(path, NULL, NULL, 
                NULL, 0, NULL, NULL, &pNamespace);
```

    

2.  <span data-ttu-id="9ac2b-153">呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 以抓取您想要呼叫之方法的類別定義。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-153">Call [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve the definition of the class of the method you want to call.</span></span>

    <span data-ttu-id="9ac2b-154">[**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)方法會傳回指向類別定義的 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)指標。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-154">The [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that points to the class definition.</span></span>

```C++
    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);
```

    

3.  <span data-ttu-id="9ac2b-155">若為需要輸入參數的方法，請呼叫 [**IWbemClassObject：： GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) 方法以取得輸入參數類別物件。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-155">For methods that require input parameters, call the [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) method to get the input parameter class object.</span></span>

    <span data-ttu-id="9ac2b-156">[**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) 會傳回指向輸入參數類別的 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) 指標。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-156">[**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that points to the input parameter class.</span></span>

```C++
    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL);
```

    

4.  <span data-ttu-id="9ac2b-157">呼叫 [**IWbemClassObject：： SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) 方法，以產生輸入參數類別的實例。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-157">Generate an instance of the input parameter class with a call to the [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

```C++
    hr = pInClass->SpawnInstance(0, &pInInst);
```

    

5.  <span data-ttu-id="9ac2b-158">使用 [**IWbemClassObject：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) 的 ui 方法的呼叫來設定輸入參數類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-158">Set the properties of the input parameter class with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

```C++
    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);
```

    

6.  <span data-ttu-id="9ac2b-159">呼叫 [**IWbemServices：： ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) 或 [**Iwbemservices：： ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)的呼叫來叫用方法。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-159">Invoke the method with a call to [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span></span>

    <span data-ttu-id="9ac2b-160">若為 [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)，WMI 會傳回呼叫中的任何輸出參數。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-160">For [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), WMI returns any output parameters in the call.</span></span> <span data-ttu-id="9ac2b-161">針對 [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)，WMI 會透過呼叫 [**IWbemObjectSink**](iwbemobjectsink.md)來傳回任何輸出參數。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-161">For [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), WMI returns any output parameters through a call to [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="9ac2b-162">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-162">For more information, see [Calling a Method](calling-a-method.md).</span></span>

```C++
    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
```

    

<span data-ttu-id="9ac2b-163">下列程式碼是呼叫提供者方法的完整範例。</span><span class="sxs-lookup"><span data-stu-id="9ac2b-163">The following code is a complete example for calling a provider method.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

int main(int iArgCnt, char ** argv)
{
    IWbemLocator *pLocator = NULL;
    IWbemServices *pNamespace = 0;
    IWbemClassObject * pClass = NULL;
    IWbemClassObject * pOutInst = NULL;
    IWbemClassObject * pInClass = NULL;
    IWbemClassObject * pInInst = NULL;
  
    BSTR path = SysAllocString(L"root\\default");
    BSTR ClassPath = SysAllocString(L"TestMeth");
    BSTR MethodName = SysAllocString(L"Echo");
    BSTR ArgName = SysAllocString(L"sInArg");
    BSTR Text;

    // Initialize COM and connect to WMI.

    HRESULT hr = CoInitialize(0);
    hr  =  CoInitializeSecurity(NULL, -1, NULL, NULL,RPC_C_AUTHN_LEVEL_DEFAULT, 
                                RPC_C_IMP_LEVEL_IMPERSONATE, NULL, EOAC_NONE, NULL); 
    hr = CoCreateInstance(CLSID_WbemLocator, 0, CLSCTX_INPROC_SERVER,
                          IID_IWbemLocator, (LPVOID *) &pLocator);
    hr = pLocator->ConnectServer(path, NULL, NULL, NULL, 0, NULL, NULL, &pNamespace);

    // Get the class object for the method definition.

    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);

    // Get the input-argument class object and 
    // create an instance.

    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL); 
    hr = pInClass->SpawnInstance(0, &pInInst);

    // Set the property.

    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);

    // Call the method.

    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
    
    // Display the results. Note that the return 
    // value is in the property "ReturnValue"
    // and the returned string is in the 
    // property "sOutArg".

    hr = pOutInst->GetObjectText(0, &Text);
    printf("\nThe object text is:\n%S", Text);

    // Free up resources.

    SysFreeString(path);
    SysFreeString(ClassPath);
    SysFreeString(MethodName);
    SysFreeString(ArgName);
    SysFreeString(Text);
    pClass->Release();
    pInInst->Release();
    pInClass->Release();
    pOutInst->Release();
    pLocator->Release();
    pNamespace->Release();
    CoUninitialize();
    printf("Terminating normally\n");
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="9ac2b-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ac2b-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ac2b-165">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="9ac2b-165">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
