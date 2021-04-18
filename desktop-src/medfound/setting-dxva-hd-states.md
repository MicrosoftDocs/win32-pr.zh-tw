---
description: .
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: 設定 DXVA-HD 狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e539796aa5d3997b35739e75c80b438a7b5da50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983371"
---
# <a name="setting-dxva-hd-states"></a>設定 DXVA-HD 狀態

在影片處理期間，Microsoft DirectX Video 加速 High 定義 (DXVA-HD) 裝置會將持續性狀態從某個畫面維持到下一個畫面格。 每個狀態都有記載的預設值。 設定裝置之後，請設定您想要變更其預設值的任何狀態。 在您處理每個畫面格之前，請更新任何應變更的狀態。

> [!Note]  
> 這種設計與 DXVA-VP 不同。 在 DXVA-VP 中，應用程式必須指定每個框架的總 VP 參數。

 

裝置狀態分為兩類：

-   *資料流程* 狀態會分別套用每個輸入資料流程。 您可以將不同的設定套用至每個資料流程。
-   *Array.blit* 狀態會全域套用至整個影片處理 array.blit。

已定義下列資料流程狀態。



| 資料流程狀態                                   | Description                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **DXVAHD \_ 資料流程 \_ 狀態 \_ D3DFORMAT**           | 輸入影片格式。                                                                                             |
| **DXVAHD \_ 資料流程 \_ 狀態 \_ 框架 \_ 格式**       | 交錯。                                                                                                    |
| **DXVAHD \_ 資料流程 \_ 狀態 \_ 輸入 \_ 色彩 \_ 空間** | 輸入色彩空間。 此狀態指定輸入資料流程的 RGB 色彩範圍和 YCbCr 傳輸矩陣。 |
| **DXVAHD \_ 資料流程 \_ 狀態 \_ 輸出 \_ 速率**        | 輸出畫面播放速率。 此狀態控制畫面播放速率的轉換。                                                   |
| **DXVAHD \_ 資料流程 \_ 狀態 \_ 來源 \_ 矩形**        | 來源矩形。                                                                                               |
| **DXVAHD \_ 資料流程 \_ 狀態 \_ 目的地 \_ 矩形**   | 目的地矩形。                                                                                          |
| **DXVAHD \_ 資料流程 \_ 狀態 \_ ALPHA**               | 平面 Alpha。                                                                                                   |
| **DXVAHD \_ 資料流程 \_ 狀態 \_ 調色板**             | 調色板。 此狀態只適用于調色盤輸入格式。                                             |
| **DXVAHD \_ 資料流程 \_ 狀態 \_ LUMA \_ 金鑰**           | Luma 鍵。                                                                                                       |
| **DXVAHD \_ 資料流程 \_ 狀態 \_ 外觀 \_ 比例**       | 圖元外觀比例。                                                                                             |
| **DXVAHD \_ 資料流程 \_ 狀態 \_ 篩選 \_ Xxxx**        | 影像篩選設定。 驅動程式可支援亮度、對比和其他影像篩選。                    |



 

以下是定義的 array.blit 狀態：



| Array.blit 狀態                                   | Description                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| **DXVAHD \_ BLT \_ 狀態 \_ 目標 \_ 矩形**         | 目標矩形。                                                            |
| **DXVAHD \_ BLT \_ 狀態 \_ 背景 \_ 色彩**    | 背景色彩。                                                            |
| **DXVAHD \_ BLT \_ 狀態 \_ 輸出 \_ 色彩 \_ 空間** | 輸出色彩空間。                                                          |
| **DXVAHD \_ BLT \_ 狀態 \_ ALPHA \_ 填滿**          | Alpha 填滿模式。                                                             |
| **DXVAHD \_ BLT \_ 狀態 \_ CONSTRICTION**         | 收縮。 此狀態控制裝置是否 downsamples 輸出。 |



 

若要設定資料流程狀態，請呼叫 [**IDXVAHD \_ VideoProcessor：： SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) 方法。 若要設定 array.blit 狀態，請呼叫 [**IDXVAHD \_ VideoProcessor：： SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) 方法。 在這兩種方法中，列舉值會指定要設定的狀態。 狀態資料是使用特定狀態的資料結構來指定，應用程式會將它轉換成 **void \*** 型別。

下列程式碼範例會設定資料流程0的輸入格式和目的矩形，並將背景色彩設為黑色。


```C++
HRESULT SetDXVAHDStates(HWND hwnd, D3DFORMAT inputFormat)
{
    // Set the initial stream states.

    // Set the format of the input stream

    DXVAHD_STREAM_STATE_D3DFORMAT_DATA d3dformat = { inputFormat };

    HRESULT hr = g_pDXVAVP->SetVideoProcessStreamState(
        0,  // Stream index
        DXVAHD_STREAM_STATE_D3DFORMAT,
        sizeof(d3dformat),
        &d3dformat
        );

    if (SUCCEEDED(hr))
    { 
        // For this example, the input stream contains progressive frames.

        DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { DXVAHD_FRAME_FORMAT_PROGRESSIVE };
        
        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index
            DXVAHD_STREAM_STATE_FRAME_FORMAT,
            sizeof(frame_format),
            &frame_format
            );
    }

    if (SUCCEEDED(hr))
    { 
        // Compute the letterbox area.

        RECT rcDest;
        GetClientRect(hwnd, &rcDest);

        RECT rcSrc;
        SetRect(&rcSrc, 0, 0, VIDEO_WIDTH, VIDEO_HEIGHT);

        rcDest = LetterBoxRect(rcSrc, rcDest);

        // Set the destination rectangle, so the frame is displayed within the 
        // letterbox area. Otherwise, the frame is stretched to cover the 
        // entire surface.

        DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA DstRect = { TRUE, rcDest };

        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index 
            DXVAHD_STREAM_STATE_DESTINATION_RECT,
            sizeof(DstRect),
            &DstRect
            );
    }

    if (SUCCEEDED(hr))
    { 
        DXVAHD_COLOR_RGBA rgbBackground = { 0.0f, 0.0f, 0.0f, 1.0f };  // RGBA

        DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA background = { FALSE, rgbBackground };

        hr = g_pDXVAVP->SetVideoProcessBltState(
            DXVAHD_BLT_STATE_BACKGROUND_COLOR,
            sizeof (background),
            &background
            );
    }

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



