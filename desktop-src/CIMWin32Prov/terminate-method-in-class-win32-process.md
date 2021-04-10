---
description: Terminate&\# 32;WMI 類別方法會終止進程及其所有線程。
ms.assetid: 6c6b27d4-cf9b-42d7-9136-42641ea56ee8
ms.tgt_platform: multiple
title: Win32_Process 類別的 Terminate 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Terminate
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 00300ca9656c3b732b9c294aeba9a6c626ac6e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936171"
---
# <a name="terminate-method-of-the-win32_process-class"></a>Win32 進程類別的 Terminate 方法 \_

**Terminate** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會終止進程及其所有線程。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*原因* \[在\]
</dt> <dd>

進程的結束程式碼，以及針對此呼叫而終止的所有線程。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功終止進程，則傳回 0 (零) ，以及表示錯誤的其他任何數位。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功完成** (0) 
</dt> <dt>

**拒絕存取** (2) 
</dt> <dt>

**許可權不足** (3) 
</dt> <dt>

**未知的失敗** (8) 
</dt> <dt>

 (9) **找不到路徑**
</dt> <dt>

**不正確參數** (21) 
</dt> <dt>

**其他** (22 4294967295) 
</dt> </dl>

## <a name="remarks"></a>備註

**概觀**

電腦問題通常是因為進程不再如預期般運作。 例如，進程可能會流失記憶體，或可能已停止回應使用者輸入。 當發生這類問題時，必須終止進程。 雖然這看起來似乎很簡單，但終止進程可能會因為數個因素而變得很複雜：

-   此程式可能會停止回應，因此不會再回應功能表或鍵盤命令以關閉應用程式。 這可讓一般使用者無法關閉應用程式並終止進程。
-   此進程可能是孤立的。 例如，腳本可能會建立 Word 的實例，然後在不終結該實例的情況下結束。 實際上，即使沒有可見的使用者介面，Word 仍會在電腦上繼續執行。 因為沒有使用者介面，所以沒有任何可用來終止進程的功能表或鍵盤命令。
-   您可能不知道需要終止的進程。 例如，您可能想要終止超過指定記憶體數量的所有程式。
-   因為工作管理員可讓您只終止您所建立的進程，所以即使您是電腦的系統管理員，也可能無法終止進程。

腳本可讓您克服這些潛在的障礙，讓您在電腦上有相當大的系統管理控制。 比方說，如果您懷疑使用者正在玩您組織中禁止的遊戲，您可以輕鬆地撰寫腳本來連接每部電腦、識別遊戲是否正在執行，並立即終止程式。

**使用 Terminate 方法**

您可以透過下列方式終止進程：

-   正在終止目前正在執行的進程。 例如，您可能需要終止在遠端電腦上執行的診斷程式。 如果沒有任何方法可從遠端控制應用程式，您可以直接結束該應用程式的處理常式。
-   防止進程在一開始就執行。 藉由持續監視電腦上的進程建立，您可以在啟動時立即識別並立即終止任何程式。 這提供了一種方法，可確保特定的應用程式 (例如，透過網際網路下載大型媒體檔案的程式，) 永遠不會在特定電腦上執行。

> [!Note]  
> 群組原則也可以用來限制在電腦上執行的程式。 不過，群組原則只能限制使用 [開始] 功能表或 Windows 檔案總管執行的程式;它對使用其他方法（例如命令列）啟動的程式沒有任何作用。 相較之下，WMI 可以防止進程執行，不論進程如何啟動。

 

**終止您不擁有的處理常式**

若要終止您不擁有的處理常式，請啟用 **SeDebugPrivilege** 許可權。 在 VBScript 中，您可以使用下列幾行程式碼來啟用此許可權：


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



如需在 c + + 中啟用此許可權的詳細資訊，請參閱 [在 c + + 中啟用和停用許可權](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--)。

## <a name="examples"></a>範例

TechNet 元件庫上的「 [在多部伺服器上終止](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) 執行的進程」 PowerShell 程式碼範例會終止在一或多部電腦上執行的處理常式。

下列 VBScript 範例會終止目前正在執行應用程式 Diagnose.exe 的進程。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



下列 VBScript 範例會使用暫時的事件取用者，在進程啟動時立即終止進程。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
 & " WITHIN 1 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 If objLatestProcess.TargetInstance.Name = "Download.exe" Then
 objLatestProcess.TargetInstance.Terminate()
 End If
Loop
```



下列 VBScript 程式碼範例會連接到遠端電腦，並在該電腦上終止 Notepad.exe。


```VB
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
strUser = InputBox("Enter user name") 
strPassword = InputBox("Enter password") 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
    "root\CIMV2", _ 
    strUser, _ 
    strPassword, _ 
    "MS_409", _ 
    "ntlmdomain:" + strDomain) 
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'notepad.exe'")
For Each objProcess in colProcessList
    objProcess.Terminate()
Next
```



下列 c + + 程式碼會在本機電腦上終止 Notepad.exe 進程。 在程式碼中指定 (處理序識別碼) 的或處理常式，以終止進程。 您可以在 [**Win32 \_ Process**](win32-process.md) 類別的 handle 屬性中找到這個值， (類別) 的索引鍵屬性。 藉由指定 Handle 屬性的值，您會提供要終止之類別實例的路徑。 如需有關連接到遠端電腦的詳細資訊，請參閱 [範例：從遠端電腦取得 WMI 資料](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer)。


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int iArgCnt, char ** argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
             << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------
    // Note: If you are using Windows 2000, specify -
    // the default authentication credentials for a user by using
    // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
    // parameter of CoInitializeSecurity ------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM negotiates service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
             << hex << hres << endl;
        CoUninitialize();
        return 1;                      // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object. "
             << "Err code = 0x"
             << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: ---------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(
        _bstr_t(L"ROOT\\CIMV2"), 
        NULL,
        NULL, 
        0, 
        NULL, 
        0, 
        0, 
        &pSvc
    );
     
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();
        pSvc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels for the proxy ------------------------

    hres = CoSetProxyBlanket(
        pSvc,                        // Indicates the proxy to set
        RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx 
        RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx 
        NULL,                        // Server principal name 
        RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
        NULL,                        // client identity
        EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // Set up to call the Win32_Process::Create method
    BSTR ClassName = SysAllocString(L"Win32_Process");

    /* YOU NEED TO CHANGE THE NUMBER VALUE OF THE HANDLE 
       (PROCESS ID) TO THE CORRECT VALUE OF THE PROCESS YOU 
       ARE TRYING TO TERMINATE (this provides a path to
       the class instance you are tying to terminate). */
    BSTR ClassNameInstance = SysAllocString(
        L"Win32_Process.Handle=\"3168\"");

    _bstr_t MethodName = (L"Terminate");
    BSTR ParameterName = SysAllocString(L"Reason");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    IWbemClassObject* pOutMethod = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, &pOutMethod);

    if (FAILED(hres))
    {
        cout << "Could not get the method. Error code = 0x" 
             << hex << hres << endl;
    }

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in parameters
    VARIANT pcVal;
    VariantInit(&pcVal);
    V_VT(&pcVal) = VT_I4;

    // Store the value for the in parameters
    hres = pClassInstance->Put(L"Reason", 0,
        &pcVal, 0);

    // Execute Method
    hres = pSvc->ExecMethod(ClassNameInstance, MethodName, 0,
    NULL, pClassInstance, NULL, NULL);

    if (FAILED(hres))
    {
        cout << "Could not execute method. Error code = 0x" 
             << hex << hres << endl;
        VariantClear(&pcVal);
        SysFreeString(ClassName);
        SysFreeString(MethodName);
        pClass->Release();
        pInParamsDefinition->Release();
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;           // Program has failed.
    }


    // Clean up
    //--------------------------
    VariantClear(&pcVal);
    SysFreeString(ClassName);
    SysFreeString(MethodName);
    pClass->Release();
    pInParamsDefinition->Release();
    pLoc->Release();
    pSvc->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ 進程**](win32-process.md)
</dt> <dt>

[WMI 工作：效能監視](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[WMI 工作：進程](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

