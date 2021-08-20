---
description: 最半同步呼叫是呼叫 WMI 方法的建議方法，例如 IWbemServices：： ExecMethod 和提供者方法，例如 Win32 LogicalDisk 類別的 Chkdsk 方法 \_ 。
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: 使用 c + + 進行半同步呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a550c5ad659ab9b640a1fcb3060b5f6cc7671f80c209d238cd859ad0ef6f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050696"
---
# <a name="making-a-semisynchronous-call-with-c"></a>使用 c + + 進行半同步呼叫

最半同步呼叫是呼叫 WMI 方法的建議方法，例如 [**IWbemServices：： ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) 和提供者方法，例如 [**Win32 \_ LogicalDisk 類別的 Chkdsk 方法**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk)。

同步處理的其中一個缺點是，呼叫端執行緒會被封鎖，直到呼叫完成為止。 瓶頸可能會導致處理時間延遲。 相反地，非同步呼叫必須在腳本中執行 [**SWbemSink**](swbemsink.md) 。 在 c + + 中，非同步程式碼必須實 [**IWbemObjectSink**](iwbemobjectsink.md) 介面、使用多個執行緒，並控制傳回給呼叫端的資訊流程。 例如，查詢中的大型結果集可能需要相當長的時間才能傳遞，並強制呼叫者花大量系統資源來處理傳遞。

最半處理處理可透過輪詢特殊狀態物件來執行 [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) 介面，以解決執行緒的問題和未受控制的傳遞問題。 透過 **IWbemCallResult**，您可以改善查詢、列舉和事件通知的速度和效率。

下列程式描述如何使用 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 介面進行半同步呼叫。

**若要使用 IWbemServices 介面進行半同步呼叫**

1.  以正常方式進行呼叫，但使用 WBEM 旗標會在 *IFlags* 參數中設定 **\_ \_ \_ 立即** 傳回旗標。

    您可以將 **WBEM \_ 旗 \_ 標 \_ 立即** 傳回與其他對特定方法有效的旗標。 例如，針對所有傳回列舉值的呼叫，請使用 **WBEM 旗標 [ \_ \_ \_ 僅轉寄** ] 旗標。 以組合方式設定這些旗標可節省時間和空間，並提升回應能力。

2.  輪詢您的結果。

    如果您呼叫的方法會傳回列舉值，例如 [**IWbemServices：： CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) 或 [**Iwbemservices：： ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)，您可以使用 [**IEnumWbemClassObject：： Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) 或 [**IEnumWbemClassObject：： NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) 方法來輪詢枚舉器。 **IEnumWbemClassObject：： NextAsync** 呼叫為非封鎖並立即傳回。 在背景中，WMI 會藉由呼叫 [**IWbemObjectSink：：指示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)，開始傳遞要求的物件數目。 WMI 接著會停止，並等候其他 **NextAsync** 呼叫。

    如果您呼叫的方法不會傳回列舉值，例如 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)，您必須將 *ppCallResult* 參數設定為有效的指標。 在傳回的指標上使用 [**IWbemCallResult：： GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) ，以 **取得 \_ WBEM \_ S 沒有 \_ 錯誤**。

3.  完成通話。

    針對傳回列舉值的呼叫，WMI 會呼叫 [**IWbemObjectSink：： SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) 來回報作業是否完成。 如果您不需要整個結果，請呼叫 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)：：[**release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法來釋放列舉值。 在 WMI 中呼叫 **釋放** 結果會取消傳遞保留的所有物件。

    若為不使用列舉值的呼叫，請透過方法的 *plStatus* 參數抓取 [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus)物件。

本主題中的 c + + 程式碼範例需要下列 \# include 語句才能正確編譯。


```C++
#include <comdef.h>
#include <wbemidl.h>
```



下列程式碼範例示範如何進行對 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)的半同步呼叫。


```C++
void GetObjSemiSync(IWbemServices *pSvc)
{

    IWbemCallResult *pCallRes = 0;
    IWbemClassObject *pObj = 0;
    
    HRESULT hRes = pSvc->GetObject(_bstr_t(L"MyClass=\"AAA\""), 0,
        0, 0, &pCallRes
        );
        
    if (hRes || pCallRes == 0)
        return;
        
    while (true)
    {
        LONG lStatus = 0;
        HRESULT hRes = pCallRes->GetCallStatus(5000, &lStatus);
        if ( hRes == WBEM_S_NO_ERROR || hRes != WBEM_S_TIMEDOUT )
            break;

        // Do another task
    }

    hRes = pCallRes->GetResultObject(5000, &pObj);
    if (hRes)
    {
        pCallRes->Release();
        return;
    }

    pCallRes->Release();

    // Use the object.

    // ...

    // Release it.
    // ===========
        
    pObj->Release();    // Release objects not owned.            
  
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[呼叫方法](calling-a-method.md)
</dt> </dl>

 

 
