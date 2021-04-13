---
description: 您可以向 XAudio2 引擎註冊執行 IXAudio2EngineCallback 介面之類別的實例，以通知 XAudio2 用戶端程式代碼引擎事件。
ms.assetid: 006a8cb6-c24c-f7d1-9e8b-9cb2baa046c0
title: 使用方法：使用引擎回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04adec0efd0625157740488d70be7896688d1176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386267"
---
# <a name="how-to-use-engine-callbacks"></a><span data-ttu-id="d0f62-103">使用方法：使用引擎回呼</span><span class="sxs-lookup"><span data-stu-id="d0f62-103">How to: Use Engine Callbacks</span></span>

<span data-ttu-id="d0f62-104">您可以向 XAudio2 引擎註冊執行 [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) 介面之類別的實例，以通知 XAudio2 用戶端程式代碼引擎事件。</span><span class="sxs-lookup"><span data-stu-id="d0f62-104">You can notify the XAudio2 client code of engine events by registering an instance of a class implementing the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface with the XAudio2 engine.</span></span> <span data-ttu-id="d0f62-105">如此一來，XAudio2 用戶端程式代碼就能追蹤音訊處理發生的時間，以及在發生嚴重錯誤時，重新開機引擎的時機。</span><span class="sxs-lookup"><span data-stu-id="d0f62-105">This allows the XAudio2 client code to keep track of when audio processing is occurring, and when to restart the engine in the event of a critical error.</span></span>

## <a name="to-use-an-engine-callback"></a><span data-ttu-id="d0f62-106">使用引擎回呼</span><span class="sxs-lookup"><span data-stu-id="d0f62-106">To use an engine callback</span></span>

<span data-ttu-id="d0f62-107">下列步驟會註冊物件來處理引擎事件。</span><span class="sxs-lookup"><span data-stu-id="d0f62-107">The following steps register an object to handle engine events.</span></span>

1.  <span data-ttu-id="d0f62-108">建立繼承自 [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) 介面的類別。</span><span class="sxs-lookup"><span data-stu-id="d0f62-108">Create a class that inherits from the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface.</span></span>

    <span data-ttu-id="d0f62-109">[**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)的所有方法都是純虛擬的，而且必須定義。</span><span class="sxs-lookup"><span data-stu-id="d0f62-109">All methods of [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) are purely virtual and must be defined.</span></span> <span data-ttu-id="d0f62-110">在此範例中，您需要的方法是 [**IXAudio2EngineCallback：： OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror)，它會設定旗標來表示重大錯誤發生時的主要遊戲迴圈。</span><span class="sxs-lookup"><span data-stu-id="d0f62-110">The method of interest in this example is [**IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), which sets a flag to signal the main game loop that a critical error has occurred.</span></span> <span data-ttu-id="d0f62-111">其餘的方法 [**IXAudio2EngineCallback：： OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) 和 [**IXAudio2EngineCallback：： OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend)是此範例中的存根。</span><span class="sxs-lookup"><span data-stu-id="d0f62-111">The remaining methods, [**IXAudio2EngineCallback::OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) and [**IXAudio2EngineCallback::OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), are stubs in this example.</span></span>

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  <span data-ttu-id="d0f62-112">使用 [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) 來建立 XAudio2 引擎的實例。</span><span class="sxs-lookup"><span data-stu-id="d0f62-112">Use [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) to create an instance of the XAudio2 engine.</span></span>

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  <span data-ttu-id="d0f62-113">使用 [**IXAudio2：： RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) 來註冊引擎回呼。</span><span class="sxs-lookup"><span data-stu-id="d0f62-113">Use [**IXAudio2::RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) to register the engine callback.</span></span>

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  <span data-ttu-id="d0f62-114">如果您不需要引擎回呼，請呼叫 [**IXAudio2：： UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks)。</span><span class="sxs-lookup"><span data-stu-id="d0f62-114">If you don't need the engine callback any more, call [**IXAudio2::UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).</span></span>

    ```
    pXAudio2->UnregisterForCallbacks( &engineCallback );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="d0f62-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0f62-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0f62-116">回撥</span><span class="sxs-lookup"><span data-stu-id="d0f62-116">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="d0f62-117">XAudio2 回呼</span><span class="sxs-lookup"><span data-stu-id="d0f62-117">XAudio2 Callbacks</span></span>](xaudio2-callbacks.md)
</dt> <dt>

[<span data-ttu-id="d0f62-118">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="d0f62-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="d0f62-119">使用方法：建立基本音訊處理圖形</span><span class="sxs-lookup"><span data-stu-id="d0f62-119">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="d0f62-120">使用方法：從磁碟串流處理音效</span><span class="sxs-lookup"><span data-stu-id="d0f62-120">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
