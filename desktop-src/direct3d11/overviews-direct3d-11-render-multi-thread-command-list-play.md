---
title: 如何播放命令清單
description: 本主題說明如何播放命令清單。
ms.assetid: 4e6c0a98-85ff-45ca-963b-7d5c55f47195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d04df73b481adea17e1f985e2c1851039fd016a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990623"
---
# <a name="how-to-play-back-a-command-list"></a><span data-ttu-id="9ad6d-103">如何：播放命令清單</span><span class="sxs-lookup"><span data-stu-id="9ad6d-103">How to: Play Back a Command List</span></span>

<span data-ttu-id="9ad6d-104">[命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)是轉譯命令的記錄清單。</span><span class="sxs-lookup"><span data-stu-id="9ad6d-104">A [command list](overviews-direct3d-11-render-multi-thread-command-list.md) is a recorded list of rendering commands.</span></span> <span data-ttu-id="9ad6d-105">使用命令清單預先記錄繪製命令，稍後再播放。</span><span class="sxs-lookup"><span data-stu-id="9ad6d-105">Use a command list to pre-record drawing commands and play them back later.</span></span> <span data-ttu-id="9ad6d-106">本主題說明如何播放 [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)。</span><span class="sxs-lookup"><span data-stu-id="9ad6d-106">This topic shows how to play back a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="9ad6d-107">命令清單可以用來線上程之間分割轉譯工作。</span><span class="sxs-lookup"><span data-stu-id="9ad6d-107">A command list can be used to split rendering tasks between threads.</span></span>

<span data-ttu-id="9ad6d-108">本節說明如何播放命令清單。</span><span class="sxs-lookup"><span data-stu-id="9ad6d-108">This section describes how to play back a command list.</span></span> <span data-ttu-id="9ad6d-109">如需錄製命令清單，請參閱 [如何：錄製命令清單](overviews-direct3d-11-render-multi-thread-command-list-record.md)。</span><span class="sxs-lookup"><span data-stu-id="9ad6d-109">For recording a command list, see [How to: Record a Command List](overviews-direct3d-11-render-multi-thread-command-list-record.md).</span></span>

<span data-ttu-id="9ad6d-110">**播放命令清單**</span><span class="sxs-lookup"><span data-stu-id="9ad6d-110">**To play back a command list**</span></span>

-   <span data-ttu-id="9ad6d-111">呼叫 [**>id3d11devicecoNtext：： ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) ，並傳遞有效的 [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) 物件。</span><span class="sxs-lookup"><span data-stu-id="9ad6d-111">Call [**ID3D11DeviceContext::ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) and pass a valid [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) object.</span></span>
    ```
    if(g_pd3dCommandList)
    {
        g_pImmediateContext->ExecuteCommandList(g_pd3dCommandList, TRUE);
    }
    ```

    

<span data-ttu-id="9ad6d-112">[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) 必須在 [立即內容](overviews-direct3d-11-devices-intro.md) 上執行，才能在圖形處理單元上執行已錄製的命令 (GPU) 。</span><span class="sxs-lookup"><span data-stu-id="9ad6d-112">[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) must be executed on the [immediate context](overviews-direct3d-11-devices-intro.md) for recorded commands to be run on the graphics processing unit (GPU).</span></span> <span data-ttu-id="9ad6d-113">使用立即內容將命令饋送至 GPU 以進行執行，使用延遲的內容來錄製命令以播放至另一個命令清單。</span><span class="sxs-lookup"><span data-stu-id="9ad6d-113">Use the immediate context to feed commands to the GPU for execution, use a deferred context to record commands for playback onto another command list.</span></span> <span data-ttu-id="9ad6d-114">當您呼叫 **ExecuteCommandList** 至另一個延遲的內容時，您會建立「合併的」延遲命令清單。</span><span class="sxs-lookup"><span data-stu-id="9ad6d-114">When you call **ExecuteCommandList** onto another deferred context, you create a ‘merged’ deferred command list.</span></span> <span data-ttu-id="9ad6d-115">若要在合併的延後命令清單上執行命令，您必須在立即內容上執行這些命令。</span><span class="sxs-lookup"><span data-stu-id="9ad6d-115">To run the commands on the merged deferred command list, you need to execute them on the immediate context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ad6d-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ad6d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ad6d-117">命令清單</span><span class="sxs-lookup"><span data-stu-id="9ad6d-117">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[<span data-ttu-id="9ad6d-118">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="9ad6d-118">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




