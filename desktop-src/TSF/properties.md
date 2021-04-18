---
title: '屬性 (通用元素) '
description: 文字服務架構 (TSF) 提供可將中繼資料與某個文字範圍產生關聯的屬性。
ms.assetid: d1d0dd99-f303-4355-9835-917de9491a0b
keywords:
- 文字服務架構 (TSF) ，屬性
- TSF (文字服務架構) ，屬性
- 文字服務，屬性
- 啟用 TSF 的應用程式，屬性
- properties
- 文字服務架構 (TSF) ，屬性類型
- TSF (文字服務架構) ，屬性類型
- 文字服務，屬性類型
- 啟用 TSF 的應用程式，屬性類型
- 屬性類型
- 文字服務架構 (TSF) 、屬性的持續性儲存
- TSF (文字服務架構) ，持續儲存屬性
- 文字服務，持續儲存屬性
- 啟用 TSF 的應用程式，屬性的持續性儲存
- 屬性的持續性儲存
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff852bccfb7d9b6c94e57a2fa0cf8eef6fbdf18
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106968526"
---
# <a name="properties-common-elements"></a><span data-ttu-id="38e30-118">屬性 (通用元素) </span><span class="sxs-lookup"><span data-stu-id="38e30-118">Properties (Common Elements)</span></span>

<span data-ttu-id="38e30-119">文字服務架構 (TSF) 提供可將中繼資料與某個文字範圍產生關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="38e30-119">Text Services Framework (TSF) provides properties that associate metadata with a range of text.</span></span> <span data-ttu-id="38e30-120">這些屬性包括（但不限於）顯示內容（例如粗體文字）、文字的語言識別項，以及文字服務所提供的原始資料（例如與語音文字服務中的文字相關聯的音訊資料）。</span><span class="sxs-lookup"><span data-stu-id="38e30-120">These properties include, but are not limited to, display attributes such as bold text, the language identifier of the text, and raw data provided by a text service such as the audio data associated with text from the speech text service.</span></span>

<span data-ttu-id="38e30-121">下列範例示範如何查看具有紅色 (R) 、綠色 (G) 或藍色 (B) 的假設文字色彩屬性。</span><span class="sxs-lookup"><span data-stu-id="38e30-121">The following example demonstrates how a hypothetical text color property with possible values of red (R), green (G), or blue (B) can be viewed.</span></span>


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="38e30-122">不同類型的屬性可能會重迭。</span><span class="sxs-lookup"><span data-stu-id="38e30-122">Properties of different types can overlap.</span></span> <span data-ttu-id="38e30-123">例如，請採用上述範例，並新增可為粗體 (B) 或斜體 () 的文字屬性。</span><span class="sxs-lookup"><span data-stu-id="38e30-123">For example, take the previous example and add a text attribute that can be either bold (B) or italic (I).</span></span>


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="38e30-124">文字 "this" 會是粗體，「是」會是粗體和紅色，「部分」會以一般方式顯示，「彩色」會是綠色和斜體，而「文字」會是斜體。</span><span class="sxs-lookup"><span data-stu-id="38e30-124">The text "this" would be bold, "is" would be both bold and red, "some" would be displayed normally, "colored" would be green and italicized and "text" would be italicized.</span></span>

<span data-ttu-id="38e30-125">相同類型的屬性不能重迭。</span><span class="sxs-lookup"><span data-stu-id="38e30-125">Properties of the same type cannot overlap.</span></span> <span data-ttu-id="38e30-126">例如，不允許下列情況，因為「是」和「彩色」具有相同類型的重迭值。</span><span class="sxs-lookup"><span data-stu-id="38e30-126">For example, the following situation is not allowed because "is" and "colored" have overlapping values of the same types.</span></span>


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a><span data-ttu-id="38e30-127">屬性類型</span><span class="sxs-lookup"><span data-stu-id="38e30-127">Property Types</span></span>

<span data-ttu-id="38e30-128">TSF 會定義三種不同類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="38e30-128">TSF defines three different types of properties.</span></span>



|                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38e30-129">Static</span><span class="sxs-lookup"><span data-stu-id="38e30-129">Static</span></span>         | <span data-ttu-id="38e30-130">靜態屬性物件會儲存具有文字的屬性資料。</span><span class="sxs-lookup"><span data-stu-id="38e30-130">A static property object stores the property data with text.</span></span> <span data-ttu-id="38e30-131">它也會儲存套用屬性之每個範圍的文字資訊範圍。</span><span class="sxs-lookup"><span data-stu-id="38e30-131">It also stores the range of text information for each range that the property applies to.</span></span> <span data-ttu-id="38e30-132">ITfReadOnlyProperty：： GetType 會傳回 GUID \_ TFCAT \_ PROPSTYLE \_ 靜態類別。</span><span class="sxs-lookup"><span data-stu-id="38e30-132">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATIC category.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="38e30-133">Static-Compact</span><span class="sxs-lookup"><span data-stu-id="38e30-133">Static-Compact</span></span> | <span data-ttu-id="38e30-134">靜態 compact 屬性物件與靜態屬性物件相同，不同之處在于靜態 compact 屬性不會儲存範圍資料。</span><span class="sxs-lookup"><span data-stu-id="38e30-134">A static-compact property object is identical to a static property object except a static-compact property does not store range data.</span></span> <span data-ttu-id="38e30-135">當要求靜態壓縮屬性所涵蓋的範圍時，就會為每個相鄰屬性群組建立一個範圍。</span><span class="sxs-lookup"><span data-stu-id="38e30-135">When the range covered by a static-compact property is requested, a range is created for each group of adjacent properties.</span></span> <span data-ttu-id="38e30-136">靜態壓縮屬性是以每個字元為基礎來儲存屬性最有效率的方式。</span><span class="sxs-lookup"><span data-stu-id="38e30-136">Static-compact properties are the most efficient way to store properties on a per-character basis.</span></span> <span data-ttu-id="38e30-137">ITfReadOnlyProperty：： GetType 傳回 GUID \_ TFCAT \_ PROPSTYLE \_ STATICCOMPACT 類別目錄。</span><span class="sxs-lookup"><span data-stu-id="38e30-137">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATICCOMPACT category.</span></span> |
| <span data-ttu-id="38e30-138">自訂</span><span class="sxs-lookup"><span data-stu-id="38e30-138">Custom</span></span>         | <span data-ttu-id="38e30-139">自訂屬性物件會儲存套用屬性之每個範圍的範圍資訊。</span><span class="sxs-lookup"><span data-stu-id="38e30-139">A custom property object stores the range information for each range that the property applies to.</span></span> <span data-ttu-id="38e30-140">但是，它不會儲存屬性的實際資料。</span><span class="sxs-lookup"><span data-stu-id="38e30-140">It does not, however, store the actual data for the property.</span></span> <span data-ttu-id="38e30-141">相反地，自訂屬性會儲存 ITfPropertyStore 物件。</span><span class="sxs-lookup"><span data-stu-id="38e30-141">Instead, a custom property stores an ITfPropertyStore object.</span></span> <span data-ttu-id="38e30-142">TSF 管理員會使用此物件來存取和維護屬性資料。ITfReadOnlyProperty：： GetType 會傳回 GUID \_ TFCAT \_ PROPSTYLE \_ 自訂分類。</span><span class="sxs-lookup"><span data-stu-id="38e30-142">The TSF manager uses this object to access and maintain the property data.ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_CUSTOM category.</span></span>                                                                    |



 

## <a name="working-with-properties"></a><span data-ttu-id="38e30-143">使用屬性</span><span class="sxs-lookup"><span data-stu-id="38e30-143">Working with Properties</span></span>

<span data-ttu-id="38e30-144">屬性值和屬性是使用 [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) 介面取得，並使用 [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) 介面進行修改。</span><span class="sxs-lookup"><span data-stu-id="38e30-144">The property value and attributes are obtained using the [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) interface and modified using the [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) interface.</span></span>

<span data-ttu-id="38e30-145">如果需要特定的屬性類型，則會使用 [ITfCoNtext：： GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) 。</span><span class="sxs-lookup"><span data-stu-id="38e30-145">If a specific property type is required, then [ITfContext::GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) is used.</span></span> <span data-ttu-id="38e30-146">**ITfCoNtext：： GetProperty** 需要可識別要取得之屬性的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="38e30-146">**ITfContext::GetProperty** requires a **GUID** that identifies the property to obtain.</span></span> <span data-ttu-id="38e30-147">TSF 會定義一組所使用的 [預先定義屬性識別碼](predefined-properties.md) ，或文字服務可以定義它自己的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="38e30-147">TSF defines a set of [predefined property identifiers](predefined-properties.md) used or a text service can define its own property identifiers.</span></span> <span data-ttu-id="38e30-148">如果使用自訂屬性，屬性提供者必須發行屬性 **GUID** 以及所取得資料的格式。</span><span class="sxs-lookup"><span data-stu-id="38e30-148">If a custom property is used, the property provider must publish the property **GUID** and the format of the data obtained.</span></span>

<span data-ttu-id="38e30-149">例如，若要取得文字範圍擁有者的 **CLSID** ，請呼叫 **ITfCoNtext：： GetProperty** 來取得屬性物件，呼叫 [ITfProperty：： FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) 取得完全涵蓋該屬性的範圍，然後呼叫 [ITfReadOnlyProperty：： GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) 取得 [TfGuidAtom](/windows/desktop/TSF/tfguidatom) ，代表擁有文字之文字服務的 **CLSID** 。</span><span class="sxs-lookup"><span data-stu-id="38e30-149">For example, to obtain the **CLSID** for the owner of a range of text, call **ITfContext::GetProperty** to obtain the property object, call [ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) to obtain the range that entirely covers the property, then call [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) to get a [TfGuidAtom](/windows/desktop/TSF/tfguidatom) that represents the **CLSID** of the text service that owns the text.</span></span> <span data-ttu-id="38e30-150">下列範例顯示的函式會提供內容、範圍和編輯 cookie，以取得擁有文字之文字服務的 **CLSID** 。</span><span class="sxs-lookup"><span data-stu-id="38e30-150">The following example shows a function that, given a context, range and an edit cookie, will obtain the **CLSID** of the text service that owns the text.</span></span>


```C++
HRESULT GetTextOwner(   ITfContext *pContext, 
                        ITfRange *pRange, 
                        TfEditCookie ec, 
                        CLSID *pclsidOwner)
{
    HRESULT     hr;
    ITfProperty *pProp;

    *pclsidOwner = GUID_NULL;

    hr = pContext->GetProperty(GUID_PROP_TEXTOWNER, &pProp);
    if(S_OK == hr)
    {
        ITfRange    *pPropRange;

        hr = pProp->FindRange(ec, pRange, &pPropRange, TF_ANCHOR_START);
        if(S_OK == hr)
        {
            VARIANT var;

            VariantInit(&var);
            hr = pProp->GetValue(ec, pPropRange, &var);
            if(S_OK == hr)
            {
                if(VT_I4 == var.vt)
                {
                    /*
                    var.lVal is a TfGuidAtom that represents the CLSID of the 
                    text owner. Use ITfCategoryMgr to obtain the CLSID from 
                    the TfGuidAtom.
                    */
                    ITfCategoryMgr  *pCatMgr;

                    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                                            NULL, 
                                            CLSCTX_INPROC_SERVER, 
                                            IID_ITfCategoryMgr, 
                                            (LPVOID*)&pCatMgr);
                    if(SUCCEEDED(hr))
                    {
                        hr = pCatMgr->GetGUID((TfGuidAtom)var.lVal, pclsidOwner);
                        if(SUCCEEDED(hr))
                        {
                            /*
                            *pclsidOwner now contains the CLSID of the text 
                            service that owns the text at the selection.
                            */
                        }

                        pCatMgr->Release();
                    }
                }
                else
                {
                    //Unrecognized VARIANT type 
                    hr = E_FAIL;
                }
                
                VariantClear(&var);
            }
            
            pPropRange->Release();
        }
        
        pProp->Release();
    }

    return hr;
}

```



<span data-ttu-id="38e30-151">藉由從[ITfCoNtext：： EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties)取得[IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties)介面，也可以列舉屬性。</span><span class="sxs-lookup"><span data-stu-id="38e30-151">Properties can also be enumerated by obtaining an [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) interface from [ITfContext::EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span></span>

## <a name="persistent-storage-of-properties"></a><span data-ttu-id="38e30-152">屬性的持續性儲存</span><span class="sxs-lookup"><span data-stu-id="38e30-152">Persistent Storage of Properties</span></span>

<span data-ttu-id="38e30-153">通常，屬性對應用程式而言是透明的，而且是由一或多個文字服務所使用。</span><span class="sxs-lookup"><span data-stu-id="38e30-153">Often, properties are transparent to an application and are used by one or more text services.</span></span> <span data-ttu-id="38e30-154">為了保留屬性資料（例如儲存至檔案時），應用程式必須在儲存屬性資料時將其序列化，並在還原資料時 unserialize 屬性資料。</span><span class="sxs-lookup"><span data-stu-id="38e30-154">In order to preserve the property data, such as when saving to a file, an application must serialize the property data when it is stored and unserialize the property data when the data is restored.</span></span> <span data-ttu-id="38e30-155">在此情況下，應用程式不應該對個別屬性有興趣，但應該列舉內容中的所有屬性，並加以儲存。</span><span class="sxs-lookup"><span data-stu-id="38e30-155">In this case, the application should not be interested in individual properties, but should enumerate all properties in the context and store them.</span></span>

<span data-ttu-id="38e30-156">儲存屬性資料時，應用程式應該執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="38e30-156">When storing property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="38e30-157">藉由呼叫 **ITfCoNtext：： EnumProperties** 來取得屬性枚舉器。</span><span class="sxs-lookup"><span data-stu-id="38e30-157">Obtain a property enumerator by calling **ITfContext::EnumProperties**.</span></span>
2.  <span data-ttu-id="38e30-158">藉由呼叫 [IEnumTfProperties：： Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next)來列舉每個屬性。</span><span class="sxs-lookup"><span data-stu-id="38e30-158">Enumerate each property by calling [IEnumTfProperties::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).</span></span>
3.  <span data-ttu-id="38e30-159">針對每個屬性，藉由呼叫 [ITfReadOnlyProperty：： EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges)來取得範圍列舉值。</span><span class="sxs-lookup"><span data-stu-id="38e30-159">For each property, obtain a range enumerator by calling [ITfReadOnlyProperty::EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span></span>
4.  <span data-ttu-id="38e30-160">藉由呼叫 [IEnumTfRanges：： Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next)來列舉屬性中的每個範圍。</span><span class="sxs-lookup"><span data-stu-id="38e30-160">Enumerate each range in the property by calling [IEnumTfRanges::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).</span></span>
5.  <span data-ttu-id="38e30-161">針對屬性中的每個範圍，呼叫 [ITextStoreACPServices：：](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) 會使用屬性、範圍、 [TF 持續 \_ 性 \_ 屬性 \_ 標頭 \_ ACP](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) 結構，以及應用程式所執行的資料流程物件來進行序列化。</span><span class="sxs-lookup"><span data-stu-id="38e30-161">For each range in the property, call [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) with the property, range, a [TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) structure, and a stream object implemented by the application.</span></span>
6.  <span data-ttu-id="38e30-162">將 **TF \_ 持續性 \_ 屬性 \_ 標頭 \_ ACP** 結構的內容寫入持續性記憶體中。</span><span class="sxs-lookup"><span data-stu-id="38e30-162">Write the contents of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure into persistent memory.</span></span>
7.  <span data-ttu-id="38e30-163">將資料流程物件的內容寫入持續性記憶體中。</span><span class="sxs-lookup"><span data-stu-id="38e30-163">Write the contents of the stream object into persistent memory.</span></span>
8.  <span data-ttu-id="38e30-164">針對所有屬性中的所有範圍，繼續進行先前的步驟。</span><span class="sxs-lookup"><span data-stu-id="38e30-164">Continue the previous steps for all of the ranges in all of the properties.</span></span>
9.  <span data-ttu-id="38e30-165">應用程式應該將某種類型的 terminiator 寫入資料流程，如此一來，當還原資料時，就可以識別出停止點。</span><span class="sxs-lookup"><span data-stu-id="38e30-165">The application should write some type of terminiator into the stream so that, when the data is restored, a stopping point can be identified.</span></span>


```C++
HRESULT SaveProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        TfEditCookie ec, 
                        IStream *pStream)
{
    HRESULT             hr;
    IEnumTfProperties   *pEnumProps;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;
    ULONG uWritten;
    
    //Enumerate the properties in the context. 
    hr = pContext->EnumProperties(&pEnumProps);
    if(SUCCEEDED(hr))
    {
        ITfProperty *pProp;
        ULONG       uFetched;

        while(SUCCEEDED(pEnumProps->Next(1, &pProp, &uFetched)) && uFetched)
        {
            //Enumerate all the ranges that contain the property. 
            IEnumTfRanges   *pEnumRanges;
            hr = pProp->EnumRanges(ec, &pEnumRanges, NULL);
            if(SUCCEEDED(hr))
            {
                IStream *pTempStream;

                //Create a temporary stream to write the property data to. 
                hr = CreateStreamOnHGlobal(NULL, TRUE, &pTempStream);
                if(SUCCEEDED(hr))
                {
                    ITfRange    *pRange;

                    while(SUCCEEDED(pEnumRanges->Next(1, &pRange, &uFetched)) && uFetched)
                    {
                        LARGE_INTEGER li;

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);
                        
                        //Get the property header and data for the range. 
                        hr = pServices->Serialize(pProp, pRange, &PropHeader, pTempStream);

                        /*
                        Write the property header into the primary stream. 
                        The header also contains the size of the property 
                        data.
                        */
                        hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);

                        //Copy the property data from the temporary stream into the primary stream. 
                        ULARGE_INTEGER  uli;
                        uli.QuadPart = PropHeader.cb;

                        hr = pTempStream->CopyTo(pStream, uli, NULL, NULL);

                        pRange->Release();
                    }
                    
                    pTempStream->Release();
                }
                
                pEnumRanges->Release();
            }
            
            pProp->Release();
        }
        
        pEnumProps->Release();
    }

    //Write a property header with zero size and guid into the stream as a terminator 
    ZeroMemory(&PropHeader, sizeof(PropHeader));
    hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

    return hr;
}

```



<span data-ttu-id="38e30-166">**ITextStoreACPServices：：序列化**[ITfPropertyStore：：序列化](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span><span class="sxs-lookup"><span data-stu-id="38e30-166">**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span></span>

<span data-ttu-id="38e30-167">還原屬性資料時，應用程式應該執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="38e30-167">When restoring property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="38e30-168">將資料流程指標設定為第一個 **TF \_ 持續性 \_ 屬性 \_ 標頭 \_ ACP** 結構的開頭。</span><span class="sxs-lookup"><span data-stu-id="38e30-168">Set the stream pointer to the start of the first **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
2.  <span data-ttu-id="38e30-169">讀取 **TF \_ 持續性 \_ 屬性 \_ 標頭 \_ ACP** 結構。</span><span class="sxs-lookup"><span data-stu-id="38e30-169">Read the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
3.  <span data-ttu-id="38e30-170">使用 **TF \_ PERSISTENT \_ 屬性 \_ 標頭 \_ ACP** 結構的 **guidType** 成員呼叫 **ITfCoNtext：： GetProperty** 。</span><span class="sxs-lookup"><span data-stu-id="38e30-170">Call **ITfContext::GetProperty** with the **guidType** member of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
4.  <span data-ttu-id="38e30-171">應用程式此時可以進行兩項作業。</span><span class="sxs-lookup"><span data-stu-id="38e30-171">The application can do one of two things at this point.</span></span>
    1.  <span data-ttu-id="38e30-172">建立應用程式必須執行之 [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="38e30-172">Create an instance of an [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) object that the application must implement.</span></span> <span data-ttu-id="38e30-173">然後，針對 *pStream* 和 **ITfPersistentPropertyLoaderACP** 指標呼叫 [ITextStoreACPServices：： Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize)搭配 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="38e30-173">Then call [ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) with **NULL** for *pStream* and the **ITfPersistentPropertyLoaderACP** pointer.</span></span>
    2.  <span data-ttu-id="38e30-174">將輸入資料流程傳遞至 **ITextStoreACPServices：： Unserialize** ，並將 **Null** 傳遞至 *pLoader*。</span><span class="sxs-lookup"><span data-stu-id="38e30-174">Pass the input stream to **ITextStoreACPServices::Unserialize** and **NULL** for *pLoader*.</span></span>

    <span data-ttu-id="38e30-175">第一個方法是慣用方法，因為它是最有效率的方法。</span><span class="sxs-lookup"><span data-stu-id="38e30-175">The first method is preferred as it is the most efficient.</span></span> <span data-ttu-id="38e30-176">執行第二個方法會在 **ITextStoreACPServices：： Unserialize** 呼叫期間，從資料流程讀取所有屬性資料。</span><span class="sxs-lookup"><span data-stu-id="38e30-176">Implementing the second method causes all of the property data to be read from the stream during the **ITextStoreACPServices::Unserialize** call.</span></span> <span data-ttu-id="38e30-177">第一個方法會在稍後視需要讀取屬性資料。</span><span class="sxs-lookup"><span data-stu-id="38e30-177">The first method causes the property data to be read on demand at a later time.</span></span>
5.  <span data-ttu-id="38e30-178">重複上述步驟，直到 unserialized 所有屬性區塊為止。</span><span class="sxs-lookup"><span data-stu-id="38e30-178">Repeat the previous steps until all property blocks are unserialized.</span></span>


```C++
HRESULT LoadProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        IStream *pStream)
{
    HRESULT hr;
    ULONG   uRead;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;

    /*
    Read each property header and property data from the stream. The 
    list of properties is terminated by a TF_PERSISTENT_PROPERTY_HEADER_ACP 
    structure with a cb member of zero.
    */
    hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    while(  SUCCEEDED(hr) && 
            (sizeof(PropHeader) == uRead) && 
            (0 != PropHeader.cb))
    {
        ITfProperty *pProp;

        hr = pContext->GetProperty(PropHeader.guidType, &pProp);
        if(SUCCEEDED(hr))
        {
            /*
            Have TSF read the property data from the stream. This call 
            requests a read-only lock, so be sure it can be granted 
            or else this method will fail.
            */
            CTSFPersistentPropertyLoader *pLoader = new CTSFPersistentPropertyLoader(&PropHeader, pStream);
            hr = pServices->Unserialize(pProp, &PropHeader, NULL, pLoader);

            pProp->Release();
        }

        //Read the next header. 
        hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    }

    return hr;
}

```



 

 
