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
# <a name="how-to-play-a-sound-with-xaudio2"></a><span data-ttu-id="3e73f-103">使用方法：使用 XAudio2 播放音效</span><span class="sxs-lookup"><span data-stu-id="3e73f-103">How to: Play a Sound with XAudio2</span></span>

<span data-ttu-id="3e73f-104">本主題說明在 XAudio2 中播放先前載入的音訊資料時所需的最少步驟。</span><span class="sxs-lookup"><span data-stu-id="3e73f-104">This topic describes the minimum steps required to play previously-loaded audio data in XAudio2.</span></span> <span data-ttu-id="3e73f-105">初始化 XAudio2 之後 (請參閱 [如何：初始化 XAudio2](how-to--initialize-xaudio2.md)) 並載入音訊資料 (請參閱如何： [如何：在 XAudio2 中載入音訊資料檔案](how-to--load-audio-data-files-in-xaudio2.md)) ，您可以建立來源語音並將音訊資料傳遞給它來播放音效。</span><span class="sxs-lookup"><span data-stu-id="3e73f-105">After you initialize XAudio2 (see [How to: Initialize XAudio2](how-to--initialize-xaudio2.md)) and load the audio data (see How to: [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), you can play a sound by creating a source voice and passing audio data to it.</span></span>

## <a name="to-play-a-sound"></a><span data-ttu-id="3e73f-106">播放音效</span><span class="sxs-lookup"><span data-stu-id="3e73f-106">To play a sound</span></span>

1.  <span data-ttu-id="3e73f-107">遵循 [如何：初始化 XAudio2](how-to--initialize-xaudio2.md)中所述的步驟，初始化 XAudio2 引擎。</span><span class="sxs-lookup"><span data-stu-id="3e73f-107">Initialize the XAudio2 engine by following the steps described in [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>
2.  <span data-ttu-id="3e73f-108">依照 how [to：在 XAUDIO2 中載入音訊資料檔案](how-to--load-audio-data-files-in-xaudio2.md)中所述的步驟，填入 [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex)和 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)結構。</span><span class="sxs-lookup"><span data-stu-id="3e73f-108">Populate a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure by following the steps described in [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="3e73f-109">根據音訊資料的格式，您可能需要使用包含 [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) 結構的較大型資料結構來取代 **WAVEFORMATEX**。</span><span class="sxs-lookup"><span data-stu-id="3e73f-109">Depending on the format of the audio data, you may need to use a larger data structure containing a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) structure in place of a **WAVEFORMATEX**.</span></span> <span data-ttu-id="3e73f-110">如需詳細資訊，請參閱 **WAVEFORMATEX** 參考頁面。</span><span class="sxs-lookup"><span data-stu-id="3e73f-110">See the **WAVEFORMATEX** reference page for more information.</span></span>

     

3.  <span data-ttu-id="3e73f-111">在 XAudio2 引擎的實例上呼叫 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) 方法，以建立來源語音。</span><span class="sxs-lookup"><span data-stu-id="3e73f-111">Create a source voice by calling the [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) method on an instance of the XAudio2 engine.</span></span> <span data-ttu-id="3e73f-112">語音的格式是以 [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) 結構中所設定的值來指定。</span><span class="sxs-lookup"><span data-stu-id="3e73f-112">The format of the voice is specified by the values set in a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) structure.</span></span>
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  <span data-ttu-id="3e73f-113">使用函式 [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer)將 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)提交至來源聲音。</span><span class="sxs-lookup"><span data-stu-id="3e73f-113">Submit an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) to the source voice using the function [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).</span></span>
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > <span data-ttu-id="3e73f-114">應用程式仍然「擁有」 *緩衝區* 點的音訊範例資料，必須維持配置並可存取，直到音效停止播放為止。</span><span class="sxs-lookup"><span data-stu-id="3e73f-114">The audio sample data to which *buffer* points is still 'owned' by the app and must remain allocated and accessible until the sound stops playing.</span></span>

     

5.  <span data-ttu-id="3e73f-115">使用 [**start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) 函數啟動來源聲音。</span><span class="sxs-lookup"><span data-stu-id="3e73f-115">Use the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function to start the source voice.</span></span> <span data-ttu-id="3e73f-116">由於所有 XAudio2 語音預設都會將其輸出傳送至「控制」聲音，因此來源語音的音訊會自動將其傳送到在初始化時選取的音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="3e73f-116">Since all XAudio2 voices send their output to the mastering voice by default, audio from the source voice automatically makes its way to the audio device selected at initialization.</span></span> <span data-ttu-id="3e73f-117">在更複雜的音訊圖形中，來源聲音必須指定要傳送其輸出的聲音。</span><span class="sxs-lookup"><span data-stu-id="3e73f-117">In a more complicated audio graph, the source voice would have to specify the voice to which its output should be sent.</span></span>
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a><span data-ttu-id="3e73f-118">Windows Store 應用程式的注意事項</span><span class="sxs-lookup"><span data-stu-id="3e73f-118">Notes for Windows Store apps</span></span>

<span data-ttu-id="3e73f-119">建議您利用 [智慧型指標](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) ，以例外狀況安全的方式來管理 XAUDIO2 物件的存留期。</span><span class="sxs-lookup"><span data-stu-id="3e73f-119">We recommend that you make use of a [smart pointer](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) to manage the lifetime of XAUDIO2 objects in an exception safe manner.</span></span> <span data-ttu-id="3e73f-120">針對 Windows Store 應用程式，您可以使用 Windows 執行階段 C++ 範本庫 (WRL) 的 [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) 智慧型指標範本。</span><span class="sxs-lookup"><span data-stu-id="3e73f-120">For Windows Store apps, you can use the [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) smart pointer template from the Windows Runtime C++ Template Library (WRL).</span></span>


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
> <span data-ttu-id="3e73f-121">在您釋放 [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) 物件之前，請確定已完全釋放 XAUDIO2 物件的所有智慧型指標。</span><span class="sxs-lookup"><span data-stu-id="3e73f-121">Ensure that all smart pointers to XAUDIO2 objects are fully released before you release the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3e73f-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e73f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e73f-123">XAudio2 開始使用</span><span class="sxs-lookup"><span data-stu-id="3e73f-123">XAudio2 Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="3e73f-124">使用方法：初始化 XAudio2</span><span class="sxs-lookup"><span data-stu-id="3e73f-124">How to: Initialize XAudio2</span></span>](how-to--initialize-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="3e73f-125">使用方法：在 XAudio2 中載入音訊資料檔</span><span class="sxs-lookup"><span data-stu-id="3e73f-125">How to: Load Audio Data Files in XAudio2</span></span>](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
