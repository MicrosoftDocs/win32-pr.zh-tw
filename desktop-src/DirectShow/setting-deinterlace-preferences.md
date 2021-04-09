---
description: 設定交錯喜好設定
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: 設定交錯喜好設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be52ae3023c8e4bc83c3305a104c389f423cffd6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687380"
---
# <a name="setting-deinterlace-preferences"></a>設定交錯喜好設定

 (VMR) 的影片混合轉譯器支援硬體加速去交錯，可改善交錯式影片的轉譯品質。 可用的確切功能取決於基礎硬體。 應用程式可以查詢硬體去交錯功能，並透過 [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) 介面設定去交錯喜好設定 (VMR-7) 或 [**IVMRDEINTERLACECONTROL9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) 介面 (VMR-9) 。 去交錯會以每個資料流程為基礎執行。

VMR-7 和 VMR-9 之間的交錯行為有一個重要的差異。 在圖形硬體不支援 advanced 去交錯的系統上，VMR-7 可以切換回硬體重迭，並指示它使用 BOB 樣式的交錯。 在此情況下，雖然 VMR 是報告30fps，但影片實際上是轉譯成每秒60個翻轉。

除了使用硬體重迭的 VMR-7 案例之外，去交錯是由 VMR 的混音器所執行。 混音器會使用 DirectX Video 加速 (DXVA) 去交錯設備磁碟機介面 (DDI) 來執行去交錯。 應用程式無法呼叫此 DDI，應用程式無法取代 VMR 的去交錯功能。 不過，應用程式可以選取所需的去交錯模式，如本節所述。

> [!Note]  
> 本節說明 **IVMRDeinterlaceControl9** 方法，但 VMR-7 版本幾乎完全相同。

 

若要取得影片串流的去交錯功能，請執行下列動作：

1.  使用影片資料流程的描述填入 [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) 結構。 稍後會提供如何填寫此結構的詳細資料。
2.  將結構傳遞給 [**IVMRDeinterlaceControl9：： GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) 方法。 呼叫方法兩次。 第一個呼叫會傳回硬體針對指定的格式所支援的交錯模式數目。 配置此大小的 Guid 陣列，然後再次呼叫方法，傳遞陣列的位址。 第二個呼叫會以 Guid 填入陣列。 每個 GUID 會識別一個去交錯模式。
3.  若要取得特定模式的 capabiltiies，請呼叫 [**IVMRDeinterlaceControl9：： GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) 方法。 傳入相同的 **VMR9VideoDesc** 結構，以及陣列中的其中一個 guid。 方法會以模式功能填入 [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) 結構。

下列程式碼顯示這些步驟：


```C++
VMR9VideoDesc VideoDesc; 
DWORD dwNumModes = 0;
// Fill in the VideoDesc structure (not shown).
hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
    &dwNumModes, NULL);
if (SUCCEEDED(hr) && (dwNumModes != 0))
{
    // Allocate an array for the GUIDs that identify the modes.
    GUID *pModes = new GUID[dwNumModes];
    if (pModes)
    {
        // Fill the array.
        hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
            &dwNumModes, pModes);
        if (SUCCEEDED(hr))
        {
            // Loop through each item and get the capabilities.
            for (int i = 0; i < dwNumModes; i++)
            {
                VMR9DeinterlaceCaps Caps;
                hr = pDeinterlace->GetDeinterlaceModeCaps(pModes + i, 
                    &VideoDesc, &Caps);
                if (SUCCEEDED(hr))
                {
                    // Examine the Caps structure.
                }
            }
        }
        delete [] pModes;
    }
}
```



現在應用程式可以使用下列方法來設定資料流程的去交錯模式：

-   [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode)方法會設定慣用模式。 使用 GUID \_ Null 來關閉去交錯。
-   如果無法使用要求的模式， [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) 方法會指定行為。
-   [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode)方法會傳回您所設定的慣用模式。
-   如果未提供慣用模式， [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) 方法會傳回使用中的實際模式，而這可能是回溯模式。

方法參考頁面會提供詳細資訊。

**使用 VMR9VideoDesc 結構**

在先前所述的程式中，第一個步驟是使用影片資料流程的描述填入 **VMR9VideoDesc** 結構。 從取得影片串流的媒體類型開始。 您可以在 VMR 篩選器的輸入 pin 上呼叫 [**IPin：： ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) 來執行這項作業。 然後確認影片資料流程是否為交錯式。 只有 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式可以交錯。 如果格式類型為 VideoInfo 格式 \_ ，則必須是漸進式框架。 如果格式類型為 VideoInfo2 格式 \_ ，請檢查 AMINTERLACE IsInterlaced 旗標的 **dwInterlaceFlags** 欄位 \_ 。 此旗標的存在表示影片是交錯式的。

假設變數 **pBMI** 是格式區塊中 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構的指標。 在 **VMR9VideoDesc** 結構中設定下列值：

-   **dwSize**：將此欄位設定為 `sizeof(VMR9VideoDesc)` 。
-   **dwSampleWidth**：將此欄位設定為 `pBMI->biWidth` 。
-   **dwSampleHeight**：將此欄位設定為 `abs(pBMI->biHeight)` 。
-   **SampleFormat**：此欄位描述媒體類型的交錯特性。 檢查 **VIDEOINFOHEADER2** 結構中的 **dwInterlaceFlags** 欄位，並將 **SampleFormat** 設定為等於相等的 [**VMR9 \_ SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat)旗標。 下面提供 helper 函式來進行這項作業。
-   **InputSampleFreq**：此欄位提供輸入頻率，可從 **VIDEOINFOHEADER2** 結構中的 **AvgTimePerFrame** 欄位計算。 在一般情況下，請將 **dwNumerator** 設定為10000000，並將 **DwDenominator** 設定為 **AvgTimePerFrame**。 不過，您也可以檢查一些已知的畫面播放速率：

    | 每個畫面格的平均時間 | 畫面播放速率 (fps)  | 分子 | 分母 |
    |------------------------|------------------|-----------|-------------|
    | 166833                 | 59.94 (NTSC)      | 60000     | 1001        |
    | 333667                 | 29.97 (NTSC)      | 30000     | 1001        |
    | 417188                 | 23.97 (NTSC)      | 24000     | 1001        |
    | 200000                 | 50.00 (PAL)       | 50        | 1           |
    | 400000                 | 25.00 (PAL)       | 25        | 1           |
    | 416667                 | 24.00 (膠捲)      | 24        | 1           |

    

     

-   **OutputFrameFreq**：此欄位提供輸出頻率，可從 **InputSampleFreq** 值和輸入資料流程的交錯特性計算：
    -   Set **OutputFrameFreq. dwDenominator** 等於 **InputSampleFreq. dwDenominator**。
    -   如果輸入影片是交錯的，請將 **OutputFrameFreq. dwNumerator** 設定為 2 x **InputSampleFreq. dwNumerator**。 去交錯之後 (，畫面播放速率會加倍。 ) 否則，請將值設定為 **InputSampleFreq. dwNumerator**。
-   **dwFourCC**：將此欄位設定為 `pBMI->biCompression` 。

下列 helper 函數會將 AMINTERLACE \_ *X* 旗標轉換成 [**VMR9 \_ SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat)值：


```C++
#define IsInterlaced(x) ((x) & AMINTERLACE_IsInterlaced)
#define IsSingleField(x) ((x) & AMINTERLACE_1FieldPerSample)
#define IsField1First(x) ((x) & AMINTERLACE_Field1First)

VMR9_SampleFormat ConvertInterlaceFlags(DWORD dwInterlaceFlags)
{
    if (IsInterlaced(dwInterlaceFlags)) {
        if (IsSingleField(dwInterlaceFlags)) {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldSingleEven;
            }
            else {
                return VMR9_SampleFieldSingleOdd;
            }
        }
        else {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldInterleavedEvenFirst;
             }
            else {
                return VMR9_SampleFieldInterleavedOddFirst;
            }
        }
    }
    else {
        return VMR9_SampleProgressiveFrame;  // Not interlaced.
    }
}
```



 

 



