---
description: 鏡像材質位址模式（由 \_ D3DTEXTUREADDRESS 列舉型別的 D3DTADDRESS 鏡像成員所識別）會導致 Direct3D 鏡像每個整數界限的材質。
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: " (Direct3D 9) 的鏡像材質位址模式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471ad8b715d9375947162c66474687b9d6376bec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385663"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a><span data-ttu-id="5ad93-103"> (Direct3D 9) 的鏡像材質位址模式</span><span class="sxs-lookup"><span data-stu-id="5ad93-103">Mirror Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="5ad93-104">鏡像材質位址模式（由 \_ [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 列舉型別的 D3DTADDRESS 鏡像成員所識別）會導致 Direct3D 鏡像每個整數界限的材質。</span><span class="sxs-lookup"><span data-stu-id="5ad93-104">The mirror texture address mode, identified by the D3DTADDRESS\_MIRROR member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to mirror the texture at every integer boundary.</span></span> <span data-ttu-id="5ad93-105">例如：假設您的應用程式建立了一個正方形的原始物件，並且指定其四個頂點座標分別為 (0.0, 0.0)、(0.0, 3.0)、(3.0, 3.0)，及 (3.0, 0.0)。</span><span class="sxs-lookup"><span data-stu-id="5ad93-105">Suppose, for example, your application creates a square primitive and specifies texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0).</span></span> <span data-ttu-id="5ad93-106">將材質定址模式設定為 D3DTADDRESS \_ 鏡像會導致紋理在 u 和 v 方向套用三次。</span><span class="sxs-lookup"><span data-stu-id="5ad93-106">Setting the texture addressing mode to D3DTADDRESS\_MIRROR results in the texture being applied three times in both the u- and v-directions.</span></span> <span data-ttu-id="5ad93-107">每一欄與每一列套用的紋理，都是前一欄或前一列紋理的鏡映影像，如下圖例所示。</span><span class="sxs-lookup"><span data-stu-id="5ad93-107">Every other row and column that it is applied to is a mirror image of the preceding row or column, as shown in the following illustration.</span></span>

![3x3 格線中鏡映影像的圖例](images/mirror.png)

<span data-ttu-id="5ad93-109">此材質位址模式的效果類似于換行模式的結果，但不同于。</span><span class="sxs-lookup"><span data-stu-id="5ad93-109">The effects of this texture address mode are similar to, but distinct from, those of the wrap mode.</span></span> <span data-ttu-id="5ad93-110">如需詳細資訊，請參閱 [Wrap (Direct3D 9) 的材質位址模式 ](wrap-texture-address-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="5ad93-110">For more information, see [Wrap Texture Address Mode (Direct3D 9)](wrap-texture-address-mode.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ad93-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ad93-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ad93-112">材質定址模式</span><span class="sxs-lookup"><span data-stu-id="5ad93-112">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
