---
title: 啟用 DirectX Video 加速
description: 啟用 DirectX Video 加速
ms.assetid: 5cb2f564-88e3-4b60-bde3-6ccf69c97c48
keywords:
- Windows Media Format SDK，啟用 DXVA
- 'Windows Media Format SDK、DirectX Video 加速 (DXVA) '
- Windows Media Format SDK，影片加速
- Advanced Systems Format (ASF) ，啟用 DXVA
- ASF (Advanced Systems Format) ，啟用 DXVA
- 'Advanced Systems Format (ASF) 、DirectX Video 加速 (DXVA) '
- 'ASF (Advanced Systems Format) 、DirectX Video 加速 (DXVA) '
- Advanced Systems Format (ASF) 、影片加速
- ASF (Advanced Systems Format) 、影片加速
- DirectX Video 加速 (DXVA) ，啟用
- DXVA (DirectX Video 加速) ，啟用
- DirectX Video 加速 (DXVA) 、作業順序
- DXVA (DirectX Video 加速) 、營運順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896147fe11b4b7f5fb91d8dc288e616b643bd5ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374394"
---
# <a name="enabling-directx-video-acceleration"></a>啟用 DirectX Video 加速

本節說明在自訂播放流程中播放串流內容時，如何啟用 Microsoft® DirectX®影片加速。

## <a name="background"></a>背景

DirectX Video 加速 (DirectX VA) 是一種 API 規格，適用于進行2D 解碼作業的硬體加速。 它可讓軟體解碼器將某些需要大量 CPU 的作業卸載至圖形配接器進行處理。 針對終端使用者，這可讓您在配備 DirectX VA 相容圖形配接器的舊電腦上，進行全螢幕 DVD 播放這類高比率的影片。

從 Windows Media Format 9 系列 SDK 開始，SQL-DMO 包裝函式篩選器支援 DirectX VA。 這表示，在本機播放中，應用程式可以使用 WM ASF 讀取器篩選器來播放 Windows Media 內容，而且如果圖形配接器支援 DirectX VA 硬體加速，將會自動叫用。 但是，「WM ASF 讀取器」篩選器不支援播放資料流程內容。 因此，如果您想要在自訂播放程式中播放資料流程處理的內容時支援 DirectX VA，您必須使用替代機制，也就是 Windows Media Player 從 Windows Media 9 系列開始使用的機制。

由於 Windows Media Player 是在開發 QASF 篩選之前設計的，因此 Windows Media Player 有自己的來源篩選器（以 Windows Media Format SDK 為基礎）來播放 Windows Media 格式的內容。 WMP Windows Media 來源篩選器會將解壓縮的資料直接提供給音訊和影片轉譯器。 相較之下，WM 的 ASF 讀取器會將壓縮的內容傳遞至 Windows Media 解碼器 DirectX 媒體物件 (DMOs) ，而這些物件是裝載于 SQL-DMO 包裝函式中。 下圖說明 WM ASF 讀取器和 WMP Windows Media 來源篩選器之間的差異。

![自訂來源篩選輸出未壓縮的範例](images/wmp-dxva-graph.png)

![qasf 來源篩選輸出壓縮的範例](images/qasf-dxva-graph.png)

若要啟用串流內容的 DirectX VA，您必須建立自訂來源篩選器，例如頂端圖表中的篩選器。 基本上，此篩選器會使用 Windows Media Format SDK 來具現化 WM 讀取器物件、解壓縮範例，並在其輸出圖釘上將它們傳送至下游。 本文假設您已建立來源篩選器，現在已準備好執行 DirectX VA 支援。

若要啟用 DirectX VA，來源篩選器的基本工作是提供影片轉譯器和 WMV 解碼，以及用來協調 DirectX VA 連線所需的介面。 來源篩選不會參與這些協商。 串流開始之後，來源篩選器唯一可以執行的 DirectX VA 相關工作，是在 WMV 解碼將它們傳遞給影片轉譯器之前，修改影片範例上的時間戳記。 這麼做的主要原因是要提供自訂的時間軸控制項，超過標準的 DirectShow®介面啟用的範圍。

定義了三個介面，以啟用 Windows Media 格式 SDK、播放機的來源篩選器、Windows Media 視訊的解碼器，以及重迭混音器或影片混合轉譯器之間的必要通訊。 下表將說明這些介面。



| 介面                                                        | 描述                                                                                                                                                                                        |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecAMVideoAccelerator**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmcodecamvideoaccelerator) | 由 Windows Media 解碼（由媒體播放機的來源篩選器）所公開，並由媒體播放機的來源篩選器所呼叫，以設定啟用 DirectX VA 以解碼 Windows Media 視訊內容所需的各種連接。 |
| [**IWMPlayerTimestampHook**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmplayertimestamphook)         | 在播放程式的來源篩選器上執行。 它可讓篩選準則修改影片範例上的時間戳記，然後再將它們傳遞給下游。                                                 |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)             | 在 WM 讀取器物件上執行。 它是由播放程式來源篩選器呼叫，以取得來自解碼器的介面。                                                                             |



 

## <a name="order-of-operations-in-directx-vaenabled-playback"></a>DirectX VA 中的作業順序-已啟用播放

本節說明在執行時間，針對已啟用 DirectX VA 的播放程式及其來源篩選作業的一般作業順序。 本節提及的元件包括：

-   協力廠商媒體播放機，稱為 player。
-   由播放程式具現化的自訂來源篩選器，它會使用 Windows Media Format SDK 來解壓縮 Windows Media 內容。
-   播放程式來源篩選的影片輸出釘選，稱為輸出圖釘。
-   DirectShow 影片播放篩選圖形，稱為圖形。
-   影片混合轉譯器，稱為 VMR。
-   Windows Media Format SDK 非同步讀取器物件，稱為「讀取器」。
-   Windows Media 視訊的解碼器 DirectX 媒體物件，稱為「解碼器」。

作業的順序如下所示：

1.  播放程式會將其來源篩選器和讀取器物件具現化。 讀取器會建立一個 video 解碼，並在其上設定 (壓縮的) 輸入類型。 在播放程式嘗試設定其影片播放圖形之前，必須先進行這項作業，因為 SDK 和解碼器 SQL-DMO 必須參與圖形的協商程式，而在步驟9中，則必須知道輸入格式。
2.  播放程式會呼叫 **IGraphBuilder：： Render**，提供影片來源篩選器的輸出圖釘。 此時，DirectShow 篩選圖形管理員會嘗試將 VMR 連接到播放程式的影片來源篩選。
3.  篩選圖形管理員會在播放程式影片來源篩選器的輸出圖釘上呼叫 **IPin：： Connect** 。

**IPin：： Connect** 內會發生步驟4到10。

1.  來源篩選器會從讀取器的 **IWMReaderAccelerator：： GetCodecInterface** 方法取得 **IWMCodecAMVideoAccelerator** 介面。 如果編解碼器不支援 DirectX VA，呼叫 **GetCodecInterface** 可能會失敗。 在此情況下，會如往常般進行協調，而不支援 DirectX VA。
2.  來源篩選器會透過 IWMCodecAMVideoAccelerator：： SetAcceleratorInterface，將 **IAMVideoAccelerator** 指標從傳入的 pin **傳遞至** **：：**。
3.  然後，來源篩選器會將 **IPin：： connect** 作業的其餘部分委派給 **CBaseOutputPin：： connect** 方法。 使用 SDK 的格式列舉會依照目前的方式繼續進行。 如果編解碼器支援所連接內容的 DirectX VA，則編解碼器會先顯示這些 DirectX VA 子類型，然後再支援 YUV 和 RGB 類型。 如果有 DirectX VA 支援，則會嘗試在 DirectX VA 子類型的內容中進行步驟7到11。 下列程式碼片段說明如何識別 DirectX VA 媒體子類型。
    ```C++
    bool IsDXVASubtype( AM_MEDIA_TYPE * pmt )
    {
        // All DXVA types have the same last 3 DWORDs.
        // guidDXVA is the base GUID for all DXVA subtypes.

        GUID guidDXVA = { 0x00000000, 0xa0c7, 0x11d3, { 0xb9,0x84,0x00,0xc0,0x4f,0x2e,0x73,0xc5 } };

        unsigned long const * plguid;
        unsigned long const * plguidDXVA;
        plguid = (unsigned long const *)&pmt->subtype;
        plguidDXVA = (unsigned long *)&guidDXVA;

        if( ( plguid[1] == plguidDXVA[1] ) &&
            ( plguid[2] == plguidDXVA[2] ) &&
            ( plguid[3] == plguidDXVA[3] ) )
        {
            return true;
        }

        return false;
    }
    
    ```

    

4.  **CBaseOutputPin：： Connect** 執行會在步驟3期間呼叫 **IPin：： CompleteConnect** 。 如果考慮到 DirectX VA 子類型，則會嘗試 DirectX VA 協商。 輸出圖釘會呼叫 **IWMCodecAMVideoAccelerator：： NegotiateConnection**，並將目前的輸出媒體類型傳遞給它。
5.  在 IAMVideoAccelerator 介面中，VMR 會透過介面執行必要的協商，並傳回兩個已同意的影片子類型 GUID。 輸出圖釘會將在此處理過程中收到的所有 **IAMVideoAcceleratorNotify** 呼叫委派給 **IAMVideoAcceleratorNotify** 介面，也可以透過 **IWMReaderAccelerator：： GetCodecInterface** 方法取得。
6.  如果 **NegotiateConnection** 成功，輸出圖釘會呼叫 **IWMCodecAMVideoAccelerator：： SetPlayerNotify** 和 **IWMPlayerTimestampHook** 介面。 此攔截器可讓來源篩選器先更新範例上的時間戳記，然後再將它們交給轉譯器。
7.  來源篩選準則會以協商的媒體類型呼叫 **IWMReaderAccelerator：： Notify** 。 這可讓讀取器更新其內部變數，並認可至 DirectX VA。 這是編解碼器或讀取器可能失敗的最後一個位置。 如果上述任何一個步驟失敗，來源篩選應該會返回步驟3，並嘗試由讀取器列舉的下一個型別。
8.  播放開始。 如果連線輸出類型為 DirectX VA，讀取器會忽略來自解碼器的輸出緩衝區。
9.  當 **IPin：:D isconnect** 時，來源篩選會使用 **Null** 來呼叫 **IWMCodecAMVideoAccelerator：： SetAcceleratorInterface** 。 這會中斷編解碼器與轉譯器之間的 DirectX VA 連接。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**讀取 ASF 檔案**](reading-asf-files.md)
</dt> </dl>

 

 




