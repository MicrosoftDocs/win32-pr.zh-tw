---
description: 設定影片壓縮屬性
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: 設定影片壓縮屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3f1d73d27acb99e5a197ec4501411669278a6fd5c7b857875141d8831c7173f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583278"
---
# <a name="setting-video-compression-properties"></a>設定影片壓縮屬性

影片壓縮篩選器可支援其輸出圖釘上的 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) 介面。 使用這個介面設定壓縮屬性，例如主要畫面格速率、預測的 (P) 每個主要畫面格的畫面格數目，以及相對的壓縮品質。

首先，呼叫 [**IBaseFilter：： EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) 方法來尋找篩選的輸出圖釘，並查詢介面的 pin。 某些篩選器可能完全不支援此介面。 其他可能會公開介面，但不支援每個壓縮屬性。 若要判斷支援的屬性，請呼叫 [**IAMVideoCompression：： GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo)。 這個方法會傳回數個資訊片段：

-   一組功能旗標
-   描述性字串和版本號碼字串
-   支援的主要畫面速率、P 畫面播放速率和品質 (的預設值) 

方法具有下列語法：


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



*PszVersion* 和 *pszDesc* 參數是可接收版本字串和描述字串的寬字元緩衝區。 *CbVersion* 和 *cbDesc* 參數會收到所需的緩衝區大小（以位元組為單位）， (不是字元) 。 *LKeyFrame*、 *lPFrame* 和 *dblQuality* 參數會接收主要畫面速率、P 畫面播放速率和品質的預設值。 品質會以從0.0 到1.0 的浮點數表示。 *LCap* 參數會接收由 [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps)列舉型別定義之功能旗標的位 **or** 。

這些參數中的任何一個都可以是 **Null**，在此情況下，方法會忽略該參數。 例如，若要為版本和描述字串配置緩衝區，請先使用第一個和第三個參數中的 **Null** 來呼叫方法。 使用 *cbVersion* 和 *cbDesc* 傳回的值來配置緩衝區，然後再次呼叫方法：


```C++
int cbVersion, cbDesc; // Size in bytes, not characters!
hr = pCompress->GetInfo(0, &cbVersion, 0, &cbDesc, 0, 0, 0, 0);
if (SUCCEEDED(hr))
{
    WCHAR *pszVersion = new WCHAR[cbVersion/2]; // Wide character = 2 bytes
    WCHAR *pszDesc = new WCHAR[cbDesc/2];
    hr = pCompress->GetInfo(pszVersion, 0, pszDesc, 0, 0, 0, 0, 0);
}
```



*LCap* 的值表示篩選準則所支援的其他 **IAMVideoCompression** 方法。 例如，如果 *lCap* 包含 CompressionCaps \_ CanKeyFrame 旗標，則您可以呼叫 [**IAMVideoCompression：： get \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) 來取得主要畫面播放速率和 [**IAMVideoCompression：:p 的 \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) ，以設定主要畫面格速率。 負數值表示篩選將會使用預設值，如同從 [**IAMVideoCompression：： GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo)取得的值。 例如：


```C++
if (lCap & CompressionCaps_CanKeyFrame)
{
    hr = pCompress->get_KeyFrameRate(&lKeyFrame);
    if (FAILED(hr) || lKeyFrame < 0)
    {
        lKeyFrame = lDefaultKeyFrame; // From GetInfo.
    }
}
```



下列程式碼範例會嘗試在輸出釘選上尋找 **IAMVideoCompression** 介面。 如果成功，則會抓取壓縮屬性的預設值和實際值：


```C++
HRESULT hr = E_FAIL;
IEnumPins *pEnum = NULL;
IPin *pPin = NULL;
IAMVideoCompression *pCompress = NULL;

// Find the pin that supports IAMVideoCompression (if any).
pFilter->EnumPins(&pEnum);
while (S_OK == pEnum->Next(1, &pPin, NULL))
{
    hr = pPin->QueryInterface(IID_IAMVideoCompression, (void**)&pCompress);
    pPin->Release();
    if (SUCCEEDED(hr)) // Found the interface.
    {
        break;
    }
}
if (SUCCEEDED(hr)) 
{
    long lCap;                     // Capability flags
    long lKeyFrame, lPFrame;       // Real values
    double m_Quality;
    long lKeyFrameDef, lPFrameDef; // Default values
    double QualityDef;
    
    // Get default values and capabilities.
    hr = pCompress->GetInfo(0, 0, 0, 0, &KeyFrameDef, &lPFrameDef,
             &QualityDef, &lCap);
    if (SUCCEEDED(hr))
    {
        // Get actual values where possible.
        if (lCap & CompressionCaps_CanKeyFrame)
        {
            hr = pCompress->get_KeyFrameRate(&lKeyFrame);
            if (FAILED(hr) || lKeyFrame < 0)
                lKeyFrame = lKeyFrameDef;
        }
        if (lCap & CompressionCaps_CanBFrame)
        {
            hr = pCompress->get_PFramesPerKeyFrame(&lPFrame);
            if (FAILED(hr) || lPFrame < 0)
                lPFrame = lPFrameDef;
        }
        if (lCap & CompressionCaps_CanQuality)
        {
            hr = pCompress->get_Quality(&Quality);
            if (FAILED(hr) || Quality < 0)
                Quality = QualityDef;
        }
    }
}
```



> [!Note]  
> 如果您使用 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)介面來建立圖形，您可以藉由呼叫 [**ICaptureGraphBuilder2：： FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)來取得 **IAMVideoCompression** 介面，而不是使用 **IBaseFilter：： EnumPins**。 **FindInterface** 方法是一個 helper 方法，可在圖形中搜尋指定介面的篩選和釘選。

 

 

 



