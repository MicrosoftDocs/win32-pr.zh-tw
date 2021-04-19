---
description: 您可以使用本主題中的程式和程式碼範例來建立完整的 WMI 用戶端應用程式，以執行 COM 初始化、連接到本機電腦上的 WMI、讀取一些資料，以及清除。
ms.assetid: d80bcf9f-e57c-499f-b7b8-cf25678c5a82
ms.tgt_platform: multiple
title: 範例：建立 WMI 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e76836090d09ecee413da34d9a15381b9d0a891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998091"
---
# <a name="example-creating-a-wmi-application"></a><span data-ttu-id="e22c3-103">範例：建立 WMI 應用程式</span><span class="sxs-lookup"><span data-stu-id="e22c3-103">Example: Creating a WMI Application</span></span>

<span data-ttu-id="e22c3-104">您可以使用本主題中的程式和程式碼範例來建立完整的 WMI 用戶端應用程式，以執行 COM 初始化、連接到本機電腦上的 WMI、讀取一些資料，以及清除。</span><span class="sxs-lookup"><span data-stu-id="e22c3-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on the local computer, reads some data, and cleans up.</span></span> <span data-ttu-id="e22c3-105">[連接至遠端電腦上的 WMI 時](connecting-to-wmi-on-a-remote-computer.md) ，會說明如何從遠端電腦取得資料。</span><span class="sxs-lookup"><span data-stu-id="e22c3-105">[Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md) describes how to obtain data from remote computers.</span></span>

<span data-ttu-id="e22c3-106">下列套裝程式含所有 c + + WMI 應用程式所需的所有步驟。</span><span class="sxs-lookup"><span data-stu-id="e22c3-106">This following procedure includes all of the steps that are required by all C++ WMI applications.</span></span>

1.  <span data-ttu-id="e22c3-107">使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)的呼叫初始化 COM 參數。</span><span class="sxs-lookup"><span data-stu-id="e22c3-107">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="e22c3-108">如需詳細資訊，請參閱 [初始化 WMI 應用程式的 COM](initializing-com-for-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="e22c3-108">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="e22c3-109">藉由呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)來初始化 COM 進程安全性。</span><span class="sxs-lookup"><span data-stu-id="e22c3-109">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="e22c3-110">如需詳細資訊，請參閱 [使用 c + + 設定預設進程安全性層級](setting-the-default-process-security-level-using-c-.md)。</span><span class="sxs-lookup"><span data-stu-id="e22c3-110">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="e22c3-111">藉由呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)，取得指定主機電腦上命名空間的 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)指標（在簡單案例中為本機電腦）。</span><span class="sxs-lookup"><span data-stu-id="e22c3-111">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for a namespace on a specified host computer—the local computer in the simple case—by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

    <span data-ttu-id="e22c3-112">若要連接到遠端電腦（例如電腦 \_ a），請使用下列物件路徑參數：</span><span class="sxs-lookup"><span data-stu-id="e22c3-112">To connect to a remote computer, for example Computer\_A, use the following object path parameter:</span></span>

    ```C++
    _bstr_t(L"\\COMPUTER_A\ROOT\\CIMV2")
    ```

    

    <span data-ttu-id="e22c3-113">如需詳細資訊，請參閱 [建立與 WMI 命名空間的連接](creating-a-connection-to-a-wmi-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="e22c3-113">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="e22c3-114">設定 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy 安全性，讓 WMI 服務可以藉由呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)來模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="e22c3-114">Set the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="e22c3-115">如需詳細資訊，請參閱 [設定 WMI 連接的安全性層級](setting-the-security-levels-on-a-wmi-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="e22c3-115">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

5.  <span data-ttu-id="e22c3-116">使用 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 指標來發出 WMI 要求。</span><span class="sxs-lookup"><span data-stu-id="e22c3-116">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests of WMI.</span></span> <span data-ttu-id="e22c3-117">例如，查詢所有的 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 實例，以判斷哪些服務已停止。</span><span class="sxs-lookup"><span data-stu-id="e22c3-117">For example, querying for all the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) instances to determine which services are stopped.</span></span>

    <span data-ttu-id="e22c3-118">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)、 [查詢 Wmi](querying-wmi.md)，以及 [接收 wmi 事件](receiving-a-wmi-event.md)。</span><span class="sxs-lookup"><span data-stu-id="e22c3-118">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Querying WMI](querying-wmi.md), and [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

6.  <span data-ttu-id="e22c3-119">清除物件和 COM。</span><span class="sxs-lookup"><span data-stu-id="e22c3-119">Clean up objects and COM.</span></span>

    <span data-ttu-id="e22c3-120">如需詳細資訊，請參閱 [清除和關閉 WMI 應用程式](cleaning-up-and-shutting-down-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="e22c3-120">For more information, see [Cleaning up and Shutting Down a WMI Application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

<span data-ttu-id="e22c3-121">下列範例程式碼是完整的 WMI 用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="e22c3-121">The following example code is a complete WMI client application.</span></span>


```C++

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int argc, char **argv)
{
    HRESULT hres;

    // Initialize COM.
    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. " 
            << "Error code = 0x" 
            << hex << hres << endl;
        return 1;              // Program has failed.
    }

    // Initialize 
    hres =  CoInitializeSecurity(
        NULL,     
        -1,      // COM negotiates service                  
        NULL,    // Authentication services
        NULL,    // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,    // authentication
        RPC_C_IMP_LEVEL_IMPERSONATE,  // Impersonation
        NULL,             // Authentication info 
        EOAC_NONE,        // Additional capabilities
        NULL              // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. " 
            << "Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;          // Program has failed.
    }

    // Obtain the initial locator to Windows Management
    // on a particular host computer.
    IWbemLocator *pLoc = 0;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object. "
            << "Error code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;       // Program has failed.
    }

    IWbemServices *pSvc = 0;

    // Connect to the root\cimv2 namespace with the
    // current user and obtain pointer pSvc
    // to make IWbemServices calls.

    hres = pLoc->ConnectServer(
        
        _bstr_t(L"ROOT\\CIMV2"), // WMI namespace
        NULL,                    // User name
        NULL,                    // User password
        0,                       // Locale
        NULL,                    // Security flags                 
        0,                       // Authority       
        0,                       // Context object
        &pSvc                    // IWbemServices proxy
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

    // Set the IWbemServices proxy so that impersonation
    // of the user (client) occurs.
    hres = CoSetProxyBlanket(
       
       pSvc,                         // the proxy to set
       RPC_C_AUTHN_WINNT,            // authentication service
       RPC_C_AUTHZ_NONE,             // authorization service
       NULL,                         // Server principal name
       RPC_C_AUTHN_LEVEL_CALL,       // authentication level
       RPC_C_IMP_LEVEL_IMPERSONATE,  // impersonation level
       NULL,                         // client identity 
       EOAC_NONE                     // proxy capabilities     
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


    // Use the IWbemServices pointer to make requests of WMI. 
    // Make requests here:

    // For example, query for all the running processes
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("SELECT * FROM Win32_Process"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for processes failed. "
             << "Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }
    else
    { 
        IWbemClassObject *pclsObj;
        ULONG uReturn = 0;
   
        while (pEnumerator)
        {
            hres = pEnumerator->Next(WBEM_INFINITE, 1, 
                &pclsObj, &uReturn);

            if(0 == uReturn)
            {
                break;
            }

            VARIANT vtProp;

            // Get the value of the Name property
            hres = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
            wcout << "Process Name : " << vtProp.bstrVal << endl;
            VariantClear(&vtProp);
            
            pclsObj->Release();
            pclsObj = NULL;
        }
         
    }
 
    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();  
    
    CoUninitialize();

    return 0;   // Program successfully completed.
}
```



 

 
