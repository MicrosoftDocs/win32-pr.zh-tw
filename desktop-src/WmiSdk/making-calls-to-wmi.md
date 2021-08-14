---
description: 提供者可以從其方法執行中呼叫 WMI 所執行的方法。
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: 對 WMI 進行呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76adae33db786a8174879e6c7e88b62fb69f3c59598ae7f055f41865b32dbf7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317672"
---
# <a name="making-calls-to-wmi"></a>對 WMI 進行呼叫

提供者可以從其方法執行中呼叫 WMI 所執行的方法。 不過，當提供者從其本身的相同方法的執行中呼叫 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 方法的 WMI 時，有一些特殊的考慮。 不論提供者是呼叫方法的同步或非同步版本，這些考慮都很重要。

提供者可以實作為的每個 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 方法都有 *pCtx* 參數，也就是 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 介面執行的指標。 當 WMI 呼叫提供者時，WMI 會在此參數中傳遞有效的指標。 提供者在處理要求時，一律必須在對 WMI 進行的任何呼叫中傳遞此相同指標。 如果未正確地設定 *pCtx* ，可能會導致 WMI 啟動無限迴圈。

下列程式碼範例顯示從 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)的執行中呼叫 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)的 WMI 執行的正確方式。


```C++
STDMETHODIMP CClassProv::GetObjectAsync (BSTR ObjectPath,
    long lFlags, IWbemContext *pCtx,
    IWbemObjectSink *pHandler)
{
  IWbemClassObject *pclObj = NULL;
  IWbemServices* m_pNamespace;
  HRESULT hr = m_pNamespace->GetObject(
      _bstr_t(L"AClass"), 0, pCtx, &pclObj, 
      NULL );
  pclObj->Release();
  return pHandler->SetStatus(0, hr, NULL, NULL);
}
```



本主題中的 c + + 程式碼範例需要下列參考，且必須 \# 要有語句才能正確編譯。


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



實例、類別和屬性提供者不得發出對 WMI 的任何呼叫，要求在服務讀取要求時修改資料。 這項規則唯一的提供者是推播提供者。 推播提供者是一種類別提供者，可將資料儲存在 WMI 儲存機制中，並依賴 WMI 來處理來自用戶端的要求。 當服務讀取要求時，推入提供者可以更新 WMI 儲存機制，但必須在適當的 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)呼叫中將 *lFlags* 參數設定為 **WBEM 旗標擁有者 \_ \_ \_ 更新**。

事件提供者不能在服務呼叫時進行任何類別變更。 它們也無法發出任何事件相關的呼叫，例如修改事件篩選。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發 WMI 提供者](developing-a-wmi-provider.md)
</dt> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> <dt>

[保護您的提供者](securing-your-provider.md)
</dt> </dl>

 

 



