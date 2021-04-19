---
description: 應用程式會將混合階段與目前材質集中的每個材質產生關聯。 Direct3D 會依序評估每個混合階段，從集合中的第一個材質開始，然後以第八個材質為結尾。
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: " (Direct3D 9) 的材質混合作業和引數"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65386e01bfff7d4bfc2ebc0cafd242e25c4265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106966617"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a><span data-ttu-id="9d51a-104"> (Direct3D 9) 的材質混合作業和引數</span><span class="sxs-lookup"><span data-stu-id="9d51a-104">Texture Blending Operations and Arguments (Direct3D 9)</span></span>

<span data-ttu-id="9d51a-105">應用程式會將混合階段與目前材質集中的每個材質產生關聯。</span><span class="sxs-lookup"><span data-stu-id="9d51a-105">Applications associate a blending stage with each texture in the set of current textures.</span></span> <span data-ttu-id="9d51a-106">Direct3D 會依序評估每個混合階段，從集合中的第一個材質開始，然後以第八個材質為結尾。</span><span class="sxs-lookup"><span data-stu-id="9d51a-106">Direct3D evaluates each blending stage in order, beginning with the first texture in the set and ending with the eighth.</span></span>

<span data-ttu-id="9d51a-107">Direct3D 會將目前材質集中每個材質的資訊套用至與其相關聯的混合階段。</span><span class="sxs-lookup"><span data-stu-id="9d51a-107">Direct3D applies the information from each texture in the set of current textures to the blending stage that is associated with it.</span></span> <span data-ttu-id="9d51a-108">應用程式會藉由呼叫 [**IDirect3DDevice9：： SetTextureStageState**](/windows/desktop/api)，來控制來自材質階段的資訊。</span><span class="sxs-lookup"><span data-stu-id="9d51a-108">Applications control what information from a texture stage is used by calling [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api).</span></span> <span data-ttu-id="9d51a-109">您可以針對色彩和 Alpha 通道設定個別的作業，每個作業都使用兩個引數。</span><span class="sxs-lookup"><span data-stu-id="9d51a-109">You can set separate operations for the color and alpha channels, and each operation uses two arguments.</span></span> <span data-ttu-id="9d51a-110">使用 D3DTSS COLOROP 階段狀態指定色彩通道作業 \_ ; 使用 D3DTSS ALPHAOP 指定 Alpha 作業 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9d51a-110">Specify color channel operations by using the D3DTSS\_COLOROP stage state; specify alpha operations by using D3DTSS\_ALPHAOP.</span></span> <span data-ttu-id="9d51a-111">這兩個階段狀態會使用 [**D3DTEXTUREOP**](./d3dtextureop.md) 列舉型別中的值。</span><span class="sxs-lookup"><span data-stu-id="9d51a-111">Both stage states use values from the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span>

<span data-ttu-id="9d51a-112">紋理混合引數使用 D3DTSS \_ COLORARG1、D3DTSS \_ COLORARG2、D3DTSS \_ ALPHARG1 和 D3DTSS \_ 列舉型別的 ALPHARG2 [](./d3dtexturestagestatetype.md) D3DTEXTURESTAGESTATETYPE 成員。</span><span class="sxs-lookup"><span data-stu-id="9d51a-112">Texture blending arguments use the D3DTSS\_COLORARG1, D3DTSS\_COLORARG2, D3DTSS\_ALPHARG1, and D3DTSS\_ALPHARG2 members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type.</span></span> <span data-ttu-id="9d51a-113">您可以使用 [D3DTA](d3dta.md)來識別對應的引數值。</span><span class="sxs-lookup"><span data-stu-id="9d51a-113">The corresponding argument values are identified using [D3DTA](d3dta.md).</span></span>

> [!Note]  
> <span data-ttu-id="9d51a-114">您可以將該階段的色彩作業設定為 [D3DTOP 停用]，以停用材質階段以及任何後續的材質混合階段 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9d51a-114">You can disable a texture stage - and any subsequent texture blending stages in the cascade - by setting the color operation for that stage to D3DTOP\_DISABLE.</span></span> <span data-ttu-id="9d51a-115">停用色彩作業也會有效地停用 Alpha 運算。</span><span class="sxs-lookup"><span data-stu-id="9d51a-115">Disabling the color operation effectively disables the alpha operation as well.</span></span> <span data-ttu-id="9d51a-116">啟用色彩作業時，無法停用 Alpha 作業。</span><span class="sxs-lookup"><span data-stu-id="9d51a-116">Alpha operations cannot be disabled when color operations are enabled.</span></span> <span data-ttu-id="9d51a-117">當色彩混合啟用時，將 Alpha 作業設定為 D3DTOP \_ 停用會導致未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="9d51a-117">Setting the alpha operation to D3DTOP\_DISABLE when color blending is enabled causes undefined behavior.</span></span>

 

<span data-ttu-id="9d51a-118">若要判斷裝置支援的材質混合作業，請查詢 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 TextureCaps 成員。</span><span class="sxs-lookup"><span data-stu-id="9d51a-118">To determine the supported texture blending operations of a device, query the TextureCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d51a-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="9d51a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d51a-120">材質混色</span><span class="sxs-lookup"><span data-stu-id="9d51a-120">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
