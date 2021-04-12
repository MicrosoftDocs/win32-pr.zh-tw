---
description: 當您建立深度緩衝區（如建立深度緩衝區 (Direct3D 9) 所述）之後，您可以藉由呼叫 IDirect3DDevice9：： Graphicsdevice 方法來啟用深度緩衝。
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: " (Direct3D 9) 啟用深度緩衝"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935d4f2e1db164a3aac2a39627be88d71887cc14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317547"
---
# <a name="enabling-depth-buffering-direct3d-9"></a><span data-ttu-id="071f3-103"> (Direct3D 9) 啟用深度緩衝</span><span class="sxs-lookup"><span data-stu-id="071f3-103">Enabling Depth Buffering (Direct3D 9)</span></span>

<span data-ttu-id="071f3-104">當您建立深度緩衝區（如 [建立深度緩衝區 (Direct3D 9)](creating-a-depth-buffer.md)所述）之後，您可以藉由呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/desktop/api) 方法來啟用深度緩衝。</span><span class="sxs-lookup"><span data-stu-id="071f3-104">After you create a depth buffer, as described in [Creating a Depth Buffer (Direct3D 9)](creating-a-depth-buffer.md), you enable depth buffering by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="071f3-105">設定 D3DRS \_ ZENABLE 轉譯狀態以啟用深度緩衝。</span><span class="sxs-lookup"><span data-stu-id="071f3-105">Set the D3DRS\_ZENABLE render state to enable depth-buffering.</span></span> <span data-ttu-id="071f3-106">使用 \_ [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) 列舉型別的 D3DZB TRUE 成員 (或 **TRUE**) 來啟用 z 緩衝、D3DZB \_ USEW 來啟用 w-緩衝或 D3DZB \_ false (或 **false**) 停用深度緩衝。</span><span class="sxs-lookup"><span data-stu-id="071f3-106">Use the D3DZB\_TRUE member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type (or **TRUE**) to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE (or **FALSE**) to disable depth buffering.</span></span>

> [!Note]  
> <span data-ttu-id="071f3-107">若要使用 w 緩衝，您的應用程式必須設定符合規範的投射矩陣，即使它不使用 Direct3D 轉換管線也一樣。</span><span class="sxs-lookup"><span data-stu-id="071f3-107">To use w-buffering, your application must set a compliant projection matrix even if it doesn't use the Direct3D transformation pipeline.</span></span> <span data-ttu-id="071f3-108">如需有關提供適當投射矩陣的詳細資訊，請參閱 [W 易記投射矩陣](projection-transform.md)</span><span class="sxs-lookup"><span data-stu-id="071f3-108">For information about providing an appropriate projection matrix, see [A W-Friendly Projection Matrix](projection-transform.md)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="071f3-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="071f3-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="071f3-110">深度緩衝區</span><span class="sxs-lookup"><span data-stu-id="071f3-110">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
