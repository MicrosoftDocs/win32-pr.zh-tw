---
description: 混合階段是一組定義紋理混合方式的紋理作業及其引數。
ms.assetid: 7f9e3041-a270-44a9-a8e1-bca5ea25a71e
title: " (Direct3D 9) 建立混合階段"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f5029d540433b22b1380435dd8092546917338
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110765"
---
# <a name="creating-blending-stages-direct3d-9"></a><span data-ttu-id="bb0ca-103"> (Direct3D 9) 建立混合階段</span><span class="sxs-lookup"><span data-stu-id="bb0ca-103">Creating Blending Stages (Direct3D 9)</span></span>

<span data-ttu-id="bb0ca-104">混合階段是一組定義紋理混合方式的紋理作業及其引數。</span><span class="sxs-lookup"><span data-stu-id="bb0ca-104">A blending stage is a set of texture operations and their arguments that define how textures are blended.</span></span> <span data-ttu-id="bb0ca-105">製作混合階段時，c + + 應用程式會叫用 [**IDirect3DDevice9：： SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) 方法。</span><span class="sxs-lookup"><span data-stu-id="bb0ca-105">When making a blending stage, C++ applications invoke the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span> <span data-ttu-id="bb0ca-106">第一個呼叫會指定執行的操作。</span><span class="sxs-lookup"><span data-stu-id="bb0ca-106">The first call specifies the operation that is performed.</span></span> <span data-ttu-id="bb0ca-107">另外兩個調用會定義套用作業的引數。</span><span class="sxs-lookup"><span data-stu-id="bb0ca-107">Two additional invocations define the arguments to which the operation is applied.</span></span> <span data-ttu-id="bb0ca-108">下列程式碼範例說明如何建立混合階段。</span><span class="sxs-lookup"><span data-stu-id="bb0ca-108">The following code example illustrates the creation of a blending stage.</span></span>


```
// This example assumes that lpD3DDev is a valid pointer to an
// IDirect3DDevice9 interface.

// Set the operation for the first texture.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_ADD);

// Set argument 1 to the texture color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);

// Set argument 2 to the iterated diffuse color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
```



<span data-ttu-id="bb0ca-109">材質中的材質資料包含色彩和 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="bb0ca-109">Texel data in textures contain color and alpha values.</span></span> <span data-ttu-id="bb0ca-110">應用程式可以在單一混色階段中定義色彩和 Alpha 值的個別作業。</span><span class="sxs-lookup"><span data-stu-id="bb0ca-110">Applications can define separate operations for both color and alpha values in a single blending stage.</span></span> <span data-ttu-id="bb0ca-111">每個運算、色彩和 Alpha 都有自己的引數。</span><span class="sxs-lookup"><span data-stu-id="bb0ca-111">Each operation, color, and alpha, has its own arguments.</span></span> <span data-ttu-id="bb0ca-112">如需詳細資訊，請參閱 [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)。</span><span class="sxs-lookup"><span data-stu-id="bb0ca-112">For details, see [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span></span>

<span data-ttu-id="bb0ca-113">雖然不是 Direct3D API 的一部分，但是您可以在應用程式中插入下列宏，以簡化建立紋理混合階段所需的程式碼。</span><span class="sxs-lookup"><span data-stu-id="bb0ca-113">Although not part of the Direct3D API, you can insert the following macros into your application to abbreviate the code required for creating texture blending stages.</span></span>


```
#define SetTextureColorStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_COLOROP, op);      \
    dev->SetTextureStageState( i, D3DTSS_COLORARG1, arg1 ); \
    dev->SetTextureStageState( i, D3DTSS_COLORARG2, arg2 );

#define SetTextureAlphaStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_ALPHAOP, op);      \
    dev->SetTextureStageState( i, D3DTSS_ALPHAARG1, arg1 );  \
    dev->SetTextureStageState( i  D3DTSS_ALPHAARG2, arg2 );
```



## <a name="related-topics"></a><span data-ttu-id="bb0ca-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb0ca-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb0ca-115">材質混色</span><span class="sxs-lookup"><span data-stu-id="bb0ca-115">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
