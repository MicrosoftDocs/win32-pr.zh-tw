---
description: Direct3D 應用程式可透過在多個轉譯階段套用各種紋理到基本類型，達到多項特效。
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Multipass (Direct3D 9) 的材質混合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0a042088694f686003a6dc259cf1d914db2b59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109149"
---
# <a name="multipass-texture-blending-direct3d-9"></a><span data-ttu-id="115ee-103">Multipass (Direct3D 9) 的材質混合</span><span class="sxs-lookup"><span data-stu-id="115ee-103">Multipass Texture Blending (Direct3D 9)</span></span>

<span data-ttu-id="115ee-104">Direct3D 應用程式可透過在多個轉譯階段套用各種紋理到基本類型，達到多項特效。</span><span class="sxs-lookup"><span data-stu-id="115ee-104">Direct3D applications can achieve numerous special effects by applying various textures to a primitive over the course of multiple rendering passes.</span></span> <span data-ttu-id="115ee-105">針對此一行動的常用字詞為多階段紋理混色。</span><span class="sxs-lookup"><span data-stu-id="115ee-105">The common term for this is multipass texture blending.</span></span> <span data-ttu-id="115ee-106">多重紋理混合的一般用途為藉由套用數種不同紋理的多重色彩，模擬複雜光源和著色模型的效果。</span><span class="sxs-lookup"><span data-stu-id="115ee-106">A typical use for multipass texture blending is to emulate the effects of complex lighting and shading models by applying multiple colors from several different textures.</span></span> <span data-ttu-id="115ee-107">這類應用方式稱為光線對應。</span><span class="sxs-lookup"><span data-stu-id="115ee-107">One such application is called light mapping.</span></span> <span data-ttu-id="115ee-108">如需詳細資訊，請參閱 [ (Direct3D 9) 的材質燈光對應 ](light-mapping-with-textures.md)。</span><span class="sxs-lookup"><span data-stu-id="115ee-108">For more information, see [Light Mapping with Textures (Direct3D 9)](light-mapping-with-textures.md).</span></span>

> [!Note]  
> <span data-ttu-id="115ee-109">某些裝置能夠在單一階段中將多個紋理套用至基本專案。</span><span class="sxs-lookup"><span data-stu-id="115ee-109">Some devices are capable of applying multiple textures to primitives in a single pass.</span></span> <span data-ttu-id="115ee-110">如需詳細資訊，請參閱 [ (Direct3D 9) 的材質混色 ](texture-blending.md)。</span><span class="sxs-lookup"><span data-stu-id="115ee-110">For details, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span>

 

<span data-ttu-id="115ee-111">如果使用者的硬體不支援多重紋理混合，您的應用程式可以使用多重紋理混合來達到相同的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="115ee-111">If the user's hardware does not support multiple texture blending, your application can use multipass texture blending to achieve the same visual effects.</span></span> <span data-ttu-id="115ee-112">不過，當使用多重紋理混合時，應用程式無法維持可行的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="115ee-112">However, the application cannot sustain the frame rates that are possible when using multiple texture blending.</span></span>

<span data-ttu-id="115ee-113">在 C/c + + 應用程式中執行 multipass 材質混色。</span><span class="sxs-lookup"><span data-stu-id="115ee-113">To perform multipass texture blending in a C/C++ application.</span></span>

1.  <span data-ttu-id="115ee-114">藉由呼叫 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 方法，設定材質階段0中的材質。</span><span class="sxs-lookup"><span data-stu-id="115ee-114">Set a texture in texture stage 0 by calling the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span>
2.  <span data-ttu-id="115ee-115">使用 [**IDirect3DDevice9：： SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) 方法，選取想要的色彩和 Alpha 混合引數和作業。</span><span class="sxs-lookup"><span data-stu-id="115ee-115">Select the desired color and alpha blending arguments and operations with the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span> <span data-ttu-id="115ee-116">預設值適用於多重紋理混合。</span><span class="sxs-lookup"><span data-stu-id="115ee-116">The default settings are well-suited for multipass texture blending.</span></span>
3.  <span data-ttu-id="115ee-117">在場景中呈現適當物件。</span><span class="sxs-lookup"><span data-stu-id="115ee-117">Render the appropriate objects in the scene.</span></span>
4.  <span data-ttu-id="115ee-118">在紋理階段 0 設定下一個紋理。</span><span class="sxs-lookup"><span data-stu-id="115ee-118">Set the next texture in texture stage 0.</span></span>
5.  <span data-ttu-id="115ee-119">設定 D3DRS \_ SRCBLEND 和 D3DRS \_ DESTBLEND 轉譯狀態，以視需要調整來源和目的地混合因素。</span><span class="sxs-lookup"><span data-stu-id="115ee-119">Set the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states to adjust the source and destination blending factors as needed.</span></span> <span data-ttu-id="115ee-120">系統根據這些參數，在呈現目標表面中混合新紋理與現有像素。</span><span class="sxs-lookup"><span data-stu-id="115ee-120">The system blends the new textures with the existing pixels in the render-target surface according to these parameters.</span></span>
6.  <span data-ttu-id="115ee-121">視需要盡量使用紋理重複步驟 3、4 及 5。</span><span class="sxs-lookup"><span data-stu-id="115ee-121">Repeat Steps 3, 4, and 5 with as many textures as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="115ee-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="115ee-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="115ee-123">材質混色</span><span class="sxs-lookup"><span data-stu-id="115ee-123">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
