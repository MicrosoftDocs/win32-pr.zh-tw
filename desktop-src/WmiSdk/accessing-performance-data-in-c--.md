---
description: WMI 高效能 API 是一系列的介面，可從效能計數器類別取得資料。
ms.assetid: ee0a2ead-f53a-4651-a287-04a62eba3f84
ms.tgt_platform: multiple
title: 存取 c + + 中的效能資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b076e1ab15b934f347ee491711d7d3d1b8fbbe0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999947"
---
# <a name="accessing-performance-data-in-c"></a><span data-ttu-id="c0f20-103">存取 c + + 中的效能資料</span><span class="sxs-lookup"><span data-stu-id="c0f20-103">Accessing Performance Data in C++</span></span>

<span data-ttu-id="c0f20-104">WMI 高效能 API 是一系列的介面，可從 [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)取得資料。</span><span class="sxs-lookup"><span data-stu-id="c0f20-104">The WMI high-performance API is a series of interfaces that obtain data from [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="c0f20-105">這些介面需要使用 [*複習*](gloss-r.md) 物件來增加取樣率。</span><span class="sxs-lookup"><span data-stu-id="c0f20-105">These interfaces require use of a [*refresher*](gloss-r.md) object to increase the sampling rate.</span></span> <span data-ttu-id="c0f20-106">如需在腳本中使用複習物件的詳細資訊，請參閱在腳本和 WMI 工作 [中存取效能資料](accessing-performance-data-in-script.md) [：效能監視](wmi-tasks--performance-monitoring.md)。</span><span class="sxs-lookup"><span data-stu-id="c0f20-106">For more information about using the refresher object in scripting, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md) and [WMI Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md).</span></span>

<span data-ttu-id="c0f20-107">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="c0f20-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="c0f20-108">重新整理效能資料</span><span class="sxs-lookup"><span data-stu-id="c0f20-108">Refreshing Performance Data</span></span>](#refreshing-performance-data)
-   [<span data-ttu-id="c0f20-109">將枚舉器新增至 WMI 重新整理器</span><span class="sxs-lookup"><span data-stu-id="c0f20-109">Adding Enumerators to the WMI Refresher</span></span>](#adding-enumerators-to-the-wmi-refresher)
-   [<span data-ttu-id="c0f20-110">範例</span><span class="sxs-lookup"><span data-stu-id="c0f20-110">Example</span></span>](#example)
-   [<span data-ttu-id="c0f20-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="c0f20-111">Related topics</span></span>](#related-topics)

## <a name="refreshing-performance-data"></a><span data-ttu-id="c0f20-112">重新整理效能資料</span><span class="sxs-lookup"><span data-stu-id="c0f20-112">Refreshing Performance Data</span></span>

<span data-ttu-id="c0f20-113">複習物件會藉由在不跨越進程界限的情況下抓取資料來提高資料提供者和用戶端效能。</span><span class="sxs-lookup"><span data-stu-id="c0f20-113">A refresher object increases data provider and client performance by retrieving data without crossing process boundaries.</span></span> <span data-ttu-id="c0f20-114">如果用戶端和伺服器都位於相同的電腦上，重新整理程式會將高效能提供者載入至用戶端，並將資料直接從提供者物件複製到用戶端物件。</span><span class="sxs-lookup"><span data-stu-id="c0f20-114">If both the client and the server are located on the same computer, a refresher loads the high-performance provider in-process to the client, and copies data directly from provider objects into client objects.</span></span> <span data-ttu-id="c0f20-115">如果用戶端和伺服器位於不同的電腦上，重新整理程式就會在遠端電腦上快取物件，並將最基本的資料集傳輸至用戶端，以提升效能。</span><span class="sxs-lookup"><span data-stu-id="c0f20-115">If the client and the server are located on different computers, the refresher increases performance by caching objects on the remote computer, and transmitting minimal data sets to the client.</span></span>

<span data-ttu-id="c0f20-116">複習也有：</span><span class="sxs-lookup"><span data-stu-id="c0f20-116">A refresher also:</span></span>

-   <span data-ttu-id="c0f20-117">當發生網路錯誤或遠端電腦重新開機時，自動將用戶端重新連接至遠端 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="c0f20-117">Automatically reconnects a client to a remote WMI service when a network error occurs, or the remote computer is restarted.</span></span>

    <span data-ttu-id="c0f20-118">根據預設，當兩部電腦之間的遠端連線失敗時，重新整理程式會嘗試將您的應用程式重新連線至相關的高效能提供者。</span><span class="sxs-lookup"><span data-stu-id="c0f20-118">By default, a refresher attempts to reconnect your application to the relevant high-performance provider when a remote connection between the two computers fails.</span></span> <span data-ttu-id="c0f20-119">若要防止重新連接，[**請在重新整理方法呼叫**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)中傳遞 **WBEM 旗標 \_ 重新整理 \_ \_ 無 \_ 自動 \_ 重新** 連線旗標。</span><span class="sxs-lookup"><span data-stu-id="c0f20-119">To prevent the reconnection, pass the **WBEM\_FLAG\_REFRESH\_NO\_AUTO\_RECONNECT** flag in the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method call.</span></span> <span data-ttu-id="c0f20-120">腳本用戶端必須將 [**SWbemRefresher. AutoReconnect**](swbemrefresher-autoreconnect.md) 屬性設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c0f20-120">Scripting clients must set the [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) property to **FALSE**.</span></span>

-   <span data-ttu-id="c0f20-121">載入由相同或不同提供者所提供的多個物件和枚舉器。</span><span class="sxs-lookup"><span data-stu-id="c0f20-121">Loads multiple objects and enumerators that are provided by the same or different providers.</span></span>

    <span data-ttu-id="c0f20-122">可讓您將多個物件、列舉值或兩者新增至複習。</span><span class="sxs-lookup"><span data-stu-id="c0f20-122">Allows you to add multiple objects, enumerators, or both to a refresher.</span></span>

-   <span data-ttu-id="c0f20-123">列舉物件。</span><span class="sxs-lookup"><span data-stu-id="c0f20-123">Enumerates objects.</span></span>

    <span data-ttu-id="c0f20-124">如同其他提供者，高效能提供者可以列舉物件。</span><span class="sxs-lookup"><span data-stu-id="c0f20-124">Like other providers, a high-performance provider can enumerate objects.</span></span>

<span data-ttu-id="c0f20-125">完成撰寫您的高效能用戶端之後，您可能會想要改善您的回應時間。</span><span class="sxs-lookup"><span data-stu-id="c0f20-125">After you finish writing your high-performance client, you may want to improve your response time.</span></span> <span data-ttu-id="c0f20-126">由於 [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) 介面是針對速度優化的，因此介面並非本質上 threadsafe。</span><span class="sxs-lookup"><span data-stu-id="c0f20-126">Because the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface is optimized for speed, the interface is not intrinsically threadsafe.</span></span> <span data-ttu-id="c0f20-127">因此，在重新整理作業期間，請勿存取可更新的物件或列舉。</span><span class="sxs-lookup"><span data-stu-id="c0f20-127">Therefore, during a refresh operation, do not access the refreshable object or enumeration.</span></span> <span data-ttu-id="c0f20-128">若要在 **IWbemObjectAccess** 方法呼叫期間保護跨執行緒的物件，請使用 [**IWbemObjectAccess：： Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) 和 [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) 方法。</span><span class="sxs-lookup"><span data-stu-id="c0f20-128">To protect objects across threads during **IWbemObjectAccess** method calls, use the [**IWbemObjectAccess::Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) and [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) methods.</span></span> <span data-ttu-id="c0f20-129">為了提升效能，請同步處理您的執行緒，如此您就不需要鎖定個別的執行緒。</span><span class="sxs-lookup"><span data-stu-id="c0f20-129">For improved performance, synchronize your threads so that you do not need to lock individual threads.</span></span> <span data-ttu-id="c0f20-130">減少執行緒和同步處理物件群組以進行重新整理作業，可提供最佳的整體效能。</span><span class="sxs-lookup"><span data-stu-id="c0f20-130">Reducing threads and synchronizing groups of objects for refresh operations provides the best overall performance.</span></span>

## <a name="adding-enumerators-to-the-wmi-refresher"></a><span data-ttu-id="c0f20-131">將枚舉器新增至 WMI 重新整理器</span><span class="sxs-lookup"><span data-stu-id="c0f20-131">Adding Enumerators to the WMI Refresher</span></span>

<span data-ttu-id="c0f20-132">每個實例中的實例和資料數目都會藉由將列舉值新增至重新整理程式來重新整理，以便每次呼叫 [**IWbemRefresher：： Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) 都會產生完整的列舉。</span><span class="sxs-lookup"><span data-stu-id="c0f20-132">Both the number of instances and data in each instance are refreshed by adding an enumerator to the refresher so that each call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) results in a complete enumeration.</span></span>

<span data-ttu-id="c0f20-133">下列 c + + 程式碼範例需要下列參考，且必須 \# 要有語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="c0f20-133">The following C++ code example requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="c0f20-134">下列程式示範如何將列舉值新增至複習。</span><span class="sxs-lookup"><span data-stu-id="c0f20-134">The following procedure shows how to add an enumerator to a refresher.</span></span>

<span data-ttu-id="c0f20-135">**將列舉值新增至複習**</span><span class="sxs-lookup"><span data-stu-id="c0f20-135">**To add an enumerator to a refresher**</span></span>

1.  <span data-ttu-id="c0f20-136">使用可重新整理之物件的路徑和 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面，呼叫 [**IWbemConfigureRefresher：： AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum)方法。</span><span class="sxs-lookup"><span data-stu-id="c0f20-136">Call the [**IWbemConfigureRefresher::AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) method using the path to the refreshable object and the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

    <span data-ttu-id="c0f20-137">重新整理程式會傳回 [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c0f20-137">The refresher returns a pointer to an [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) interface.</span></span> <span data-ttu-id="c0f20-138">您可以使用 **IWbemHiPerfEnum** 介面來存取列舉中的物件。</span><span class="sxs-lookup"><span data-stu-id="c0f20-138">You can use the **IWbemHiPerfEnum** interface to access the objects in the enumeration.</span></span>

    ```C++
    IWbemHiPerfEnum* pEnum = NULL;
    long lID;
    IWbemConfigureRefresher* pConfig;
    IWbemServices* pNameSpace;

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL,
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;
    ```

    

2.  <span data-ttu-id="c0f20-139">建立可執行下列動作的迴圈：</span><span class="sxs-lookup"><span data-stu-id="c0f20-139">Create a loop that performs the following actions:</span></span>

    -   <span data-ttu-id="c0f20-140">使用 [**IWbemRefresher：： Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)的呼叫來重新整理物件。</span><span class="sxs-lookup"><span data-stu-id="c0f20-140">Refreshes the object by using a call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).</span></span>
    -   <span data-ttu-id="c0f20-141">提供 [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) 介面指標的陣列給 [**IWbemHiPerfEnum：： GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) 方法。</span><span class="sxs-lookup"><span data-stu-id="c0f20-141">Provides an array of [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface pointers to the [**IWbemHiPerfEnum::GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) method.</span></span>
    -   <span data-ttu-id="c0f20-142">使用傳遞至 [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects)的 [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess)方法，存取列舉值的屬性。</span><span class="sxs-lookup"><span data-stu-id="c0f20-142">Accesses the properties of the enumerator by using the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) methods passed into [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span></span>

        <span data-ttu-id="c0f20-143">屬性控制碼可以傳遞至每個 [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) 實例，以取得重新整理的值。</span><span class="sxs-lookup"><span data-stu-id="c0f20-143">A property handle can be passed to each [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) instance to retrieve the refreshed value.</span></span> <span data-ttu-id="c0f20-144">用戶端必須呼叫 [**release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)來釋放 [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects)所傳回的 **IWbemObjectAccess** 指標。</span><span class="sxs-lookup"><span data-stu-id="c0f20-144">The client must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the **IWbemObjectAccess** pointers returned by [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span></span>

## <a name="example"></a><span data-ttu-id="c0f20-145">範例</span><span class="sxs-lookup"><span data-stu-id="c0f20-145">Example</span></span>

<span data-ttu-id="c0f20-146">下列 c + + 程式碼範例會列舉高效能類別，在此類別中，用戶端會從第一個物件抓取屬性控制碼，並在重新整理作業的其餘部分重複使用控制碼。</span><span class="sxs-lookup"><span data-stu-id="c0f20-146">The following C++ code example enumerates a high-performance class, where the client retrieves a property handle from the first object, and reuses the handle for the remainder of the refresh operation.</span></span> <span data-ttu-id="c0f20-147">重新 [**整理方法的**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) 每個呼叫都會更新實例和實例資料的數目。</span><span class="sxs-lookup"><span data-stu-id="c0f20-147">Each call to the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method updates the number of instances and the instance data.</span></span>


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int __cdecl wmain(int argc, wchar_t* argv[])
{
    // To add error checking,
    // check returned HRESULT below where collected.
    HRESULT                 hr = S_OK;
    IWbemRefresher          *pRefresher = NULL;
    IWbemConfigureRefresher *pConfig = NULL;
    IWbemHiPerfEnum         *pEnum = NULL;
    IWbemServices           *pNameSpace = NULL;
    IWbemLocator            *pWbemLocator = NULL;
    IWbemObjectAccess       **apEnumAccess = NULL;
    BSTR                    bstrNameSpace = NULL;
    long                    lID = 0;
    long                    lVirtualBytesHandle = 0;
    long                    lIDProcessHandle = 0;
    DWORD                   dwVirtualBytes = 0;
    DWORD                   dwProcessId = 0;
    DWORD                   dwNumObjects = 0;
    DWORD                   dwNumReturned = 0;
    DWORD                   dwIDProcess = 0;
    DWORD                   i=0;
    int                     x=0;

    if (FAILED (hr = CoInitializeEx(NULL,COINIT_MULTITHREADED)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_NONE,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, EOAC_NONE, 0)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemLocator, 
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemLocator,
        (void**) &pWbemLocator)))
    {
        goto CLEANUP;
    }

    // Connect to the desired namespace.
    bstrNameSpace = SysAllocString(L"\\\\.\\root\\cimv2");
    if (NULL == bstrNameSpace)
    {
        hr = E_OUTOFMEMORY;
        goto CLEANUP;
    }
    if (FAILED (hr = pWbemLocator->ConnectServer(
        bstrNameSpace,
        NULL, // User name
        NULL, // Password
        NULL, // Locale
        0L,   // Security flags
        NULL, // Authority
        NULL, // Wbem context
        &pNameSpace)))
    {
        goto CLEANUP;
    }
    pWbemLocator->Release();
    pWbemLocator=NULL;
    SysFreeString(bstrNameSpace);
    bstrNameSpace = NULL;

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher, 
        (void**) &pRefresher)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = pRefresher->QueryInterface(
        IID_IWbemConfigureRefresher,
        (void **)&pConfig)))
    {
        goto CLEANUP;
    }

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL, 
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;

    // Get a property handle for the VirtualBytes property.

    // Refresh the object ten times and retrieve the value.
    for(x = 0; x < 10; x++)
    {
        dwNumReturned = 0;
        dwIDProcess = 0;
        dwNumObjects = 0;

        if (FAILED (hr =pRefresher->Refresh(0L)))
        {
            goto CLEANUP;
        }

        hr = pEnum->GetObjects(0L, 
            dwNumObjects, 
            apEnumAccess, 
            &dwNumReturned);
        // If the buffer was not big enough,
        // allocate a bigger buffer and retry.
        if (hr == WBEM_E_BUFFER_TOO_SMALL 
            && dwNumReturned > dwNumObjects)
        {
            apEnumAccess = new IWbemObjectAccess*[dwNumReturned];
            if (NULL == apEnumAccess)
            {
                hr = E_OUTOFMEMORY;
                goto CLEANUP;
            }
            SecureZeroMemory(apEnumAccess,
                dwNumReturned*sizeof(IWbemObjectAccess*));
            dwNumObjects = dwNumReturned;

            if (FAILED (hr = pEnum->GetObjects(0L, 
                dwNumObjects, 
                apEnumAccess, 
                &dwNumReturned)))
            {
                goto CLEANUP;
            }
        }
        else
        {
            if (hr == WBEM_S_NO_ERROR)
            {
                hr = WBEM_E_NOT_FOUND;
                goto CLEANUP;
            }
        }

        // First time through, get the handles.
        if (0 == x)
        {
            CIMTYPE VirtualBytesType;
            CIMTYPE ProcessHandleType;
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"VirtualBytes",
                &VirtualBytesType,
                &lVirtualBytesHandle)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"IDProcess",
                &ProcessHandleType,
                &lIDProcessHandle)))
            {
                goto CLEANUP;
            }
        }
           
        for (i = 0; i < dwNumReturned; i++)
        {
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lVirtualBytesHandle,
                &dwVirtualBytes)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lIDProcessHandle,
                &dwIDProcess)))
            {
                goto CLEANUP;
            }

            wprintf(L"Process ID %lu is using %lu bytes\n",
                dwIDProcess, dwVirtualBytes);

            // Done with the object
            apEnumAccess[i]->Release();
            apEnumAccess[i] = NULL;
        }

        if (NULL != apEnumAccess)
        {
            delete [] apEnumAccess;
            apEnumAccess = NULL;
        }

       // Sleep for a second.
       Sleep(1000);
    }
    // exit loop here
    CLEANUP:

    if (NULL != bstrNameSpace)
    {
        SysFreeString(bstrNameSpace);
    }

    if (NULL != apEnumAccess)
    {
        for (i = 0; i < dwNumReturned; i++)
        {
            if (apEnumAccess[i] != NULL)
            {
                apEnumAccess[i]->Release();
                apEnumAccess[i] = NULL;
            }
        }
        delete [] apEnumAccess;
    }
    if (NULL != pWbemLocator)
    {
        pWbemLocator->Release();
    }
    if (NULL != pNameSpace)
    {
        pNameSpace->Release();
    }
    if (NULL != pEnum)
    {
        pEnum->Release();
    }
    if (NULL != pConfig)
    {
        pConfig->Release();
    }
    if (NULL != pRefresher)
    {
        pRefresher->Release();
    }

    CoUninitialize();

    if (FAILED (hr))
    {
        wprintf (L"Error status=%08x\n",hr);
    }

    return 1;
}
```



## <a name="related-topics"></a><span data-ttu-id="c0f20-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="c0f20-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0f20-149">效能計數器類別</span><span class="sxs-lookup"><span data-stu-id="c0f20-149">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="c0f20-150">存取腳本中的效能資料</span><span class="sxs-lookup"><span data-stu-id="c0f20-150">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="c0f20-151">更新腳本中的 WMI 資料</span><span class="sxs-lookup"><span data-stu-id="c0f20-151">Refreshing WMI Data in Scripts</span></span>](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[<span data-ttu-id="c0f20-152">WMI 工作：效能監視</span><span class="sxs-lookup"><span data-stu-id="c0f20-152">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="c0f20-153">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="c0f20-153">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="c0f20-154">格式化效能計數器類別的屬性限定詞</span><span class="sxs-lookup"><span data-stu-id="c0f20-154">Property Qualifiers for Formatted Performance Counter Classes</span></span>](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="c0f20-155">WMI 效能計數器類型</span><span class="sxs-lookup"><span data-stu-id="c0f20-155">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

[<span data-ttu-id="c0f20-156">**Wmiadap.exe**</span><span class="sxs-lookup"><span data-stu-id="c0f20-156">**Wmiadap.exe**</span></span>](wmiadap.md)
</dt> <dt>

[<span data-ttu-id="c0f20-157">**QueryPerformanceCounter**</span><span class="sxs-lookup"><span data-stu-id="c0f20-157">**QueryPerformanceCounter**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
