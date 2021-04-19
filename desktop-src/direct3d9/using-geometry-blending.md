---
description: 下列使用者定義結構可以用於將在兩個矩陣之間混合的頂點。
ms.assetid: 6bcabcf9-d14e-446a-8dd2-e741211cc704
title: 使用 (Direct3D 9) 的幾何混合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc12c4d7d83ce4c01c76bd338a07f8e0aac7c003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991590"
---
# <a name="using-geometry-blending-direct3d-9"></a><span data-ttu-id="e4503-103">使用 (Direct3D 9) 的幾何混合</span><span class="sxs-lookup"><span data-stu-id="e4503-103">Using Geometry Blending (Direct3D 9)</span></span>

<span data-ttu-id="e4503-104">下列使用者定義結構可以用於將在兩個矩陣之間混合的頂點。</span><span class="sxs-lookup"><span data-stu-id="e4503-104">The following user-defined structure can be used for vertices that will be blended between two matrices.</span></span>


```
// The flexible vertex format (FVF) descriptor for this vertex would be:
//   FVF = D3DFVF_XYZB1 | D3DFVF_NORMAL | D3DFVF_TEX1; 

struct D3DBLENDVERTEX {
    D3DVECTOR v;
    FLOAT     blend; 
    D3DVECTOR n;
    FLOAT     tu, tv;
};
```



<span data-ttu-id="e4503-105">Blend 權數必須出現在 FVF 中的位置和 RHW 資料之後，以及頂點正常之前。</span><span class="sxs-lookup"><span data-stu-id="e4503-105">The blend weight must appear after the position and RHW data in the FVF, and before the vertex normal.</span></span>

<span data-ttu-id="e4503-106">請注意，前一個頂點格式只包含一個混合加權值。</span><span class="sxs-lookup"><span data-stu-id="e4503-106">Notice that the preceding vertex format contains only one blending weight value.</span></span> <span data-ttu-id="e4503-107">這是因為會有兩個世界矩陣，定義于 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (0) 和 **D3DTS \_ WORLDMATRIX** (1) 轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="e4503-107">This is because there will be two world matrices, defined in the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md)(0) and **D3DTS\_WORLDMATRIX**(1) transform states.</span></span> <span data-ttu-id="e4503-108">系統會使用單一權數值來混合這兩個矩陣之間的每個頂點。</span><span class="sxs-lookup"><span data-stu-id="e4503-108">The system blends each vertex between these two matrices using the single weight value.</span></span> <span data-ttu-id="e4503-109">針對三個矩陣，只需要兩個加權，依此類推。</span><span class="sxs-lookup"><span data-stu-id="e4503-109">For three matrices, only two weights are required, and so on.</span></span>

> [!Note]
>
> <span data-ttu-id="e4503-110">定義外觀權數很簡單。</span><span class="sxs-lookup"><span data-stu-id="e4503-110">Defining skin weights is easy.</span></span> <span data-ttu-id="e4503-111">使用接點之間距離的線性功能是不錯的起點，但是更平滑的 sigmoid 函式看起來更好。</span><span class="sxs-lookup"><span data-stu-id="e4503-111">Using a linear function of the distance between joints is good start, but a smoother sigmoid function looks better.</span></span> <span data-ttu-id="e4503-112">如果想要的話，選擇外觀權重分佈函式可能會導致 creases 的接點，並在短距離內使用較大的外觀權數變化。</span><span class="sxs-lookup"><span data-stu-id="e4503-112">Choosing a skin-weight distribution function can result in sharp creases at joints, if desired, by using a large variation in skin weight over a short distance.</span></span>

 

## <a name="setting-blending-matrices"></a><span data-ttu-id="e4503-113">設定混色矩陣</span><span class="sxs-lookup"><span data-stu-id="e4503-113">Setting Blending Matrices</span></span>

<span data-ttu-id="e4503-114">您可以藉由呼叫 [**IDirect3DDevice9：： SetTransform**](/windows/desktop/api) 方法，來設定系統混合的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="e4503-114">You set the transformation matrices between which the system blends by calling the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method.</span></span> <span data-ttu-id="e4503-115">將第一個參數設定為 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) 巨集定義的值，並將第二個參數設定為要設定之矩陣的位址。</span><span class="sxs-lookup"><span data-stu-id="e4503-115">Set the first parameter to a value defined by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, and set the second parameter to the address of the matrix to be set.</span></span>

<span data-ttu-id="e4503-116">下列 c + + 程式碼範例會設定兩個世界矩陣，在這兩個矩陣之間混合幾何來建立 double-jointed arm 的假像。</span><span class="sxs-lookup"><span data-stu-id="e4503-116">The following C++ code example sets two world matrices, between which geometry is blended to create the illusion of a jointed arm.</span></span>


```
// For this example, the d3dDevice variable is assumed to be a valid pointer
//   to an IDirect3DDevice9 interface for an initialized 3D scene.

float     BendAngle = 3.1415926f / 4.0f; // 45 degrees
D3DMATRIX matUpperArm, matLowerArm;

// The upper arm is immobile. Use the identity matrix.
D3DXMatrixIdentity( matUpperArm );
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matUpperArm );

// The lower arm rotates about the x-axis, attached to the upper arm.
D3DXMatrixRotationX( matLowerArm, -BendAngle ); 
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(1), &matLowerArm );
```



<span data-ttu-id="e4503-117">設定混色矩陣只會讓系統快取矩陣以供稍後使用。它不會指示系統開始混合頂點。</span><span class="sxs-lookup"><span data-stu-id="e4503-117">Setting a blending matrix merely causes the system to cache the matrix for later use; it doesn't instruct the system to begin blending vertices.</span></span>

## <a name="enabling-geometry-blending"></a><span data-ttu-id="e4503-118">啟用幾何混合</span><span class="sxs-lookup"><span data-stu-id="e4503-118">Enabling Geometry Blending</span></span>

<span data-ttu-id="e4503-119">幾何混合預設為停用。</span><span class="sxs-lookup"><span data-stu-id="e4503-119">Geometry blending is disabled by default.</span></span> <span data-ttu-id="e4503-120">若要啟用幾何混合，請呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/desktop/api) 方法，將 D3DRS \_ VERTEXBLEND 轉譯狀態設定為 [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) 列舉類型的值。</span><span class="sxs-lookup"><span data-stu-id="e4503-120">To enable geometry blending, call the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method to set the D3DRS\_VERTEXBLEND render state to a value from the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="e4503-121">下列程式碼範例顯示在兩個世界矩陣之間設定 blend 的呈現狀態時，此呼叫可能會顯示的樣子。</span><span class="sxs-lookup"><span data-stu-id="e4503-121">The following code example shows what this call might look like when setting the render state for a blend between two world matrices.</span></span>


```
d3dDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_1WEIGHTS );
```



<span data-ttu-id="e4503-122">當 D3DRS \_ VERTEXBLEND 設定為 D3DVBF DISABLE 以外的任何值時 \_ ，系統會假設頂點格式會包含適當的混色加權數目。</span><span class="sxs-lookup"><span data-stu-id="e4503-122">When D3DRS\_VERTEXBLEND is set to any value other than D3DVBF\_DISABLE, the system assumes that the appropriate number of blending weights will be included in the vertex format.</span></span> <span data-ttu-id="e4503-123">您必須負責提供符合規範的頂點格式，以及提供該格式對 Direct3D 轉譯方法的適當描述。</span><span class="sxs-lookup"><span data-stu-id="e4503-123">It is your responsibility to provide a compliant vertex format, and to provide a proper description of that format to the Direct3D rendering methods.</span></span>

<span data-ttu-id="e4503-124">啟用時，系統會針對 DrawPrimitive 轉譯方法所呈現的所有物件執行幾何混合。</span><span class="sxs-lookup"><span data-stu-id="e4503-124">When enabled, the system performs geometry blending for all objects rendered by the DrawPrimitive rendering methods.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4503-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4503-125">See Also</span></span>

[<span data-ttu-id="e4503-126">修正 (Direct3D 9) 的函式 FVF 碼 </span><span class="sxs-lookup"><span data-stu-id="e4503-126">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)


## <a name="related-topics"></a><span data-ttu-id="e4503-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4503-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4503-128">幾何混合</span><span class="sxs-lookup"><span data-stu-id="e4503-128">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 
