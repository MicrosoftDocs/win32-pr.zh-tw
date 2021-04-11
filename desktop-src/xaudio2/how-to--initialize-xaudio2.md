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
# <a name="how-to-initialize-xaudio2"></a><span data-ttu-id="cac56-103">使用方法：初始化 XAudio2</span><span class="sxs-lookup"><span data-stu-id="cac56-103">How to: Initialize XAudio2</span></span>

<span data-ttu-id="cac56-104">藉由建立 XAudio2 引擎的實例，並建立主控聲音，XAudio2 會針對音訊播放進行初始化。</span><span class="sxs-lookup"><span data-stu-id="cac56-104">XAudio2 is initialized for audio playback by creating an instance of the XAudio2 engine, and creating a mastering voice.</span></span>

<span data-ttu-id="cac56-105">**若要初始化 XAudio2**</span><span class="sxs-lookup"><span data-stu-id="cac56-105">**To initialize XAudio2**</span></span>

1.  <span data-ttu-id="cac56-106">請確定您已初始化 COM。</span><span class="sxs-lookup"><span data-stu-id="cac56-106">Make sure you have initialized COM.</span></span> <span data-ttu-id="cac56-107">在 Windows Store 應用程式中，這是在初始化 Windows 執行階段的過程中完成的。</span><span class="sxs-lookup"><span data-stu-id="cac56-107">For a Windows Store app, this is done as part of initializing the Windows Runtime.</span></span> <span data-ttu-id="cac56-108">否則，請使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)。</span><span class="sxs-lookup"><span data-stu-id="cac56-108">Otherwise, use [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  <span data-ttu-id="cac56-109">您可以使用 [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) 函數來建立 XAudio2 引擎的實例。</span><span class="sxs-lookup"><span data-stu-id="cac56-109">Use the [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) function to create an instance of the XAudio2 engine.</span></span>

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  <span data-ttu-id="cac56-110">使用 [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) 方法來建立主控語音。</span><span class="sxs-lookup"><span data-stu-id="cac56-110">Use the [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) method to create a mastering voice.</span></span>

    <span data-ttu-id="cac56-111">主控語音會封裝音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="cac56-111">The mastering voices encapsulates an audio device.</span></span> <span data-ttu-id="cac56-112">它是通過音訊圖形之所有音訊的最終目的地。</span><span class="sxs-lookup"><span data-stu-id="cac56-112">It is the ultimate destination for all audio that passes through an audio graph.</span></span>

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a><span data-ttu-id="cac56-113">Windows Store 應用程式的注意事項</span><span class="sxs-lookup"><span data-stu-id="cac56-113">Notes for Windows Store apps</span></span>

<span data-ttu-id="cac56-114">建議您利用 [智慧型指標](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) ，以例外狀況安全的方式來管理 XAUDIO2 物件的存留期。</span><span class="sxs-lookup"><span data-stu-id="cac56-114">We recommend that you make use of a [smart pointer](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) to manage the lifetime of XAUDIO2 objects in an exception safe manner.</span></span> <span data-ttu-id="cac56-115">針對 Windows Store 應用程式，您可以使用 Windows 執行階段 C++ 範本庫 (WRL) 的 [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) 智慧型指標範本。</span><span class="sxs-lookup"><span data-stu-id="cac56-115">For Windows Store apps, you can use the [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) smart pointer template from the Windows Runtime C++ Template Library (WRL).</span></span>


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
> <span data-ttu-id="cac56-116">釋放 [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) 物件之前，請先確定所有 XAUDIO2 的子物件都已完全釋放。</span><span class="sxs-lookup"><span data-stu-id="cac56-116">Ensure that all XAUDIO2 child objects are fully released before you release the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cac56-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="cac56-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cac56-118">XAudio2 開始使用</span><span class="sxs-lookup"><span data-stu-id="cac56-118">XAudio2 Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="cac56-119">使用方法：在 XAudio2 中載入音訊資料檔</span><span class="sxs-lookup"><span data-stu-id="cac56-119">How to: Load Audio Data Files in XAudio2</span></span>](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="cac56-120">使用方法：使用 XAudio2 播放音效</span><span class="sxs-lookup"><span data-stu-id="cac56-120">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 
