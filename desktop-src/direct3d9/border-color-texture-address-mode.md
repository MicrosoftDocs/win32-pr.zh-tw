---
description: 框線色彩材質位址模式（由 \_ D3DTEXTUREADDRESS 列舉型別的 D3DTADDRESS border 成員識別）會導致 Direct3D 針對0.0 到1.0 （含）範圍以外的任何材質座標，使用任意色彩（稱為框線色彩）。
ms.assetid: 689dbda1-0692-411d-9727-2fdf1df960ec
title: " (Direct3D 9) 的框線色彩材質位址模式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b42b18d88f3b9305d0602e43a9528357a9397d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385978"
---
# <a name="border-color-texture-address-mode-direct3d-9"></a><span data-ttu-id="1a159-103"> (Direct3D 9) 的框線色彩材質位址模式</span><span class="sxs-lookup"><span data-stu-id="1a159-103">Border Color Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="1a159-104">框線色彩材質位址模式（由 \_ [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 列舉型別的 D3DTADDRESS border 成員識別）會導致 Direct3D 針對0.0 到1.0 （含）範圍以外的任何材質座標，使用任意色彩（稱為框線色彩）。</span><span class="sxs-lookup"><span data-stu-id="1a159-104">The border color texture address mode, identified by the D3DTADDRESS\_BORDER member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to use an arbitrary color, known as the border color, for any texture coordinates outside the range of 0.0 through 1.0, inclusive.</span></span>

<span data-ttu-id="1a159-105">在以下圖例中，應用程式指定紋理使用紅色的邊框並套用至原始物件。</span><span class="sxs-lookup"><span data-stu-id="1a159-105">In the following illustration, the application specifies that the texture be applied to the primitive using a red border.</span></span>

![紋理及紅色邊框紋理的圖例](images/border.png)

<span data-ttu-id="1a159-107">應用程式會藉由呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)來設定框線色彩。</span><span class="sxs-lookup"><span data-stu-id="1a159-107">Applications set the border color by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="1a159-108">將呼叫的第一個參數設定為所需的材質階段識別碼、將第二個參數設定為 [D3DSAMP] 的 [顏色組合] \_ 階段狀態值，以及將第三個參數設定為新的 RGBA 框線色彩。</span><span class="sxs-lookup"><span data-stu-id="1a159-108">Set the first parameter for the call to the desired texture stage identifier, the second parameter to the D3DSAMP\_BORDERCOLOR stage state value, and the third parameter to the new RGBA border color.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a159-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="1a159-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a159-110">材質定址模式</span><span class="sxs-lookup"><span data-stu-id="1a159-110">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
