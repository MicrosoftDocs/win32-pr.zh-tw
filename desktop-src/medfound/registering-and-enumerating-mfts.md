---
description: 本節說明如何列舉媒體基礎轉換，以及如何註冊自訂的 MFT，讓應用程式可以探索它。
ms.assetid: 76d2a703-4162-428e-a4ff-643e346eacfb
title: 註冊和列舉 MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771a22b469d472dbc59d07c2754405276883bef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943725"
---
# <a name="registering-and-enumerating-mfts"></a><span data-ttu-id="04863-103">註冊和列舉 MFTs</span><span class="sxs-lookup"><span data-stu-id="04863-103">Registering and Enumerating MFTs</span></span>

<span data-ttu-id="04863-104">本節說明如何列舉媒體基礎轉換，以及如何註冊自訂的 MFT，讓應用程式可以探索它。</span><span class="sxs-lookup"><span data-stu-id="04863-104">This section describes how to enumerate Media Foundation transforms, and how to register a custom MFT so that applications can discover it.</span></span>

-   [<span data-ttu-id="04863-105">列舉 MFTs</span><span class="sxs-lookup"><span data-stu-id="04863-105">Enumerating MFTs</span></span>](#registering-and-enumerating-mfts)
-   [<span data-ttu-id="04863-106">註冊 MFTs</span><span class="sxs-lookup"><span data-stu-id="04863-106">Registering MFTs</span></span>](#registering-mfts)
-   [<span data-ttu-id="04863-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="04863-107">Related topics</span></span>](#related-topics)

## <a name="enumerating-mfts"></a><span data-ttu-id="04863-108">列舉 MFTs</span><span class="sxs-lookup"><span data-stu-id="04863-108">Enumerating MFTs</span></span>

<span data-ttu-id="04863-109">若要探索在系統上註冊的 MFTs，應用程式可以呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數。</span><span class="sxs-lookup"><span data-stu-id="04863-109">To discover MFTs that are registered on the system, an application can call the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

> [!Note]  
> <span data-ttu-id="04863-110">此函數需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="04863-110">This function requires to Windows 7.</span></span> <span data-ttu-id="04863-111">在 Windows 7 之前，應用程式應該改用 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 函數。</span><span class="sxs-lookup"><span data-stu-id="04863-111">Prior to Windows 7, applications should use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function instead.</span></span>

 

<span data-ttu-id="04863-112">此函式會採用下列資訊作為輸入：</span><span class="sxs-lookup"><span data-stu-id="04863-112">This function takes the following information as input:</span></span>

-   <span data-ttu-id="04863-113">要列舉的 MFT 類別，例如影片解碼或音訊解碼器。</span><span class="sxs-lookup"><span data-stu-id="04863-113">The category of MFT to enumerate, such as video decoder or audio decoder.</span></span>
-   <span data-ttu-id="04863-114">要比對的輸入或輸出格式。</span><span class="sxs-lookup"><span data-stu-id="04863-114">An input or output format to match.</span></span>
-   <span data-ttu-id="04863-115">指定其他搜尋條件的旗標。</span><span class="sxs-lookup"><span data-stu-id="04863-115">Flags that specify additional search conditions.</span></span>

<span data-ttu-id="04863-116">此函式會傳回 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標的陣列，每個指標都代表符合列舉準則的一個 MFT。</span><span class="sxs-lookup"><span data-stu-id="04863-116">The function returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, each of which represents an MFT that matches the enumeration criteria.</span></span>

<span data-ttu-id="04863-117">例如，下列程式碼會列舉 Windows Media 視訊的解碼器：</span><span class="sxs-lookup"><span data-stu-id="04863-117">For example, the following code enumerates Windows Media Video decoders:</span></span>


```C++
HRESULT hr = S_OK;
UINT32 count = 0;

IMFActivate **ppActivate = NULL;    // Array of activation objects.
IMFTransform *pDecoder = NULL;      // Pointer to the decoder.

// Match WMV3 video.
MFT_REGISTER_TYPE_INFO info = { MFMediaType_Video, MFVideoFormat_WMV3 };

UINT32 unFlags = MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;

hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );


if (SUCCEEDED(hr) && count == 0)
{
    hr = MF_E_TOPO_CODEC_NOT_FOUND;
}

// Create the first decoder in the list.

if (SUCCEEDED(hr))
{
    hr = ppActivate[0]->ActivateObject(IID_PPV_ARGS(&pDecoder));
}

for (UINT32 i = 0; i < count; i++)
{
    ppActivate[i]->Release();
}
CoTaskMemFree(ppActivate);
```



<span data-ttu-id="04863-118">根據預設，某些類型的 MFT 會從列舉中排除，包括非同步 MFTs、硬體 MFTs，以及使用「使用中」 restructions 的 MFTs。</span><span class="sxs-lookup"><span data-stu-id="04863-118">By default, some types of MFT are excluded from the enumeration, including asynchronous MFTs, hardware MFTs, and MFTs with field-of-use restructions.</span></span> <span data-ttu-id="04863-119">這些會被排除，因為它們都需要某種類型的特殊處理。</span><span class="sxs-lookup"><span data-stu-id="04863-119">These are excluded because they all require special handling of some kind.</span></span> <span data-ttu-id="04863-120">使用 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)的 *Flags* 參數變更預設值。</span><span class="sxs-lookup"><span data-stu-id="04863-120">Use the *Flags* parameter of [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) to change the default.</span></span> <span data-ttu-id="04863-121">例如，若要在列舉結果中包含硬體 MFTs，請設定 **MFT \_ 列舉 \_ 旗標 \_ 硬體** 旗標：</span><span class="sxs-lookup"><span data-stu-id="04863-121">For example, to include hardware MFTs in the enumeration results, set the **MFT\_ENUM\_FLAG\_HARDWARE** flag:</span></span>


```C++
UINT32 unFlags = MFT_ENUM_FLAG_HARDWARE |
                 MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;
hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );
```



## <a name="registering-mfts"></a><span data-ttu-id="04863-122">註冊 MFTs</span><span class="sxs-lookup"><span data-stu-id="04863-122">Registering MFTs</span></span>

<span data-ttu-id="04863-123">當您註冊媒體基礎轉換 (MFT) 時，會將兩種類型的資訊寫入登錄：</span><span class="sxs-lookup"><span data-stu-id="04863-123">When you register a Media Foundation transform (MFT), two types of information are written to the registry:</span></span>

-   <span data-ttu-id="04863-124">MFT 的 CLSID，讓用戶端可以呼叫 **CoCreateInstance** 或 **CoGetClassObject** 來建立該 mft 的實例。</span><span class="sxs-lookup"><span data-stu-id="04863-124">The CLSID of the MFT, so that clients can call **CoCreateInstance** or **CoGetClassObject** to create an instance of the MFT.</span></span> <span data-ttu-id="04863-125">此登錄專案會遵循 COM class factory 的標準格式。</span><span class="sxs-lookup"><span data-stu-id="04863-125">This registry entry follows the standard format for COM class factories.</span></span> <span data-ttu-id="04863-126">如需詳細資訊，請參閱 (COM) 的元件物件模型 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="04863-126">For more information, see the Windows SDK documentation for the Component Object Model (COM).</span></span>
-   <span data-ttu-id="04863-127">可讓應用程式依功能類別列舉 MFTs 的資訊。</span><span class="sxs-lookup"><span data-stu-id="04863-127">Information that enables an application to enumerate MFTs by functional category.</span></span>

<span data-ttu-id="04863-128">若要在登錄中建立 MFT 列舉專案，請呼叫 [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) 函數。</span><span class="sxs-lookup"><span data-stu-id="04863-128">To create the MFT enumeration entries in the registry, call the [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) function.</span></span> <span data-ttu-id="04863-129">您可以包含下列有關 MFT 的資訊：</span><span class="sxs-lookup"><span data-stu-id="04863-129">You can include the following information about the MFT:</span></span>

-   <span data-ttu-id="04863-130">MFT 的類別，例如影片編碼器或影片編碼器。</span><span class="sxs-lookup"><span data-stu-id="04863-130">The category of the MFT, such as video decoder or video encoder.</span></span> <span data-ttu-id="04863-131">如需分類清單，請參閱 [**MFT \_ 類別目錄**](mft-category.md)。</span><span class="sxs-lookup"><span data-stu-id="04863-131">For a list of categories, see [**MFT\_CATEGORY**](mft-category.md).</span></span>
-   <span data-ttu-id="04863-132">MFT 支援的輸入和輸出格式清單。</span><span class="sxs-lookup"><span data-stu-id="04863-132">A list of input and output formats that the MFT supports.</span></span> <span data-ttu-id="04863-133">每種格式都是由主要類型和子類型所定義。</span><span class="sxs-lookup"><span data-stu-id="04863-133">Each format is defined by a major type and a subtype.</span></span> <span data-ttu-id="04863-134"> (若要取得更詳細的格式資訊，用戶端必須建立 MFT 並呼叫 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 方法。 ) 拓撲載入器會在解析部分拓撲時使用此資訊。</span><span class="sxs-lookup"><span data-stu-id="04863-134">(To get more detailed format information, the client must create the MFT and call [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods.) The topology loader uses this information when it resolves a partial topology.</span></span>

<span data-ttu-id="04863-135">若要從登錄中移除專案，請呼叫 [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister)。</span><span class="sxs-lookup"><span data-stu-id="04863-135">To remove the entries from the registry, call [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).</span></span>

<span data-ttu-id="04863-136">下列程式碼說明如何註冊 MFT。</span><span class="sxs-lookup"><span data-stu-id="04863-136">The following code shows how to register an MFT.</span></span> <span data-ttu-id="04863-137">此範例假設 MFT 是支援輸入和輸出相同格式的影片效果。</span><span class="sxs-lookup"><span data-stu-id="04863-137">This example assumes that the MFT is a video effect that supports the same formats for both input and output.</span></span>


```C++
// CLSID of the MFT.
extern const GUID CLSID_MyVideoEffectMFT;

// DllRegisterServer: Creates the registry entries.
STDAPI DllRegisterServer()
{
    HRESULT hr = S_OK;

    // Array of media types.
    MFT_REGISTER_TYPE_INFO aMediaTypes[] =
    {
        {   MFMediaType_Video, MFVideoFormat_NV12 },
        {   MFMediaType_Video, MFVideoFormat_YUY2 },
        {   MFMediaType_Video, MFVideoFormat_UYVY },
    };

    // Size of the array.
    const DWORD cNumMediaTypes = ARRAY_SIZE(aMediaTypes);

    hr = MFTRegister(
        CLSID_MyVideoEffectMFT,     // CLSID.
        MFT_CATEGORY_VIDEO_EFFECT,  // Category.
        L"My Video Effect",         // Friendly name.
        0,                          // Reserved, must be zero.
        cNumMediaTypes,             // Number of input types.
        aMediaTypes,                // Input types.
        cNumMediaTypes,             // Number of output types.
        aMediaTypes,                // Output types.
        NULL                        // Attributes (optional).
        );

    if (SUCCEEDED(hr))
    {
        // Register the CLSID for CoCreateInstance (not shown).
    }
    return hr;
}

// DllUnregisterServer: Removes the registry entries.
STDAPI DllUnregisterServer()
{
    HRESULT hr = MFTUnregister(CLSID_MyVideoEffectMFT);

    // Unregister the CLSID for CoCreateInstance (not shown).

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="04863-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="04863-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04863-139">使用限制領域</span><span class="sxs-lookup"><span data-stu-id="04863-139">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)
</dt> <dt>

[<span data-ttu-id="04863-140">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="04863-140">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 



