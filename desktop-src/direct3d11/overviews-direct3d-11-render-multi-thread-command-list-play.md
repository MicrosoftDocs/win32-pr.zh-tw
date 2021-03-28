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
# <a name="how-to-play-back-a-command-list"></a>如何：播放命令清單

[命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)是轉譯命令的記錄清單。 使用命令清單預先記錄繪製命令，稍後再播放。 本主題說明如何播放 [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)。 命令清單可以用來線上程之間分割轉譯工作。

本節說明如何播放命令清單。 如需錄製命令清單，請參閱 [如何：錄製命令清單](overviews-direct3d-11-render-multi-thread-command-list-record.md)。

**播放命令清單**

-   呼叫 [**>id3d11devicecoNtext：： ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) ，並傳遞有效的 [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) 物件。
    ```
    if(g_pd3dCommandList)
    {
        g_pImmediateContext->ExecuteCommandList(g_pd3dCommandList, TRUE);
    }
    ```

    

[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) 必須在 [立即內容](overviews-direct3d-11-devices-intro.md) 上執行，才能在圖形處理單元上執行已錄製的命令 (GPU) 。 使用立即內容將命令饋送至 GPU 以進行執行，使用延遲的內容來錄製命令以播放至另一個命令清單。 當您呼叫 **ExecuteCommandList** 至另一個延遲的內容時，您會建立「合併的」延遲命令清單。 若要在合併的延後命令清單上執行命令，您必須在立即內容上執行這些命令。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




