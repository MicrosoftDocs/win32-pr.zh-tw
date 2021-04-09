---
description: 您可以使用本主題中的程式和程式碼範例來建立完整的 WMI 用戶端應用程式，以執行 COM 初始化、連接到本機電腦上的 WMI、取出資料半同步方式，然後清除。
ms.assetid: 35dc97aa-dcef-48c1-af8b-ce43e3cf1d3e
ms.tgt_platform: multiple
title: 範例：從本機電腦取得 WMI 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840cd4ada941bdfd8ba7fca9b8ca9393c0b5eb55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848741"
---
# <a name="example-getting-wmi-data-from-the-local-computer"></a><span data-ttu-id="dbb5b-103">範例：從本機電腦取得 WMI 資料</span><span class="sxs-lookup"><span data-stu-id="dbb5b-103">Example: Getting WMI Data from the Local Computer</span></span>

<span data-ttu-id="dbb5b-104">您可以使用本主題中的程式和程式碼範例來建立完整的 WMI 用戶端應用程式，以執行 COM 初始化、連接到本機電腦上的 WMI、取出資料半同步方式，然後清除。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on the local computer, retrieves data semisynchronously, and then cleans up.</span></span> <span data-ttu-id="dbb5b-105">這個範例會取得本機電腦上的作業系統名稱，並加以顯示。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-105">This example gets the name of the operating system on the local computer and displays it.</span></span> <span data-ttu-id="dbb5b-106">若要從遠端電腦取出資料，請參閱 [範例：從遠端電腦取得 WMI 資料](example--getting-wmi-data-from-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-106">To retrieve data from a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span> <span data-ttu-id="dbb5b-107">若要以非同步方式取得資料，請參閱 [範例：以非同步方式從本機電腦取得 WMI 資料](example--getting-wmi-data-from-the-local-computer-asynchronously.md)。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-107">For getting the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

<span data-ttu-id="dbb5b-108">下列程式是用來執行 WMI 應用程式。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-108">The following procedure is used to execute the WMI application.</span></span> <span data-ttu-id="dbb5b-109">步驟1到5包含設定和連線至 WMI 所需的所有步驟，而步驟6和7則是查詢及接收資料的位置。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-109">Steps 1 through 5 contain all the steps required to set up and connect to WMI, and steps 6 and 7 are where data is queried and received.</span></span>

1.  <span data-ttu-id="dbb5b-110">使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)的呼叫初始化 COM 參數。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-110">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="dbb5b-111">如需詳細資訊，請參閱 [初始化 WMI 應用程式的 COM](initializing-com-for-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-111">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="dbb5b-112">藉由呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)來初始化 COM 進程安全性。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-112">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="dbb5b-113">如需詳細資訊，請參閱 [使用 c + + 設定預設進程安全性層級](setting-the-default-process-security-level-using-c-.md)。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-113">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="dbb5b-114">藉由呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來取得 WMI 的初始定位器。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-114">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="dbb5b-115">如需詳細資訊，請參閱 [建立與 WMI 命名空間的連接](creating-a-connection-to-a-wmi-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-115">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="dbb5b-116">藉 [](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \\ 由呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)，取得本機電腦上根 cimv2 命名空間的 IWbemServices 指標。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-116">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the root\\cimv2 namespace on the local computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="dbb5b-117">若要連接到遠端電腦，請參閱 [範例：從遠端電腦取得 WMI 資料](example--getting-wmi-data-from-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-117">To connect to a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span>

    <span data-ttu-id="dbb5b-118">如需詳細資訊，請參閱 [建立與 WMI 命名空間的連接](creating-a-connection-to-a-wmi-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-118">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

5.  <span data-ttu-id="dbb5b-119">設定 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy 安全性，讓 WMI 服務可以藉由呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)來模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-119">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so the WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="dbb5b-120">如需詳細資訊，請參閱 [設定 WMI 連接的安全性層級](setting-the-security-levels-on-a-wmi-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-120">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

6.  <span data-ttu-id="dbb5b-121">使用 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 指標來發出 WMI 要求。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-121">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests of WMI.</span></span> <span data-ttu-id="dbb5b-122">此範例會呼叫 [**IWbemServices：： ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)來執行作業系統名稱的查詢。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-122">This example executes a query for the name of the operating system by calling [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="dbb5b-123">下列 WQL 查詢是其中一個方法引數。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-123">The following WQL query is one of the method arguments.</span></span>

    `SELECT * FROM Win32_OperatingSystem`

    <span data-ttu-id="dbb5b-124">此查詢的結果會儲存在 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) 指標中。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-124">The result of this query is stored in an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer.</span></span> <span data-ttu-id="dbb5b-125">這可讓您使用 **IEnumWbemClassObject** 介面來半同步方式查詢中的資料物件。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-125">This allows the data objects from the query to be retrieved semisynchronously with the **IEnumWbemClassObject** interface.</span></span> <span data-ttu-id="dbb5b-126">如需詳細資訊，請參閱 [列舉 WMI](enumerating-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-126">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span> <span data-ttu-id="dbb5b-127">若要以非同步方式取得資料，請參閱 [範例：以非同步方式從本機電腦取得 WMI 資料](example--getting-wmi-data-from-the-local-computer-asynchronously.md)。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-127">For getting the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

    <span data-ttu-id="dbb5b-128">如需對 WMI 提出要求的詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)、 [查詢 WMI](querying-wmi.md)，以及 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-128">For more information about making requests to WMI, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Querying WMI](querying-wmi.md), and [Calling a Method](calling-a-method.md).</span></span>

7.  <span data-ttu-id="dbb5b-129">取得並顯示 WQL 查詢的資料。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-129">Get and display the data from the WQL query.</span></span> <span data-ttu-id="dbb5b-130">[**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)指標會連結到查詢所傳回的資料物件，而且可以使用 [**IEnumWbemClassObject：： Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next)方法來抓取資料物件。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-130">The [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer is linked to the data objects that the query returned, and the data objects can be retrieved with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span> <span data-ttu-id="dbb5b-131">這個方法會將資料物件連結至傳遞給方法的 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) 指標。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-131">This method links the data objects to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that is passed into the method.</span></span> <span data-ttu-id="dbb5b-132">您可以使用 [**IWbemClassObject：： get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) 方法，從資料物件取得所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-132">Use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method to get the desired information from the data objects.</span></span>

    <span data-ttu-id="dbb5b-133">下列程式碼範例會用來從資料物件取得 Name 屬性，它會提供作業系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-133">The following code example is used to get the Name property from the data object, which provides the name of the operating system.</span></span>

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    ```

    

    <span data-ttu-id="dbb5b-134">當 Name 屬性的值儲存在 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 變數 vtProp 之後，就可以對使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-134">After the value of the Name property is stored in the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable vtProp, it can then be displayed to the user.</span></span>

    <span data-ttu-id="dbb5b-135">如需詳細資訊，請參閱 [列舉 WMI](enumerating-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-135">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="dbb5b-136">下列程式碼範例會從本機電腦抓取 WMI 資料半同步方式。</span><span class="sxs-lookup"><span data-stu-id="dbb5b-136">The following code example retrieves WMI data semisynchronously from a local computer.</span></span>


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
        -1,                          // COM authentication
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
        return 1;                    // Program has failed.
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
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the root\cimv2 namespace with
    // the current user and obtain pointer pSvc
    // to make IWbemServices calls.
    hres = pLoc->ConnectServer(
         _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
         NULL,                    // User name. NULL = current user
         NULL,                    // User password. NULL = current
         0,                       // Locale. NULL indicates current
         NULL,                    // Security flags.
         0,                       // Authority (for example, Kerberos)
         0,                       // Context object 
         &pSvc                    // pointer to IWbemServices proxy
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
    // Set security levels on the proxy -------------------------

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

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("SELECT * FROM Win32_OperatingSystem"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: -------------------------------------------------
    // Get the data from the query in step 6 -------------------
 
    IWbemClassObject *pclsObj = NULL;
    ULONG uReturn = 0;
   
    while (pEnumerator)
    {
        HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
            &pclsObj, &uReturn);

        if(0 == uReturn)
        {
            break;
        }

        VARIANT vtProp;

        // Get the value of the Name property
        hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
        wcout << " OS Name : " << vtProp.bstrVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
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



 

 
