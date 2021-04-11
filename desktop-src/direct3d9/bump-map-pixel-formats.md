---
description: 凹凸地圖是使用特製化像素格式的 IDirect3DTexture9 物件。
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: " (Direct3D 9) 的凹凸地圖像素格式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21bbe4a9999d875e43d33389f86b35d22c81b3bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025985"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a><span data-ttu-id="17d3e-103"> (Direct3D 9) 的凹凸地圖像素格式</span><span class="sxs-lookup"><span data-stu-id="17d3e-103">Bump Map Pixel Formats (Direct3D 9)</span></span>

<span data-ttu-id="17d3e-104">凹凸地圖是使用特製化像素格式的 [**IDirect3DTexture9**](/windows/desktop/api) 物件。</span><span class="sxs-lookup"><span data-stu-id="17d3e-104">A bump map is an [**IDirect3DTexture9**](/windows/desktop/api) object that uses a specialized pixel format.</span></span> <span data-ttu-id="17d3e-105">並不是儲存紅色、綠色和藍色色彩的元件，而是在 [放大] 地圖中的每個圖元都會儲存您和 v (D<sub>U</sub> 和<sub>D) 的</sub> 差異值，有時也會儲存亮度元件 L。這些值是由系統套用，如 (Direct3D 9 中的 [將 [對應公式 Direct3D 9) ](bump-mapping-formulas.md) 主題所述。</span><span class="sxs-lookup"><span data-stu-id="17d3e-105">Rather than storing red, green, and blue color components, each pixel in a bump map stores the delta values for u and v (D<sub>U</sub> and D<sub>V</sub>) and sometimes a luminance component, L. These values are applied by the system as described in the [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md) topic.</span></span>

<span data-ttu-id="17d3e-106">您可以藉由將格式設定為下列其中一種方式來指定 [凹凸地圖圖元] 格式： D3DFMT \_ CxV8U8、D3DFMT \_ V8U8、D3DFMT \_ L6V5U5、D3DFMT \_ X8L8V8U8、D3DFMT \_ Q8W8V8U8 或 D3DFMT \_ V16U16。</span><span class="sxs-lookup"><span data-stu-id="17d3e-106">You can specify a bump map pixel format by setting the format to one of the following: D3DFMT\_CxV8U8, D3DFMT\_V8U8, D3DFMT\_L6V5U5, D3DFMT\_X8L8V8U8, D3DFMT\_Q8W8V8U8, or D3DFMT\_V16U16.</span></span> <span data-ttu-id="17d3e-107">如需相關說明，請參閱 [D3DFORMAT](d3dformat.md)。</span><span class="sxs-lookup"><span data-stu-id="17d3e-107">For descriptions, see [D3DFORMAT](d3dformat.md).</span></span>

<span data-ttu-id="17d3e-108">圖元的 D<sub>U</sub> 和 d<sub>V</sub> 元件是帶正負號的值，範圍從-1.0 到 + 1.0。</span><span class="sxs-lookup"><span data-stu-id="17d3e-108">The D<sub>U</sub> and D<sub>V</sub> components of a pixel are signed values that range from - 1.0 to +1.0.</span></span> <span data-ttu-id="17d3e-109">使用亮度元件時，是不帶正負號的整數值，範圍介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="17d3e-109">The luminance component, when used, is an unsigned integer value that ranges from 0 to 255.</span></span>

> [!Note]  
> <span data-ttu-id="17d3e-110">在挑選「凸塊地圖圖元」格式之前，請先檢查是否支援特定的格式。</span><span class="sxs-lookup"><span data-stu-id="17d3e-110">Before picking a bump map pixel format, check if the particular format is supported.</span></span> <span data-ttu-id="17d3e-111">如需詳細資訊，請參閱 [使用 (Direct3D 9) 的 [凹凸對應 ](using-bump-mapping.md)]。</span><span class="sxs-lookup"><span data-stu-id="17d3e-111">For more information, see [Using Bump Mapping (Direct3D 9)](using-bump-mapping.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="17d3e-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="17d3e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17d3e-113">凹凸對應</span><span class="sxs-lookup"><span data-stu-id="17d3e-113">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 



