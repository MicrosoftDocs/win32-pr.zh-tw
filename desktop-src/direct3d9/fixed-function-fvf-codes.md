---
description: FVF 程式碼會描述在單一資料流程中，以交錯方式儲存的頂點內容。
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: 修正 (Direct3D 9) 的函式 FVF 碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd10b655c0692881e5d93b6c716ec9bcd8a76c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970274"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a><span data-ttu-id="6b124-103">修正 (Direct3D 9) 的函式 FVF 碼</span><span class="sxs-lookup"><span data-stu-id="6b124-103">Fixed Function FVF Codes (Direct3D 9)</span></span>

<span data-ttu-id="6b124-104">FVF 程式碼會描述在單一資料流程中，以交錯方式儲存的頂點內容。</span><span class="sxs-lookup"><span data-stu-id="6b124-104">A FVF code describes the contents of vertices stored interleaved in a single data stream.</span></span> <span data-ttu-id="6b124-105">它通常會指定固定函式頂點處理管線所要處理的資料。</span><span class="sxs-lookup"><span data-stu-id="6b124-105">It generally specifies data to be processed by the fixed function vertex processing pipeline.</span></span> <span data-ttu-id="6b124-106">這是較舊樣式的頂點宣告;若要查看目前的頂點宣告樣式，請參閱 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)。</span><span class="sxs-lookup"><span data-stu-id="6b124-106">This is an older-style vertex declaration; to see the current vertex declaration style, see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

<span data-ttu-id="6b124-107">Direct3D 應用程式可以透過數種不同的方式來定義模型頂點。</span><span class="sxs-lookup"><span data-stu-id="6b124-107">Direct3D applications can define model vertices in several different ways.</span></span> <span data-ttu-id="6b124-108">支援彈性頂點定義（也稱為彈性頂點格式或彈性頂點格式的程式碼），讓您的應用程式可以只使用它所需的頂點元件，以排除未使用的元件。</span><span class="sxs-lookup"><span data-stu-id="6b124-108">Support for flexible vertex definitions, also known as flexible vertex formats or flexible vertex format codes, makes it possible for your application to use only the vertex components it needs, eliminating those components that aren't used.</span></span> <span data-ttu-id="6b124-109">藉由只使用所需的頂點元件，您的應用程式可以節省記憶體，並將呈現模型所需的處理頻寬降至最低。</span><span class="sxs-lookup"><span data-stu-id="6b124-109">By using only the needed vertex components, your application can conserve memory and minimize the processing bandwidth required to render models.</span></span> <span data-ttu-id="6b124-110">您可以使用 [D3DFVF](d3dfvf.md) 碼的組合來描述頂點的格式化方式。</span><span class="sxs-lookup"><span data-stu-id="6b124-110">You describe how your vertices are formatted by using a combination of [D3DFVF](d3dfvf.md) codes.</span></span>

<span data-ttu-id="6b124-111">FVF 規格包含 D3DFVF PSIZE 所指定的點大小格式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6b124-111">The FVF specification includes formats for point size, specified by D3DFVF\_PSIZE.</span></span> <span data-ttu-id="6b124-112">這種大小是以相機空間單位表示，適用于非轉換和亮 (TL) 頂點，以及在 TL 頂點的裝置空間單位中。</span><span class="sxs-lookup"><span data-stu-id="6b124-112">This size is expressed in camera space units for non-transformed and lit (TL) vertices, and in device-space units for TL vertices.</span></span>

<span data-ttu-id="6b124-113">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的轉譯方法會使用接受這些旗標組合的方法來提供 c + + 應用程式，並使用它們來決定如何呈現基本專案。</span><span class="sxs-lookup"><span data-stu-id="6b124-113">The rendering methods of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface provide C++ applications with methods that accept a combination of these flags, and use them to determine how to render primitives.</span></span> <span data-ttu-id="6b124-114">基本上，這些旗標會告訴系統哪些頂點元件-位置、頂點混色加權、正常、色彩，以及紋理座標的數目和格式-您的應用程式會使用和間接地使用您希望 Direct3D 套用至哪些轉譯管線部分。</span><span class="sxs-lookup"><span data-stu-id="6b124-114">Basically, these flags tell the system which vertex components - position, vertex blending weights, normal, colors, and the number and format of texture coordinates - your application uses and, indirectly, which parts of the rendering pipeline you want Direct3D to apply to them.</span></span> <span data-ttu-id="6b124-115">此外，特定頂點格式旗標的存在與否會與系統通訊，也就是有哪些頂點元件欄位存在於記憶體中，以及您省略了哪些。</span><span class="sxs-lookup"><span data-stu-id="6b124-115">In addition, the presence or absence of a particular vertex format flag communicates to the system which vertex component fields are present in memory and which you've omitted.</span></span>

<span data-ttu-id="6b124-116">若要判斷裝置的限制，您可以 \_ \_ 在 [**FVFCaps**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 D3DCAPS9 成員中，查詢裝置的 D3DFVFCAPS DONOTSTRIPELEMENTS 和 D3DFVFCAPS TEXCOORDCOUNTMASK 的值。</span><span class="sxs-lookup"><span data-stu-id="6b124-116">To determine device limitations, you can query a device for the values of D3DFVFCAPS\_DONOTSTRIPELEMENTS and D3DFVFCAPS\_TEXCOORDCOUNTMASK in the FVFCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

<span data-ttu-id="6b124-117">您可以使用不同的格式來宣告材質座標，讓材質可以使用最少的一個座標，或多達四個材質座標來定址， (2D 投射的材質座標) 。</span><span class="sxs-lookup"><span data-stu-id="6b124-117">Texture coordinates can be declared in different formats, allowing textures to be addressed using as few as one coordinate or as many as four texture coordinates (for 2D projected texture coordinates).</span></span> <span data-ttu-id="6b124-118">如需詳細資訊，請參閱 [ (Direct3D 9) 的材質座標格式 ](texture-coordinate-formats.md)。</span><span class="sxs-lookup"><span data-stu-id="6b124-118">For more information, see [Texture Coordinate Formats (Direct3D 9)](texture-coordinate-formats.md).</span></span> <span data-ttu-id="6b124-119">使用 [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) 的宏集來建立位模式，以識別頂點格式所使用的材質座標格式。</span><span class="sxs-lookup"><span data-stu-id="6b124-119">Use the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros to create bit patterns that identify the texture coordinate formats that your vertex format uses.</span></span>

<span data-ttu-id="6b124-120">沒有任何應用程式會使用每個元件。</span><span class="sxs-lookup"><span data-stu-id="6b124-120">No application will use every component.</span></span> <span data-ttu-id="6b124-121">互異的同質 W (RHW) 和頂點一般欄位互斥。</span><span class="sxs-lookup"><span data-stu-id="6b124-121">The reciprocal homogeneous W (RHW) and vertex normal fields are mutually exclusive.</span></span> <span data-ttu-id="6b124-122">大部分的應用程式也都不會嘗試使用所有八組紋理座標，但是 Direct3D 具有這個容量。</span><span class="sxs-lookup"><span data-stu-id="6b124-122">Nor will most applications try to use all eight sets of texture coordinates, but Direct3D has this capacity.</span></span> <span data-ttu-id="6b124-123">您可以搭配其他旗標使用的旗標有幾項限制。</span><span class="sxs-lookup"><span data-stu-id="6b124-123">There are several restrictions on which flags you can use with other flags.</span></span> <span data-ttu-id="6b124-124">例如，您不能同時使用 D3DFVF \_ XYZ 和 D3DFVF \_ XYZRHW 旗標，因為這表示您的應用程式會使用未轉換和已轉換的頂點來描述頂點的位置。</span><span class="sxs-lookup"><span data-stu-id="6b124-124">For example, you cannot use the D3DFVF\_XYZ and D3DFVF\_XYZRHW flags together, as this would indicate that your application is describing a vertex's position with both untransformed and transformed vertices.</span></span>

<span data-ttu-id="6b124-125">若要使用索引頂點混色，D3DFVF \_ LASTBETA \_ UBYTE4 旗標應該會出現在 FVF 宣告的結尾。</span><span class="sxs-lookup"><span data-stu-id="6b124-125">To use indexed vertex blending, the D3DFVF\_LASTBETA\_UBYTE4 flag should appear at the end of the FVF declaration.</span></span> <span data-ttu-id="6b124-126">此旗標的存在表示第五個混色加權將被視為 DWORD 而不是 float。</span><span class="sxs-lookup"><span data-stu-id="6b124-126">The presence of this flag indicates that the fifth blending weight will be treated as a DWORD instead of float.</span></span> <span data-ttu-id="6b124-127">如需詳細資訊，請參閱 [ (Direct3D 9) 的索引頂點混色 ](indexed-vertex-blending.md)。</span><span class="sxs-lookup"><span data-stu-id="6b124-127">For more information, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span>

<span data-ttu-id="6b124-128">下列程式碼範例顯示使用 D3DFVF LASTBETA UBYTE4 旗標的 FVF 程式碼與不是的程式碼之間的差異 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="6b124-128">The following code samples shows the difference between an FVF code that uses the D3DFVF\_LASTBETA\_UBYTE4 flag and one that doesn't.</span></span> <span data-ttu-id="6b124-129">\_使用四個混合索引時，會出現旗標 D3DFVF XYZB3，因為您一律會從數位1減去前三個的總和，以取得第四個 (blend ₄ = 1- (blend ₁ + blend ₂ + blend ₃) ) 。</span><span class="sxs-lookup"><span data-stu-id="6b124-129">The flag D3DFVF\_XYZB3 is present when four blending indices are used because you always subtract the sum of the first three from the number one to obtain the fourth (blend₄ = 1 - (blend₁ + blend₂ + blend₃)).</span></span>


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB3|D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



<span data-ttu-id="6b124-130">以下定義的 FVF 會使用 D3DFVF \_ LAST \_ UBYTE4 旗標。</span><span class="sxs-lookup"><span data-stu-id="6b124-130">The FVF defined below uses the D3DFVF\_LAST\_UBYTE4 flag.</span></span>


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB4 | D3DFVF_LASTBETA_UBYTE4 |D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    DWORD       indices; // Referenced as v2.xyzw in the vertex shader 
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



## <a name="related-topics"></a><span data-ttu-id="6b124-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b124-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b124-132">頂點宣告</span><span class="sxs-lookup"><span data-stu-id="6b124-132">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
