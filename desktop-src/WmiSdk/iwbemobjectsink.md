---
description: IWbemObjectSink 介面會建立接收介面，以接收 WMI 程式設計模型內的所有通知類型。
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: 'IWbemObjectSink 介面 (Wbemcli .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemObjectSink
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 980865605eadfd5e4cb61a511317dec7838b8e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983428"
---
# <a name="iwbemobjectsink-interface"></a>IWbemObjectSink 介面

**IWbemObjectSink** 介面會建立接收介面，以接收 WMI 程式設計模型內的所有通知類型。 用戶端必須執行這個介面，以接收 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)的 [非同步方法](making-an-asynchronous-call-with-c--.md)和特定類型的事件通知的結果。 提供者會使用，但不會執行此介面將事件和物件提供給 WMI。

一般而言，提供者會呼叫由 WMI 提供給它們的實作為。 在這些情況下，呼叫 [**表示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) 提供物件給 WMI 服務。 之後，請呼叫 [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) 來指出通知序列的結尾。 當接收沒有任何物件時，您也可以呼叫 **SetStatus** 來指出錯誤。

當您對 WMI 的非同步用戶端進行程式設計時，使用者會提供執行。 WMI 會呼叫傳遞物件的方法，並設定結果的狀態。

> [!Note]  
> 如果用戶端應用程式在兩個不同的重迭非同步呼叫中傳遞相同的接收介面，WMI 將無法保證回呼的順序。 進行重迭非同步呼叫的用戶端應用程式應該傳遞不同的接收物件，或序列化其呼叫。

 

> [!Note]  
> 由於回呼的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

## <a name="members"></a>成員

**IWbemObjectSink** 介面具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWbemObjectSink** 介面具有這些方法。



| 方法                                         | 描述                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**表明**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | 接收通知物件。<br/>                                                                               |
| [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | 由來源呼叫以指出通知順序的結尾，或將其他狀態碼傳送至接收。<br/> |



 

## <a name="remarks"></a>備註

當 (**IWbemObjectSink** 或 [**IWbemEventSink**](iwbemeventsink.md)) 執行事件訂閱接收時，請勿從接收器物件的 [**指示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) 或 [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) 方法內呼叫 WMI。 例如，呼叫 [**IWbemServices：： CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) 以從實作為中取消接收 [**，可能會**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) 干擾 WMI 狀態。 若要取消事件訂閱，請設定旗標，並從另一個執行緒或物件呼叫 **IWbemServices：： CancelAsyncCall** 。 對於與事件接收無關的執行（例如物件、列舉和查詢查詢），您可以回呼 WMI。

接收程式應在100毫秒內處理事件通知，因為傳遞事件通知的 WMI 執行緒無法執行其他工作，直到接收物件處理完成為止。 如果通知需要大量處理，接收端可以使用另一個執行緒的內部佇列來處理處理。

## <a name="examples"></a>範例

下列程式碼範例是物件接收的簡單執行。 此範例可搭配 [**iwbemservices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) 或 [**Iwbemservices：： CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) 使用，以接收傳回的實例：


```C++
#include <iostream>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone; 

public:
    QuerySink() { m_lRef = 0; }
   ~QuerySink() { bDone = TRUE; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE 
        QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            /* [in] */
            LONG lObjectCount,
            /* [size_is][in] */
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};


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


HRESULT QuerySink::Indicate(long lObjCount, IWbemClassObject **pArray)
{
    for (long i = 0; i < lObjCount; i++)
    {
        IWbemClassObject *pObj = pArray[i];

        // ... use the object.

        // AddRef() is only required if the object will be held after
        // the return to the caller.
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
    printf("QuerySink::SetStatus hResult = 0x%X\n", hResult);
    return WBEM_S_NO_ERROR;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                           |
| 標頭<br/>                   | <dl> <dt>Wbemcli (包含 Wbemidl) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Wbemuuid .lib</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl>                  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[適用于 WMI 的 COM API](com-api-for-wmi.md)
</dt> <dt>

[使用 c + + 進行非同步呼叫](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[在您的應用程式期間接收事件](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




