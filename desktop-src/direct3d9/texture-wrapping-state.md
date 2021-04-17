---
description: D3DRS \_ WRAP0 到 D3DRS \_ WRAP7 轉譯狀態可針對裝置的多紋理串聯中的各種材質啟用和停用 u 和 v 換行。
ms.assetid: c584eee6-1187-4741-b3af-4bd79d93be77
title: " (Direct3D 9) 的材質換行狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cb025df6716371397d62cc730c5584e2dab862
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467866"
---
# <a name="texture-wrapping-state-direct3d-9"></a><span data-ttu-id="f9f58-103"> (Direct3D 9) 的材質換行狀態</span><span class="sxs-lookup"><span data-stu-id="f9f58-103">Texture Wrapping State (Direct3D 9)</span></span>

<span data-ttu-id="f9f58-104">D3DRS \_ WRAP0 到 D3DRS \_ WRAP7 轉譯狀態可針對裝置的多紋理串聯中的各種材質啟用和停用 u 和 v 換行。</span><span class="sxs-lookup"><span data-stu-id="f9f58-104">The D3DRS\_WRAP0 through D3DRS\_WRAP7 render states enable and disable u- and v-wrapping for various textures in the device's multitexture cascade.</span></span> <span data-ttu-id="f9f58-105">您可以將這些轉譯狀態設定為 D3DWRAPCOORD \_ 0、D3DWRAPCOORD \_ 1、D3DWRAPCOORD \_ 2 和 D3DWRAPCOORD \_ 3 旗標的組合，以啟用紋理的第一、第二、第三和第四個方向的換行。</span><span class="sxs-lookup"><span data-stu-id="f9f58-105">You can set these render states to a combination of the D3DWRAPCOORD\_0, D3DWRAPCOORD\_1, D3DWRAPCOORD\_2, and D3DWRAPCOORD\_3 flags to enable wrapping in first, second, third, and fourth directions of the texture.</span></span> <span data-ttu-id="f9f58-106">使用零值可完全停用換行。</span><span class="sxs-lookup"><span data-stu-id="f9f58-106">Use a value of zero to disable wrapping altogether.</span></span> <span data-ttu-id="f9f58-107">預設會針對所有紋理階段停用材質換行。</span><span class="sxs-lookup"><span data-stu-id="f9f58-107">Texture wrapping is disabled in all directions for all texture stages by default.</span></span>

<span data-ttu-id="f9f58-108">如需概念的總覽，請參閱 [ (Direct3D 9) 的材質包裝 ](texture-wrapping.md)。</span><span class="sxs-lookup"><span data-stu-id="f9f58-108">For a conceptual overview, see [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9f58-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="f9f58-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9f58-110">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="f9f58-110">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



