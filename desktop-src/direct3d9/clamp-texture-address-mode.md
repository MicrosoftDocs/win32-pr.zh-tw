---
description: 由 D3DTEXTUREADDRESS 列舉型別之 D3DTADDRESS 的夾具成員所識別的夾具材質位址模式， \_ 會導致 Direct3D 將您的材質座標帶到 \[ 0.0 1.0 的 \] 範圍。
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: " (Direct3D 9) 的夾具材質位址模式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153ed1f044bacaec6b87420eb7df22a2557349a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970115"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a><span data-ttu-id="29200-103"> (Direct3D 9) 的夾具材質位址模式</span><span class="sxs-lookup"><span data-stu-id="29200-103">Clamp Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="29200-104">由 D3DTEXTUREADDRESS 列舉型別之 D3DTADDRESS 的夾具成員所識別的夾具材質位址模式， \_ 會導致 Direct3D 將您的材質座標帶到[](./d3dtextureaddress.md) \[ 0.0 1.0 的 \] 範圍。</span><span class="sxs-lookup"><span data-stu-id="29200-104">The clamp texture address mode, identified by the D3DTADDRESS\_CLAMP member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to clamp your texture coordinates to the \[0.0, 1.0\] range.</span></span> <span data-ttu-id="29200-105">也就是說，它會套用紋理一次，然後 smears 邊緣圖元的色彩。</span><span class="sxs-lookup"><span data-stu-id="29200-105">That is, it applies the texture once, then smears the color of edge pixels.</span></span> <span data-ttu-id="29200-106">例如，假設您的應用程式會建立一個平方根，並將 (0.0、0.0) 、 (0.0、3.0) 、 (3.0、3.0) 和 (3.0、0.0) 的材質座標指派給基本頂點。</span><span class="sxs-lookup"><span data-stu-id="29200-106">For example, suppose that your application creates a square primitive and assigns texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0) to the primitive's vertices.</span></span> <span data-ttu-id="29200-107">將材質定址模式設定為 D3DTADDRESS \_ 的夾具會導致紋理套用一次。</span><span class="sxs-lookup"><span data-stu-id="29200-107">Setting the texture addressing mode to D3DTADDRESS\_CLAMP results in the texture being applied once.</span></span> <span data-ttu-id="29200-108">在欄頂端及列末端的像素色彩會分別延伸至原始物件的頂端及右端。</span><span class="sxs-lookup"><span data-stu-id="29200-108">The pixel colors at the top of the columns and the end of the rows are extended to the top and right of the primitive respectively.</span></span>

<span data-ttu-id="29200-109">以下圖例為一個鉗位紋理。</span><span class="sxs-lookup"><span data-stu-id="29200-109">The following illustration shows a clamped texture.</span></span>

![紋理及鉗位紋理的圖例](images/clamp.png)

## <a name="related-topics"></a><span data-ttu-id="29200-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="29200-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29200-112">材質定址模式</span><span class="sxs-lookup"><span data-stu-id="29200-112">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
