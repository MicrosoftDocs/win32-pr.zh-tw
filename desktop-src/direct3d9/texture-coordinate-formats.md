---
description: Direct3D 中的材質座標可以包含一個、兩個、三個或四個浮點數元素，以處理具有不同維度層級的材質。
ms.assetid: d841af62-41b0-4b80-960b-4630b9a7210c
title: " (Direct3D 9) 的材質座標格式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c95eada1cf21f0a4db38589794b08b88023e72d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688484"
---
# <a name="texture-coordinate-formats-direct3d-9"></a><span data-ttu-id="64fb4-103"> (Direct3D 9) 的材質座標格式</span><span class="sxs-lookup"><span data-stu-id="64fb4-103">Texture Coordinate Formats (Direct3D 9)</span></span>

<span data-ttu-id="64fb4-104">Direct3D 中的材質座標可以包含一個、兩個、三個或四個浮點數元素，以處理具有不同維度層級的材質。</span><span class="sxs-lookup"><span data-stu-id="64fb4-104">Texture coordinates in Direct3D can include one, two, three, or four floating point elements to address textures with varying levels of dimension.</span></span> <span data-ttu-id="64fb4-105">一維材質-維度為1到 n 材質的材質介面，由一個材質座標定址。</span><span class="sxs-lookup"><span data-stu-id="64fb4-105">A 1D texture - a texture surface with dimensions of 1-by-n texels - is addressed by one texture coordinate.</span></span> <span data-ttu-id="64fb4-106">最常見的案例（2D 材質）會使用兩個材質座標（通常稱為您和 v）來定址。</span><span class="sxs-lookup"><span data-stu-id="64fb4-106">The most common case, 2D textures, are addressed with two texture coordinates commonly called u and v.</span></span> <span data-ttu-id="64fb4-107">Direct3D 支援兩種類型的3D 紋理：三層環境對應和磁片區紋理。</span><span class="sxs-lookup"><span data-stu-id="64fb4-107">Direct3D supports two types of 3D textures, cubic-environment maps and volume textures.</span></span> <span data-ttu-id="64fb4-108">三種環境對應不是真正的3D，但會使用3個元素的向量定址。</span><span class="sxs-lookup"><span data-stu-id="64fb4-108">Cubic environment maps aren't truly 3D, but they are addressed with a 3-element vector.</span></span> <span data-ttu-id="64fb4-109">如需詳細資訊，請參閱 [ (Direct3D 9) 的三次環境對應 ](cubic-environment-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="64fb4-109">For details, see [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>

<span data-ttu-id="64fb4-110">如 [ (Direct3D 9) 的固定 ](fixed-function-fvf-codes.md)函式 FVF 程式碼中所述，應用程式會以頂點格式來編碼材質座標。</span><span class="sxs-lookup"><span data-stu-id="64fb4-110">As described in [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md), applications encode texture coordinates in the vertex format.</span></span> <span data-ttu-id="64fb4-111">頂點格式可包含多組材質座標。</span><span class="sxs-lookup"><span data-stu-id="64fb4-111">The vertex format can include multiple sets of texture coordinates.</span></span> <span data-ttu-id="64fb4-112">您可以使用 D3DFVF \_ TEX0，透過 D3DFVF \_ TEX8 [D3DFVF](d3dfvf.md) 來描述不含材質座標或最多8個集合的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="64fb4-112">Use the D3DFVF\_TEX0 through D3DFVF\_TEX8 [D3DFVF](d3dfvf.md) to describe a vertex format that includes no texture coordinates, or as many as eight sets.</span></span>

<span data-ttu-id="64fb4-113">每個材質座標集可以有一到四個元素。</span><span class="sxs-lookup"><span data-stu-id="64fb4-113">Each texture coordinate set can have between one and four elements.</span></span> <span data-ttu-id="64fb4-114">D3DFVF \_ TEXTUREFORMAT1 到 D3DFVF \_ TEXTUREFORMAT4 旗標描述了集合中紋理座標內的元素數目，但這些旗標並不會單獨使用。</span><span class="sxs-lookup"><span data-stu-id="64fb4-114">The D3DFVF\_TEXTUREFORMAT1 through D3DFVF\_TEXTUREFORMAT4 flags describe the number of elements in a texture coordinate in a set, but these flags aren't used by themselves.</span></span> <span data-ttu-id="64fb4-115">相反地， [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) 的巨集群組會使用這些旗標來建立位模式，以描述頂點格式的特定材質座標集合所使用的專案數目。</span><span class="sxs-lookup"><span data-stu-id="64fb4-115">Rather, the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros use these flags to create bit patterns that describe the number of elements used by a particular set of texture coordinates in the vertex format.</span></span> <span data-ttu-id="64fb4-116">這些宏會接受單一參數，以識別要定義其元素數目之座標集的索引。</span><span class="sxs-lookup"><span data-stu-id="64fb4-116">These macros accept a single parameter that identifies the index of the coordinate set whose number of elements is being defined.</span></span> <span data-ttu-id="64fb4-117">下列範例說明如何使用這些宏。</span><span class="sxs-lookup"><span data-stu-id="64fb4-117">The following example illustrates how these macros are used.</span></span>


```
// This vertex format contains two sets of texture coordinates.
// The first set (index 0) has 2 elements, and the second set 
// has 1 element. The description for this vertex format would be: 
//     dwFVF = D3DFVF_XYZ  | D3DFVF_NORMAL | D3DFVF_DIFFUSE | D3DFVF_TEX2 |
//             D3DFVF_TEXCOORDSIZE2(0) | D3DFVF_TEXCOORDSIZE1(1); 
//
typedef struct CVF
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DCOLOR  diffuse;
    float     u, v;   // 1st set, 2D
    float     t;      // 2nd set, 1D
} CustomVertexFormat;
```



> [!Note]  
> <span data-ttu-id="64fb4-118">除了立方環境對應和磁片區材質之外，rasterizers 無法使用兩個以上的元素來處理紋理。</span><span class="sxs-lookup"><span data-stu-id="64fb4-118">With the exception of cubic-environment maps and volume textures, rasterizers cannot address textures by using any more than two elements.</span></span> <span data-ttu-id="64fb4-119">應用程式可以針對材質座標提供最多三個元素，但只有在材質為立方體圖、磁片區材質或 D3DTTFF 投射的材質轉換旗標時才會 \_ 使用。</span><span class="sxs-lookup"><span data-stu-id="64fb4-119">Applications can supply up to three elements for a texture coordinate, but only if the texture is a cube map, a volume texture, or the D3DTTFF\_PROJECTED texture transform flag is used.</span></span> <span data-ttu-id="64fb4-120">D3DTTFF \_ 投射旗標會讓轉譯器將前兩個元素除以第三個 (或 n 個) 元素。</span><span class="sxs-lookup"><span data-stu-id="64fb4-120">The D3DTTFF\_PROJECTED flag causes the rasterizer to divide the first two elements by the third (or n) element.</span></span> <span data-ttu-id="64fb4-121">如需詳細資訊，請參閱 [ (Direct3D 9) 的材質座標轉換 ](texture-coordinate-transformations.md)。</span><span class="sxs-lookup"><span data-stu-id="64fb4-121">For more information, see [Texture Coordinate Transformations (Direct3D 9)](texture-coordinate-transformations.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="64fb4-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="64fb4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64fb4-123">材質座標</span><span class="sxs-lookup"><span data-stu-id="64fb4-123">Texture Coordinates</span></span>](texture-coordinates.md)
</dt> </dl>

 

 



