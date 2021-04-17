---
description: 重新連接您的輸入，以確保特定的輸出類型
ms.assetid: c83d002e-59bf-4d03-9917-e39ceab9a4ce
title: 重新連接您的輸入，以確保特定的輸出類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d74d6914989231542ddfea9f97e93ce860d34eb4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385653"
---
# <a name="reconnecting-your-input-to-ensure-specific-output-types"></a><span data-ttu-id="e8920-103">重新連接您的輸入，以確保特定的輸出類型</span><span class="sxs-lookup"><span data-stu-id="e8920-103">Reconnecting Your Input to Ensure Specific Output Types</span></span>

<span data-ttu-id="e8920-104">篩選準則會先執行 [**IAMStreamConfig：： SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) 方法，以在連接篩選器的釘選之前設定音訊或影片格式。</span><span class="sxs-lookup"><span data-stu-id="e8920-104">Filters implement the [**IAMStreamConfig::SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method to set the audio or video format before the filter's pins are connected.</span></span> <span data-ttu-id="e8920-105">如果您的輸出 pin 已連線，且您可以提供新的類型，請重新連接您的 pin，但只有在其他篩選器可以接受新的類型時才能重新連接。</span><span class="sxs-lookup"><span data-stu-id="e8920-105">If your output pin is already connected and you can provide a new type, then reconnect your pin, but only if the other filter can accept the new type.</span></span> <span data-ttu-id="e8920-106">如果另一個篩選準則無法接受媒體類型，請將 **SetFormat** 的呼叫失敗，並單獨離開您的連接。</span><span class="sxs-lookup"><span data-stu-id="e8920-106">If the other filter cannot accept the media type, fail the call to **SetFormat** and leave your connection alone.</span></span>

<span data-ttu-id="e8920-107">轉換篩選可能沒有任何慣用的輸出類型，除非它們的輸入 pin 已連接。</span><span class="sxs-lookup"><span data-stu-id="e8920-107">A transform filter may not have any preferred output types unless their input pin is connected.</span></span> <span data-ttu-id="e8920-108">在這種情況下， **SetFormat** 和 [**IAMStreamConfig：： GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) 方法應該會傳回 VFW \_ E \_ 未連線， \_ 直到輸入 pin 連線為止。</span><span class="sxs-lookup"><span data-stu-id="e8920-108">In that case, the **SetFormat** and [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) methods should return VFW\_E\_NOT\_CONNECTED until the input pin is connected.</span></span> <span data-ttu-id="e8920-109">否則，這些方法可以正常運作。</span><span class="sxs-lookup"><span data-stu-id="e8920-109">Otherwise, these methods can function as usual.</span></span>

<span data-ttu-id="e8920-110">在某些情況下，當您在已建立的連線上提供格式時，將 pin 重新連接會很有用。</span><span class="sxs-lookup"><span data-stu-id="e8920-110">In certain cases it is useful to reconnect pins when you are offering a format on an established connection.</span></span> <span data-ttu-id="e8920-111">例如，假設篩選器可以將24位 RGB 影片壓縮為 X 格式，而且它可以將8位 RGB 影片壓縮成格式 Y。輸出 pin 可以執行下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="e8920-111">For example, suppose that a filter can compress 24-bit RGB video into format X, and that it can compress 8-bit RGB video into format Y. The output pin can do either of the following:</span></span>

-   <span data-ttu-id="e8920-112">一律在 **GetStreamCaps** 中提供 x 和 y，且一律接受 **SetFormat** 中的 x 和 y。</span><span class="sxs-lookup"><span data-stu-id="e8920-112">Always offer both X and Y in **GetStreamCaps**, and always accept both X and Y in **SetFormat**.</span></span>
-   <span data-ttu-id="e8920-113">如果輸入類型是24位 RGB，則 [提供] 和 [僅接受格式] 為 X。</span><span class="sxs-lookup"><span data-stu-id="e8920-113">Offer and accept just format X if the input type is 24-bit RGB.</span></span> <span data-ttu-id="e8920-114">如果輸入類型是8位 RGB，則提供並接受格式 Y。</span><span class="sxs-lookup"><span data-stu-id="e8920-114">Offer and accept just format Y if the input type 8-bit RGB.</span></span> <span data-ttu-id="e8920-115">如果輸入 pin 未連線，這兩種方法都會失敗。</span><span class="sxs-lookup"><span data-stu-id="e8920-115">Fail both methods if the input pin is not connected.</span></span>

<span data-ttu-id="e8920-116">無論是哪一種情況，您都需要一些重新連接的程式碼，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e8920-116">In either case, you will need some reconnecting code that looks like this:</span></span>


```C++
HRESULT MyOutputPin::CheckMediaType(const CMediaType *pmtOut)
{
    // Fail if the input pin is not connected.
    if (!m_pFilter->m_pInput->IsConnected()) {
        return VFW_E_NOT_CONNECTED;
    }

    // (Not shown: Reject any media types that you know in advance your 
    // filter cannot use. Check the major type and subtype GUIDs.)

    // (Not shown: If SetFormat was previously called, check whether
    // pmtOut exactly matches the format that was specified in SetFormat.
    // Return S_OK if they match, or VFW_E_INVALIDMEDIATYPE otherwise.)
   
    // Now do the normal check for this media type.
    HRESULT hr;
    hr = m_pFilter->CheckTransform(
        &m_pFilter->m_pInput->CurrentMediaType(),  // The input type.
        pmtOut  // The proposed output type.
    );
    if (hr == S_OK)
    {
        // This format is compatible with the current input type.
        return S_OK;
    }
 
    // This format is not compatible with the current input type. 
    // Maybe we can reconnect the input pin with a new input type.
    
    // Enumerate the upstream filter's preferred output types, and 
    // see if one of them will work.
    CMediaType *pmtEnum;
    BOOL fFound = FALSE;
    IEnumMediaTypes *pEnum;
    hr = m_pFilter->m_pInput->GetConnected()->EnumMediaTypes(&pEnum);
    if (hr != S_OK)
    {
        return E_FAIL;
    }
    while (hr = pEnum->Next(1, (AM_MEDIA_TYPE **)&pmtEnum, NULL), hr == S_OK)
    {
        // Check this input type against the proposed output type.
        hr = m_pFilter->CheckTransform(pmtEnum, pmtOut);
        if (hr != S_OK) 
        {
            DeleteMediaType(pmtEnum);
            continue; // Try the next one.
        }

        // This input type is a possible candidate. But, we have to make
        // sure that the upstream filter can switch to this type. 
        hr = m_pFilter->m_pInput->GetConnected()->QueryAccept(pmtEnum);
        if (hr != S_OK) 
        {
            // The upstream filter will not switch to this type.
            DeleteMediaType(pmtEnum);
            continue; // Try the next one.
        }
        fFound = TRUE;
        DeleteMediaType(pmtEnum);
        break;
    }
    pEnum->Release();

    if (fFound)
    {
        // This output type is OK, but if we are asked to use it, we will
        // need to reconnect our input pin. (See SetFormat, below.)
        return S_OK;
    }
    else
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
}

HRESULT MyOutputPin::SetFormat(AM_MEDIA_TYPE *pmt)
{
    CheckPointer(pmt, E_POINTER);
    HRESULT hr;

    // Hold the filter state lock, to make sure that streaming isn't 
    // in the middle of starting or stopping:
    CAutoLock cObjectLock(&m_pFilter->m_csFilter);

    // Cannot set the format unless the filter is stopped.
    if (m_pFilter->m_State != State_Stopped)
    {
        return VFW_E_NOT_STOPPED;
    }

    // The set of possible output formats depends on the input format,
    // so if the input pin is not connected, return a failure code.
    if (!m_pFilter->m_pInput->IsConnected())
    {
        return VFW_E_NOT_CONNECTED;
    }

    // If the pin is already using this format, there's nothing to do.
    if (IsConnected() && CurrentMediaType() == *pmt)
    {
        return S_OK;
    }

    // See if this media type is acceptable.
    if ((hr = CheckMediaType((CMediaType *)pmt)) != S_OK) 
    {
        return hr;
    }

    // If we're connected to a downstream filter, we have to make
    // sure that the downstream filter accepts this media type.
    if (IsConnected()) 
    {
        hr = GetConnected()->QueryAccept(pmt);
        if (hr != S_OK)
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
    }

    // Now make a note that from now on, this is the only format allowed,
    // and refuse anything but this in the CheckMediaType code above.

    // Changing the format means reconnecting if necessary.
    if (IsConnected())
    {
        m_pFilter->m_pGraph->Reconnect(this);
    }

    return NOERROR;
}


// Override CTransformFilter::SetMediaType to reconnect the input pin. 
// This method is called immediately after the media type is set on a pin.
HRESULT MyFilter::SetMediaType(
    PIN_DIRECTION direction, 
    const CMediaType *pmt
)
{
    HRESULT hr;
    if (direction == PINDIR_OUTPUT) 
    {
        // Before we set the output type, we might need to reconnect 
        // the input pin with a new type.
        if (m_pInput && m_pInput->IsConnected()) 
        {
            // Check if the current input type is compatible.
            hr = CheckTransform(
                    &m_pInput->CurrentMediaType(),
                    &m_pOutput->CurrentMediaType());
            if (SUCCEEDED(hr))
            {
                return S_OK;
            }
            // Otherwise, we need to reconnect the input pin.
            // Note: The CheckMediaType method has already called 
            // QueryAccept on the upstream filter. 
            hr = m_pGraph->Reconnect(m_pInput);
            return hr;
        }
    }
    return S_OK;
}
```



 

 



