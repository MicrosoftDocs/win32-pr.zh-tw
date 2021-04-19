---
description: WMI 存放庫包含預先安裝的效能類別，適用于所有效能程式庫物件。
ms.assetid: 2158385f-d0dc-4102-84db-ce02d2b0ee53
ms.tgt_platform: multiple
title: 存取 WMI 預先安裝的效能類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265f9b4008913a463545ed03cd6f1025b58ef5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985660"
---
# <a name="accessing-wmi-preinstalled-performance-classes"></a>存取 WMI 預先安裝的效能類別

WMI 存放庫包含預先安裝的效能類別，適用于所有效能程式庫物件。 例如，原始資料效能類別 [**Win32 \_ PerfRawData \_ perfproc.dll \_ 進程**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) 的實例代表進程。 這個效能物件會顯示在系統監視器中，做為處理常式物件。

[**Win32 \_ PerfRawData \_ Perfproc.dll \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)的 **PageFaultsPerSec** 屬性代表進程的每秒分頁錯誤數效能計數器。 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)類別包含系統監視器 (Perfmon.exe) 中顯示的計算資料值。 [**Win32 \_ PerfFormattedData \_ Perfproc.dll \_ 進程**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)的 **PageFaultsPerSec** 屬性值與出現在系統監視器中的值相同。

您可以使用 [適用于 wmi 的 COM API](com-api-for-wmi.md) 或 [適用于 WMI 的腳本 API](scripting-api-for-wmi.md) ，透過 [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)來存取效能資料。 在這兩種情況下，必須要有 [*複習*](gloss-r.md) 物件才能取得每個資料範例。 如需使用刷新程式和存取效能類別的詳細資訊和腳本範例，請參閱 [WMI 工作：效能監視](wmi-tasks--performance-monitoring.md)。 如需詳細資訊，請參閱 [在腳本中存取效能資料](accessing-performance-data-in-script.md)。

## <a name="accessing-performance-data-from-c"></a>從 c + + 存取效能資料

下列 c + + 程式碼範例會使用效能計數器提供者來存取預先定義的高效能類別。 它會建立複習物件，並將物件新增至複習。 物件是 [**Win32 \_ PerfRawData \_ perfproc.dll \_ 進程**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) 實例，可監視特定進程的效能。 程式碼只會讀取處理常式物件（ **VirtualBytes** 屬性）中的一個計數器屬性。 程式碼需要下列參考，且必須要 **\# 有** 語句才能正確編譯。


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



下列程式說明如何從 c + + 的高效能提供者存取資料。

**從 c + + 的高效能提供者存取資料**

1.  建立與 WMI 命名空間的連線，並使用 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 和 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)的呼叫來設定 wmi 安全性。

    此步驟是建立任何 WMI 用戶端應用程式的標準步驟。 如需詳細資訊，請參閱 [使用 c + + 建立 WMI 應用程式](creating-a-wmi-application-using-c-.md)。

2.  使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 搭配 CLSID WbemRefresher 來建立複習物件 \_ 。 透過 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法要求 [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher)介面。 透過 **QueryInterface** 方法要求 [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)介面。

    [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)介面 [**是 WMI 重新**](swbemrefreshableitem-refresher.md)整理程式物件的主要介面。

    下列 c + + 程式碼範例顯示如何取出 [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)。

    ```C++
    IWbemRefresher* pRefresher = NULL;

    HRESULT hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher,
        (void**) &pRefresher);

    IWbemConfigureRefresher* pConfig = NULL;

    pRefresher->QueryInterface( 
        IID_IWbemConfigureRefresher,
        (void**) &pConfig
      );
    ```

    

3.  透過 [**IWbemConfigureRefresher：： AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) 方法的呼叫，將物件新增至複習。

    當您將物件加入至重新整理程式時，WMI 會在您每次呼叫 [**IWbemRefresher：： Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) 方法時重新整理物件。 您加入的物件會在其類別限定詞中指定提供者。

    下列 c + + 程式碼範例顯示如何呼叫 [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath)。

    ```C++
    IWbemClassObject* pObj = NULL;
    IWbemServices* pNameSpace = NULL;

    // Add the instance to be refreshed.
    hr = pConfig->AddObjectByPath(
         pNameSpace,
         L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
         0L,
         NULL,
         &pObj,
         NULL
    );
    if (FAILED(hr))
    {
       cout << "Could not add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }
    ```

    

4.  若要設定更快速存取物件，請透過 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)介面上的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))連接至 [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess)介面。

    下列 c + + 程式碼範例示範如何使用 [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) （而非 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)）抓取物件的指標。

    ```C++
        // For quick property retrieval, use IWbemObjectAccess.
        IWbemObjectAccess* pAcc = NULL;
        pObj->QueryInterface( IID_IWbemObjectAccess, (void**) &pAcc );
        // This is not required.
        pObj->Release();
    ```

    

    [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess)介面會提高效能，因為您可以取得特定計數器屬性的控制碼，而且需要您在程式碼中鎖定和解除鎖定物件，這是 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)針對每個屬性存取所執行的作業。

5.  使用 [**IWbemObjectAccess：： GetPropertyHandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) 方法的呼叫，取得要檢查之屬性的控制碼。

    類別的所有實例都有相同的屬性控制碼，這表示您可以使用您從特定實例取得的屬性控制碼來取得特定類別的所有實例。 您也可以從類別物件取得控制碼，以從實例物件取出屬性值。

    下列 c + + 程式碼範例顯示如何取出屬性控制碼。

    ```C++
        // Get a property handle for the VirtualBytes property
        long lVirtualBytesHandle = 0;
        DWORD dwVirtualBytes = 0;
        CIMTYPE variant;

        hr = pAcc->GetPropertyHandle(L"VirtualBytes",
             &variant,
             &lVirtualBytesHandle 
        );
        if (FAILED(hr))
        {
           cout << "Could not get property handle. Error code: 0x"
                << hex << hr << endl;
           return hr;
        }
    ```

    

6.  建立程式設計迴圈，以執行下列動作：

    -   使用先前呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)所建立的指標，以 [**IWbemRefresher：： refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)的呼叫來重新整理物件。

        在此呼叫中，WMI 複習會使用提供者提供的資料來重新整理用戶端物件。

    -   視需要在物件上執行任何動作，例如抓取屬性名稱、資料類型或值。

        您可以透過稍早取得的屬性控制碼來存取屬性。 由於重新整理 [**呼叫的**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) 緣故，WMI 會在每次迴圈時重新整理屬性。

下列 c + + 範例顯示如何使用 WMI 高效能 API。


```C++
// Get the local locator object
IWbemServices* pNameSpace = NULL;
IWbemLocator* pWbemLocator = NULL;
CIMTYPE variant;
VARIANT VT;

CoCreateInstance( CLSID_WbemLocator, NULL,
    CLSCTX_INPROC_SERVER, IID_IWbemLocator, (void**) &pWbemLocator
);

// Connect to the desired namespace
BSTR bstrNameSpace = SysAllocString( L"\\\\.\\root\\cimv2" );

HRESULT hr = WBEM_S_NO_ERROR;

hr = pWbemLocator->ConnectServer(
     bstrNameSpace,      // Namespace name
     NULL,               // User name
     NULL,               // Password
     NULL,               // Locale
     0L,                 // Security flags
     NULL,               // Authority
     NULL,               // Wbem context
     &pNameSpace         // Namespace
);

if ( SUCCEEDED( hr ) )
{
    // Set namespace security.
    IUnknown* pUnk = NULL;
    pNameSpace->QueryInterface( IID_IUnknown, (void**) &pUnk );

    hr = CoSetProxyBlanket(
         pNameSpace, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }

    hr = CoSetProxyBlanket(pUnk, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pUnk->Release();
       return hr;
    }

    // Clean up the IUnknown.
    pUnk->Release();

    IWbemRefresher* pRefresher = NULL;
    IWbemConfigureRefresher* pConfig = NULL;

    // Create a WMI Refresher and get a pointer to the
    // IWbemConfigureRefresher interface.
    CoCreateInstance(CLSID_WbemRefresher, 
                     NULL,
                     CLSCTX_INPROC_SERVER, 
                     IID_IWbemRefresher, 
                     (void**) &pRefresher 
    );
    
    pRefresher->QueryInterface(IID_IWbemConfigureRefresher,
                               (void**) &pConfig );

    IWbemClassObject* pObj = NULL;

    // Add the instance to be refreshed.
    pConfig->AddObjectByPath(
       pNameSpace,
       L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
       0L,
       NULL,
       &pObj,
       NULL 
    );
    if (FAILED(hr))
    {
       cout << "Cannot add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       
       return hr;
    }

    // For quick property retrieval, use IWbemObjectAccess.
    IWbemObjectAccess* pAcc = NULL;
    pObj->QueryInterface(IID_IWbemObjectAccess, 
                         (void**) &pAcc );

    // This is not required.
    pObj->Release();

    // Get a property handle for the VirtualBytes property.
    long lVirtualBytesHandle = 0;
    DWORD dwVirtualBytes = 0;

    pAcc->GetPropertyHandle(L"VirtualBytes", 
                            &variant, 
                            &lVirtualBytesHandle );

    // Refresh the object ten times and retrieve the value.
    for( int x = 0; x < 10; x++ )
    {
        pRefresher->Refresh( 0L );
        pAcc->ReadDWORD( lVirtualBytesHandle, &dwVirtualBytes );
        printf( "Process is using %lu bytes\n", dwVirtualBytes );
        // Sleep for a second.
        Sleep( 1000 );
    }
    // Clean up all the objects.
    pAcc->Release();
    // Done with these too.
    pConfig->Release();
    pRefresher->Release();
    pNameSpace->Release();
}
SysFreeString( bstrNameSpace );
pWbemLocator->Release();
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[WMI 工作：效能監視](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
