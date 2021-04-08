---
title: IADsExtension 介面
description: 本主題包含使用 IADsExtension 介面的 c + + 程式碼範例。
ms.assetid: fa94cc55-1ab2-4b6e-a3b6-8c20542adb42
ms.tgt_platform: multiple
keywords:
- 使用 IADsExtension ADSI
- ADSI ADSI，範例程式碼 C/c + +，使用 IADsExtension
- 延伸模組 ADSI、IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c950b6d305cc4c90ed75ff0cc96b5f7f344e12
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683089"
---
# <a name="iadsextension-interface"></a>IADsExtension 介面

[**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)介面的定義如下：


```C++
IADsExtension : public IUnknown
    {
    public:
        virtual HRESULT STDMETHODCALLTYPE Operate( 
            /* [in] */ DWORD dwCode,
            /* [in] */ VARIANT varData1,
            /* [in] */ VARIANT varData2,
            /* [in] */ VARIANT varData3) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateGetIDsOfNames( 
            /* [in] */ REFIID riid,
            /* [in] */ OLECHAR **rgszNames,
            /* [in] */ unsigned int cNames,
            /* [in] */ LCID lcid,
            /* [out] */ DISPID *rgDispid) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateInvoke( 
            /* [in] */ DISPID dispidMember,
            /* [in] */ REFIID riid,
            /* [in] */ LCID lcid,
            /* [in] */ WORD wFlags,
            /* [in] */ DISPPARAMS *pdispparams,
            /* [out] */ VARIANT *pvarResult,
            /* [out] */ EXCEPINFO *pexcepinfo,
            /* [out] */ unsigned int *puArgErr) = 0;
    };
```



ADSI) 的匯總工具 (會呼叫 [**IADsExtension：：操作**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) 方法。 擴充功能應該根據提供者的檔，來解讀 *dwCode* 參數和每個 *varData* 參數。

 (ADSI) 的匯總工具，會呼叫 [**IADsExtension：:P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) 方法。 它是在 ADSI 決定服務分派的延伸模組之後呼叫。 延伸模組可以使用型別資訊來取得 DISPID，也就是使用 [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) 函數。

ADSI 通常會在呼叫 [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames)函數之後呼叫 [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke)方法。 擴充功能應該呼叫它所執行的實際方法。 或者，擴充功能可以使用類型資訊，並呼叫 [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) 函式。

所有參數的意義與標準 [**IDispatch：： Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) 方法中的參數相同。

 

 