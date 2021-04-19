---
description: 非同步呼叫會帶來嚴重的安全性風險，因為對接收器的回呼可能不是原始應用程式或腳本的非同步呼叫結果。
ms.assetid: 2b839ea9-e1e6-4123-a98a-04ebee907b3b
ms.tgt_platform: multiple
title: 在非同步呼叫上設定安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39f78315814d3b66c97e60a6b8045d7ea9e7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996980"
---
# <a name="setting-security-on-an-asynchronous-call"></a>在非同步呼叫上設定安全性

非同步呼叫會帶來嚴重的安全性風險，因為對 [*接收器*](gloss-s.md) 的回呼可能不是原始應用程式或腳本的非同步呼叫結果。 遠端連線中的安全性是以遠端電腦上用戶端與提供者之間的通訊加密為基礎。 在 c + + 中，您可以透過 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)呼叫中的驗證層級參數設定加密。 在腳本中，請在 [**SWbemSecurity**](swbemsecurity.md)物件上設定 *AuthenticationLevel* 。 如需詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。

非同步呼叫的安全性風險存在，因為 WMI 會降低回呼的驗證層級，直到回呼成功為止。 在連出的非同步呼叫上，用戶端可以設定與 WMI 的連線上的驗證層級。 WMI 會抓取用戶端呼叫上的安全性設定，並嘗試使用相同的驗證層級回撥。 回呼一律會在 **RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權** 等級起始。 如果回呼失敗，WMI 會將驗證層級減少到回呼可以成功的層級（如有必要）至 **RPC \_ C \_ 驗證 \_ 層級 \_ 無**。 在本機系統（驗證服務不是 Kerberos）內的呼叫內容中，永遠會在 **RPC \_ C \_ 驗證 \_ 層級 \_** 傳回回呼。

最小驗證層級為腳本) 的 **RPC \_ C \_ 驗證 \_ 層級 \_ PKT** (**wbemAuthenticationLevelPkt**。 不過，您可以指定較高的層級，例如 **RPC \_ C \_ 驗證 \_ Level \_ PKT \_ 隱私權** (**wbemAuthenticationLevelPktPrivacy**) 。 建議用戶端應用程式或腳本將驗證層級設定為 **RPC \_ C \_ 驗證 \_ level \_ DEFAULT** (**wbemAuthenticationLevelDefault**) 這可讓驗證等級與伺服器所指定的層級進行協調。

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** 登錄值控制 WMI 是否會檢查回呼中可接受的驗證層級。 這是保護在腳本或 Visual Basic 中進行的非同步呼叫之接收安全性的唯一機制。 依預設，此登錄機碼設定為零。 如果登錄機碼為零，則 WMI 不會驗證驗證層級。 若要保護腳本中的非同步呼叫，請將登錄機碼設定為1。 C + + 用戶端可以呼叫 [**IWbemUnsecuredApartment：： CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) 來控制接收的存取。 預設會在任何位置建立這個值。

下列主題提供設定非同步呼叫安全性的範例：

-   [在 VBScript 中設定非同步呼叫的安全性](setting-security-on-an-asynchronous-call-in-vbscript.md)
-   設定 c + + 中的非同步呼叫安全性

## <a name="setting-asynchronous-call-security-in-c"></a>設定 c + + 中的非同步呼叫安全性

[**IWbemUnsecuredApartment：： CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub)方法類似于 [**IUnsecuredApartment：： CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub)方法，會在個別的進程中建立接收，Unsecapp.exe 來接收回呼。 但是， **CreateSinkStub** 方法具有 *>dwflag* 參數，可指定個別進程處理存取控制的方式。

*>dwflag* 參數會為 Unsecapp.exe 指定下列其中一個動作：

-   使用登錄機碼設定來判斷是否要檢查存取權。
-   略過登錄機碼，並一律檢查存取權。
-   略過登錄機碼，而且絕不檢查存取權。

本主題中的程式碼範例需要下列 \# include 語句才能正確編譯。


```C++
#include <wbemidl.h>
```



下列程式描述如何使用 [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment)執行非同步呼叫。

**使用 IWbemUnsecuredApartment 執行非同步呼叫**

1.  使用對 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的呼叫來建立專用的進程。

    下列程式碼範例會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立專用的進程。

    ```C++
    CLSID                    CLSID_WbemUnsecuredApartment;
    IWbemUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_WbemUnsecuredApartment, 
                     NULL, 
                     CLSCTX_LOCAL_SERVER, 
                     IID_IWbemUnsecuredApartment, 
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

    下列程式碼範例會建立接收器的存根。

    ```C++
    LPCWSTR          wszReserved = NULL;           
    IWbemObjectSink* pStubSink   = NULL;
    IUnknown*        pStubUnk    = NULL; 

    pUnsecApp->CreateSinkStub(pSink,
                              WBEM_FLAG_UNSECAPP_CHECK_ACCESS,  //Authenticate callbacks regardless of registry key
                              wszReserved,
                              &pStubSink);
    ```

    

4.  釋放接收器物件指標。

    您可以釋放物件指標，因為存根現在擁有指標。

    下列程式碼範例會釋放物件指標。

    ```C++
    pSink->Release();
    ```

    

5.  在任何非同步呼叫中使用存根。

    完成呼叫時，釋放本機參考計數。

    下列程式碼範例會在非同步呼叫中使用存根。

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    有時您可能必須在進行呼叫後取消非同步呼叫。 如果您需要取消呼叫，請使用原先發出呼叫的相同指標取消呼叫。

    下列程式碼範例說明如何取消非同步呼叫。

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

6.  當您使用非同步呼叫完成時，請釋放本機參考計數。

    請務必在確認非同步呼叫不需要取消之後，才釋放 *pStubSink* 指標。 此外，在 WMI 釋放 *pSink* 接收器指標之後，請勿釋放 *pStubSink* 。 在 *pSink* 之後釋放 *pStubSink* 會建立迴圈參考計數，讓接收和存根永遠留在記憶體中。 相反地，釋放指標的可能位置是在 [**IWbemObjectSink：： SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) 呼叫中，由 WMI 發出，以報告原始非同步呼叫已完成。

7.  完成時，透過呼叫 [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)將 COM 解除初始化。

    下列程式碼範例顯示如何在 *pUnsecApp* 指標上呼叫 [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 。

    ```C++
    pUnsecApp->Release();
    ```

    

如需 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函數和參數的詳細資訊，請參閱 [COM](../cossdk/component-services-portal.md) 檔。

 

 
