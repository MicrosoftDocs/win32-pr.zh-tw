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
# <a name="using-display-attributes"></a><span data-ttu-id="80a94-108">使用顯示內容</span><span class="sxs-lookup"><span data-stu-id="80a94-108">Using Display Attributes</span></span>

<span data-ttu-id="80a94-109">文字服務架構 (TSF) 可讓文字服務提供文字的顯示內容。</span><span class="sxs-lookup"><span data-stu-id="80a94-109">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="80a94-110">這可讓應用程式顯示其他視覺效果的意見反應。</span><span class="sxs-lookup"><span data-stu-id="80a94-110">This enables an application to display additional visual feedback.</span></span> <span data-ttu-id="80a94-111">例如，拼寫檢查文字服務可以反白顯示有紅色底線的拼錯字組。</span><span class="sxs-lookup"><span data-stu-id="80a94-111">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="80a94-112">可以提供的顯示內容是由 [TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) 結構所定義，其中包含文字色彩、文字背景色彩、底線樣式、底線色彩和底線粗細。</span><span class="sxs-lookup"><span data-stu-id="80a94-112">The display attributes that can be provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="80a94-113">轉譯文字時，應用程式應該取得所繪製文字的顯示內容，並使用屬性來修改文字的繪製方式。</span><span class="sxs-lookup"><span data-stu-id="80a94-113">When rendering text, an application should obtain the display attributes for the text drawn and use the attributes to modify how the text is drawn.</span></span> <span data-ttu-id="80a94-114">請完成下列步驟來取得顯示內容。</span><span class="sxs-lookup"><span data-stu-id="80a94-114">Complete the following steps to obtain display attributes.</span></span>

1.  <span data-ttu-id="80a94-115">藉 \_ \_ 由呼叫 [ITfCoNtext：： GETPROPERTY](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)，取得 GUID 屬性屬性的屬性物件。</span><span class="sxs-lookup"><span data-stu-id="80a94-115">Obtain a property object for GUID\_PROP\_ATTRIBUTE by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span></span>
2.  <span data-ttu-id="80a94-116">藉 \_ \_ 由呼叫 [ITfReadOnlyProperty：： GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)，取得指定範圍的 GUID 屬性屬性值。</span><span class="sxs-lookup"><span data-stu-id="80a94-116">Obtain the value of the GUID\_PROP\_ATTRIBUTE for the specified range by calling [ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span></span> <span data-ttu-id="80a94-117">這會提供 [TfGuidAtom](tfguidatom.md) 值。</span><span class="sxs-lookup"><span data-stu-id="80a94-117">This supplies a [TfGuidAtom](tfguidatom.md) value.</span></span>
3.  <span data-ttu-id="80a94-118">藉由呼叫[ITfCategoryMgr：： GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)，將[TfGuidAtom](tfguidatom.md)值轉換成 GUID。</span><span class="sxs-lookup"><span data-stu-id="80a94-118">Convert the [TfGuidAtom](tfguidatom.md) value into a GUID by calling [ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span></span>
4.  <span data-ttu-id="80a94-119">藉由呼叫[ITfDisplayAttributeMgr：： GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)來建立顯示內容的[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)物件。</span><span class="sxs-lookup"><span data-stu-id="80a94-119">Create an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for the display attribute by calling [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>
5.  <span data-ttu-id="80a94-120">藉由呼叫 [ITfDisplayAttributeInfo：： GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)來取得顯示內容資訊。</span><span class="sxs-lookup"><span data-stu-id="80a94-120">Obtain the display attribute information by calling [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>

<span data-ttu-id="80a94-121">下列程式碼範例示範從提供的內容、範圍和編輯 cookie 取得顯示內容的函式。</span><span class="sxs-lookup"><span data-stu-id="80a94-121">The following code example demonstrates a function that obtains the display attributes from a supplied context, range, and edit cookie.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="80a94-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="80a94-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80a94-123">TF \_ DISPLAYATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="80a94-123">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="80a94-124">ITfCoNtext：： GetProperty</span><span class="sxs-lookup"><span data-stu-id="80a94-124">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="80a94-125">ITfReadOnlyProperty：： GetValue</span><span class="sxs-lookup"><span data-stu-id="80a94-125">ITfReadOnlyProperty::GetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[<span data-ttu-id="80a94-126">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="80a94-126">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="80a94-127">ITfCategoryMgr：： GetGUID</span><span class="sxs-lookup"><span data-stu-id="80a94-127">ITfCategoryMgr::GetGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="80a94-128">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="80a94-128">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="80a94-129">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="80a94-129">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="80a94-130">ITfDisplayAttributeInfo::GetAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="80a94-130">ITfDisplayAttributeInfo::GetAttributeInfo</span></span> 
</dt> </dl>

 

 




