---
description: Windows Management Instrumentation (WMI) 可以建立接收，以接收用戶端應用程式在個別進程中的非同步回呼。
ms.assetid: 3d3111ac-7d83-48d6-94e4-36cb46a506fa
ms.tgt_platform: multiple
title: 降低接收器在個別進程中的安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aec8bcb451d254961acae8278cb45cb4454f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979808"
---
# <a name="lowering-the-security-for-a-sink-in-a-separate-process"></a>降低接收器在個別進程中的安全性

Windows Management Instrumentation (WMI) 可以建立接收，以接收用戶端應用程式在個別進程中的非同步回呼。 Unsecapp.exe 個別的進程。 使用 [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) 介面。 **IWbemUnsecuredApartment** 可讓您控制 Unsecapp.exe 是否驗證接收器的回呼。 如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。

然後，您可以降低該程式的安全性，WMI 可以存取接收器而不受限制。 為了協助進行這項技術，WMI 提供了 Unsecapp.exe 的流程，可作為個別的進程。 您可以使用 [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) 介面的呼叫來裝載 Unsecapp.exe。

[**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment)介面可讓用戶端應用程式建立個別的專用進程，執行 Unsecapp.exe 來裝載 [**IWbemObjectSink**](iwbemobjectsink.md)的執行。 專用的進程可以呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ，將 WMI 存取權授與專用進程，而不會危及主要進程的安全性。 初始化之後，專用進程會扮演主要進程與 WMI 之間的媒介。

下列程式描述如何使用 [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment)執行非同步呼叫。

**使用 IUnsecuredApartment 執行非同步呼叫**

1.  使用對 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的呼叫來建立專用的進程。

    下列程式碼範例會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立專用的進程。

    ```C++
    IUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
      CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
      (void**)&pUnsecApp);
    ```

    

2.  將接收器物件具現化。

    下列程式碼範例會建立新的接收物件。

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  建立接收的存根。

    存根是從接收產生的包裝函式函數。

    下列程式碼範例會呼叫 [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) 來建立接收器的存根。

    ```C++
    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);
    ```

    

4.  呼叫包裝函式的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，並要求 [**IWbemObjectSink**](iwbemobjectsink.md) 介面的指標。

    下列程式碼範例會呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，並要求 [**IWbemObjectSink**](iwbemobjectsink.md) 介面的指標。

    ```C++
    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink, (void **)&pStubSink); pStubUnk->Release();
    ```

    

5.  釋放接收器物件指標。

    您可以釋放物件指標，因為存根現在擁有指標。

    下列程式碼範例會釋放接收器物件指標。

    ```C++
    pSink->Release();
    ```

    

6.  在任何非同步呼叫中使用存根。

    完成呼叫時，釋放本機參考計數。

    下列程式碼範例會在非同步呼叫中使用存根。

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    有時您可能必須在進行呼叫後取消非同步呼叫。 如果您需要取消呼叫，請使用原先發出呼叫的相同指標取消呼叫。

    下列程式碼範例顯示如何取消非同步呼叫。

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

7.  當您使用非同步呼叫完成時，請釋放本機參考計數。

    確認不需要取消非同步呼叫之後，請務必釋放 *pStubSink* 指標。 此外，在 WMI 釋放 *pSink* 接收器指標之後，請勿釋放 *pStubSink* 。 在 *pSink* 之後釋放 *pStubSink* 會建立迴圈參考計數，讓接收和存根永遠留在記憶體中。 相反地，釋放指標的可能位置是在 [**IWbemObjectSink：： SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) 呼叫中，由 WMI 發出，以報告原始非同步呼叫已完成。

8.  完成時，透過呼叫 [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)將 COM 解除初始化。

    下列程式碼範例顯示如何在 *pUnsecApp* 指標上呼叫 [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 。

    ```C++
    pUnsecApp->Release();
    ```

    

    本主題中的程式碼範例需要下列參考和 \# include 語句，才能正確編譯。

    ```C++
    #include <wbemidl.h>
    #pragma comment(lib, "wbemuuid.lib")
    ```

    

如需有關 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函式和參數的詳細資訊，請參閱平臺軟體發展工具組中的 [COM](../cossdk/component-services-portal.md) 檔 (SDK) 。

 

 
