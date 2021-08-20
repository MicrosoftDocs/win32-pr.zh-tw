---
description: WMI 高效能 API 是一系列的介面，可從效能計數器類別取得資料。
ms.assetid: ee0a2ead-f53a-4651-a287-04a62eba3f84
ms.tgt_platform: multiple
title: 存取 c + + 中的效能資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e566fb5803e598e42fac06d8f04fe3e71935008668e397a47d0226a96560eec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820325"
---
# <a name="accessing-performance-data-in-c"></a>存取 c + + 中的效能資料

WMI 高效能 API 是一系列的介面，可從 [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)取得資料。 這些介面需要使用 [*複習*](gloss-r.md) 物件來增加取樣率。 如需在腳本中使用複習物件的詳細資訊，請參閱在腳本和 WMI 工作 [中存取效能資料](accessing-performance-data-in-script.md) [：效能監視](wmi-tasks--performance-monitoring.md)。

本主題將討論下列各節：

-   [重新整理效能資料](#refreshing-performance-data)
-   [將枚舉器新增至 WMI 重新整理器](#adding-enumerators-to-the-wmi-refresher)
-   [範例](#example)
-   [相關主題](#related-topics)

## <a name="refreshing-performance-data"></a>重新整理效能資料

複習物件會藉由在不跨越進程界限的情況下抓取資料來提高資料提供者和用戶端效能。 如果用戶端和伺服器都位於相同的電腦上，重新整理程式會將高效能提供者載入至用戶端，並將資料直接從提供者物件複製到用戶端物件。 如果用戶端和伺服器位於不同的電腦上，重新整理程式就會在遠端電腦上快取物件，並將最基本的資料集傳輸至用戶端，以提升效能。

複習也有：

-   當發生網路錯誤或遠端電腦重新開機時，自動將用戶端重新連接至遠端 WMI 服務。

    根據預設，當兩部電腦之間的遠端連線失敗時，重新整理程式會嘗試將您的應用程式重新連線至相關的高效能提供者。 若要防止重新連接，[**請在重新整理方法呼叫**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)中傳遞 **WBEM 旗標 \_ 重新整理 \_ \_ 無 \_ 自動 \_ 重新** 連線旗標。 腳本用戶端必須將 [**SWbemRefresher. AutoReconnect**](swbemrefresher-autoreconnect.md) 屬性設定為 **FALSE**。

-   載入由相同或不同提供者所提供的多個物件和枚舉器。

    可讓您將多個物件、列舉值或兩者新增至複習。

-   列舉物件。

    如同其他提供者，高效能提供者可以列舉物件。

完成撰寫您的高效能用戶端之後，您可能會想要改善您的回應時間。 由於 [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) 介面是針對速度優化的，因此介面並非本質上 threadsafe。 因此，在重新整理作業期間，請勿存取可更新的物件或列舉。 若要在 **IWbemObjectAccess** 方法呼叫期間保護跨執行緒的物件，請使用 [**IWbemObjectAccess：： Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) 和 [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) 方法。 為了提升效能，請同步處理您的執行緒，如此您就不需要鎖定個別的執行緒。 減少執行緒和同步處理物件群組以進行重新整理作業，可提供最佳的整體效能。

## <a name="adding-enumerators-to-the-wmi-refresher"></a>將枚舉器新增至 WMI 重新整理器

每個實例中的實例和資料數目都會藉由將列舉值新增至重新整理程式來重新整理，以便每次呼叫 [**IWbemRefresher：： Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) 都會產生完整的列舉。

下列 c + + 程式碼範例需要下列參考，且必須 \# 要有語句才能正確編譯。


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



下列程式示範如何將列舉值新增至複習。

**將列舉值新增至複習**

1.  使用可重新整理之物件的路徑和 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面，呼叫 [**IWbemConfigureRefresher：： AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum)方法。

    重新整理程式會傳回 [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) 介面的指標。 您可以使用 **IWbemHiPerfEnum** 介面來存取列舉中的物件。

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

    

2.  建立可執行下列動作的迴圈：

    -   使用 [**IWbemRefresher：： Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)的呼叫來重新整理物件。
    -   提供 [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) 介面指標的陣列給 [**IWbemHiPerfEnum：： GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) 方法。
    -   使用傳遞至 [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects)的 [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess)方法，存取列舉值的屬性。

        屬性控制碼可以傳遞至每個 [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) 實例，以取得重新整理的值。 用戶端必須呼叫 [**release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)來釋放 [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects)所傳回的 **IWbemObjectAccess** 指標。

## <a name="example"></a>範例

下列 c + + 程式碼範例會列舉高效能類別，在此類別中，用戶端會從第一個物件抓取屬性控制碼，並在重新整理作業的其餘部分重複使用控制碼。 重新 [**整理方法的**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) 每個呼叫都會更新實例和實例資料的數目。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[存取腳本中的效能資料](accessing-performance-data-in-script.md)
</dt> <dt>

[更新腳本中的 WMI 資料](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[WMI 工作：效能監視](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[監視效能資料](monitoring-performance-data.md)
</dt> <dt>

[格式化效能計數器類別的屬性限定詞](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[WMI 效能計數器類型](wmi-performance-counter-types.md)
</dt> <dt>

[**Wmiadap.exe**](wmiadap.md)
</dt> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
