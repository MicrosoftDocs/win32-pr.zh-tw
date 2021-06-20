---
title: 使用顯示內容
description: 精簡如何使用顯示內容。 文字服務架構 (TSF) 可讓文字服務提供文字的顯示內容。
ms.assetid: b0f6e8e8-586a-4b51-a498-fb22bd36161f
keywords:
- 文字服務架構 (TSF) ，顯示內容
- TSF (文字服務架構) ，顯示內容
- 啟用 TSF 的應用程式，顯示內容
- 顯示屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3c576064ab22571b5a7822f5e6ff143add55d03
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406131"
---
# <a name="using-display-attributes"></a>使用顯示內容

文字服務架構 (TSF) 可讓文字服務提供文字的顯示內容。 這可讓應用程式顯示其他視覺效果的意見反應。 例如，拼寫檢查文字服務可以反白顯示有紅色底線的拼錯字組。 可以提供的顯示內容是由 [TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) 結構所定義，其中包含文字色彩、文字背景色彩、底線樣式、底線色彩和底線粗細。

轉譯文字時，應用程式應該取得所繪製文字的顯示內容，並使用屬性來修改文字的繪製方式。 請完成下列步驟來取得顯示內容。

1.  藉 \_ \_ 由呼叫 [ITfCoNtext：： GETPROPERTY](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)，取得 GUID 屬性屬性的屬性物件。
2.  藉 \_ \_ 由呼叫 [ITfReadOnlyProperty：： GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)，取得指定範圍的 GUID 屬性屬性值。 這會提供 [TfGuidAtom](tfguidatom.md) 值。
3.  藉由呼叫[ITfCategoryMgr：： GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)，將[TfGuidAtom](tfguidatom.md)值轉換成 GUID。
4.  藉由呼叫[ITfDisplayAttributeMgr：： GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)來建立顯示內容的[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)物件。
5.  藉由呼叫 [ITfDisplayAttributeInfo：： GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)來取得顯示內容資訊。

下列程式碼範例示範從提供的內容、範圍和編輯 cookie 取得顯示內容的函式。


```C++
HRESULT GetDispAttrFromRange(   ITfContext *pContext, 
                                ITfRange *pRange, 
                                TfEditCookie ec, 
                                TF_DISPLAYATTRIBUTE *pDispAttr)
{
    HRESULT     hr;
    
    //Create the category manager. 
    ITfCategoryMgr  *pCategoryMgr;
    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_ITfCategoryMgr, 
                            (LPVOID*)&pCategoryMgr);
    if(FAILED(hr))
    {
        return hr;
    }

    //Create the display attribute manager. 
    ITfDisplayAttributeMgr  *pDispMgr;
    hr = CoCreateInstance(  CLSID_TF_DisplayAttributeMgr,
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_ITfDisplayAttributeMgr, 
                            (LPVOID*)&pDispMgr);
    if(FAILED(hr))
    {
        pCategoryMgr->Release();
        return hr;
    }
    
    //Get the display attribute property. 
    ITfProperty *pProp;
    hr = pContext->GetProperty(GUID_PROP_ATTRIBUTE, &pProp);
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);
        hr = pProp->GetValue(ec, pRange, &var);
        if(S_OK == hr)  //Returns S_FALSE if the range is not completely covered by the property.  
        {
            if(VT_I4 == var.vt)
            {
                //The property is a guidatom. 
                GUID    guid;

                //Convert the guidatom into a GUID. 
                hr = pCategoryMgr->GetGUID((TfGuidAtom)var.lVal, &guid);
                if(SUCCEEDED(hr))
                {
                    ITfDisplayAttributeInfo *pDispInfo;

                    //Get the display attribute info object for this attribute. 
                    hr = pDispMgr->GetDisplayAttributeInfo(guid, &pDispInfo, NULL);
                    if(SUCCEEDED(hr))
                    {
                        //Get the display attribute info. 
                        hr = pDispInfo->GetAttributeInfo(pDispAttr);

                        pDispInfo->Release();
                    }
                }
            }
            else
            {
                //An error occurred; GUID_PROP_ATTRIBUTE must always be VT_I4. 
                hr = E_FAIL;
            }
            VariantClear(&var);
        }
    pProp->Release();
    }

    pCategoryMgr->Release();
    pDispMgr->Release();

    return hr;
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfCoNtext：： GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[ITfReadOnlyProperty：： GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[ITfCategoryMgr：： GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 ITfDisplayAttributeInfo::GetAttributeInfo 
</dt> </dl>

 

 




