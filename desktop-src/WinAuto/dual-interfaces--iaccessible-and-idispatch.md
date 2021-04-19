---
title: 雙重介面 IAccessible 和 IDispatch
description: 伺服器開發人員必須提供標準元件物件模型 (COM) 介面 IDispatch 的可存取物件。
ms.assetid: 043d6777-6f9a-4e93-aadc-9cbe9a9119c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bbe19e35a04414253dc8f22c4edbc19a041b27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968698"
---
# <a name="dual-interfaces-iaccessible-and-idispatch"></a>雙重介面： IAccessible 和 IDispatch

伺服器開發人員必須提供標準元件物件模型 (COM) 介面 [**IDispatch**](idispatch-interface.md) 的可存取物件。 IDispatch 介面可讓以 Microsoft Visual Basic 撰寫的用戶端應用程式和各種指令碼語言，來使用 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)所公開的方法和屬性。 因為可存取的物件會透過 [IDispatch：： Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) 或直接使用 **IAccessible** 來提供物件的存取權，所以稱為具有雙重介面。

當 C/c + + 用戶端取回 IDispatch 介面指標時，用戶端可以呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來嘗試將 idispatch 介面指標轉換成 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標。 若要間接呼叫 **IAccessible** 方法，C/c + + 用戶端會呼叫 IDispatch：： Invoke。 為了提升效能，請呼叫 **IAccessible** 方法直接使用物件。

如需 **IDispatch** 用來識別 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法和屬性 (Dispid) 的分派識別碼清單，請參閱 [附錄 C： IAccessible dispid](appendix-c--iaccessible-dispids.md)。

> [!Note]  
> 在 Microsoft Active Accessibility 2.0 版和更新版本下，伺服器不需要完全實作為 [**IDispatch**](idispatch-interface.md) 的方法，但是可以 \_ 在初始化任何 out 參數之後，直接傳回 E >notimpl，如下列範例所示。

 


```C++
HRESULT STDMETHODCALLTYPE AccServer::GetTypeInfoCount(UINT* pctinfo)
{
    *pctinfo = 0;
    return E_NOTIMPL;
};
```



 

 