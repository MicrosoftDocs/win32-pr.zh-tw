---
description: 啟用 XAudio2 以播放音訊資料的最低需求是音訊處理圖形，它是由單一的控制語音和單一來源語音所構成。
ms.assetid: 40f79959-23c9-4513-363b-2f2fc85e4c0a
title: 使用方法：建立基本音訊處理圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a11601514e3bcad5536ed1a8599178bcc52aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988278"
---
# <a name="how-to-build-a-basic-audio-processing-graph"></a>使用方法：建立基本音訊處理圖形

啟用 XAudio2 以播放音訊資料的最低需求是音訊處理圖形，它是由單一的控制語音和單一來源語音所構成。

## <a name="to-build-a-basic-audio-processing-graph"></a>建立基本音訊處理圖形

1.  遵循 [如何：初始化 XAudio2](how-to--initialize-xaudio2.md)中所述的步驟，初始化 XAudio2 引擎。
2.  依照 how [to：在 XAUDIO2 中載入音訊資料檔案](how-to--load-audio-data-files-in-xaudio2.md)中所述的步驟，填入 **WAVEFORMATEX** 和 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)結構。
3.  使用 [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) 函數建立來源語音。

    當您針對 [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)的 pSendList 引數指定 Null 時，來源語音的輸出會移至在步驟1中建立的「控制」聲音。

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    完成此步驟之後，會有一個簡單的音訊圖表，其中包含來源語音、主控語音和音訊裝置。 此「作法」主題中的其餘步驟會示範如何啟動流經圖形的音訊資料。

    簡單的音訊圖形

    ![簡單的音訊圖形。](images/xaudio2-audio-graph.png)

4.  使用函式 [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) 提交 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) 至來源聲音。

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  使用 [**start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) 函數啟動來源聲音。

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊圖形](audio-graphs.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> </dl>

 

 
