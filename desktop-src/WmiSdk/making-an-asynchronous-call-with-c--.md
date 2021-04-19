---
description: 以 c + + 撰寫的 WMI 應用程式，可以使用 IWbemServices COM 介面的許多方法進行非同步呼叫。
ms.assetid: 5179969f-bc7d-4408-84ef-7b003950a59f
ms.tgt_platform: multiple
title: 使用 c + + 進行非同步呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f093aef4b1a1b4dbede53333e77d737f8efd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979836"
---
# <a name="making-an-asynchronous-call-with-c"></a>使用 c + + 進行非同步呼叫

以 c + + 撰寫的 WMI 應用程式，可以使用 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) COM 介面的許多方法進行非同步呼叫。 不過，呼叫 [*WMI 方法*](gloss-w.md) 或 [*提供者方法*](gloss-p.md) 的建議程式是使用半同步呼叫，因為半同步呼叫比非同步呼叫更安全。 如需詳細資訊，請參閱 [使用 c + + 進行半同步呼叫](making-a-semisynchronous-call-with-c--.md) ，以及 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。

下列程式描述如何在您的進程中使用接收器進行非同步呼叫。

**使用 c + + 進行非同步呼叫**

1.  執行 [**IWbemObjectSink**](iwbemobjectsink.md) 介面。

    進行非同步呼叫的所有應用程式都必須執行 [**IWbemObjectSink**](iwbemobjectsink.md)。 暫存事件取用者也會執行 **IWbemObjectSink** 來接收事件的通知。

2.  登入目標 WMI 命名空間。

    應用程式一律需要在初始化階段呼叫 COM 函數 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 。 如果在進行非同步呼叫之前沒有這麼做，WMI 就會釋放應用程式接收，而不會完成非同步呼叫。 如需詳細資訊，請參閱 [初始化 WMI 應用程式的 COM](initializing-com-for-a-wmi-application.md)。

3.  設定接收的安全性。

    非同步呼叫會建立您可能必須處理的各種安全性問題，例如允許 WMI 存取您的應用程式。 如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。

4.  進行非同步呼叫。

    方法會立即傳回，而 **不會有 \_ \_ \_ 錯誤** 的成功碼。 在等候作業完成時，應用程式可以繼續執行其他工作。 WMI 會在應用程式的 [**IWbemObjectSink**](iwbemobjectsink.md) 執行中呼叫方法，以將其回報給應用程式。

5.  如有必要，請定期檢查您的執行是否有更新。

    應用程式可以藉由在對 **WBEM \_ 旗標 \_ 傳送 \_ 狀態** 的非同步呼叫中設定 *lFlags* 參數，來接收中繼狀態的通知。 WMI 會將 [**IWbemObjectSink**](iwbemobjectsink.md)的 *lFlags* 參數設定為 **WBEM \_ 狀態 \_ 進度**，以報告呼叫的狀態。

6.  如有必要，您可以呼叫 [**IWbemServices：： CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) 方法，在 WMI 完成處理之前取消呼叫。

    [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall)方法會藉由立即釋出 [**IWbemObjectSink**](iwbemobjectsink.md)介面的指標來取消非同步處理，並保證在 **CancelAsyncCall** 傳回之前釋放指標。

    如果您使用執行 **IUnsecured** 介面的包裝函式物件來裝載 [**IWbemObjectSink**](iwbemobjectsink.md)，您可能會發現一些額外的複雜性。 由於應用程式必須將相同的指標傳遞至在原始非同步呼叫中傳遞的 [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) ，因此應用程式必須在包裝函式物件之前保持不變，直到它清楚不需要取消。 如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。

7.  完成時，請清除指標並關閉應用程式。

    WMI 透過 [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) 方法提供最後的狀態呼叫。

    > [!Note]  
    > 傳送最終狀態更新之後，WMI 會藉由呼叫實 [**IWbemObjectSink**](iwbemobjectsink.md)介面之類別的 **發行** 方法，來釋出物件接收。 在上述範例中，這是 **QuerySink：： Release** 方法。 如果您想要控制接收物件的存留期，您可以使用一個 (1) 的初始參考計數來執行接收器。

     

    如果用戶端應用程式在兩個不同的重迭非同步呼叫中傳遞相同的接收介面，WMI 將無法保證回呼的順序。 進行重迭的非同步呼叫的用戶端應用程式應該傳遞不同的接收物件或序列化呼叫。

下列範例需要下列參考和 \# include 語句。


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



下列範例說明如何使用 [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) 方法進行非同步查詢，但不會建立安全性設定或釋放 [**IWbemObjectSink**](iwbemobjectsink.md) 物件。 如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。


```C++
// Set input parameters to ExecQueryAsync.
BSTR QueryLang = SysAllocString(L"WQL");
BSTR Query = SysAllocString(L"SELECT * FROM MyClass");

// Create IWbemObjectSink object and set pointer.
QuerySink *pSink = new QuerySink;

IWbemServices* pSvc = 0;

// Call ExecQueryAsync.
HRESULT hRes = pSvc->ExecQueryAsync(QueryLang, 
                                    Query, 
                                    0, 
                                    NULL, 
                                    pSink);

// Check for errors.
if (hRes)
{
    printf("ExecQueryAsync failed with = 0x%X\n", hRes);
    SysFreeString(QueryLang);
    SysFreeString(Query);
    delete pSink;    
    return ERROR;
}
```



> [!Note]  
> 上述程式碼不會進行編譯而不會發生錯誤，因為尚未定義 **QuerySink** 類別。 如需 **QuerySink** 的詳細資訊，請參閱 [**IWbemObjectSink**](iwbemobjectsink.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[呼叫方法](calling-a-method.md)
</dt> </dl>

 

 
