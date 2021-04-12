---
title: 執行 DoProcessOutput
description: 執行 DoProcessOutput
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- Windows Media Player 外掛程式、音訊 DSP
- 外掛程式、音訊 DSP
- 數位信號處理外掛程式，DoProcessOutput
- DSP 外掛程式，DoProcessOutput
- 音訊 DSP 外掛程式，DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68562444a3a8f0bfacad26fc5246181d33cefa2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372299"
---
# <a name="implementing-doprocessoutput"></a>執行 DoProcessOutput

若要處理音訊資料，您必須在 **DoProcessOutput** 中執行幾個步驟。 下列步驟會使用外掛程式 wizard 範例程式碼做為範例。 如果您想要建立音訊 DSP 外掛程式，以處理外掛程式嚮導範例程式碼所使用之相同類型的媒體內容，您只需要變更步驟6中所參考的實際處理常式代碼。 以下是在 **DoProcessOutput** 中執行的所有步驟：

-   如果目前未啟用外掛程式，只需將資料原封不動地複製到輸出緩衝區。 如果外掛程式將資料轉換成不同的格式，您也必須在這裡進行轉換處理。

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   取得輸入格式結構的指標。 您將需要從此結構取出成員資料，因此請複製 *m \_ mtInput* 的指標。**pbformat** 至類型的本機指標變數，此變數符合格式結構類型。 下列範例會儲存 **WAVEFORMATEX** 輸入格式結構的指標：

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   計算要處理的樣本數目。 外掛程式 wizard 產生的範例程式碼會藉由將 WAVEFORMATEX 輸入格式結構的 **nBlockAlign** 成員所處理的位元組數目相除，然後將結果乘以儲存在 **nChannels** 成員中的通道數目，來執行此步驟。 下列範例取自外掛程式 wizard 範例程式碼：

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  判斷音訊的位深度。 外掛程式 wizard 範例程式碼會檢查 **WAVEFORMATEX** 結構的 **wBitsPerSample** 成員，以決定8位或16位音訊。 然後，它會在 switch 語句中使用該值，為每個位深度提供個別的處理常式。 當您處理其他格式類型和位深度時，可能需要使用不同的技巧。
    2.  建立迴圈，以逐步執行輸入緩衝區中的音訊範例。
    3.  從輸入緩衝區取出範例。 若要這麼做，請將輸入資料指標取值，並將結果儲存在 int 類型的變數中。若是16位音訊，您必須重新轉換短指標的位元組指標，以處理較大的音訊樣本精確度。 有了值之後，您就可以立即遞增 *pbInputData* 指標，使其指向下一個範例。 下列範例示範：

    ```C++
    // For 8-bit audio.
    int i = *pbInputData++;  
    
    ```

    

    -或-

    ```C++
    // For 16-bit audio.
    // Recast the pointer.
    short *pwInputData = (short *) pbInputData; 

    // Enter the loop and then get the input sample.
    int i = *pwInputData++;
    
    ```

    

    1.  執行處理。 這是您套用以某種方式變更範例的演算法的位置。 您可以自行決定。
    2.  將處理過的資料寫入至輸出緩衝區。 立即將指標遞增至輸出緩衝區，如下列範例所示：

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  重複執行迴圈，直到處理完所有樣本為止。
    2.  傳回適當的 **HRESULT**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行音訊 DSP 外掛程式**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




