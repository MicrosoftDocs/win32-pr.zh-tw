---
description: 設定中的媒體類型
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: 設定中的媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106974768"
---
# <a name="setting-media-types-on-a-dmo"></a>設定中的媒體類型

在 SQL-DMO 可以處理任何資料之前，用戶端必須設定每個資料流程的媒體類型。  (此規則有一個次要例外狀況;請參閱 [選擇性資料流程](optional-streams.md)。 ) 若要尋找資料流程的數目，請呼叫 [**IMediaObject：： GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) 方法：


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



這個方法會傳回兩個值，也就是輸入數目和輸出數目。 這些值在每個的存留期都是固定的。

**慣用類型**

針對每個資料流程，每個資料流程會依喜好設定指派可能媒體類型的清單。 例如，慣用的類型可能是 32-RGB、24位 RGB 和16位 RGB （依該順序）。 當用戶端設定媒體類型時，它可以使用這些清單做為提示。 若要取得資料流程的慣用型別，請呼叫 [**IMediaObject：： GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) 方法或 [**IMediaObject：： GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) 方法。 指定從零) 開始 (類型的資料流程號碼和索引值。 例如，下列程式碼會從第一個輸入資料流程抓取第一個慣用的型別：


```C++
DMO_MEDIA_TYPE mt
hr = pDMO->GetInputType(0, 0, &mt)
if (SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
}
```



若要列舉給定資料流程上所有慣用的媒體類型，請使用會遞增類型索引的迴圈，直到該方法傳回 SQL-DMO \_ E \_ NO \_ 其他 \_ 專案，如下列範例所示：


```C++
DMO_MEDIA_TYPE mt;
DWORD dwType = 0;
while (hr = pDMO->GetInputType(0, dwType, &mt), SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
    ++dwType;
}
```



您應該注意下列關於慣用類型的重點：

-   SQL-DMO 可能會傳回沒有格式區塊的型別。 例如，當您不提供影像的寬度和高度時，可以指定像24位 RGB 的影片類型。 但是，當您設定型別時，您必須提供完整的格式區塊。  (部分媒體類型（例如 MIDI）永遠不需要格式區塊，在這種情況下，此備註不適用。 ) 
-   不需要用來支援它所傳回的每個慣用類型組合。 比方說，如果有兩個數據流，而每個資料流程有四個慣用型別，則有16個可能的組合，但並非全部都保證有效。
-   當用戶端設定某個資料流程的媒體類型時，每個資料流程可能會更新慣用的類型，以反映新的狀態。 但是，不需要這麼做。
-   若為某些資料流程，則： < 可能無法提供任何慣用的類型。 一般情況下，您應該至少在某些資料流程上提供一些慣用的類型。
-   您不需要使用 SQL-DMO 來提供可接受之媒體類型的完整清單。 您可能會有 "unadvertised" 類型，例如，

簡單地說，用戶端應該將慣用的型別視為指導方針。 若要瞭解支援的特定類型，唯一的方法是進行測試，如下一節所述。

**設定資料流程上的媒體類型**

您可以使用 [**IMediaObject：： SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) 和 [**IMediaObject：： SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) 方法來設定每個資料流程的類型。 您必須提供包含媒體類型完整描述的一 **\_ \_ 種媒體類型** 結構。 下列範例會使用 44.1-kHz 16 位的身歷聲 PCM 音訊，設定輸入資料流程0上的媒體類型：


```C++
DMO_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(DMO_MEDIA_TYPE));
// Allocate memory for the format block.
HRESULT hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    // Set the type GUIDs.
    mt.majortype  = MEDIATYPE_Audio;
    mt.subtype    = MEDIASUBTYPE_PCM;
    mt.formattype = FORMAT_WaveFormatEx;

    // Initialize the format block.
    WAVEFORMATEX *pWave = reinterpret_cast<WAVEFORMATEX*>(mt.pbFormat);
    pWave->wFormatTag = WAVE_FORMAT_PCM;
    pWave->nChannels = 2;
    pWave->nSamplesPerSec = 44100;
    pWave->wBitsPerSample = 16;
    pWave->nBlockAlign = (pWave->nChannels * pWave->wBitsPerSample) / 8;
    pWave->nAvgBytesPerSec = pWave->nSamplesPerSec * pWave->nBlockAlign;
    pWave->cbSize = 0;

    // Set the media type.
    hr = pDMO->SetInputType(0, &mt, 0); 

    // Release the format block.
    MoFreeMediaType(&mt);
}
```



若要在不設定的情況下測試媒體類型， 請使用 Sql-dmo  \_ SET \_ TYPEF \_ test \_ ONLY 旗標來呼叫 SetInputType 或 SetOutputType。 \_如果類型是可接受的，則方法會傳回 s OK， \_ 否則傳回 FALSE：


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



因為某個資料流程上的設定可能會影響另一個資料流程，所以您可能需要清除資料流程的媒體類型。 若要這樣做，請呼叫 **SetInputType** 或 **SetOutputType** ，並使用 sql-dmo \_ SET \_ TYPEF \_ CLEAR 旗標。

若是的是解碼器，用戶端通常會先設定輸入型別，然後選擇輸出型別。 針對編碼器，用戶端會先設定輸出類型，然後再設定輸入類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[直接裝載](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



