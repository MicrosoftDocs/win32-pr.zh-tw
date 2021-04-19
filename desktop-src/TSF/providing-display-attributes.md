---
title: 提供顯示內容
description: 文字服務架構 (TSF) 可讓文字服務提供文字的顯示內容。
ms.assetid: 5809f5b8-0396-4abd-b5fe-61ecc8cd0914
keywords:
- 文字服務架構 (TSF) ，顯示內容
- TSF (文字服務架構) ，顯示內容
- 文字服務，顯示內容
- 顯示屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f59bb64ef4f06df020a40189d273c703768d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967417"
---
# <a name="providing-display-attributes"></a>提供顯示內容

文字服務架構 (TSF) 可讓文字服務提供文字的顯示內容。 這可提供其他視覺回饋給使用者。 例如，拼寫檢查文字服務可以反白顯示有紅色底線的拼錯字組。 提供的顯示內容是由 [TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) 結構所定義，其中包含文字色彩、文字背景色彩、底線樣式、底線色彩和底線粗細。

使用此顯示內容資訊的用戶端最常是應用程式，但也可以包含文字服務。 TSF 管理員會在顯示內容提供者與用戶端之間協調，並追蹤特定顯示內容的顯示內容提供者。

若要提供顯示內容，文字服務必須執行下列動作。

1.  藉由呼叫 [ITfCategoryMgr：： RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) 與第一個參數的文字服務的類別識別碼、GUID TFCAT DISPLAYATTRIBUTEPROVIDER 做為第二個參數 \_ \_ 以及第三個參數的文字服務類別識別碼，來將文字服務註冊為顯示內容提供者。
2.  執行 [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) ，並將它提供給 class factory。
3.  執行 [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) ，並將它提供給 [ITfDisplayAttributeProvider：： EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)。
4.  針對文字服務提供的每個顯示內容類型，執行 [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) 物件。

## <a name="applying-the-display-attributes"></a>套用顯示內容

文字服務必須將顯示內容套用至某範圍的文字。 文字服務只能在讀取/寫入編輯會話期間修改屬性值。

假設這是在讀取/寫入編輯會話內，則會以下列方式套用顯示內容。

1.  取得 [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) 物件，其中包含將套用顯示內容的文字。
2.  藉由呼叫[ITfCoNtext：： GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)與 GUID 屬性屬性，取得 text 屬性的[ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty)物件 \_ \_ 。
3.  藉由呼叫 [ITfCategoryMgr：： RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)，從文字服務定義的顯示內容識別碼 **GUID** 建立 [TfGuidAtom](tfguidatom.md) 。
4.  將 VARIANT 變數初始化為 VT \_ I4，並將 **lVal** 成員設定為上一個步驟中建立的 **TfGuidAtom** 。
5.  藉由呼叫 [ITfProperty：： SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) 與讀取/寫入編輯 cookie、範圍以及在上一個步驟中初始化的變異數，將顯示內容套用至範圍。


```C++
STDAPI CEditSession::DoEditSession(TfEditCookie ec)
{
    HRESULT hr;
    ITfCategoryMgr *pCategoryMgr;
    TfGuidAtom  gaDisplayAttribute = TF_INVALID_GUIDATOM;

    //Create a TfGuidAtom for the display attribute identifier. 
    hr = CoCreateInstance(CLSID_TF_CategoryMgr,
                         NULL, 
                         CLSCTX_INPROC_SERVER, 
                         IID_ITfCategoryMgr, 
                         (void**)&pCategoryMgr);
    
    if(SUCCEEDED(hr))
    {
        hr = pCategoryMgr->RegisterGUID(guidDisplayAttribute, &gaDisplayAttribute);

        pCategoryMgr->Release();
    }
    
    //Apply the display attribute to the selected text. 
    if(TF_INVALID_GUIDATOM != gaDisplayAttribute)
    {
        TF_SELECTION tfSel;
        ULONG cFetched;

        //Get the selection. 
        hr = m_pContext->GetSelection(ec, TF_DEFAULT_SELECTION, 1, &tfSel, &cFetched);
        if(SUCCEEDED(hr) && cFetched)
        {
            ITfProperty *pDisplayAttributeProperty;

            //Get the display attribute property. 
            hr = m_pContext->GetProperty(GUID_PROP_ATTRIBUTE, &pDisplayAttributeProperty);
            if(SUCCEEDED(hr))
            {
                VARIANT var;

                VariantInit(&var);

                //All display attributes are TfGuidAtoms and TfGuidAtoms are VT_I4. 
                var.vt = VT_I4; 
                var.lVal = gaDisplayAttribute;

                //Set the display attribute value over the range. 
                hr = pDisplayAttributeProperty->SetValue(ec, tfSel.range, &var);

                pDisplayAttributeProperty->Release();
            }

            tfSel.range->Release();
        }
    }

    return S_OK;
}
```



## <a name="supplying-the-display-attribute-information-object"></a>提供顯示內容資訊物件

用戶端會以兩種方式之一取得 **ITfDisplayAttributeInfo** 物件。

1.  用戶端會呼叫 [ITfDisplayAttributeMgr：： GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) 與顯示內容的 **GUID** 識別碼。 當用戶端第一次呼叫 **ITfDisplayAttributeMgr：： GetDisplayAttributeInfo** 時，TSF 管理員會藉由呼叫 CoCreateInstance，並將類別識別碼做為第一個參數傳遞至 **ITfCategoryMgr：： RegisterCategory**，藉以建立顯示內容提供者的實例。 後續呼叫 **ITfDisplayAttributeMgr：： GetDisplayAttributeInfo** 將會重複使用顯示內容提供者物件。

    TSF 管理員接著會使用顯示內容 **GUID** 來呼叫 [ITfDisplayAttributeProvider：： GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) ，以取得 **ITfDisplayAttributeInfo** 物件。

    TSF 管理員接著會將 **ITfDisplayAttributeInfo** 物件傳遞回用戶端。

2.  用戶端會呼叫 [ITfDisplayAttributeMgr：： EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) 來取得 **IEnumTfDisplayAttributeInfo** 物件，其中包含所有顯示內容提供者所提供的所有顯示內容。 TSF manager 會列舉每個顯示內容提供者，並藉由呼叫 CoCreateInstance，並將類別識別碼做為第三個參數傳遞至 **ITfCategoryMgr：： RegisterCategory**，以建立每個提供者的實例。

    然後，TSF 管理員會呼叫每個提供者的 **ITfDisplayAttributeProvider：： EnumDisplayAttributeInfo** ，以取得包含提供者所提供之所有顯示內容的 **IEnumTfDisplayAttributeInfo** 物件。

    然後，TSF 管理員會呼叫提供者的 [IEnumTfDisplayAttributeInfo：： Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) 方法，將每個取得的 **ITfDisplayAttributeInfo** 物件新增至管理員本身的列舉值，直到到達提供者列舉的結尾為止。

    當所有顯示內容提供者的所有 **ITfDisplayAttributeInfo** 物件都加入至 TSF manager 的列舉值時，管理員會將它的列舉值傳回給用戶端。 然後，用戶端會呼叫 **IEnumTfDisplayAttributeInfo：： Next** 一次或多次，以取得 **ITfDisplayAttributeInfo** 物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[ITfCoNtext：： GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[ITfProperty：： SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 IEnumTfDisplayAttributeInfo 
</dt> <dt>

 ITfDisplayAttributeProvider::EnumDisplayAttributeInfo 
</dt> <dt>

[IEnumTfDisplayAttributeInfo：： Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




