---
title: 如何錄製命令清單
description: 本主題說明如何建立和記錄命令清單。
ms.assetid: f5b90dfb-0b07-432e-813b-1541efbe3de5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712f48386e0625c58a1f11c122d105064477ca8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673896"
---
# <a name="how-to-record-a-command-list"></a><span data-ttu-id="a976b-103">如何：錄製命令清單</span><span class="sxs-lookup"><span data-stu-id="a976b-103">How to: Record a Command List</span></span>

<span data-ttu-id="a976b-104">[命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)是轉譯命令的記錄清單。</span><span class="sxs-lookup"><span data-stu-id="a976b-104">A [command list](overviews-direct3d-11-render-multi-thread-command-list.md) is a recorded list of rendering commands.</span></span> <span data-ttu-id="a976b-105">本主題說明如何建立和記錄 [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)。</span><span class="sxs-lookup"><span data-stu-id="a976b-105">This topic shows how to create and record a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="a976b-106">使用命令清單來錄製轉譯命令，稍後再播放。</span><span class="sxs-lookup"><span data-stu-id="a976b-106">Use a command list to record render commands and play them back later.</span></span> <span data-ttu-id="a976b-107">命令清單可方便線上程之間分割轉譯工作。</span><span class="sxs-lookup"><span data-stu-id="a976b-107">A command list is convenient for splitting rendering tasks between threads.</span></span>

<span data-ttu-id="a976b-108">**錄製命令清單**</span><span class="sxs-lookup"><span data-stu-id="a976b-108">**To record a command list**</span></span>

1.  <span data-ttu-id="a976b-109">命令清單必須從延遲的內容建立，其中包含裝置狀態和轉譯動作。</span><span class="sxs-lookup"><span data-stu-id="a976b-109">A command list must be created from a deferred context, which contains device state and rendering actions.</span></span> <span data-ttu-id="a976b-110">針對裝置，藉由呼叫 [**ID3D11Device：： CreateDeferredCoNtext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext)來建立延遲的內容。</span><span class="sxs-lookup"><span data-stu-id="a976b-110">Given a device, create a deferred context by calling [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

    ```
    HRESULT hr;
    ID3D11DeviceContext* pDeferredContext = NULL;

    hr = g_pd3dDevice->CreateDeferredContext(0, &pDeferredContext);
    ```

    

2.  <span data-ttu-id="a976b-111">使用延後的內容來呈現。</span><span class="sxs-lookup"><span data-stu-id="a976b-111">Use the deferred context to render.</span></span>

    ```
    float ClearColor[4] = { 0.0f, 0.125f, 0.3f, 1.0f };
    pDeferredContext->ClearRenderTargetView( g_pRenderTargetView, ClearColor );
        
    // Add additional rendering commands
    ...
    ```

    

    <span data-ttu-id="a976b-112">這個簡單的範例會清除轉譯目標，但您可以新增其他轉譯命令。</span><span class="sxs-lookup"><span data-stu-id="a976b-112">This simple example clears a render target, but you could add additional render commands.</span></span>

3.  <span data-ttu-id="a976b-113">藉由呼叫 [**>id3d11devicecoNtext：： FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) ，並將指標傳遞至未初始化的 [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) 介面，來建立/記錄命令清單。</span><span class="sxs-lookup"><span data-stu-id="a976b-113">Create/record a command list by calling [**ID3D11DeviceContext::FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) and passing a pointer to an uninitialized [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) interface.</span></span>

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    <span data-ttu-id="a976b-114">當方法傳回時，會建立包含所有轉譯命令的命令清單，並將介面傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="a976b-114">When the method returns, a command list is created containing all the render commands and an interface is returned to the application.</span></span>

    <span data-ttu-id="a976b-115">布林值參數會告知執行時間要如何處理延遲內容中的管線狀態。</span><span class="sxs-lookup"><span data-stu-id="a976b-115">The boolean parameter tells the runtime what to do with the pipeline state in the deferred context.</span></span> <span data-ttu-id="a976b-116">**TRUE** 表示在錄製完成時，將裝置內容的狀態還原至其前置命令清單條件， **FALSE** 表示在錄製之後不會變更狀態。</span><span class="sxs-lookup"><span data-stu-id="a976b-116">**TRUE** means restore the state of the device context to its pre-command list condition when recording is completed, **FALSE** means do not change the state after recording.</span></span> <span data-ttu-id="a976b-117">這表示裝置內容會反映命令清單中所包含的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="a976b-117">This means that the device context will reflect the state changes contained in the command list.</span></span>

<span data-ttu-id="a976b-118">若要查看播放命令清單的範例，請參閱 [如何：播放命令清單](overviews-direct3d-11-render-multi-thread-command-list-play.md)。</span><span class="sxs-lookup"><span data-stu-id="a976b-118">To see an example for playing back a command list, see [How to: Play Back a Command List](overviews-direct3d-11-render-multi-thread-command-list-play.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a976b-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="a976b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a976b-120">命令清單</span><span class="sxs-lookup"><span data-stu-id="a976b-120">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[<span data-ttu-id="a976b-121">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="a976b-121">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




