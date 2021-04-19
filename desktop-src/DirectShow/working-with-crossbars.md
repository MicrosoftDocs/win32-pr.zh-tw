---
description: 使用 Crossbars
ms.assetid: 6e8ee9c3-6776-498b-ad38-36f8172a27ae
title: 使用 Crossbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d3a1c43703ac662d44854b0fc6bad8b280c368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975508"
---
# <a name="working-with-crossbars"></a>使用 Crossbars

如果影片捕獲卡有一個以上的實體輸入，或支援多個資料路徑，則篩選圖形可能會包含 [類比視頻縱橫條篩選](analog-video-crossbar-filter.md)。 [Capture Graph Builder] 會在需要時自動新增此篩選;它會從 capture 篩選器上游。 視硬體而定，篩選圖形可能包含多個多個多個縱橫濾波器的實例。

這條縱橫濾波器會公開 [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) 介面，可讓您用來將特定輸入路由傳送至特定的輸出。 例如，視訊卡可能會有一個同軸連接器和一個 S-video 輸入。 這些會在多個十字篩選器上表示為輸入圖釘。 若要選取輸入，請使用 [**IAMCrossbar：： route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) 方法，將對應的輸入 pin 路由傳送至十字線的輸出圖釘。

您可以使用 [**ICaptureGraphBuilder2：： FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 方法來搜尋支援 **IAMCrossbar** 的篩選準則，以在圖形中找出縱橫比對篩選。 例如，下列程式碼會搜尋兩個 crossbars：


```C++
// Search upstream for a crossbar.
IAMCrossbar *pXBar1 = NULL;
hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
if (SUCCEEDED(hr)) 
{
    // Found one crossbar. Get its IBaseFilter interface.
    IBaseFilter *pFilter = NULL;
    hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pFilter);
    if (SUCCEEDED(hr)) 
    {
        // Search upstream for another crossbar.
        IAMCrossbar *pXBar2 = NULL;
        hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pFilter,
                 IID_IAMCrossbar, (void**)&pXBar2);
        pFilter->Release();

        if (SUCCEEDED(hr))
        {
            /* ... */
            pXBar2->Release();
        }
    }
    pXBar1->Release();
}
```



如需更一般化的方法，請參閱 [AmCap 範例](amcap-sample.md)中的 CCrossbar 類別。

當您有 **IAMCrossbar** 介面的指標時，您可以取得有關資料線篩選的資訊，包括每個釘選的實體類型，以及可將輸入釘選到哪些輸出圖釘的矩陣。

-   若要判斷 pin 所對應的實體連接器類型，請呼叫 [**IAMCrossbar：： get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) 方法。 方法會傳回 [**PhysicalConnectorType**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) 列舉的成員。 例如，S 影片 pin 會傳回 PhysConn Video SVideo 的值 \_ \_ 。

    **Get \_ CrossbarInfo** 方法也會指出兩個圖釘是否彼此相關。 例如，影片調諧器釘選可能與音訊調諧器 pin 相關。 相關的 pin 具有相同的 pin 方向，而且通常是卡片上相同實體插頭或連接器的一部分。

-   若要判斷是否可以將輸入 pin 路由傳送至特定的輸出 pin，請呼叫 [**IAMCrossbar：： CanRoute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) 方法。
-   若要判斷 pin 之間的目前路由，請呼叫 [**IAMCrossbar：： get \_ IsRoutedTo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) 方法。

先前的方法都是以索引編號來指定釘選，且輸出釘選和輸入圖釘都從零編制索引。 呼叫 **IAMCrossbar：： get \_ PinCounts** 方法，以找出篩選器上的釘選數目。

例如，下列程式碼會在主控台視窗中顯示有關縱橫濾波器的資訊：


```C++
// Helper function to associate a name with the type.
const char * GetPhysicalPinName(long lType)
{
    switch (lType) 
    {
    case PhysConn_Video_Tuner:            return "Video Tuner";
    case PhysConn_Video_Composite:        return "Video Composite";
    case PhysConn_Video_SVideo:           return "S-Video";
    case PhysConn_Video_RGB:              return "Video RGB";
    case PhysConn_Video_YRYBY:            return "Video YRYBY";
    case PhysConn_Video_SerialDigital:    return "Video Serial Digital";
    case PhysConn_Video_ParallelDigital:  return "Video Parallel Digital"; 
    case PhysConn_Video_SCSI:             return "Video SCSI";
    case PhysConn_Video_AUX:              return "Video AUX";
    case PhysConn_Video_1394:             return "Video 1394";
    case PhysConn_Video_USB:              return "Video USB";
    case PhysConn_Video_VideoDecoder:     return "Video Decoder";
    case PhysConn_Video_VideoEncoder:     return "Video Encoder";
        
    case PhysConn_Audio_Tuner:            return "Audio Tuner";
    case PhysConn_Audio_Line:             return "Audio Line";
    case PhysConn_Audio_Mic:              return "Audio Microphone";
    case PhysConn_Audio_AESDigital:       return "Audio AES/EBU Digital";
    case PhysConn_Audio_SPDIFDigital:     return "Audio S/PDIF";
    case PhysConn_Audio_SCSI:             return "Audio SCSI";
    case PhysConn_Audio_AUX:              return "Audio AUX";
    case PhysConn_Audio_1394:             return "Audio 1394";
    case PhysConn_Audio_USB:              return "Audio USB";
    case PhysConn_Audio_AudioDecoder:     return "Audio Decoder";
        
    default:                              return "Unknown Type";
    }    
}

void DisplayCrossbarInfo(IAMCrossbar *pXBar)
{
    HRESULT hr;
    long cOutput = -1, cInput = -1;
    hr = pXBar->get_PinCounts(&cOutput, &cInput);

    for (long i = 0; i < cOutput; i++)
    {
        long lRelated = -1, lType = -1, lRouted = -1;

        hr = pXBar->get_CrossbarPinInfo(FALSE, i, &lRelated, &lType);
        hr = pXBar->get_IsRouted(i, &lRouted);

        printf("Output pin %d: %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated out: %d, Routed in: %d\n", lRelated, lRouted);
        printf("\tSwitching Matrix: ");

        for (long j = 0; j < cInput; j++)
        {
            hr = pXBar->CanRoute(i, j);
            printf("%d-%s", j, (S_OK == hr ? "Yes" : "No"));
        }
        printf("\n\n");
    }

    for (i = 0; i < cInput; i++)
    {
        long lRelated = -1, lType = -1;

        hr = pXBar->get_CrossbarPinInfo(TRUE, i, &lRelated, &lType);

        printf("Input pin %d - %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated in: %d\n", lRelated);
    }
}
```



若為假設性卡片，此函式可能會產生下列輸出：


```C++
Output pin 0: S-Video
    Related out: 2, Routed in: 0
    Switching Matrix: 0-Yes 1-No 2-No 3-No
Output pin 1 - Video Tuner
    Related out: 2, Routed in: 1
    Switching Matrix: 0-No 1-Yes 2-No 3-No
Output pin 2 - Audio decoder
    Related out: 1, Routed in: -1
    Switching Matrix: 0-No 1-No 2-Yes 3-Yes

Input pin 0 - S-Video
    Related in: 2
Input pin 1 - Video Tuner
    Related in: 3
Input pin 2 - Audio line
    Related in: 0
Input pin 3 - Audio tuner
    Related in: 1
```



在輸出端，S 影片和影片調諧器都與音訊解碼器相關。 在輸入端，影片調諧器與音訊調諧器相關聯，而 s-video 與音訊行相關。 S-Video 輸入會路由傳送到 s-video 輸出;影片調諧器的輸入會路由傳送至影片調諧器輸出。 目前不會將任何內容路由傳送到音訊解碼器，但音訊行或音訊調諧器可能會路由傳送到音訊。

您可以藉由呼叫 [**IAMCrossbar：： Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) 方法來變更現有的路由。

 

 



