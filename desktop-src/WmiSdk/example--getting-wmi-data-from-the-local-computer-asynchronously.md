---
description: 您可以使用本主題中的程式和程式碼範例來建立完整的 WMI 用戶端應用程式，以執行 COM 初始化、連接到本機電腦上的 WMI、以非同步方式取得資料，然後清除。
ms.assetid: 1e11ca27-e67d-486c-8fc5-a10382edfff3
ms.tgt_platform: multiple
title: 範例：以非同步方式從本機電腦取得 WMI 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5acf8df91b5ff279d70a9f76f0a353df90e8ff3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115861"
---
# <a name="example-getting-wmi-data-from-the-local-computer-asynchronously"></a><span data-ttu-id="282cd-103">範例：以非同步方式從本機電腦取得 WMI 資料</span><span class="sxs-lookup"><span data-stu-id="282cd-103">Example: Getting WMI Data from the Local Computer Asynchronously</span></span>

<span data-ttu-id="282cd-104">您可以使用本主題中的程式和程式碼範例來建立完整的 WMI 用戶端應用程式，以執行 COM 初始化、連接到本機電腦上的 WMI、以非同步方式取得資料，然後清除。</span><span class="sxs-lookup"><span data-stu-id="282cd-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on the local computer, gets data asynchronously, and then cleans up.</span></span> <span data-ttu-id="282cd-105">這個範例會取得本機電腦上的作業系統名稱，並加以顯示。</span><span class="sxs-lookup"><span data-stu-id="282cd-105">This example gets the name of the operating system on the local computer and displays it.</span></span>

<span data-ttu-id="282cd-106">下列程式是用來執行 WMI 應用程式。</span><span class="sxs-lookup"><span data-stu-id="282cd-106">The following procedure is used to execute the WMI application.</span></span> <span data-ttu-id="282cd-107">步驟1到5包含設定和連線至 WMI 所需的所有步驟，而步驟6和7則是以非同步方式抓取作業系統名稱。</span><span class="sxs-lookup"><span data-stu-id="282cd-107">Steps 1 through 5 contain all of the steps required to set up and connect to WMI, and steps 6 and seven are where the operating system name is retrieved asynchronously.</span></span>

<span data-ttu-id="282cd-108">**以非同步方式從本機電腦取得 WMI 資料**</span><span class="sxs-lookup"><span data-stu-id="282cd-108">**To get WMI data from the local computer asynchronously**</span></span>

1.  <span data-ttu-id="282cd-109">使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)的呼叫初始化 COM 參數。</span><span class="sxs-lookup"><span data-stu-id="282cd-109">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="282cd-110">如需詳細資訊，請參閱 [初始化 WMI 應用程式的 COM](initializing-com-for-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="282cd-110">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="282cd-111">藉由呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)來初始化 COM 進程安全性。</span><span class="sxs-lookup"><span data-stu-id="282cd-111">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="282cd-112">如需詳細資訊，請參閱 [使用 c + + 設定預設進程安全性層級](setting-the-default-process-security-level-using-c-.md)。</span><span class="sxs-lookup"><span data-stu-id="282cd-112">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="282cd-113">藉由呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來取得 WMI 的初始定位器。</span><span class="sxs-lookup"><span data-stu-id="282cd-113">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="282cd-114">如需詳細資訊，請參閱 [建立與 WMI 命名空間的連接](creating-a-connection-to-a-wmi-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="282cd-114">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="282cd-115">藉 [](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \\ 由呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)，取得本機電腦上根 cimv2 命名空間的 IWbemServices 指標。</span><span class="sxs-lookup"><span data-stu-id="282cd-115">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the root\\cimv2 namespace on the local computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="282cd-116">如需有關如何連接到遠端電腦的詳細資訊，請參閱 [範例：從遠端電腦取得 WMI 資料](example--getting-wmi-data-from-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="282cd-116">For more information about how to connect to a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span>

    <span data-ttu-id="282cd-117">如需詳細資訊，請參閱 [建立與 WMI 命名空間的連接](creating-a-connection-to-a-wmi-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="282cd-117">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

5.  <span data-ttu-id="282cd-118">設定 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy 安全性，讓 WMI 服務可以藉由呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)來模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="282cd-118">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so the WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="282cd-119">如需詳細資訊，請參閱 [設定 WMI 連接的安全性層級](setting-the-security-levels-on-a-wmi-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="282cd-119">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

6.  <span data-ttu-id="282cd-120">使用 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 指標對 WMI 提出要求。</span><span class="sxs-lookup"><span data-stu-id="282cd-120">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests to WMI.</span></span> <span data-ttu-id="282cd-121">這個範例會使用 [**IWbemServices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) 方法，以非同步方式接收資料。</span><span class="sxs-lookup"><span data-stu-id="282cd-121">This example uses the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method to receive the data asynchronously.</span></span> <span data-ttu-id="282cd-122">每當您以非同步方式接收資料時，您必須提供 [**IWbemObjectSink**](iwbemobjectsink.md)的執行。</span><span class="sxs-lookup"><span data-stu-id="282cd-122">Whenever you receive data asynchronously, you must provide an implementation of [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="282cd-123">這個範例會提供 QuerySink 類別中的實作為。</span><span class="sxs-lookup"><span data-stu-id="282cd-123">This example provides the implementation in the QuerySink class.</span></span> <span data-ttu-id="282cd-124">此類別的執行程式碼和標頭檔碼會在主要範例之後提供。</span><span class="sxs-lookup"><span data-stu-id="282cd-124">The implementation code and header file code for this class are provided following the main example.</span></span> <span data-ttu-id="282cd-125">每當接收到資料時， **IWbemServices：： ExecQueryAsync** 方法都會呼叫 QuerySink：：指示方法。</span><span class="sxs-lookup"><span data-stu-id="282cd-125">The **IWbemServices::ExecQueryAsync** method calls the QuerySink::Indicate method whenever the data is received.</span></span>

    <span data-ttu-id="282cd-126">如需有關如何建立 WMI 要求的詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md) 和 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="282cd-126">For more information about how to create a WMI request, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Calling a Method](calling-a-method.md).</span></span>

7.  <span data-ttu-id="282cd-127">等候資料以非同步方式取出。</span><span class="sxs-lookup"><span data-stu-id="282cd-127">Wait for the data to be retrieved asynchronously.</span></span> <span data-ttu-id="282cd-128">使用 [**IWbemServices：： CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) 方法手動停止非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="282cd-128">Use the [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method to manually stop the asynchronous call.</span></span>

<span data-ttu-id="282cd-129">下列程式碼範例會以非同步方式從本機電腦取得 WMI 資料。</span><span class="sxs-lookup"><span data-stu-id="282cd-129">The following code example gets WMI data from the local computer asynchronously.</span></span>


```C++
#include "querysink.h"


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

    hres =  CoInitializeSecurity(NULL, 
                                 -1,                          // COM authentication
                                 NULL,                        // Authentication services
                                 NULL,                        // Reserved
                                 RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
                                 RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
                                 NULL,                        // Authentication info
                                 EOAC_NONE,                   // Additional capabilities 
                                 NULL);                       // Reserved

                      
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
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(_bstr_t(L"ROOT\\CIMV2"), 
                               NULL,
                               NULL,
                               0,
                               NULL,
                               0,
                               0, 
                               &pSvc);
    
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

    hres = CoSetProxyBlanket(pSvc,                        // Indicates the proxy to set
                             RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx
                             RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx
                             NULL,                        // Server principal name 
                             RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
                             RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
                             NULL,                        // client identity
                             EOAC_NONE);                  // proxy capabilities 

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

    // For example, get the name of the operating system.
    // The IWbemService::ExecQueryAsync method will call
    // the QuerySink::Indicate method when it receives a result
    // and the QuerySink::Indicate method will display the OS name
    QuerySink* pResponseSink = new QuerySink();
    pResponseSink->AddRef();
    hres = pSvc->ExecQueryAsync(bstr_t("WQL"), 
                                bstr_t("SELECT * FROM Win32_OperatingSystem"),
                                WBEM_FLAG_BIDIRECTIONAL, 
                                NULL,
                                pResponseSink);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        pResponseSink->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: -------------------------------------------------
    // Wait to get the data from the query in step 6 -----------
    Sleep(500);
    pSvc->CancelAsyncCall(pResponseSink);

    // Cleanup
    // ========
    pSvc->Release();
    pLoc->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



<span data-ttu-id="282cd-130">下列標頭檔是用於 QuerySink 類別。</span><span class="sxs-lookup"><span data-stu-id="282cd-130">The following header file is used for the QuerySink class.</span></span> <span data-ttu-id="282cd-131">QuerySink 類別是在先前的程式碼範例中使用。</span><span class="sxs-lookup"><span data-stu-id="282cd-131">The QuerySink class is used in the previous code example.</span></span>


```C++
// QuerySink.h
#ifndef QUERYSINK_H
#define QUERYSINK_H

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone;
 CRITICAL_SECTION threadLock; // for thread safety

public:
    QuerySink() { m_lRef = 0; bDone = false; 
     InitializeCriticalSection(&threadLock); }
    ~QuerySink() { bDone = true;
        DeleteCriticalSection(&threadLock); }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid,
        void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            LONG lObjectCount,
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );

 bool IsDone();
};

#endif    // end of QuerySink.h
```



<span data-ttu-id="282cd-132">下列程式碼範例是 QuerySink 類別的實作為。</span><span class="sxs-lookup"><span data-stu-id="282cd-132">The following code example is an implementation of the QuerySink class.</span></span>


```C++
// QuerySink.cpp
#include "querysink.h"

ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjectCount,
    IWbemClassObject **apObjArray)
{
 HRESULT hres = S_OK;

    for (int i = 0; i < lObjectCount; i++)
    {
        VARIANT varName;
        hres = apObjArray[i]->Get(_bstr_t(L"Name"),
            0, &varName, 0, 0);

        if (FAILED(hres))
        {
            cout << "Failed to get the data from the query"
                << " Error code = 0x"
                << hex << hres << endl;
            return WBEM_E_FAILED;       // Program has failed.
        }

        printf("Name: %ls\n", V_BSTR(&varName));
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
 if(lFlags == WBEM_STATUS_COMPLETE)
 {
  printf("Call complete.\n");

  EnterCriticalSection(&threadLock);
  bDone = true;
  LeaveCriticalSection(&threadLock);
 }
 else if(lFlags == WBEM_STATUS_PROGRESS)
 {
  printf("Call in progress.\n");
 }
    
    return WBEM_S_NO_ERROR;
}


bool QuerySink::IsDone()
{
    bool done = true;

 EnterCriticalSection(&threadLock);
 done = bDone;
 LeaveCriticalSection(&threadLock);

    return done;
}    // end of QuerySink.cpp
```



 

 
