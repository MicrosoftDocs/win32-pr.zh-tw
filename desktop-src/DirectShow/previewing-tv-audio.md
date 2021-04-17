---
description: 預覽電視音訊
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: 預覽電視音訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cc63583c946d47ed744eacd51f0939ec852d53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467632"
---
# <a name="previewing-tv-audio"></a>預覽電視音訊

若要預覽電視音訊，請將十字線篩選器上的音訊解碼器釘選到音訊調諧器釘選。 若要將音訊靜音，請將音訊解碼器釘選到-1，如下列圖表所示。 [使用 Crossbars](working-with-crossbars.md)時，會描述 (的橫線篩選器。 ) 

![路由音訊解碼器 pin](images/vidcap07.png)

基本方法如下所示：

1.  您可以使用 [**ICaptureGraphBuilder2：： FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 方法找出縱橫比對篩選。
2.  使用 [**IAMCrossbar：： get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) 方法來列舉縱橫比對的輸入和輸出圖釘。 搜尋音訊解碼器輸出釘選和音訊調諧器輸入圖釘。
3.  如果您找到正確的 pin，請呼叫 [**IAMCrossbar：： route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) 來路由傳送 pin。 如果沒有，請查看其他縱橫條的上游，然後重複此程式。
4.  若要將音訊靜音，請將音訊解碼器釘選到-1。

大部分的電視調諧器都使用單一的雙縱橫濾波器，但有些會使用兩個雙橫線濾波器。 因此，如果第一個縱橫條失敗，您可能必須搜尋第二個。

> [!Note]  
> 跟您預期的一樣，因為調諧器介面卡與音效卡之間有實體連線，所以不需要音訊捕獲篩選器或音訊轉譯器就能預覽音訊。

 

下列程式碼會更詳細地顯示這些步驟。 第一，以下是協助程式函式，可搜尋指定 pin 類型的縱橫濾波器：


```C++
HRESULT FindCrossbarPin(
    IAMCrossbar *pXBar,                 // Pointer to the crossbar.
    PhysicalConnectorType PhysicalType, // Pin type to match.
    PIN_DIRECTION Dir,                  // Pin direction.
    long *pIndex)       // Receives the index of the pin, if found.
{
    BOOL bInput = (Dir == PINDIR_INPUT ? TRUE : FALSE);

    // Find out how many pins the crossbar has.
    long cOut, cIn;
    HRESULT hr = pXBar->get_PinCounts(&cOut, &cIn);
    if (FAILED(hr)) return hr;
    // Enumerate pins and look for a matching pin.
    long count = (bInput ? cIn : cOut);
    for (long i = 0; i < count; i++)
    {
        long iRelated = 0;
        long ThisPhysicalType = 0;
        hr = pXBar->get_CrossbarPinInfo(bInput, i, &iRelated,
            &ThisPhysicalType);
        if (SUCCEEDED(hr) && ThisPhysicalType == PhysicalType)
        {
            // Found a match, return the index.
            *pIndex = i;
            return S_OK;
        }
    }
    // Did not find a matching pin.
    return E_FAIL;
}
```



下一個函式會根據 *bActivate* 參數的值，嘗試啟用或將音訊靜音。 它會在指定的縱橫條篩選準則中搜尋所需的釘選。 如果找不到，則會傳回錯誤碼。


```C++
HRESULT ConnectAudio(IAMCrossbar *pXBar, BOOL bActivate)
{
    // Look for the Audio Decoder output pin.
    long i = 0;
    HRESULT hr = FindCrossbarPin(pXBar, PhysConn_Audio_AudioDecoder,
        PINDIR_OUTPUT, &i);
    if (SUCCEEDED(hr))
    {
        if (bActivate)  // Activate the audio. 
        {
            // Look for the Audio Tuner input pin.
            long j = 0;
            hr = FindCrossbarPin(pXBar, PhysConn_Audio_Tuner, 
                PINDIR_INPUT, &j);
            if (SUCCEEDED(hr))
            {
                return pXBar->Route(i, j);
            }
        }
        else  // Mute the audio
        {
            return pXBar->Route(i, -1);
        }
    }
    return E_FAIL;
}
```



下一個函式會在篩選圖形中搜尋橫線篩選。 如果找到一個，就會嘗試使用先前的函式) 來啟用或靜音 (的音訊。 如果該作業失敗，此方法會搜尋上游是否有第二個縱橫條，然後再試一次。 如需更一般化的方式來管理圖形中的多個縱橫比對篩選，請參閱 AmCap 範例應用程式中的 CCrossbar 類別。


```C++
HRESULT ActivateAudio(ICaptureGraphBuilder2 *pBuild, IBaseFilter *pSrc,
  BOOL bActivate)
{
    // Search upstream for a crossbar.
    IAMCrossbar *pXBar1 = NULL;
    HRESULT hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
    if (SUCCEEDED(hr)) 
    {
        hr = ConnectAudio(pXBar1, bActivate);
        if (FAILED(hr))
        {
            // Look for another crossbar.
            IBaseFilter *pF = NULL;
            hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pF);
            if (SUCCEEDED(hr)) 
            {
                // Search upstream for another one.
                IAMCrossbar *pXBar2 = NULL;
                hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pF,
                    IID_IAMCrossbar, (void**)&pXBar2);
                pF->Release();
                if (SUCCEEDED(hr))
                {
                    hr = ConnectAudio(pXBar2, bActivate);
                    pXBar2->Release();
                }
            }
        }
        pXBar1->Release();
    }
    return hr;
}
```



下列程式碼說明如何呼叫這些函式：


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



請注意，這些範例函數會重複許多相同的函式呼叫。 例如，它們會每次列舉一次縱橫條的釘選。 在實際的應用程式中，您可能會快取這部分資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[類比電視音訊](analog-television-audio.md)
</dt> <dt>

[使用 Crossbars](working-with-crossbars.md)
</dt> </dl>

 

 



