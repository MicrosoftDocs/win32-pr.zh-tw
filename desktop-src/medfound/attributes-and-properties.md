---
description: 屬性是索引鍵/值組，其中索引鍵是 GUID，而值則是 PROPVARIANT。 在 Microsoft 媒體基礎中，屬性是用來設定物件、描述媒體格式、查詢物件屬性，以及其他用途。
ms.assetid: 44af5e03-5f0a-4564-b9d6-b8c935df35b2
title: 媒體基礎中的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e7893586aa1e966b95c1af5d04246bbb0c82ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689368"
---
# <a name="attributes-in-media-foundation"></a><span data-ttu-id="adbf5-104">媒體基礎中的屬性</span><span class="sxs-lookup"><span data-stu-id="adbf5-104">Attributes in Media Foundation</span></span>

<span data-ttu-id="adbf5-105">屬性是索引鍵/值組，其中索引鍵是 GUID，而值則是 **PROPVARIANT**。</span><span class="sxs-lookup"><span data-stu-id="adbf5-105">An attribute is a key/value pair, where the key is a GUID and the value is a **PROPVARIANT**.</span></span> <span data-ttu-id="adbf5-106">在 Microsoft 媒體基礎中，屬性是用來設定物件、描述媒體格式、查詢物件屬性，以及其他用途。</span><span class="sxs-lookup"><span data-stu-id="adbf5-106">Attributes are used throughout Microsoft Media Foundation to configure objects, describe media formats, query object properties, and other purposes.</span></span>

<span data-ttu-id="adbf5-107">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="adbf5-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="adbf5-108">關於屬性</span><span class="sxs-lookup"><span data-stu-id="adbf5-108">About Attributes</span></span>](#about-attributes)
-   [<span data-ttu-id="adbf5-109">序列化屬性</span><span class="sxs-lookup"><span data-stu-id="adbf5-109">Serializing Attributes</span></span>](#serializing-attributes)
-   [<span data-ttu-id="adbf5-110">執行 IMFAttributes</span><span class="sxs-lookup"><span data-stu-id="adbf5-110">Implementing IMFAttributes</span></span>](#implementing-imfattributes)
-   [<span data-ttu-id="adbf5-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="adbf5-111">Related topics</span></span>](#related-topics)

## <a name="about-attributes"></a><span data-ttu-id="adbf5-112">關於屬性</span><span class="sxs-lookup"><span data-stu-id="adbf5-112">About Attributes</span></span>

<span data-ttu-id="adbf5-113">屬性是索引鍵/值組，其中索引鍵是 GUID，而值則是 **PROPVARIANT**。</span><span class="sxs-lookup"><span data-stu-id="adbf5-113">An attribute is a key/value pair, where the key is a GUID and the value is a **PROPVARIANT**.</span></span> <span data-ttu-id="adbf5-114">屬性值限制為下列資料類型：</span><span class="sxs-lookup"><span data-stu-id="adbf5-114">Attribute values are restricted to the following data types:</span></span>

-   <span data-ttu-id="adbf5-115">不帶正負號的32位整數 (**UINT32**) 。</span><span class="sxs-lookup"><span data-stu-id="adbf5-115">Unsigned 32-bit integer (**UINT32**).</span></span>
-   <span data-ttu-id="adbf5-116">不帶正負號的64位整數 (**UINT64**) 。</span><span class="sxs-lookup"><span data-stu-id="adbf5-116">Unsigned 64-bit integer (**UINT64**).</span></span>
-   <span data-ttu-id="adbf5-117">64位浮點數。</span><span class="sxs-lookup"><span data-stu-id="adbf5-117">64-bit floating-point number.</span></span>
-   <span data-ttu-id="adbf5-118">GUID。</span><span class="sxs-lookup"><span data-stu-id="adbf5-118">GUID.</span></span>
-   <span data-ttu-id="adbf5-119">以 Null 結尾的寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="adbf5-119">Null-terminated wide-character string.</span></span>
-   <span data-ttu-id="adbf5-120">位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="adbf5-120">Byte array.</span></span>
-   <span data-ttu-id="adbf5-121">**IUnknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="adbf5-121">**IUnknown** pointer.</span></span>

<span data-ttu-id="adbf5-122">這些類型是在 [**MF \_ 屬性 \_ 類型**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type) 列舉中定義。</span><span class="sxs-lookup"><span data-stu-id="adbf5-122">These types are defined in the [**MF\_ATTRIBUTE\_TYPE**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type) enumeration.</span></span> <span data-ttu-id="adbf5-123">若要設定或抓取屬性值，請使用 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。</span><span class="sxs-lookup"><span data-stu-id="adbf5-123">To set or retrieve attribute values, use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="adbf5-124">這個介面包含型別安全方法，可依資料類型取得和設定值。</span><span class="sxs-lookup"><span data-stu-id="adbf5-124">This interface contains type-safe methods to get and set values by data type.</span></span> <span data-ttu-id="adbf5-125">例如，若要設定32位整數，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="adbf5-125">For example, to set a 32-bit integer, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span> <span data-ttu-id="adbf5-126">屬性索引鍵在物件內是唯一的。</span><span class="sxs-lookup"><span data-stu-id="adbf5-126">Attribute keys are unique within an object.</span></span> <span data-ttu-id="adbf5-127">如果您使用相同的索引鍵來設定兩個不同的值，則第二個值會覆寫第一個。</span><span class="sxs-lookup"><span data-stu-id="adbf5-127">If you set two different values with the same key, the second value overwrites the first.</span></span>

<span data-ttu-id="adbf5-128">數個媒體基礎介面會繼承 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。</span><span class="sxs-lookup"><span data-stu-id="adbf5-128">Several Media Foundation interfaces inherit the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="adbf5-129">公開此介面的物件具有應用程式應該在物件上設定的選擇性或強制性屬性，或具有應用程式可取得的屬性。</span><span class="sxs-lookup"><span data-stu-id="adbf5-129">Objects that expose this interface have optional or mandatory attributes that the application should set on the object, or have attributes that the application can retrieve.</span></span> <span data-ttu-id="adbf5-130">此外，某些方法和函式會採用 **IMFAttributes** 指標做為參數，讓應用程式能夠設定設定資訊。</span><span class="sxs-lookup"><span data-stu-id="adbf5-130">Also, some methods and functions take an **IMFAttributes** pointer as a parameter, which enables the application to set configuration information.</span></span> <span data-ttu-id="adbf5-131">應用程式必須建立屬性存放區來保存設定屬性。</span><span class="sxs-lookup"><span data-stu-id="adbf5-131">The application must create an attribute store to hold the configuration attributes.</span></span> <span data-ttu-id="adbf5-132">若要建立空的屬性存放區，請呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)。</span><span class="sxs-lookup"><span data-stu-id="adbf5-132">To create an empty attribute store, call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>

<span data-ttu-id="adbf5-133">下列程式碼顯示兩個函式。</span><span class="sxs-lookup"><span data-stu-id="adbf5-133">The following code shows two functions.</span></span> <span data-ttu-id="adbf5-134">第一個會建立新的屬性存放區，並將名為 MY attribute 的假設屬性設定為 \_ 字串值。</span><span class="sxs-lookup"><span data-stu-id="adbf5-134">The first creates a new attribute store and sets a hypothetical attribute named MY\_ATTRIBUTE with a string value.</span></span> <span data-ttu-id="adbf5-135">第二個函式會捕獲這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="adbf5-135">The second function retrieves the value of this attribute.</span></span>


```C++
extern const GUID MY_ATTRIBUTE;

HRESULT ShowCreateAttributeStore(IMFAttributes **ppAttributes)
{
    IMFAttributes *pAttributes = NULL;
    const UINT32 cElements = 10;  // Starting size.

    // Create the empty attribute store.
    HRESULT hr = MFCreateAttributes(&pAttributes, cElements);

    // Set the MY_ATTRIBUTE attribute with a string value.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MY_ATTRIBUTE,
            L"This is a string value"
            );
    }

    // Return the IMFAttributes pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }

    SAFE_RELEASE(pAttributes);

    return hr;
}

HRESULT ShowGetAttributes()
{
    IMFAttributes *pAttributes = NULL;
    WCHAR *pwszValue = NULL;
    UINT32 cchLength = 0;

    // Create the attribute store.
    HRESULT hr = ShowCreateAttributeStore(&pAttributes);

    // Get the attribute.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetAllocatedString(
            MY_ATTRIBUTE,
            &pwszValue,
            &cchLength
            );
    }

    CoTaskMemFree(pwszValue);
    SAFE_RELEASE(pAttributes);

    return hr;
}
```



<span data-ttu-id="adbf5-136">如需媒體基礎屬性的完整清單，請參閱 [媒體基礎屬性](media-foundation-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="adbf5-136">For a complete list of Media Foundation attributes, see [Media Foundation Attributes](media-foundation-attributes.md).</span></span> <span data-ttu-id="adbf5-137">每個屬性的預期資料類型記載于該處。</span><span class="sxs-lookup"><span data-stu-id="adbf5-137">The expected data type for each attribute is documented there.</span></span>

## <a name="serializing-attributes"></a><span data-ttu-id="adbf5-138">序列化屬性</span><span class="sxs-lookup"><span data-stu-id="adbf5-138">Serializing Attributes</span></span>

<span data-ttu-id="adbf5-139">媒體基礎有兩個函數可序列化屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="adbf5-139">Media Foundation has two functions for serializing attribute stores.</span></span> <span data-ttu-id="adbf5-140">其中一個會將屬性寫入位元組陣列，另一個則會將它們寫入支援 **IStream** 介面的資料流程。</span><span class="sxs-lookup"><span data-stu-id="adbf5-140">One writes the attributes to a byte array, the other writes them to a stream that supports the **IStream** interface.</span></span> <span data-ttu-id="adbf5-141">每個函式都有一個載入資料的對應函數。</span><span class="sxs-lookup"><span data-stu-id="adbf5-141">Each function has a corresponding function that loads the data.</span></span>



| <span data-ttu-id="adbf5-142">作業</span><span class="sxs-lookup"><span data-stu-id="adbf5-142">Operation</span></span> | <span data-ttu-id="adbf5-143">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="adbf5-143">Byte Array</span></span>                                                   | <span data-ttu-id="adbf5-144">IStream</span><span class="sxs-lookup"><span data-stu-id="adbf5-144">IStream</span></span>                                                                        |
|-----------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="adbf5-145">儲存</span><span class="sxs-lookup"><span data-stu-id="adbf5-145">Save</span></span>      | [<span data-ttu-id="adbf5-146">**MFGetAttributesAsBlob**</span><span class="sxs-lookup"><span data-stu-id="adbf5-146">**MFGetAttributesAsBlob**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob)       | [<span data-ttu-id="adbf5-147">**MFSerializeAttributesToStream**</span><span class="sxs-lookup"><span data-stu-id="adbf5-147">**MFSerializeAttributesToStream**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream)         |
| <span data-ttu-id="adbf5-148">載入</span><span class="sxs-lookup"><span data-stu-id="adbf5-148">Load</span></span>      | [<span data-ttu-id="adbf5-149">**MFInitAttributesFromBlob**</span><span class="sxs-lookup"><span data-stu-id="adbf5-149">**MFInitAttributesFromBlob**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob) | [<span data-ttu-id="adbf5-150">**MFDeserializeAttributesFromStream**</span><span class="sxs-lookup"><span data-stu-id="adbf5-150">**MFDeserializeAttributesFromStream**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream) |



 

<span data-ttu-id="adbf5-151">若要將屬性存放區的內容寫入位元組陣列中，請呼叫 [**MFGetAttributesAsBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob)。</span><span class="sxs-lookup"><span data-stu-id="adbf5-151">To write the contents of an attribute store into a byte array, call [**MFGetAttributesAsBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob).</span></span> <span data-ttu-id="adbf5-152">系統會忽略具有 **IUnknown** 指標值的屬性。</span><span class="sxs-lookup"><span data-stu-id="adbf5-152">Attributes with **IUnknown** pointer values are ignored.</span></span> <span data-ttu-id="adbf5-153">若要將屬性（attribute）載入回屬性存放區，請呼叫 [**MFInitAttributesFromBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob)。</span><span class="sxs-lookup"><span data-stu-id="adbf5-153">To load the attributes back into an attribute store, call [**MFInitAttributesFromBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob).</span></span>

<span data-ttu-id="adbf5-154">若要將屬性存放區寫入資料流程，請呼叫 [**MFSerializeAttributesToStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream)。</span><span class="sxs-lookup"><span data-stu-id="adbf5-154">To write an attribute store to a stream, call [**MFSerializeAttributesToStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream).</span></span> <span data-ttu-id="adbf5-155">此函數可以封送處理 **IUnknown** 指標值。</span><span class="sxs-lookup"><span data-stu-id="adbf5-155">This function can marshal **IUnknown** pointer values.</span></span> <span data-ttu-id="adbf5-156">呼叫端必須提供可執行 **IStream** 介面的資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="adbf5-156">The caller must provide a stream object that implements the **IStream** interface.</span></span> <span data-ttu-id="adbf5-157">若要從資料流程載入屬性存放區，請呼叫 [**MFDeserializeAttributesFromStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream)。</span><span class="sxs-lookup"><span data-stu-id="adbf5-157">To load an attribute store from a stream, call [**MFDeserializeAttributesFromStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream).</span></span>

## <a name="implementing-imfattributes"></a><span data-ttu-id="adbf5-158">執行 IMFAttributes</span><span class="sxs-lookup"><span data-stu-id="adbf5-158">Implementing IMFAttributes</span></span>

<span data-ttu-id="adbf5-159">媒體基礎提供 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)的內建執行，其是透過呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 函數來取得。</span><span class="sxs-lookup"><span data-stu-id="adbf5-159">Media Foundation provides a stock implementation of [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), which is obtained by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span> <span data-ttu-id="adbf5-160">在大多數情況下，您應該使用此實作為，而不提供您自己的自訂執行。</span><span class="sxs-lookup"><span data-stu-id="adbf5-160">In most situations, you should use this implementation, and not provide your own custom implementation.</span></span>

<span data-ttu-id="adbf5-161">當您需要執行 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面時，有一種情況：如果您執行的是繼承 **IMFAttributes** 的第二個介面。</span><span class="sxs-lookup"><span data-stu-id="adbf5-161">There is one situation when you might need to implement the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface: If you implement a second interface that inherits **IMFAttributes**.</span></span> <span data-ttu-id="adbf5-162">在這種情況下，您必須為第二個介面所繼承的 **IMFAttributes** 方法提供實作為。</span><span class="sxs-lookup"><span data-stu-id="adbf5-162">In that case, you must provide implementations for the **IMFAttributes** methods inherited by the second interface.</span></span>

<span data-ttu-id="adbf5-163">在此情況下，建議您包裝現有的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)媒體基礎執行。</span><span class="sxs-lookup"><span data-stu-id="adbf5-163">In this situation, it is recommended to wrap the existing Media Foundation implementation of [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="adbf5-164">下列程式碼顯示的類別範本會保存 **IMFAttributes** 指標並包裝每個 **IMFAttributes** 方法，但 **IUnknown** 方法除外。</span><span class="sxs-lookup"><span data-stu-id="adbf5-164">The following code shows a class template that holds an **IMFAttributes** pointer and wraps every **IMFAttributes** method, except for the **IUnknown** methods.</span></span>


```C++
#include <assert.h>

// Helper class to implement IMFAttributes. 

// This is an abstract class; the derived class must implement the IUnknown 
// methods. This class is a wrapper for the standard attribute store provided 
// in Media Foundation.

// template parameter: 
// The interface you are implementing, either IMFAttributes or an interface 
// that inherits IMFAttributes, such as IMFActivate

template <class IFACE=IMFAttributes>
class CBaseAttributes : public IFACE
{
protected:
    IMFAttributes *m_pAttributes;

    // This version of the constructor does not initialize the 
    // attribute store. The derived class must call Initialize() in 
    // its own constructor.
    CBaseAttributes() : m_pAttributes(NULL)
    {
    }

    // This version of the constructor initializes the attribute 
    // store, but the derived class must pass an HRESULT parameter 
    // to the constructor.

    CBaseAttributes(HRESULT& hr, UINT32 cInitialSize = 0) : m_pAttributes(NULL)
    {
        hr = Initialize(cInitialSize);
    }

    // The next version of the constructor uses a caller-provided 
    // implementation of IMFAttributes.

    // (Sometimes you want to delegate IMFAttributes calls to some 
    // other object that implements IMFAttributes, rather than using 
    // MFCreateAttributes.)

    CBaseAttributes(HRESULT& hr, IUnknown *pUnk)
    {
        hr = Initialize(pUnk);
    }

    virtual ~CBaseAttributes()
    {
        if (m_pAttributes)
        {
            m_pAttributes->Release();
        }
    }

    // Initializes the object by creating the standard Media Foundation attribute store.
    HRESULT Initialize(UINT32 cInitialSize = 0)
    {
        if (m_pAttributes == NULL)
        {
            return MFCreateAttributes(&m_pAttributes, cInitialSize); 
        }
        else
        {
            return S_OK;
        }
    }

    // Initializes this object from a caller-provided attribute store.
    // pUnk: Pointer to an object that exposes IMFAttributes.
    HRESULT Initialize(IUnknown *pUnk)
    {
        if (m_pAttributes)
        {
            m_pAttributes->Release();
            m_pAttributes = NULL;
        }


        return pUnk->QueryInterface(IID_PPV_ARGS(&m_pAttributes));
    }

public:

    // IMFAttributes methods

    STDMETHODIMP GetItem(REFGUID guidKey, PROPVARIANT* pValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItem(guidKey, pValue);
    }

    STDMETHODIMP GetItemType(REFGUID guidKey, MF_ATTRIBUTE_TYPE* pType)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItemType(guidKey, pType);
    }

    STDMETHODIMP CompareItem(REFGUID guidKey, REFPROPVARIANT Value, BOOL* pbResult)
    {
        assert(m_pAttributes);
        return m_pAttributes->CompareItem(guidKey, Value, pbResult);
    }

    STDMETHODIMP Compare(
        IMFAttributes* pTheirs, 
        MF_ATTRIBUTES_MATCH_TYPE MatchType, 
        BOOL* pbResult
        )
    {
        assert(m_pAttributes);
        return m_pAttributes->Compare(pTheirs, MatchType, pbResult);
    }

    STDMETHODIMP GetUINT32(REFGUID guidKey, UINT32* punValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUINT32(guidKey, punValue);
    }

    STDMETHODIMP GetUINT64(REFGUID guidKey, UINT64* punValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUINT64(guidKey, punValue);
    }

    STDMETHODIMP GetDouble(REFGUID guidKey, double* pfValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetDouble(guidKey, pfValue);
    }

    STDMETHODIMP GetGUID(REFGUID guidKey, GUID* pguidValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetGUID(guidKey, pguidValue);
    }

    STDMETHODIMP GetStringLength(REFGUID guidKey, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetStringLength(guidKey, pcchLength);
    }

    STDMETHODIMP GetString(REFGUID guidKey, LPWSTR pwszValue, UINT32 cchBufSize, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetString(guidKey, pwszValue, cchBufSize, pcchLength);
    }

    STDMETHODIMP GetAllocatedString(REFGUID guidKey, LPWSTR* ppwszValue, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetAllocatedString(guidKey, ppwszValue, pcchLength);
    }

    STDMETHODIMP GetBlobSize(REFGUID guidKey, UINT32* pcbBlobSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetBlobSize(guidKey, pcbBlobSize);
    }

    STDMETHODIMP GetBlob(REFGUID guidKey, UINT8* pBuf, UINT32 cbBufSize, UINT32* pcbBlobSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetBlob(guidKey, pBuf, cbBufSize, pcbBlobSize);
    }

    STDMETHODIMP GetAllocatedBlob(REFGUID guidKey, UINT8** ppBuf, UINT32* pcbSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetAllocatedBlob(guidKey, ppBuf, pcbSize);
    }

    STDMETHODIMP GetUnknown(REFGUID guidKey, REFIID riid, LPVOID* ppv)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUnknown(guidKey, riid, ppv);
    }

    STDMETHODIMP SetItem(REFGUID guidKey, REFPROPVARIANT Value)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetItem(guidKey, Value);
    }

    STDMETHODIMP DeleteItem(REFGUID guidKey)
    {
        assert(m_pAttributes);
        return m_pAttributes->DeleteItem(guidKey);
    }

    STDMETHODIMP DeleteAllItems()
    {
        assert(m_pAttributes);
        return m_pAttributes->DeleteAllItems();
    }

    STDMETHODIMP SetUINT32(REFGUID guidKey, UINT32 unValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUINT32(guidKey, unValue);
    }

    STDMETHODIMP SetUINT64(REFGUID guidKey,UINT64 unValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUINT64(guidKey, unValue);
    }

    STDMETHODIMP SetDouble(REFGUID guidKey, double fValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetDouble(guidKey, fValue);
    }

    STDMETHODIMP SetGUID(REFGUID guidKey, REFGUID guidValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetGUID(guidKey, guidValue);
    }

    STDMETHODIMP SetString(REFGUID guidKey, LPCWSTR wszValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetString(guidKey, wszValue);
    }

    STDMETHODIMP SetBlob(REFGUID guidKey, const UINT8* pBuf, UINT32 cbBufSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetBlob(guidKey, pBuf, cbBufSize);
    }

    STDMETHODIMP SetUnknown(REFGUID guidKey, IUnknown* pUnknown)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUnknown(guidKey, pUnknown);
    }

    STDMETHODIMP LockStore()
    {
        assert(m_pAttributes);
        return m_pAttributes->LockStore();
    }

    STDMETHODIMP UnlockStore()
    {
        assert(m_pAttributes);
        return m_pAttributes->UnlockStore();
    }

    STDMETHODIMP GetCount(UINT32* pcItems)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetCount(pcItems);
    }

    STDMETHODIMP GetItemByIndex(UINT32 unIndex, GUID* pguidKey, PROPVARIANT* pValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItemByIndex(unIndex, pguidKey, pValue);
    }

    STDMETHODIMP CopyAllItems(IMFAttributes* pDest)
    {
        assert(m_pAttributes);
        return m_pAttributes->CopyAllItems(pDest);
    }

    // Helper functions
    
    HRESULT SerializeToStream(DWORD dwOptions, IStream* pStm)      
        // dwOptions: Flags from MF_ATTRIBUTE_SERIALIZE_OPTIONS
    {
        assert(m_pAttributes);
        return MFSerializeAttributesToStream(m_pAttributes, dwOptions, pStm);
    }

    HRESULT DeserializeFromStream(DWORD dwOptions, IStream* pStm)
    {
        assert(m_pAttributes);
        return MFDeserializeAttributesFromStream(m_pAttributes, dwOptions, pStm);
    }

    // SerializeToBlob: Stores the attributes in a byte array. 
    // 
    // ppBuf: Receives a pointer to the byte array. 
    // pcbSize: Receives the size of the byte array.
    //
    // The caller must free the array using CoTaskMemFree.
    HRESULT SerializeToBlob(UINT8 **ppBuffer, UINT32 *pcbSize)
    {
        assert(m_pAttributes);

        if (ppBuffer == NULL)
        {
            return E_POINTER;
        }
        if (pcbSize == NULL)
        {
            return E_POINTER;
        }

        *ppBuffer = NULL;
        *pcbSize = 0;

        UINT32 cbSize = 0;
        BYTE *pBuffer = NULL;

        HRESULT hr = MFGetAttributesAsBlobSize(m_pAttributes, &cbSize);

        if (FAILED(hr))
        {
            return hr;
        }

        pBuffer = (BYTE*)CoTaskMemAlloc(cbSize);
        if (pBuffer == NULL)
        {
            return E_OUTOFMEMORY;
        }

        hr = MFGetAttributesAsBlob(m_pAttributes, pBuffer, cbSize);

        if (SUCCEEDED(hr))
        {
            *ppBuffer = pBuffer;
            *pcbSize = cbSize;
        }
        else
        {
            CoTaskMemFree(pBuffer);
        }
        return hr;
    }
    
    HRESULT DeserializeFromBlob(const UINT8* pBuffer, UINT cbSize)
    {
        assert(m_pAttributes);
        return MFInitAttributesFromBlob(m_pAttributes, pBuffer, cbSize);
    }

    HRESULT GetRatio(REFGUID guidKey, UINT32* pnNumerator, UINT32* punDenominator)
    {
        assert(m_pAttributes);
        return MFGetAttributeRatio(m_pAttributes, guidKey, pnNumerator, punDenominator);
    }

    HRESULT SetRatio(REFGUID guidKey, UINT32 unNumerator, UINT32 unDenominator)
    {
        assert(m_pAttributes);
        return MFSetAttributeRatio(m_pAttributes, guidKey, unNumerator, unDenominator);
    }

    // Gets an attribute whose value represents the size of something (eg a video frame).
    HRESULT GetSize(REFGUID guidKey, UINT32* punWidth, UINT32* punHeight)
    {
        assert(m_pAttributes);
        return MFGetAttributeSize(m_pAttributes, guidKey, punWidth, punHeight);
    }

    // Sets an attribute whose value represents the size of something (eg a video frame).
    HRESULT SetSize(REFGUID guidKey, UINT32 unWidth, UINT32 unHeight)
    {
        assert(m_pAttributes);
        return MFSetAttributeSize (m_pAttributes, guidKey, unWidth, unHeight);
    }
};
```



<span data-ttu-id="adbf5-165">下列程式碼說明如何從這個範本衍生類別：</span><span class="sxs-lookup"><span data-stu-id="adbf5-165">The following code shows how to derive a class from this template:</span></span>


```C++
#include <shlwapi.h>

class MyObject : public CBaseAttributes<>
{
    MyObject() : m_nRefCount(1) { }
    ~MyObject() { }

    long m_nRefCount;

public:

    // IUnknown
    STDMETHODIMP MyObject::QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(MyObject, IMFAttributes),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) MyObject::AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }

    STDMETHODIMP_(ULONG) MyObject::Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // Static function to create an instance of the object.

    static HRESULT CreateInstance(MyObject **ppObject)
    {
        HRESULT hr = S_OK;

        MyObject *pObject = new MyObject();
        if (pObject == NULL)
        {
            return E_OUTOFMEMORY;
        }

        // Initialize the attribute store.
        hr = pObject->Initialize();

        if (FAILED(hr))
        {
            delete pObject;
            return hr;
        }

        *ppObject = pObject;
        (*ppObject)->AddRef();

        return S_OK;
    }
};
```



<span data-ttu-id="adbf5-166">您必須呼叫 `CBaseAttributes::Initialize` 來建立屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="adbf5-166">You must call `CBaseAttributes::Initialize` to create the attribute store.</span></span> <span data-ttu-id="adbf5-167">在上述範例中，這是在靜態建立函式中完成的。</span><span class="sxs-lookup"><span data-stu-id="adbf5-167">In the previous example, that is done inside a static creation function.</span></span>

<span data-ttu-id="adbf5-168">範本引數是介面類別型，預設為 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)。</span><span class="sxs-lookup"><span data-stu-id="adbf5-168">The template argument is an interface type, which defaults to [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="adbf5-169">如果您的物件會執行繼承 **IMFAttributes** 的介面（例如 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)），請將範本引數設定為等於衍生介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="adbf5-169">If your object implements an interface that inherits **IMFAttributes**, such as [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate), set the template argument equal to name of the derived interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="adbf5-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="adbf5-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adbf5-171">媒體基礎基本</span><span class="sxs-lookup"><span data-stu-id="adbf5-171">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



