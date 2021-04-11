---
description: 藉由建立 XAudio2 引擎的實例，並建立主控聲音，XAudio2 會針對音訊播放進行初始化。
ms.assetid: 4db2e7fc-0a87-0344-a07c-3abf2b21af32
title: 使用方法：初始化 XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a613c1ae2b7c3a7f0c55ab5349a0a605aaeb2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848207"
---
# <a name="how-to-initialize-xaudio2"></a>使用方法：初始化 XAudio2

藉由建立 XAudio2 引擎的實例，並建立主控聲音，XAudio2 會針對音訊播放進行初始化。

**若要初始化 XAudio2**

1.  請確定您已初始化 COM。 在 Windows Store 應用程式中，這是在初始化 Windows 執行階段的過程中完成的。 否則，請使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)。

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  您可以使用 [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) 函數來建立 XAudio2 引擎的實例。

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  使用 [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) 方法來建立主控語音。

    主控語音會封裝音訊裝置。 它是通過音訊圖形之所有音訊的最終目的地。

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Windows Store 應用程式的注意事項

建議您利用 [智慧型指標](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) ，以例外狀況安全的方式來管理 XAUDIO2 物件的存留期。 針對 Windows Store 應用程式，您可以使用 Windows 執行階段 C++ 範本庫 (WRL) 的 [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) 智慧型指標範本。


```C++
Microsoft::WRL::ComPtr<IXAudio2> XAudio2;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &XAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    throw Platform::Exception::CreateException(hr);

IXAudio2MasteringVoice* pMasterVoice = nullptr;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
    return hr;
```



> [!Note]  
> 釋放 [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) 物件之前，請先確定所有 XAUDIO2 的子物件都已完全釋放。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[XAudio2 開始使用](getting-started.md)
</dt> <dt>

[使用方法：在 XAudio2 中載入音訊資料檔](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[使用方法：使用 XAudio2 播放音效](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 
