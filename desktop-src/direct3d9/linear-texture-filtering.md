---
description: Direct3D 使用一種稱為雙線性篩選的線性材質篩選形式。
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: " (Direct3D 9) 的線性材質篩選"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7940bd693ec42ef4f48920a5a362fad5f5b0bf02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510143"
---
# <a name="linear-texture-filtering-direct3d-9"></a><span data-ttu-id="4b4a1-103"> (Direct3D 9) 的線性材質篩選</span><span class="sxs-lookup"><span data-stu-id="4b4a1-103">Linear Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="4b4a1-104">Direct3D 使用一種稱為雙線性篩選的線性材質篩選形式。</span><span class="sxs-lookup"><span data-stu-id="4b4a1-104">Direct3D uses a form of linear texture filtering called bilinear filtering.</span></span> <span data-ttu-id="4b4a1-105">如同 [最接近的點取樣 (Direct3D 9) ](nearest-point-sampling.md)，雙線性紋理篩選會先計算材質位址，這通常不是整數位址。</span><span class="sxs-lookup"><span data-stu-id="4b4a1-105">Like [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md), bilinear texture filtering first computes a texel address, which is usually not an integer address.</span></span> <span data-ttu-id="4b4a1-106">雙線性篩選接著會尋找其整數位址最接近計算位址的材質。</span><span class="sxs-lookup"><span data-stu-id="4b4a1-106">Bilinear filtering then finds the texel whose integer address is closest to the computed address.</span></span> <span data-ttu-id="4b4a1-107">此外，Direct3D 轉譯模組會計算材質的加權平均值，其位於下方、下方、位於最接近樣本點的左邊、右邊。</span><span class="sxs-lookup"><span data-stu-id="4b4a1-107">In addition, the Direct3D rendering module computes a weighted average of the texels that are immediately above, below, to the left of, and to the right of the nearest sample point.</span></span>

<span data-ttu-id="4b4a1-108">藉由叫用 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 方法，選取雙線性紋理篩選。</span><span class="sxs-lookup"><span data-stu-id="4b4a1-108">Select bilinear texture filtering by invoking the [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) method.</span></span> <span data-ttu-id="4b4a1-109">將第一個參數的值設定為您要選取材質篩選方法之材質 (0-7) 的整數索引編號。</span><span class="sxs-lookup"><span data-stu-id="4b4a1-109">Set the value of the first parameter to the integer index number (0-7) of the texture for which you are selecting a texture filtering method.</span></span> <span data-ttu-id="4b4a1-110">\_ \_ 針對第二個參數傳遞 D3DSAMP MAGFILTER、D3DSAMP MINFILTER 或 D3DSAMP \_ MIPFILTER，以設定放大、縮制或 mipmap 篩選。</span><span class="sxs-lookup"><span data-stu-id="4b4a1-110">Pass D3DSAMP\_MAGFILTER, D3DSAMP\_MINFILTER, or D3DSAMP\_MIPFILTER for the second parameter to set the magnification, minification, or mipmapping filter.</span></span> <span data-ttu-id="4b4a1-111">\_在第三個參數中傳遞 D3DTEXF 線性。</span><span class="sxs-lookup"><span data-stu-id="4b4a1-111">Pass D3DTEXF\_LINEAR in the third parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b4a1-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b4a1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b4a1-113">材質篩選</span><span class="sxs-lookup"><span data-stu-id="4b4a1-113">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 
