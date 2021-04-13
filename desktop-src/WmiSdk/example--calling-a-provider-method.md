---
description: 您可以使用本主題中的程式和程式碼範例來建立完整的 WMI 用戶端應用程式，以執行 COM 初始化、連接到本機電腦上的 WMI、呼叫提供者方法，然後清除。
ms.assetid: ee8faa14-74ec-49a2-88d6-187627c40071
ms.tgt_platform: multiple
title: 範例：呼叫提供者方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa20d6e3a90b7d2f7826d7f62b4092bc18d2d917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319671"
---
# <a name="example-calling-a-provider-method"></a><span data-ttu-id="66fff-103">範例：呼叫提供者方法</span><span class="sxs-lookup"><span data-stu-id="66fff-103">Example: Calling a Provider Method</span></span>

<span data-ttu-id="66fff-104">您可以使用本主題中的程式和程式碼範例來建立完整的 WMI 用戶端應用程式，以執行 COM 初始化、連接到本機電腦上的 WMI、呼叫提供者方法，然後清除。</span><span class="sxs-lookup"><span data-stu-id="66fff-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on the local computer, calls a provider method, and then cleans up.</span></span> <span data-ttu-id="66fff-105">[**Win32 \_ Process：： Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)方法可用來在新的進程中啟動 Notepad.exe。</span><span class="sxs-lookup"><span data-stu-id="66fff-105">The [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method is used to start Notepad.exe in a new process.</span></span>

<span data-ttu-id="66fff-106">下列程式是用來執行 WMI 應用程式。</span><span class="sxs-lookup"><span data-stu-id="66fff-106">The following procedure is used to execute the WMI application.</span></span> <span data-ttu-id="66fff-107">步驟1到5包含設定和連線至 WMI 所需的所有步驟，而6是呼叫提供者方法的位置。</span><span class="sxs-lookup"><span data-stu-id="66fff-107">Steps 1 through 5 contain all of the steps needed to set up and connect to WMI, and 6 is where the provider method is called.</span></span>

<span data-ttu-id="66fff-108">**呼叫提供者方法**</span><span class="sxs-lookup"><span data-stu-id="66fff-108">**To call a provider method**</span></span>

1.  <span data-ttu-id="66fff-109">使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)的呼叫初始化 COM 參數。</span><span class="sxs-lookup"><span data-stu-id="66fff-109">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="66fff-110">如需詳細資訊，請參閱 [初始化 WMI 應用程式的 COM](initializing-com-for-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="66fff-110">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="66fff-111">藉由呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)來初始化 COM 進程安全性。</span><span class="sxs-lookup"><span data-stu-id="66fff-111">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="66fff-112">如需詳細資訊，請參閱 [使用 c + + 設定預設進程安全性層級](setting-the-default-process-security-level-using-c-.md)。</span><span class="sxs-lookup"><span data-stu-id="66fff-112">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="66fff-113">藉由呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來取得 WMI 的初始定位器。</span><span class="sxs-lookup"><span data-stu-id="66fff-113">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="66fff-114">如需詳細資訊，請參閱 [建立與 WMI 命名空間的連接](creating-a-connection-to-a-wmi-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="66fff-114">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="66fff-115">藉 [](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \\ 由呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)，取得本機電腦上根 cimv2 命名空間的 IWbemServices 指標。</span><span class="sxs-lookup"><span data-stu-id="66fff-115">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the root\\cimv2 namespace on the local computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="66fff-116">若要連接到遠端電腦，請參閱 [範例：從遠端電腦取得 WMI 資料](example--getting-wmi-data-from-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="66fff-116">To connect to a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span>

    <span data-ttu-id="66fff-117">如需詳細資訊，請參閱 [建立與 WMI 命名空間的連接](creating-a-connection-to-a-wmi-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="66fff-117">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

5.  <span data-ttu-id="66fff-118">設定 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy 安全性，讓 WMI 服務可以藉由呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)來模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="66fff-118">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so the WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="66fff-119">如需詳細資訊，請參閱 [設定 WMI 連接的安全性層級](setting-the-security-levels-on-a-wmi-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="66fff-119">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

6.  <span data-ttu-id="66fff-120">使用 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 指標對 WMI 提出要求。</span><span class="sxs-lookup"><span data-stu-id="66fff-120">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests to WMI.</span></span> <span data-ttu-id="66fff-121">此範例會使用 [**IWbemServices：： ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) 來呼叫提供者方法 [**Win32 \_ Process：： Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)。</span><span class="sxs-lookup"><span data-stu-id="66fff-121">This example uses [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) to call the provider method [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span>

    <span data-ttu-id="66fff-122">如需對 WMI 提出要求的詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md) 和 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="66fff-122">For more information about making requests to WMI, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="66fff-123">如果提供者方法具有任何 in 參數或 out 參數，則必須將參數的值提供給 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) 指標。</span><span class="sxs-lookup"><span data-stu-id="66fff-123">If the provider method has any in-parameters or out-parameters, then values of the parameters must be given to [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointers.</span></span> <span data-ttu-id="66fff-124">對於 in 參數，您必須產生 in 參數定義的實例，然後設定這些新實例的值。</span><span class="sxs-lookup"><span data-stu-id="66fff-124">For in-parameters, you must spawn an instance of the in-parameter definitions, and then set the values of these new instances.</span></span> <span data-ttu-id="66fff-125">[**Win32 \_ Process：： Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)方法需要 *命令列* in 參數的值，才能正常執行。</span><span class="sxs-lookup"><span data-stu-id="66fff-125">The [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method requires a value for the *CommandLine* in-parameter to execute properly.</span></span>

    <span data-ttu-id="66fff-126">下列程式碼範例會建立 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) 指標、產生 Win32 進程的新實例 [**\_ ：： Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) in 參數定義，然後將 *命令列* in 參數的值設定為 Notepad.exe。</span><span class="sxs-lookup"><span data-stu-id="66fff-126">The following code example creates an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer, spawns a new instance of the [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) in-parameter definitions, and then sets the value of the *CommandLine* in-parameter to Notepad.exe.</span></span>

    ```C++
    // Set up to call the Win32_Process::Create method
    BSTR MethodName = SysAllocString(L"Create");
    BSTR ClassName = SysAllocString(L"Win32_Process");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, NULL);

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in-parameters
    VARIANT varCommand;
    varCommand.vt = VT_BSTR;
    varCommand.bstrVal = _bstr_t(L"notepad.exe");

    // Store the value for the in-parameters
    hres = pClassInstance->Put(L"CommandLine", 0,
        &varCommand, 0);
    wprintf(L"The command is: %s\n", V_BSTR(&varCommand));
    ```

    

    <span data-ttu-id="66fff-127">下列程式碼範例顯示如何將 [**Win32 \_ Process：： Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) 方法 out 參數提供給 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) 指標。</span><span class="sxs-lookup"><span data-stu-id="66fff-127">The following code example shows how the [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method out-parameters are given to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer.</span></span> <span data-ttu-id="66fff-128">Out 參數值是使用 [**IWbemClassObject：： Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) 方法來取得，並儲存在 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 變數中，以便向使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="66fff-128">The out-parameter value is obtained with the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method and stored in a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable so that it can be displayed to the user.</span></span>

    ```C++
    // Execute Method
    IWbemClassObject* pOutParams = NULL;
    hres = pSvc->ExecMethod(ClassName, MethodName, 0,
        NULL, pClassInstance, &pOutParams, NULL);

    VARIANT varReturnValue;
    hres = pOutParams->Get(_bstr_t(L"ReturnValue"), 0, 
        &varReturnValue, NULL, 0);
    ```

    

<span data-ttu-id="66fff-129">下列程式碼範例顯示如何使用 WMI 呼叫提供者方法。</span><span class="sxs-lookup"><span data-stu-id="66fff-129">The following code example shows how to call a provider method using WMI.</span></span>


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

    // set up to call the Win32_Process::Create method
    BSTR MethodName = SysAllocString(L"Create");
    BSTR ClassName = SysAllocString(L"Win32_Process");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, NULL);

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in parameters
    VARIANT varCommand;
    varCommand.vt = VT_BSTR;
    varCommand.bstrVal = _bstr_t(L"notepad.exe");

    // Store the value for the in parameters
    hres = pClassInstance->Put(L"CommandLine", 0,
        &varCommand, 0);
    wprintf(L"The command is: %s\n", V_BSTR(&varCommand));

    // Execute Method
    IWbemClassObject* pOutParams = NULL;
    hres = pSvc->ExecMethod(ClassName, MethodName, 0,
    NULL, pClassInstance, &pOutParams, NULL);

    if (FAILED(hres))
    {
        cout << "Could not execute method. Error code = 0x" 
             << hex << hres << endl;
        VariantClear(&varCommand);
        SysFreeString(ClassName);
        SysFreeString(MethodName);
        pClass->Release();
        pClassInstance->Release();
        pInParamsDefinition->Release();
        pOutParams->Release();
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // To see what the method returned,
    // use the following code.  The return value will
    // be in &varReturnValue
    VARIANT varReturnValue;
    hres = pOutParams->Get(_bstr_t(L"ReturnValue"), 0, 
        &varReturnValue, NULL, 0);


    // Clean up
    //--------------------------
    VariantClear(&varCommand);
    VariantClear(&varReturnValue);
    SysFreeString(ClassName);
    SysFreeString(MethodName);
    pClass->Release();
    pClassInstance->Release();
    pInParamsDefinition->Release();
    pOutParams->Release();
    pLoc->Release();
    pSvc->Release();
    CoUninitialize();
    return 0;
}
```



 

 
