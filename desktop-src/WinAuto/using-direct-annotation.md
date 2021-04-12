---
title: 使用直接注釋
description: 使用直接注釋
ms.assetid: d9d78e74-dcab-4974-945f-e8c5d42c04b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f0bdea5af896329b6836d21ca1dcee25bc2739
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315661"
---
# <a name="using-direct-annotation"></a>使用直接注釋

**若要使用直接注釋來覆寫屬性的值**

1.  使用 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 或 [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) 函式來建立 [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) 物件。
2.  呼叫 [**IAccPropServices：： SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop)，傳遞 **HWND**、物件識別碼、子識別碼、要覆寫的屬性，以及包含屬性新值的 [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) 。 此步驟會標注值。
3.  釋放介面指標和可用記憶體。

下列範例顯示如何標注靜態文字控制項的 [**Role**](role-property.md) 屬性。


```C++
HRESULT CMyTextControl::SetAccessibleProperties()
{
  // COM is assumed to be initialized...
  IAccPropServices* pAccPropServices = NULL;

  HRESULT hr = CoCreateInstance(CLSID_AccPropServices,
    NULL, CLSCTX_SERVER, IID_IAccPropServices, 
    (void**)&pAccPropServices);

  if (SUCCEEDED(hr))
  {
    // Annotating the Role of this object to be STATICTEXT
    VARIANT var;
    var.vt = VT_I4;
    var.lVal = ROLE_SYSTEM_STATICTEXT;

    hr = pAccPropServices->SetHwndProp(_hwnd,
      OBJID_CLIENT,
      CHILDID_SELF,
      PROPID_ACC_ROLE,
      var);

    pAccPropServices->Release();
  }
  return hr;
}
```



## <a name="properties-supported-when-specifying-a-value"></a>指定值時支援的屬性

當您指定值時，可以標注下列 Microsoft Active Accessibility 屬性 (其中的值必須是直接注釋) 的附注型別。 若要覆寫或加入 Microsoft 消費者介面自動化屬性至控制項，您可以指定消費者介面自動化屬性識別碼，而不是 Microsoft Active Accessibility 屬性識別碼。 如需消費者介面自動化識別碼的清單，請參閱 [屬性識別碼](uiauto-entry-propids.md)。



| 屬性                      | 類型     |
|-------------------------------|----------|
| PROPID \_ ACC \_ 名稱             | VT \_ BSTR |
| PROPID \_ ACC \_ 描述      | VT \_ BSTR |
| PROPID \_ ACC \_ 角色             | VT \_ I4   |
| PROPID \_ ACC \_ 狀態            | VT \_ I4   |
| PROPID \_ ACC \_ 說明             | VT \_ BSTR |
| PROPID \_ ACC \_ KEYBOARDSHORTCUT | VT \_ BSTR |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR |
| PROPID \_ ACC 的 \_ VALUEMAP         | VT \_ BSTR |
| PROPID \_ ACC \_ ROLEMAP          | VT \_ BSTR |
| PROPID \_ ACC \_ STATEMAP         | VT \_ BSTR |



 

 

 