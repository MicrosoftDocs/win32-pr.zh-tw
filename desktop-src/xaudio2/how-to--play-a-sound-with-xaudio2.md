---
description: 本主題說明在 XAudio2 中播放先前載入的音訊資料時所需的最少步驟。
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: 使用方法：使用 XAudio2 播放音效
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ee2636ae9b6513dba9a479d63e0fd14be2c198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511916"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a>使用方法：使用 XAudio2 播放音效

本主題說明在 XAudio2 中播放先前載入的音訊資料時所需的最少步驟。 初始化 XAudio2 之後 (請參閱 [如何：初始化 XAudio2](how-to--initialize-xaudio2.md)) 並載入音訊資料 (請參閱如何： [如何：在 XAudio2 中載入音訊資料檔案](how-to--load-audio-data-files-in-xaudio2.md)) ，您可以建立來源語音並將音訊資料傳遞給它來播放音效。

## <a name="to-play-a-sound"></a>播放音效

1.  遵循 [如何：初始化 XAudio2](how-to--initialize-xaudio2.md)中所述的步驟，初始化 XAudio2 引擎。
2.  依照 how [to：在 XAUDIO2 中載入音訊資料檔案](how-to--load-audio-data-files-in-xaudio2.md)中所述的步驟，填入 [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex)和 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)結構。
    > [!Note]  
    > 根據音訊資料的格式，您可能需要使用包含 [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) 結構的較大型資料結構來取代 **WAVEFORMATEX**。 如需詳細資訊，請參閱 **WAVEFORMATEX** 參考頁面。

     

3.  在 XAudio2 引擎的實例上呼叫 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) 方法，以建立來源語音。 語音的格式是以 [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) 結構中所設定的值來指定。
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  使用函式 [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer)將 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)提交至來源聲音。
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > 應用程式仍然「擁有」 *緩衝區* 點的音訊範例資料，必須維持配置並可存取，直到音效停止播放為止。

     

5.  使用 [**start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) 函數啟動來源聲音。 由於所有 XAudio2 語音預設都會將其輸出傳送至「控制」聲音，因此來源語音的音訊會自動將其傳送到在初始化時選取的音訊裝置。 在更複雜的音訊圖形中，來源聲音必須指定要傳送其輸出的聲音。
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Windows Store 應用程式的注意事項

建議您利用 [智慧型指標](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) ，以例外狀況安全的方式來管理 XAUDIO2 物件的存留期。 針對 Windows Store 應用程式，您可以使用 Windows 執行階段 C++ 範本庫 (WRL) 的 [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) 智慧型指標範本。


```
Microsoft::WRL::ComPtr<IXAudio2SourceVoice> SourceVoice;
HRESULT hr;
if( FAILED(hr = pXAudio2->CreateSourceVoice( &SourceVoice, (WAVEFORMATEX*)&wfx ) ) )
    throw Platform::Exception::CreateException(hr); 

if( FAILED(hr = SourceVoice->SubmitSourceBuffer( &buffer ) ) )
    throw Platform::Exception::CreateException(hr); 

if ( FAILED(hr = SourceVoice->Start( 0 ) ) )
    throw Platform::Exception::CreateException(hr);
```



> [!Note]  
> 在您釋放 [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) 物件之前，請確定已完全釋放 XAUDIO2 物件的所有智慧型指標。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[XAudio2 開始使用](getting-started.md)
</dt> <dt>

[使用方法：初始化 XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[使用方法：在 XAudio2 中載入音訊資料檔](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
