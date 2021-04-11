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
# <a name="sami-media-source"></a>薩米媒體來源

已同步處理的可存取媒體交換 (薩米) 是一種將標題新增至數位媒體的格式。 這些標題會儲存在副檔名為 smi-s 或薩米文的個別文字檔中。

在媒體基礎中，會透過薩米文的媒體來源支援薩米字幕檔案。 使用 [來源解析程式](source-resolver.md) ，從 URL 或位元組資料流程建立薩米文媒體來源的實例。 媒體基礎不會提供顯示薩米文的元件。 應用程式必須解讀從薩米文媒體來源接收的標題資料。

以下顯示範例薩米文的檔案。

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

`<STYLE>`元素包含樣式資訊。 此範例包含元素的基底樣式 `<P>` ，以及兩個命名樣式 "standard" 和 "hilite"。 使用命名樣式來修改基底樣式。 標題位於元素內 `<SYNC>` 。 Start 屬性提供該標題的呈現時間（以毫秒為單位）。 此範例中的標題提供兩種語言，由其 RFC-1766 語言標記（"en-us" 和 "fr-fr"）指定。 在標題中，語言是以其類別名稱來識別;在此案例中為 "ENUSCC" 和 "FRFRCC"。

薩米媒體來源會為每個語言建立一個媒體串流。 預設會選取第一個資料流程，並取消選取其餘的資料流程。 應用程式可以藉由呼叫 [**IMFPresentationDescriptor：： SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) 和 [**IMFPresentationDescriptor：:D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream)來變更資料流程選取專案。 每個資料流程描述項都包含下列屬性。



| 屬性                                                       | 描述                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [**MF \_ SD \_ 語言**](mf-sd-language-attribute.md)            | Language 標記，如屬性所提供 `lang` 。  |
| [**MF \_ SD \_ 薩米文 \_ 語言**](mf-sd-sami-language-attribute.md) | 語言名稱，如屬性所提供 `Name` 。 |



 

每個串流都有下列媒體類型：



| 屬性                                                                            | 值                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md)                            | **MFMediaType \_ 薩米文** |
| [**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**](mf-mt-all-samples-independent-attribute.md) | **TRUE**              |



 

薩米文來源會在個別的媒體範例中提供每個標題。 範例時間戳記和持續時間是衍生自 `<SYNC>` 元素。 範例中包含的媒體緩衝區將標題保存為 ASCII 文字。 標題樣式以內嵌屬性的形式內嵌在標題中 `STYLE` 。 例如，假設有上一個薩米文的檔案，並使用包含預設樣式的英文語言資料流程，則第一個媒體緩衝區會包含下列資料。  (分行符號可能與此處顯示的不同。 ) 

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a>薩米文樣式

若要變更目前的樣式，請使用 [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) 介面。 在薩米媒體來源上呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ，即可取得這個介面。  (如果您要使用具有媒體會話的薩米媒體來源，請在媒體會話上呼叫 **GetService** 。 ) 服務識別碼為 **MF \_ 薩米文 \_ 服務**。

下列範例會設定依索引所指定的目前薩米型樣式。


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



此範例會在薩米媒體來源上呼叫下列方法：

-   [**IMFSAMIStyle：： GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) 會取得樣式的數目。
-   [**IMFSAMIStyle：： GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) 會取得儲存在 **PROPVARIANT** 中的樣式名稱清單。
-   [**IMFSAMIStyle：： SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) 會依名稱設定樣式。

樣式名稱清單也會儲存在展示描述項的 [ [**MF \_ PD \_ 薩米 \_**](mf-pd-sami-stylelist-attribute.md) 文] STYLELIST 屬性中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體來源和接收](media-sources-and-sinks.md)
</dt> <dt>

[媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



