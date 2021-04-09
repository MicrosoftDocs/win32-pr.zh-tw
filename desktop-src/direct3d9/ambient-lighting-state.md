---
description: 環境光源的周圍是從所有方向 radiates 的光源。 如需 Direct3D 如何使用環境光線的詳細資訊，請參閱 (Direct3D 9) 的數學運算。
ms.assetid: c5aa493e-09b8-433c-a21c-e39af795b3c9
title: '環境光源狀態 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bd604941961f5b4abdb301d5c23efba9980791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111120"
---
# <a name="ambient-lighting-state-direct3d-9"></a><span data-ttu-id="55740-104">環境光源狀態 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="55740-104">Ambient Lighting State (Direct3D 9)</span></span>

<span data-ttu-id="55740-105">環境光源的周圍是從所有方向 radiates 的光源。</span><span class="sxs-lookup"><span data-stu-id="55740-105">Ambient light is surrounding light that radiates from all directions.</span></span> <span data-ttu-id="55740-106">如需 Direct3D 如何使用環境光線的詳細資訊，請參閱 [ (Direct3D 9) 的數學 ](mathematics-of-lighting.md)運算。</span><span class="sxs-lookup"><span data-stu-id="55740-106">For information about how Direct3D uses ambient light, see [Mathematics of Lighting (Direct3D 9)](mathematics-of-lighting.md).</span></span>

<span data-ttu-id="55740-107">C + + 應用程式藉由叫用 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法，並將列舉值 D3DRS \_ 環境傳遞為第一個參數，來設定環境光源的色彩。</span><span class="sxs-lookup"><span data-stu-id="55740-107">A C++ application sets the color of ambient lighting by invoking the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method and passing the enumerated value D3DRS\_AMBIENT as the first parameter.</span></span> <span data-ttu-id="55740-108">第二個參數是色彩值。</span><span class="sxs-lookup"><span data-stu-id="55740-108">The second parameter is a color value.</span></span> <span data-ttu-id="55740-109">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="55740-109">The default value is zero.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the ambient light.

d3dDevice->SetRenderState(D3DRS_AMBIENT, 0x00202020);
```



## <a name="related-topics"></a><span data-ttu-id="55740-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="55740-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55740-111">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="55740-111">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
