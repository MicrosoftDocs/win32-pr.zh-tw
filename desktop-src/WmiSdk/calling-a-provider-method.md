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
# <a name="calling-a-provider-method"></a>呼叫提供者方法

提供者方法是由 Windows Management Instrumentation (WMI) 提供者所執行的方法。 在提供者所定義的類別中找到方法，以代表軟體或硬體的資料。 例如， [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 類別具有可啟動、停止、繼續、暫停及變更服務的方法。

提供者方法不應與下列類型的方法混淆：

-   [WMI 系統類別](wmi-system-classes.md)上的方法，例如 [**\_ \_ SystemSecurity**](--systemsecurity.md)上的 [**GetSD**](--systemsecurity-getsd.md)方法。
-   [適用于 WMI 的腳本 API](scripting-api-for-wmi.md)中物件的方法，例如 [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)。
-   [適用于 WMI 的 COM API](com-api-for-wmi.md)中的方法，例如 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)。

## <a name="calling-a-provider-method-using-scripting"></a>使用腳本呼叫提供者方法

任何自動化語言（例如 VBScript、PowerShell 或 Perl）都可以呼叫 WMI 方法。 某些語言可以使用 [直接存取](/windows)，但其他語言必須使用 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) 來間接執行提供者方法。

<span id="direct_access"></span><span id="DIRECT_ACCESS"></span>

下列程式描述如何使用腳本 API 和直接存取來呼叫提供者方法。

**使用腳本 API 和直接存取來呼叫提供者方法**

1.  將此方法用於 VBScript 或 PowerShell。
2.  判斷您想要執行的方法是否已執行。

    某些類別有定義了提供者不支援的方法。 如果未執行方法，則無法執行。 您可以藉由檢查方法是否具有已 [**執行**](standard-wmi-qualifiers.md) 的辨識符號來判斷是否已執行方法。 如需詳細資訊，請參閱 [Wmi 限定詞](wmi-qualifiers.md) 和 [存取 wmi 辨識符號](accessing-a-qualifier.md)。 您也可以藉由執行不受支援的 Wbemtest.exe 公用程式（可在任何已安裝 WMI 的作業系統上取得）來判斷提供者類別方法是否具有所設定的已 **執行** 限定詞。

3.  判斷您想要執行的方法是 [*靜態方法*](gloss-s.md) 或非靜態方法。

    靜態方法只適用于 WMI 類別，而不會套用至類別的特定實例。 例如， [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)類別的 [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)方法是靜態方法，因為使用它來建立新的進程，而不使用這個類別的實例。 非靜態方法只適用于類別的實例。 例如， **Win32 \_ 進程** 類別的 [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process)方法是非靜態方法，因為如果該進程的實例存在，則終止進程會有意義。 您可以藉由檢查 [**靜態**](standard-wmi-qualifiers.md) 限定詞是否與方法相關聯，判斷方法是否為靜態。

4.  取出類別或實例，其中包含您想要執行的方法。

    如需詳細資訊，請參閱抓取 [WMI 類別或實例資料](retrieving-class-or-instance-data.md)。

5.  設定方法可能需要的任何安全性設定。

    您通常可以藉由檢查方法之 [**許可權**](swbemsecurity-privileges.md) 辨識符號中的值，來判斷方法所需的許可權。 例如， [**Win32 \_ 作業系統**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) class [**Shutdown**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) 方法需要您設定 "SeShutdownPrivilege" 許可權。 如需詳細資訊，請參閱 [執行特殊許可權作業](executing-privileged-operations.md)。

6.  呼叫方法並檢查傳回值，以判斷方法是否成功。

下列程式碼範例會建立「記事本」處理常式，並使用直接存取來取得處理序識別碼。


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

下列程式描述如何使用腳本 API 和 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)來呼叫提供者方法。

**使用腳本 API 和 SWbemServices.ExecMethod 來呼叫提供者方法**

1.  取出 WMI 類別定義來執行靜態方法。 取出 WMI 類別實例，以執行非靜態方法。
2.  使用 [**swbemobjectset 搭配使用. Item**](swbemobjectset-item.md)方法，從您的類別或實例的 [**\_ SWbemObject 方法**](swbemobject-methods-.md)集合中取出要執行的方法。
3.  取得方法的 [**InParameters**](swbemmethod-inparameters.md) 物件，並依照 [建立 InParameters 物件](constructing-inparameters-objects.md)中所述的方式設定參數。
4.  呼叫 **SWbemServices.ExecMethod** 方法來執行，並將傳回值指派給 [**SWbemObject**](swbemobject.md) 物件，以儲存輸出參數。
5.  檢查 output parameters 物件中的值，以確認方法是否正確執行。

下列 VBScript 程式碼範例會透過呼叫 [**SWBemServices.ExecMethod**](swbemservices-execmethod.md)，以間接方法執行與先前腳本相同的作業。


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




下列程式說明如何使用 c + + 呼叫提供者方法。

**使用 c + + 呼叫提供者方法**

1.  連接到 WMI。

    若要在 WMI 中呼叫方法，您必須先擁有與 WMI 命名空間的工作連接。 如需詳細資訊，請參閱 [使用 c + + 建立 Wmi 應用程式](creating-a-wmi-application-using-c-.md) ，以及 [初始化 wmi 應用程式的 COM](initializing-com-for-a-wmi-application.md)。

    下列範例示範如何連接至 WMI。 如需 WMI 提供者呼叫中安全性問題的詳細資訊，請參閱 [維護 Wmi 安全性](maintaining-wmi-security.md)。

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

    

2.  呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 以抓取您想要呼叫之方法的類別定義。

    [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)方法會傳回指向類別定義的 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)指標。

```C++
    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);
```

    

3.  若為需要輸入參數的方法，請呼叫 [**IWbemClassObject：： GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) 方法以取得輸入參數類別物件。

    [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) 會傳回指向輸入參數類別的 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) 指標。

```C++
    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL);
```

    

4.  呼叫 [**IWbemClassObject：： SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) 方法，以產生輸入參數類別的實例。

```C++
    hr = pInClass->SpawnInstance(0, &pInInst);
```

    

5.  使用 [**IWbemClassObject：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) 的 ui 方法的呼叫來設定輸入參數類別的屬性。

```C++
    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);
```

    

6.  呼叫 [**IWbemServices：： ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) 或 [**Iwbemservices：： ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)的呼叫來叫用方法。

    若為 [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)，WMI 會傳回呼叫中的任何輸出參數。 針對 [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)，WMI 會透過呼叫 [**IWbemObjectSink**](iwbemobjectsink.md)來傳回任何輸出參數。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

```C++
    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
```

    

下列程式碼是呼叫提供者方法的完整範例。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[呼叫方法](calling-a-method.md)
</dt> </dl>

 

 
