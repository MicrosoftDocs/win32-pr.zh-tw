---
title: 提供顯示內容
description: 瞭解如何提供顯示內容。 文字服務架構 (TSF) 可讓文字服務提供文字的顯示內容。
ms.assetid: 5809f5b8-0396-4abd-b5fe-61ecc8cd0914
keywords:
- 文字服務架構 (TSF) ，顯示內容
- TSF (文字服務架構) ，顯示內容
- 文字服務，顯示內容
- 顯示屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780cc191e39d5b1d0c3329bab87af5267e4a6c73
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406111"
---
# <a name="providing-display-attributes"></a><span data-ttu-id="07530-108">提供顯示內容</span><span class="sxs-lookup"><span data-stu-id="07530-108">Providing Display Attributes</span></span>

<span data-ttu-id="07530-109">文字服務架構 (TSF) 可讓文字服務提供文字的顯示內容。</span><span class="sxs-lookup"><span data-stu-id="07530-109">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="07530-110">這可提供其他視覺回饋給使用者。</span><span class="sxs-lookup"><span data-stu-id="07530-110">This enables additional visual feedback to be supplied to the user.</span></span> <span data-ttu-id="07530-111">例如，拼寫檢查文字服務可以反白顯示有紅色底線的拼錯字組。</span><span class="sxs-lookup"><span data-stu-id="07530-111">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="07530-112">提供的顯示內容是由 [TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) 結構所定義，其中包含文字色彩、文字背景色彩、底線樣式、底線色彩和底線粗細。</span><span class="sxs-lookup"><span data-stu-id="07530-112">The display attributes provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="07530-113">使用此顯示內容資訊的用戶端最常是應用程式，但也可以包含文字服務。</span><span class="sxs-lookup"><span data-stu-id="07530-113">Clients that use this display attribute information will most often be applications, but can also include text services.</span></span> <span data-ttu-id="07530-114">TSF 管理員會在顯示內容提供者與用戶端之間協調，並追蹤特定顯示內容的顯示內容提供者。</span><span class="sxs-lookup"><span data-stu-id="07530-114">The TSF manager mediates between the display attribute provider and the client and tracks the display attribute provider of the specific display attributes.</span></span>

<span data-ttu-id="07530-115">若要提供顯示內容，文字服務必須執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="07530-115">To provide display attributes, a text service must do the following.</span></span>

1.  <span data-ttu-id="07530-116">藉由呼叫 [ITfCategoryMgr：： RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) 與第一個參數的文字服務的類別識別碼、GUID TFCAT DISPLAYATTRIBUTEPROVIDER 做為第二個參數 \_ \_ 以及第三個參數的文字服務類別識別碼，來將文字服務註冊為顯示內容提供者。</span><span class="sxs-lookup"><span data-stu-id="07530-116">Register the text service as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span>
2.  <span data-ttu-id="07530-117">執行 [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) ，並將它提供給 class factory。</span><span class="sxs-lookup"><span data-stu-id="07530-117">Implement [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) and make it available from the class factory.</span></span>
3.  <span data-ttu-id="07530-118">執行 [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) ，並將它提供給 [ITfDisplayAttributeProvider：： EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)。</span><span class="sxs-lookup"><span data-stu-id="07530-118">Implement [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) and make it available from [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span></span>
4.  <span data-ttu-id="07530-119">針對文字服務提供的每個顯示內容類型，執行 [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) 物件。</span><span class="sxs-lookup"><span data-stu-id="07530-119">Implement an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for each type of display attribute that the text service provides.</span></span>

## <a name="applying-the-display-attributes"></a><span data-ttu-id="07530-120">套用顯示內容</span><span class="sxs-lookup"><span data-stu-id="07530-120">Applying the Display Attributes</span></span>

<span data-ttu-id="07530-121">文字服務必須將顯示內容套用至某範圍的文字。</span><span class="sxs-lookup"><span data-stu-id="07530-121">The text service must apply the display attribute to a range of text.</span></span> <span data-ttu-id="07530-122">文字服務只能在讀取/寫入編輯會話期間修改屬性值。</span><span class="sxs-lookup"><span data-stu-id="07530-122">A text service can only modify the property value during a read/write edit session.</span></span>

<span data-ttu-id="07530-123">假設這是在讀取/寫入編輯會話內，則會以下列方式套用顯示內容。</span><span class="sxs-lookup"><span data-stu-id="07530-123">Assuming this is within a read/write edit session, a display attribute is applied in the following manner.</span></span>

1.  <span data-ttu-id="07530-124">取得 [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) 物件，其中包含將套用顯示內容的文字。</span><span class="sxs-lookup"><span data-stu-id="07530-124">Obtain an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) object that covers the text that the display attribute will be applied to.</span></span>
2.  <span data-ttu-id="07530-125">藉由呼叫[ITfCoNtext：： GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)與 GUID 屬性屬性，取得 text 屬性的[ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty)物件 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="07530-125">Obtain an [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) object for the text attributes by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) with GUID\_PROP\_ATTRIBUTE.</span></span>
3.  <span data-ttu-id="07530-126">藉由呼叫 [ITfCategoryMgr：： RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)，從文字服務定義的顯示內容識別碼 **GUID** 建立 [TfGuidAtom](tfguidatom.md) 。</span><span class="sxs-lookup"><span data-stu-id="07530-126">Create a [TfGuidAtom](tfguidatom.md) from the text service-defined display attribute identifier **GUID** by calling [ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>
4.  <span data-ttu-id="07530-127">將 VARIANT 變數初始化為 VT \_ I4，並將 **lVal** 成員設定為上一個步驟中建立的 **TfGuidAtom** 。</span><span class="sxs-lookup"><span data-stu-id="07530-127">Initialize a VARIANT variable to VT\_I4 and set the **lVal** member to the **TfGuidAtom** created in the previous step.</span></span>
5.  <span data-ttu-id="07530-128">藉由呼叫 [ITfProperty：： SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) 與讀取/寫入編輯 cookie、範圍以及在上一個步驟中初始化的變異數，將顯示內容套用至範圍。</span><span class="sxs-lookup"><span data-stu-id="07530-128">Apply the display attribute to the range by calling [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) with the read/write edit cookie, the range and the VARIANT initialized in the previous step.</span></span>


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



## <a name="supplying-the-display-attribute-information-object"></a><span data-ttu-id="07530-129">提供顯示內容資訊物件</span><span class="sxs-lookup"><span data-stu-id="07530-129">Supplying the Display Attribute Information Object</span></span>

<span data-ttu-id="07530-130">用戶端會以兩種方式之一取得 **ITfDisplayAttributeInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="07530-130">A client obtains an **ITfDisplayAttributeInfo** object in one of two ways.</span></span>

1.  <span data-ttu-id="07530-131">用戶端會呼叫 [ITfDisplayAttributeMgr：： GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) 與顯示內容的 **GUID** 識別碼。</span><span class="sxs-lookup"><span data-stu-id="07530-131">The client calls [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) with the **GUID** identifier of the display attribute.</span></span> <span data-ttu-id="07530-132">當用戶端第一次呼叫 **ITfDisplayAttributeMgr：： GetDisplayAttributeInfo** 時，TSF 管理員會藉由呼叫 CoCreateInstance，並將類別識別碼做為第一個參數傳遞至 **ITfCategoryMgr：： RegisterCategory**，藉以建立顯示內容提供者的實例。</span><span class="sxs-lookup"><span data-stu-id="07530-132">The first time the client calls **ITfDisplayAttributeMgr::GetDisplayAttributeInfo**, the TSF manager will create an instance of the display attribute provider by calling CoCreateInstance with the class identifier passed as the first parameter to **ITfCategoryMgr::RegisterCategory**.</span></span> <span data-ttu-id="07530-133">後續呼叫 **ITfDisplayAttributeMgr：： GetDisplayAttributeInfo** 將會重複使用顯示內容提供者物件。</span><span class="sxs-lookup"><span data-stu-id="07530-133">Subsequent calls to **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** will reuse the display attribute provider object.</span></span>

    <span data-ttu-id="07530-134">TSF 管理員接著會使用顯示內容 **GUID** 來呼叫 [ITfDisplayAttributeProvider：： GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) ，以取得 **ITfDisplayAttributeInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="07530-134">The TSF manager then calls [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) with the display attribute **GUID** to obtain the **ITfDisplayAttributeInfo** object.</span></span>

    <span data-ttu-id="07530-135">TSF 管理員接著會將 **ITfDisplayAttributeInfo** 物件傳遞回用戶端。</span><span class="sxs-lookup"><span data-stu-id="07530-135">The TSF manager then passes the **ITfDisplayAttributeInfo** object back to the client.</span></span>

2.  <span data-ttu-id="07530-136">用戶端會呼叫 [ITfDisplayAttributeMgr：： EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) 來取得 **IEnumTfDisplayAttributeInfo** 物件，其中包含所有顯示內容提供者所提供的所有顯示內容。</span><span class="sxs-lookup"><span data-stu-id="07530-136">The client calls [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by all of the display attribute providers.</span></span> <span data-ttu-id="07530-137">TSF manager 會列舉每個顯示內容提供者，並藉由呼叫 CoCreateInstance，並將類別識別碼做為第三個參數傳遞至 **ITfCategoryMgr：： RegisterCategory**，以建立每個提供者的實例。</span><span class="sxs-lookup"><span data-stu-id="07530-137">The TSF manager enumerates each display attribute provider and creates an instance of each provider by calling CoCreateInstance with the class identifier passed as the third parameter to **ITfCategoryMgr::RegisterCategory**.</span></span>

    <span data-ttu-id="07530-138">然後，TSF 管理員會呼叫每個提供者的 **ITfDisplayAttributeProvider：： EnumDisplayAttributeInfo** ，以取得包含提供者所提供之所有顯示內容的 **IEnumTfDisplayAttributeInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="07530-138">The TSF manager then calls each provider's **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by the provider.</span></span>

    <span data-ttu-id="07530-139">然後，TSF 管理員會呼叫提供者的 [IEnumTfDisplayAttributeInfo：： Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) 方法，將每個取得的 **ITfDisplayAttributeInfo** 物件新增至管理員本身的列舉值，直到到達提供者列舉的結尾為止。</span><span class="sxs-lookup"><span data-stu-id="07530-139">The TSF manager then calls the provider's [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) method, adding each **ITfDisplayAttributeInfo** object obtained to the manager's own enumerator, until the end of the provider's enumeration is reached.</span></span>

    <span data-ttu-id="07530-140">當所有顯示內容提供者的所有 **ITfDisplayAttributeInfo** 物件都加入至 TSF manager 的列舉值時，管理員會將它的列舉值傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="07530-140">When all of the **ITfDisplayAttributeInfo** objects for all of the display attribute providers are added to the TSF manager's enumerator, the manager returns its enumerator to the client.</span></span> <span data-ttu-id="07530-141">然後，用戶端會呼叫 **IEnumTfDisplayAttributeInfo：： Next** 一次或多次，以取得 **ITfDisplayAttributeInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="07530-141">The client then calls **IEnumTfDisplayAttributeInfo::Next** one or more times to obtain the **ITfDisplayAttributeInfo** objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07530-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="07530-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07530-143">TF \_ DISPLAYATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="07530-143">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="07530-144">ITfCategoryMgr::RegisterCategory</span><span class="sxs-lookup"><span data-stu-id="07530-144">ITfCategoryMgr::RegisterCategory</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[<span data-ttu-id="07530-145">ITfDisplayAttributeProvider</span><span class="sxs-lookup"><span data-stu-id="07530-145">ITfDisplayAttributeProvider</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[<span data-ttu-id="07530-146">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="07530-146">IEnumTfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="07530-147">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="07530-147">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="07530-148">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="07530-148">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="07530-149">ITfRange</span><span class="sxs-lookup"><span data-stu-id="07530-149">ITfRange</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[<span data-ttu-id="07530-150">ITfProperty</span><span class="sxs-lookup"><span data-stu-id="07530-150">ITfProperty</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[<span data-ttu-id="07530-151">ITfCoNtext：： GetProperty</span><span class="sxs-lookup"><span data-stu-id="07530-151">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="07530-152">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="07530-152">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="07530-153">ITfCategoryMgr::RegisterGUID</span><span class="sxs-lookup"><span data-stu-id="07530-153">ITfCategoryMgr::RegisterGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[<span data-ttu-id="07530-154">ITfProperty：： SetValue</span><span class="sxs-lookup"><span data-stu-id="07530-154">ITfProperty::SetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[<span data-ttu-id="07530-155">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="07530-155">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="07530-156">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="07530-156">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="07530-157">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="07530-157">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="07530-158">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="07530-158">IEnumTfDisplayAttributeInfo</span></span> 
</dt> <dt>

 <span data-ttu-id="07530-159">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="07530-159">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span> 
</dt> <dt>

[<span data-ttu-id="07530-160">IEnumTfDisplayAttributeInfo：： Next</span><span class="sxs-lookup"><span data-stu-id="07530-160">IEnumTfDisplayAttributeInfo::Next</span></span>](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




