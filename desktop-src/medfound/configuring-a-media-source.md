---
description: 設定媒體來源
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: 設定媒體來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e6737d643db2ee473214586cd7ded4f9596133dac5f4fb177df4d7b6b19757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880589"
---
# <a name="configuring-a-media-source"></a>設定媒體來源

當您使用 [來源解析程式](source-resolver.md) 來建立媒體來源時，您可以指定包含設定屬性的屬性存放區。 這些屬性將用來初始化媒體來源。 一組支援的屬性取決於媒體來源的執行。 並非每個媒體來源都定義了設定屬性。

下表列出媒體基礎中提供之媒體來源的設定屬性。 協力廠商媒體來源可以定義自己的自訂屬性。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>媒體來源</th>
<th>屬性</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>網路來源</td>
<td>請參閱 <a href="network-source-features.md">網路來源功能</a>。</td>
</tr>
<tr class="even">
<td>ASF 媒體來源</td>
<td><ul>
<li><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></li>
<li><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></li>
<li><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></li>
<li><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></li>
</ul></td>
</tr>
</tbody>
</table>



 

若要設定來源，請執行下列步驟。

1.  呼叫 **PSCreateMemoryPropertyStore** 來建立新的屬性存放區。 此函數會傳回 **IPropertyStore** 指標。
2.  呼叫 **IPropertyStore：： SetValue** 可設定一或多個設定屬性。
3.  呼叫其中一個來源解析程式的建立函數，例如 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)，然後在 *pProps* 參數中傳遞 **IPropertyStore** 指標。


```C++
// Creates a media source from a URL.

HRESULT CreateMediaSource(
    PCWSTR pszURL, 
    IPropertyStore *pConfig,    // Optional, can be NULL
    IMFMediaSource **ppSource
    )
{
    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        DbgLog(L"CreateObjectFromURL");

        hr = pSourceResolver->CreateObjectFromURL(
            pszURL,                     
            MF_RESOLUTION_MEDIASOURCE,  // Create a media source.
            pConfig,                    // Configuration properties.
            &ObjectType,                // Receives the object type. 
            &pSource            
            );

        DbgLog(L"CreateObjectFromURL - FINISHED");

    }

    if (SUCCEEDED(hr))
    {
        hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));
    }

    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



來源解析程式會將 **IPropertyStore** 指標直接傳遞至配置處理常式或建立來源的位元組資料流程處理常式。 來源解析程式不會嘗試驗證屬性。

一般而言，這些屬性會用於 advanced 設定。 如果您未提供內容存放區，媒體來源仍應正常運作，並使用預設設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[來源解析程式](source-resolver.md)
</dt> </dl>

 

 



