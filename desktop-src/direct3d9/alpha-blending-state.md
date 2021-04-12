---
description: 色彩的 Alpha 值會控制其透明度。 啟用 Alpha 混色可將介面上的色彩、材質和材質混合成另一個表面的透明度。
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: " (Direct3D 9) 的 Alpha 混色狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884ecad07fb9aefba08a0abbab92969937ec6361
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385956"
---
# <a name="alpha-blending-state-direct3d-9"></a><span data-ttu-id="1a127-104"> (Direct3D 9) 的 Alpha 混色狀態</span><span class="sxs-lookup"><span data-stu-id="1a127-104">Alpha Blending State (Direct3D 9)</span></span>

<span data-ttu-id="1a127-105">色彩的 Alpha 值會控制其透明度。</span><span class="sxs-lookup"><span data-stu-id="1a127-105">The alpha value of a color controls its transparency.</span></span> <span data-ttu-id="1a127-106">啟用 Alpha 混色可將介面上的色彩、材質和材質混合成另一個表面的透明度。</span><span class="sxs-lookup"><span data-stu-id="1a127-106">Enabling alpha blending allows colors, materials, and textures on a surface to be blended with transparency onto another surface.</span></span>

<span data-ttu-id="1a127-107">如需詳細資訊，請參閱 [ (direct3d 9 的 Alpha 材質混合) ](alpha-texture-blending.md) 和 [材質混合 (direct3d 9) ](texture-blending.md)。</span><span class="sxs-lookup"><span data-stu-id="1a127-107">For more information, see [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) and [Texture Blending (Direct3D 9)](texture-blending.md).</span></span>

<span data-ttu-id="1a127-108">以 c + + 撰寫的應用程式會使用 [**D3DRS \_ ALPHABLENDENABLE**](./d3drenderstatetype.md) 轉譯狀態來啟用 Alpha 透明度混合。</span><span class="sxs-lookup"><span data-stu-id="1a127-108">Applications written in C++ use the [**D3DRS\_ALPHABLENDENABLE**](./d3drenderstatetype.md) render state to enable alpha transparency blending.</span></span> <span data-ttu-id="1a127-109">Direct3D API 允許多種類型的 Alpha 混色。</span><span class="sxs-lookup"><span data-stu-id="1a127-109">The Direct3D API allows many types of alpha blending.</span></span> <span data-ttu-id="1a127-110">不過，請務必注意，使用者的3D 硬體可能不支援 Direct3D 所允許的所有混合狀態。</span><span class="sxs-lookup"><span data-stu-id="1a127-110">However, it is important to note the user's 3D hardware might not support all the blending states allowed by Direct3D.</span></span>

<span data-ttu-id="1a127-111">完成的 Alpha 混色類型取決於 [**D3DRS \_ SRCBLEND**](./d3drenderstatetype.md) 和 **D3DRS \_ DESTBLEND** 轉譯狀態。</span><span class="sxs-lookup"><span data-stu-id="1a127-111">The type of alpha blending that is done depends on the [**D3DRS\_SRCBLEND**](./d3drenderstatetype.md) And **D3DRS\_DESTBLEND** render states.</span></span> <span data-ttu-id="1a127-112">來源和目的地 blend 狀態會成對使用。</span><span class="sxs-lookup"><span data-stu-id="1a127-112">Source and destination blend states are used in pairs.</span></span> <span data-ttu-id="1a127-113">下列程式碼範例示範如何將來源 blend 狀態設定為 D3DBLEND \_ SRCCOLOR，並將目的地 blend 狀態設定為 D3DBLEND \_ INVSRCCOLOR。</span><span class="sxs-lookup"><span data-stu-id="1a127-113">The following code example demonstrates how the source blend state is set to D3DBLEND\_SRCCOLOR and the destination blend state is set to D3DBLEND\_INVSRCCOLOR.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



<span data-ttu-id="1a127-114">改變來源和目的地 blend 狀態可提供霧或塵封大氣中放射物件的外觀。</span><span class="sxs-lookup"><span data-stu-id="1a127-114">Altering the source and destination blend states can give the appearance of emissive objects in a foggy or dusty atmosphere.</span></span> <span data-ttu-id="1a127-115">比方說，如果您的應用程式模型點火、強制欄位、等離子字形狀或類似的 radiant 物件在霧環境中，請將來源和目的地 blend 狀態設定為 D3DBLEND \_ 一。</span><span class="sxs-lookup"><span data-stu-id="1a127-115">For instance, if your application models flames, force fields, plasma beams, or similarly radiant objects in a foggy environment, set the source and destination blend states to D3DBLEND\_ONE.</span></span>

<span data-ttu-id="1a127-116">Alpha 混合的另一個應用是在3D 場景中控制光源，也稱為「光線對應」。</span><span class="sxs-lookup"><span data-stu-id="1a127-116">Another application of alpha blending is to control the lighting in a 3D scene, also called light mapping.</span></span> <span data-ttu-id="1a127-117">將 [來源 blend 狀態] 設定為 [D3DBLEND \_ 0]，並將 [目的地 blend 狀態] 設定為 [D3DBLEND SRCALPHA] 會 \_ 根據來源 Alpha 資訊來變暗場景。</span><span class="sxs-lookup"><span data-stu-id="1a127-117">Setting the source blend state to D3DBLEND\_ZERO and the destination blend state to D3DBLEND\_SRCALPHA darkens a scene according to the source alpha information.</span></span> <span data-ttu-id="1a127-118">來源基本型別會用來做為淺色地圖，以調整框架緩衝區的內容，並在適當時將它變得更簡。</span><span class="sxs-lookup"><span data-stu-id="1a127-118">The source primitive is used as a light map that scales the contents of the frame buffer to darken it when appropriate.</span></span> <span data-ttu-id="1a127-119">這會產生單色燈光對應。</span><span class="sxs-lookup"><span data-stu-id="1a127-119">This produces monochrome light mapping.</span></span>

<span data-ttu-id="1a127-120">您可以藉由將來源 Alpha 混色狀態設為 D3DBLEND \_ 0，並將目的地 blend 狀態設定為 D3DBLEND SRCCOLOR，來達到色燈對應 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1a127-120">You can achieve color light mapping by setting the source alpha blending state to D3DBLEND\_ZERO and the destination blend state to D3DBLEND\_SRCCOLOR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a127-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="1a127-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a127-122">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="1a127-122">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
