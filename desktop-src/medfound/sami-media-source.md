---
description: 已同步處理的可存取媒體交換 (薩米) 是一種將標題新增至數位媒體的格式。
ms.assetid: 007c8181-089e-4e56-a31d-9d1942f90b07
title: 薩米媒體來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340b51815b130cb41061478358b2ab9dcf68f60
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104027666"
---
# <a name="sami-media-source"></a><span data-ttu-id="1d5f7-103">薩米媒體來源</span><span class="sxs-lookup"><span data-stu-id="1d5f7-103">SAMI Media Source</span></span>

<span data-ttu-id="1d5f7-104">已同步處理的可存取媒體交換 (薩米) 是一種將標題新增至數位媒體的格式。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-104">Synchronized Accessible Media Interchange (SAMI) is a format for adding captions to digital media.</span></span> <span data-ttu-id="1d5f7-105">這些標題會儲存在副檔名為 smi-s 或薩米文的個別文字檔中。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-105">The captions are stored in a separate text file with the file name extension .smi or .sami.</span></span>

<span data-ttu-id="1d5f7-106">在媒體基礎中，會透過薩米文的媒體來源支援薩米字幕檔案。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-106">In Media Foundation, SAMI caption files are supported through the SAMI media source.</span></span> <span data-ttu-id="1d5f7-107">使用 [來源解析程式](source-resolver.md) ，從 URL 或位元組資料流程建立薩米文媒體來源的實例。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-107">Use the [Source Resolver](source-resolver.md) to create an instance of the SAMI media source from a URL or byte stream.</span></span> <span data-ttu-id="1d5f7-108">媒體基礎不會提供顯示薩米文的元件。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-108">Media Foundation does not provide a component that displays SAMI captions.</span></span> <span data-ttu-id="1d5f7-109">應用程式必須解讀從薩米文媒體來源接收的標題資料。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-109">The application must interpret the caption data that it receives from the SAMI media source.</span></span>

<span data-ttu-id="1d5f7-110">以下顯示範例薩米文的檔案。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-110">The following shows an example SAMI file.</span></span>

``` syntax
<SAMI>
<HEAD>
    <STYLE TYPE="text/css">
    <!--
    P {
        font-family: Arial;
        background: #000000;
        text-align: center;
        }

#standard {Name: Standard; color: #FFFFFF; font-size: 14pt; } 
#hilite {Name: Youth; color: greenyellow; font-size: 18pt;}

    .ENUSCC { Name: English; lang: EN-US-CC; }
    .FRFRCC { Name: French; lang: fr-FR; } 

    -->
    </STYLE>
</HEAD>
<BODY>
    <SYNC Start="0">
        <P Class="ENUSCC">The <I>first</I> caption.</P>
        <P Class="FRFRCC">Un</P>
    </SYNC>
    <SYNC Start="3000">
        <P Class="ENUSCC">The <I>second</I> caption.</P>
        <P Class="FRFRCC">Deux</P>
    </SYNC>
    <SYNC Start="5000">
        <P Class="ENUSCC">The <I>third</I> caption.</P>
        <P Class="FRFRCC">Trois</P>
    </SYNC>
</BODY>
</SAMI>
```

<span data-ttu-id="1d5f7-111">`<STYLE>`元素包含樣式資訊。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-111">The `<STYLE>` element contains style information.</span></span> <span data-ttu-id="1d5f7-112">此範例包含元素的基底樣式 `<P>` ，以及兩個命名樣式 "standard" 和 "hilite"。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-112">This example contains a base style for `<P>` elements, along with two named styles, "standard" and "hilite".</span></span> <span data-ttu-id="1d5f7-113">使用命名樣式來修改基底樣式。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-113">The named styles are used to modify the base style.</span></span> <span data-ttu-id="1d5f7-114">標題位於元素內 `<SYNC>` 。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-114">Captions are placed within `<SYNC>` elements.</span></span> <span data-ttu-id="1d5f7-115">Start 屬性提供該標題的呈現時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-115">The start attribute gives the presentation time in milliseconds for that caption.</span></span> <span data-ttu-id="1d5f7-116">此範例中的標題提供兩種語言，由其 RFC-1766 語言標記（"en-us" 和 "fr-fr"）指定。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-116">The captions in this example are given in two languages, specified by their RFC-1766 language tags, "en-US" and "fr -FR".</span></span> <span data-ttu-id="1d5f7-117">在標題中，語言是以其類別名稱來識別;在此案例中為 "ENUSCC" 和 "FRFRCC"。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-117">Within the captions, languages are identified by their class names; in this case, "ENUSCC" and "FRFRCC".</span></span>

<span data-ttu-id="1d5f7-118">薩米媒體來源會為每個語言建立一個媒體串流。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-118">The SAMI media source creates one media stream for each language.</span></span> <span data-ttu-id="1d5f7-119">預設會選取第一個資料流程，並取消選取其餘的資料流程。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-119">By default, the first stream is selected and the remaining streams are deselected.</span></span> <span data-ttu-id="1d5f7-120">應用程式可以藉由呼叫 [**IMFPresentationDescriptor：： SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) 和 [**IMFPresentationDescriptor：:D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream)來變更資料流程選取專案。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-120">The application can change the stream selection by calling [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) and [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span></span> <span data-ttu-id="1d5f7-121">每個資料流程描述項都包含下列屬性。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-121">Each stream descriptor contains the following attributes.</span></span>



| <span data-ttu-id="1d5f7-122">屬性</span><span class="sxs-lookup"><span data-stu-id="1d5f7-122">Attribute</span></span>                                                       | <span data-ttu-id="1d5f7-123">描述</span><span class="sxs-lookup"><span data-stu-id="1d5f7-123">Description</span></span>                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="1d5f7-124">**MF \_ SD \_ 語言**</span><span class="sxs-lookup"><span data-stu-id="1d5f7-124">**MF\_SD\_LANGUAGE**</span></span>](mf-sd-language-attribute.md)            | <span data-ttu-id="1d5f7-125">Language 標記，如屬性所提供 `lang` 。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-125">Language tag, as given by the `lang` attribute.</span></span>  |
| [<span data-ttu-id="1d5f7-126">**MF \_ SD \_ 薩米文 \_ 語言**</span><span class="sxs-lookup"><span data-stu-id="1d5f7-126">**MF\_SD\_SAMI\_LANGUAGE**</span></span>](mf-sd-sami-language-attribute.md) | <span data-ttu-id="1d5f7-127">語言名稱，如屬性所提供 `Name` 。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-127">Language name, as given by the `Name` attribute.</span></span> |



 

<span data-ttu-id="1d5f7-128">每個串流都有下列媒體類型：</span><span class="sxs-lookup"><span data-stu-id="1d5f7-128">Each stream has the following media type:</span></span>



| <span data-ttu-id="1d5f7-129">屬性</span><span class="sxs-lookup"><span data-stu-id="1d5f7-129">Attribute</span></span>                                                                            | <span data-ttu-id="1d5f7-130">值</span><span class="sxs-lookup"><span data-stu-id="1d5f7-130">Value</span></span>                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [<span data-ttu-id="1d5f7-131">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="1d5f7-131">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                            | <span data-ttu-id="1d5f7-132">**MFMediaType \_ 薩米文**</span><span class="sxs-lookup"><span data-stu-id="1d5f7-132">**MFMediaType\_SAMI**</span></span> |
| [<span data-ttu-id="1d5f7-133">**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**</span><span class="sxs-lookup"><span data-stu-id="1d5f7-133">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) | <span data-ttu-id="1d5f7-134">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="1d5f7-134">**TRUE**</span></span>              |



 

<span data-ttu-id="1d5f7-135">薩米文來源會在個別的媒體範例中提供每個標題。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-135">The SAMI source delivers each caption in a separate media sample.</span></span> <span data-ttu-id="1d5f7-136">範例時間戳記和持續時間是衍生自 `<SYNC>` 元素。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-136">The sample time stamp and duration are derived from the `<SYNC>` element.</span></span> <span data-ttu-id="1d5f7-137">範例中包含的媒體緩衝區將標題保存為 ASCII 文字。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-137">The media buffer contained in the sample holds the caption as ASCII text.</span></span> <span data-ttu-id="1d5f7-138">標題樣式以內嵌屬性的形式內嵌在標題中 `STYLE` 。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-138">The caption style is embedded in the caption as an inline `STYLE` attribute.</span></span> <span data-ttu-id="1d5f7-139">例如，假設有上一個薩米文的檔案，並使用包含預設樣式的英文語言資料流程，則第一個媒體緩衝區會包含下列資料。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-139">For example, given the previous SAMI file, and using the English-language stream with the default styles, the first media buffer would contain the following data.</span></span> <span data-ttu-id="1d5f7-140"> (分行符號可能與此處顯示的不同。 ) </span><span class="sxs-lookup"><span data-stu-id="1d5f7-140">(The line breaks might differ from what is shown here.)</span></span>

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a><span data-ttu-id="1d5f7-141">薩米文樣式</span><span class="sxs-lookup"><span data-stu-id="1d5f7-141">SAMI Styles</span></span>

<span data-ttu-id="1d5f7-142">若要變更目前的樣式，請使用 [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) 介面。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-142">To change the current style, use the [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) interface.</span></span> <span data-ttu-id="1d5f7-143">在薩米媒體來源上呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ，即可取得這個介面。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-143">This interface is obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the SAMI media source.</span></span> <span data-ttu-id="1d5f7-144"> (如果您要使用具有媒體會話的薩米媒體來源，請在媒體會話上呼叫 **GetService** 。 ) 服務識別碼為 **MF \_ 薩米文 \_ 服務**。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-144">(If you are using the SAMI media source with the Media Session, call **GetService** on the Media Session.) The service identifier is **MF\_SAMI\_SERVICE**.</span></span>

<span data-ttu-id="1d5f7-145">下列範例會設定依索引所指定的目前薩米型樣式。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-145">The following example sets the current SAMI style, specified by index.</span></span>


```C++
HRESULT SetSAMIStyleByIndex(IMFMediaSource *pSource, DWORD index)
{
    IMFSAMIStyle *pSami = NULL;

    DWORD cStyles;
    PROPVARIANT varStyles;

    HRESULT hr = MFGetService(pSource, MF_SAMI_SERVICE, IID_PPV_ARGS(&pSami));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->GetStyleCount(&cStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    if (index >= cStyles)
    {
        hr = E_INVALIDARG;
        goto done;
    }

    hr = pSami->GetStyles(&varStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->SetSelectedStyle(varStyles.calpwstr.pElems[index]);

done:
    PropVariantClear(&varStyles);
    SafeRelease(&pSami);
    return hr;
}
```



<span data-ttu-id="1d5f7-146">此範例會在薩米媒體來源上呼叫下列方法：</span><span class="sxs-lookup"><span data-stu-id="1d5f7-146">This example calls the following methods on the SAMI media source:</span></span>

-   <span data-ttu-id="1d5f7-147">[**IMFSAMIStyle：： GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) 會取得樣式的數目。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-147">[**IMFSAMIStyle::GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) gets the number of styles.</span></span>
-   <span data-ttu-id="1d5f7-148">[**IMFSAMIStyle：： GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) 會取得儲存在 **PROPVARIANT** 中的樣式名稱清單。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-148">[**IMFSAMIStyle::GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) gets a list of the style names, stored in a **PROPVARIANT**.</span></span>
-   <span data-ttu-id="1d5f7-149">[**IMFSAMIStyle：： SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) 會依名稱設定樣式。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-149">[**IMFSAMIStyle::SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) sets a style by name.</span></span>

<span data-ttu-id="1d5f7-150">樣式名稱清單也會儲存在展示描述項的 [ [**MF \_ PD \_ 薩米 \_**](mf-pd-sami-stylelist-attribute.md) 文] STYLELIST 屬性中。</span><span class="sxs-lookup"><span data-stu-id="1d5f7-150">The list of style names is also stored on the presentation descriptor, in the [**MF\_PD\_SAMI\_STYLELIST**](mf-pd-sami-stylelist-attribute.md) attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d5f7-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d5f7-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d5f7-152">媒體來源和接收</span><span class="sxs-lookup"><span data-stu-id="1d5f7-152">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="1d5f7-153">媒體基礎中支援的媒體格式</span><span class="sxs-lookup"><span data-stu-id="1d5f7-153">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



