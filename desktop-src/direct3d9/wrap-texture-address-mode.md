---
description: 包裝紋理位址模式（由 \_ D3DTEXTUREADDRESS 列舉型別的 D3DTADDRESS wrap 成員識別）讓 Direct3D 在每個整數連接點上重複紋理。
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: '將材質位址模式換行 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721ace45599236022f32e6b0ec3723e346befbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187407"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a><span data-ttu-id="d223d-103">將材質位址模式換行 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="d223d-103">Wrap Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="d223d-104">包裝紋理位址模式（由 \_ [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 列舉型別的 D3DTADDRESS wrap 成員識別）讓 Direct3D 在每個整數連接點上重複紋理。</span><span class="sxs-lookup"><span data-stu-id="d223d-104">The wrap texture address mode, identified by the D3DTADDRESS\_WRAP member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, makes Direct3D repeat the texture on every integer junction.</span></span> <span data-ttu-id="d223d-105">例如：假設您的應用程式建立了一個正方形的原始物件，並且指定其四個頂點座標分別為 (0.0, 0.0)、(0.0, 3.0)、(3.0, 3.0)，及 (3.0, 0.0)。</span><span class="sxs-lookup"><span data-stu-id="d223d-105">Suppose, for example, your application creates a square primitive and specifies texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0).</span></span> <span data-ttu-id="d223d-106">將材質定址模式設定為 D3DTADDRESS，會在 \_ 兩個方向中，將材質套用三次，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="d223d-106">Setting the texture addressing mode to D3DTADDRESS\_WRAP results in the texture being applied three times in both the u-and v-directions, as shown in the following illustration.</span></span>

![在 u 及 v 方向覆蓋臉部紋理之圖例](images/wrap.png)

<span data-ttu-id="d223d-108">此材質位址模式的效果與鏡像模式的效果類似，但不同。</span><span class="sxs-lookup"><span data-stu-id="d223d-108">The effects of this texture address mode are similar to, but distinct from, those of the mirror mode.</span></span> <span data-ttu-id="d223d-109">如需詳細資訊，請參閱 [ (Direct3D 9) 的鏡像材質位址模式 ](mirror-texture-address-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="d223d-109">For more information, see [Mirror Texture Address Mode (Direct3D 9)](mirror-texture-address-mode.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d223d-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="d223d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d223d-111">材質定址模式</span><span class="sxs-lookup"><span data-stu-id="d223d-111">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
