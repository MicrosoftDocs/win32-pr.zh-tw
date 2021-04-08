---
title: 使用顯示內容
description: 文字服務架構 (TSF) 可讓文字服務提供文字的顯示內容。
ms.assetid: b0f6e8e8-586a-4b51-a498-fb22bd36161f
keywords:
- 文字服務架構 (TSF) ，顯示內容
- TSF (文字服務架構) ，顯示內容
- 啟用 TSF 的應用程式，顯示內容
- 顯示屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc725f67fab904db23f6232ac5efb5d63c62c26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671763"
---
# <a name="using-display-attributes"></a><span data-ttu-id="7d766-107">使用顯示內容</span><span class="sxs-lookup"><span data-stu-id="7d766-107">Using Display Attributes</span></span>

<span data-ttu-id="7d766-108">文字服務架構 (TSF) 可讓文字服務提供文字的顯示內容。</span><span class="sxs-lookup"><span data-stu-id="7d766-108">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="7d766-109">這可讓應用程式顯示其他視覺效果的意見反應。</span><span class="sxs-lookup"><span data-stu-id="7d766-109">This enables an application to display additional visual feedback.</span></span> <span data-ttu-id="7d766-110">例如，拼寫檢查文字服務可以反白顯示有紅色底線的拼錯字組。</span><span class="sxs-lookup"><span data-stu-id="7d766-110">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="7d766-111">可以提供的顯示內容是由 [TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) 結構所定義，其中包含文字色彩、文字背景色彩、底線樣式、底線色彩和底線粗細。</span><span class="sxs-lookup"><span data-stu-id="7d766-111">The display attributes that can be provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="7d766-112">轉譯文字時，應用程式應該取得所繪製文字的顯示內容，並使用屬性來修改文字的繪製方式。</span><span class="sxs-lookup"><span data-stu-id="7d766-112">When rendering text, an application should obtain the display attributes for the text drawn and use the attributes to modify how the text is drawn.</span></span> <span data-ttu-id="7d766-113">請完成下列步驟來取得顯示內容。</span><span class="sxs-lookup"><span data-stu-id="7d766-113">Complete the following steps to obtain display attributes.</span></span>

1.  <span data-ttu-id="7d766-114">藉 \_ \_ 由呼叫 [ITfCoNtext：： GETPROPERTY](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)，取得 GUID 屬性屬性的屬性物件。</span><span class="sxs-lookup"><span data-stu-id="7d766-114">Obtain a property object for GUID\_PROP\_ATTRIBUTE by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span></span>
2.  <span data-ttu-id="7d766-115">藉 \_ \_ 由呼叫 [ITfReadOnlyProperty：： GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)，取得指定範圍的 GUID 屬性屬性值。</span><span class="sxs-lookup"><span data-stu-id="7d766-115">Obtain the value of the GUID\_PROP\_ATTRIBUTE for the specified range by calling [ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span></span> <span data-ttu-id="7d766-116">這會提供 [TfGuidAtom](tfguidatom.md) 值。</span><span class="sxs-lookup"><span data-stu-id="7d766-116">This supplies a [TfGuidAtom](tfguidatom.md) value.</span></span>
3.  <span data-ttu-id="7d766-117">藉由呼叫[ITfCategoryMgr：： GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)，將[TfGuidAtom](tfguidatom.md)值轉換成 GUID。</span><span class="sxs-lookup"><span data-stu-id="7d766-117">Convert the [TfGuidAtom](tfguidatom.md) value into a GUID by calling [ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span></span>
4.  <span data-ttu-id="7d766-118">藉由呼叫[ITfDisplayAttributeMgr：： GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)來建立顯示內容的[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)物件。</span><span class="sxs-lookup"><span data-stu-id="7d766-118">Create an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for the display attribute by calling [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>
5.  <span data-ttu-id="7d766-119">藉由呼叫 [ITfDisplayAttributeInfo：： GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)來取得顯示內容資訊。</span><span class="sxs-lookup"><span data-stu-id="7d766-119">Obtain the display attribute information by calling [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>

<span data-ttu-id="7d766-120">下列程式碼範例示範從提供的內容、範圍和編輯 cookie 取得顯示內容的函式。</span><span class="sxs-lookup"><span data-stu-id="7d766-120">The following code example demonstrates a function that obtains the display attributes from a supplied context, range, and edit cookie.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7d766-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d766-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d766-122">TF \_ DISPLAYATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="7d766-122">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="7d766-123">ITfCoNtext：： GetProperty</span><span class="sxs-lookup"><span data-stu-id="7d766-123">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="7d766-124">ITfReadOnlyProperty：： GetValue</span><span class="sxs-lookup"><span data-stu-id="7d766-124">ITfReadOnlyProperty::GetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[<span data-ttu-id="7d766-125">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="7d766-125">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="7d766-126">ITfCategoryMgr：： GetGUID</span><span class="sxs-lookup"><span data-stu-id="7d766-126">ITfCategoryMgr::GetGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="7d766-127">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="7d766-127">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="7d766-128">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="7d766-128">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="7d766-129">ITfDisplayAttributeInfo::GetAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="7d766-129">ITfDisplayAttributeInfo::GetAttributeInfo</span></span> 
</dt> </dl>

 

 




