---
description: " (Direct3D 9) 的鑲嵌"
ms.assetid: ae39b0e1-d2ae-449e-89db-0a2b24171531
title: " (Direct3D 9) 的鑲嵌"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82378caac1218158ffc1834c9a9b56fb8cbd250e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688144"
---
# <a name="tessellation-direct3d-9"></a><span data-ttu-id="38a80-103"> (Direct3D 9) 的鑲嵌</span><span class="sxs-lookup"><span data-stu-id="38a80-103">Tessellation (Direct3D 9)</span></span>

## <a name="tessellator-unit"></a><span data-ttu-id="38a80-104">鑲嵌單位</span><span class="sxs-lookup"><span data-stu-id="38a80-104">Tessellator Unit</span></span>

<span data-ttu-id="38a80-105">已增強鑲嵌單位。</span><span class="sxs-lookup"><span data-stu-id="38a80-105">The tessellator unit has been enhanced.</span></span> <span data-ttu-id="38a80-106">您現在可以使用它來：</span><span class="sxs-lookup"><span data-stu-id="38a80-106">You can now use it to:</span></span>

-   <span data-ttu-id="38a80-107">執行所有高序位基本專案的調適型鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="38a80-107">Perform adaptive tessellation of all higher-order primitives.</span></span>
-   <span data-ttu-id="38a80-108">從置換地圖中查詢每個頂點的位移值，並將其傳遞至頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="38a80-108">Look up per-vertex displacement values from a displacement map and pass them on to a vertex shader.</span></span>
-   <span data-ttu-id="38a80-109">支援矩形-修補程式鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="38a80-109">Support rectangle-patch tessellation.</span></span> <span data-ttu-id="38a80-110">這是透過使用 D3DDECLMETHOD \_ PARTIALU 或 D3DDECLMETHOD PARTIALV 的頂點宣告來指定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="38a80-110">This is specified through a vertex declaration using D3DDECLMETHOD\_PARTIALU or D3DDECLMETHOD\_PARTIALV.</span></span> <span data-ttu-id="38a80-111">如果使用包含這些方法的頂點宣告來繪製三角形修補程式， [**IDirect3DDevice9：:D rawtripatch**](/windows/desktop/api) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="38a80-111">If a vertex declaration containing these methods is used to draw a triangle patch, [**IDirect3DDevice9::DrawTriPatch**](/windows/desktop/api) will fail.</span></span> <span data-ttu-id="38a80-112">如需頂點宣告的詳細資訊，請參閱 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)。</span><span class="sxs-lookup"><span data-stu-id="38a80-112">For more information about vertex declarations, see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

<span data-ttu-id="38a80-113">在 DirectX 8.x 中，所謂的順序其實是什麼程度。</span><span class="sxs-lookup"><span data-stu-id="38a80-113">In DirectX 8.x, what was called ORDER was really the degree.</span></span> <span data-ttu-id="38a80-114">在 Direct3D 9 中， [**D3DDEGREETYPE**](./d3ddegreetype.md)的角度現在已指定。</span><span class="sxs-lookup"><span data-stu-id="38a80-114">In Direct3D 9, the degree is now specified by [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>


```
 // This used to be D3DORDERTYPE and D3DORDER* 
 typedef enum _D3DDEGREETYPE 
 { 
 D3DDEGREE_LINEAR = 1, 
 D3DDEGREE_QUADRATIC = 2, 
 D3DDEGREE_CUBIC = 3, 
 D3DDEGREE_QUINTIC = 5, 
 D3DDEGREE_FORCE_DWORD = 0x7fffffff, 
 } D3DDEGREETYPE; 
```



<span data-ttu-id="38a80-115">度數類型的變更會影響其他兩個結構。</span><span class="sxs-lookup"><span data-stu-id="38a80-115">The change in degree type affected two other structures.</span></span>


```
typedef struct _D3DRECTPATCH_INFO 
 { 
 UINT StartVertexOffsetWidth; 
 UINT StartVertexOffsetHeight; 
 UINT Width; 
 UINT Height; 
 UINT Stride; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DRECTPATCH_INFO; 
```




```
 typedef struct _D3DTRIPATCH_INFO 
 { 
 UINT StartVertexOffset; 
 UINT NumVertices; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DTRIPATCH_INFO; 
```



<span data-ttu-id="38a80-116">驅動程式需要修正編譯錯誤，這些錯誤會在使用新標頭進行編譯時產生此變更。</span><span class="sxs-lookup"><span data-stu-id="38a80-116">Drivers need to fix compilation errors that will result from this change when they compile with the new headers.</span></span> <span data-ttu-id="38a80-117">不需要變更任何功能。</span><span class="sxs-lookup"><span data-stu-id="38a80-117">No functionality has to be changed.</span></span>

## <a name="adaptive-tessellation"></a><span data-ttu-id="38a80-118">適應性鑲嵌</span><span class="sxs-lookup"><span data-stu-id="38a80-118">Adaptive Tessellation</span></span>

<span data-ttu-id="38a80-119">調適型鑲嵌可以套用至高序位基本專案，包括 N 個修補程式、矩形修補程式和三角形修補程式。</span><span class="sxs-lookup"><span data-stu-id="38a80-119">Adaptive tessellation can be applied to high-order primitives including N-patches, rectangle patches, and triangle patches.</span></span> <span data-ttu-id="38a80-120">D3DRS ENABLEADAPTIVETESSELLATION 會啟用這項功能 \_ ，並根據眼睛空間中控制頂點的深度值，以自我調整方式 tessellates 修補程式。</span><span class="sxs-lookup"><span data-stu-id="38a80-120">This feature is enabled by the D3DRS\_ENABLEADAPTIVETESSELLATION and adaptively tessellates a patch, based on the depth value of the control vertex in eye space.</span></span>

<span data-ttu-id="38a80-121">Z 座標 (Zi) 的控制項頂點 (Vi) ，其會藉由執行具有4個向量的點乘積來轉換為眼睛空間 (Zieye) ，作為深度值使用。</span><span class="sxs-lookup"><span data-stu-id="38a80-121">The z-coordinates (Zi) of control vertices (Vi), which are transformed into eye space (Zieye) by performing a dot product with a 4-vector, are used as the depth values.</span></span> <span data-ttu-id="38a80-122"> (使用 D3DRS \_ ADAPTIVETESS \_ X、D3DRS \_ ADAPTIVETESS \_ Y、D3DRS \_ ADAPTIVETESS \_ Z 和 D3DRS \_ ADAPTIVETESS \_ W) 時，應用程式會指定 (Mdm) 的4d 向量。</span><span class="sxs-lookup"><span data-stu-id="38a80-122">The 4D vector (Mdm) is specified by the application using four render states (D3DRS\_ADAPTIVETESS\_X, D3DRS\_ADAPTIVETESS\_Y, D3DRS\_ADAPTIVETESS\_Z, and D3DRS\_ADAPTIVETESS\_W).</span></span> <span data-ttu-id="38a80-123">這個4向量可以是串連世界的第三個數據行，也可以是視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="38a80-123">This 4-vector could be the third column of the concatenated world and view matrices.</span></span> <span data-ttu-id="38a80-124">它也可以用來將刻度套用至 Zieye。</span><span class="sxs-lookup"><span data-stu-id="38a80-124">It also could be used to apply a scale to Zieye.</span></span>

<span data-ttu-id="38a80-125">從 Zieye 計算鑲嵌層級 Ti 的函式會假設為 (MaxTessellationLevel/Zieye) ，這表示 MaxTessellationLevel 是在眼睛空間中 Z = 1 的鑲嵌層級。</span><span class="sxs-lookup"><span data-stu-id="38a80-125">The function to compute a tessellation level Ti from Zieye is assumed to be (MaxTessellationLevel/Zieye), which means that the MaxTessellationLevel is the tessellation level at Z = 1 in eye space.</span></span> <span data-ttu-id="38a80-126">MaxTessellationLevel 等於 [**IDirect3DDevice9：： SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) 針對 N 個修補程式所設定的值，若為 RT 修補程式，則等於 pNumSegs。</span><span class="sxs-lookup"><span data-stu-id="38a80-126">The MaxTessellationLevel is equal to a value set by [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) for N-patches and, for RT-patches, it is equal to pNumSegs.</span></span> <span data-ttu-id="38a80-127">鑲嵌式層級接著會壓制至值（由兩個額外的轉譯狀態所定義 D3DRS \_ MINTESSELLATIONLEVEL 和 D3DRS \_ MAXTESSELLATIONLEVEL），其定義要壓制至的最小和最大鑲嵌層級。</span><span class="sxs-lookup"><span data-stu-id="38a80-127">The tessellation level is then clamped to values, defined by the two additional render states D3DRS\_MINTESSELLATIONLEVEL and D3DRS\_MAXTESSELLATIONLEVEL, which define the minimum and maximum tessellation levels to be clamped to.</span></span> <span data-ttu-id="38a80-128">每個頂點的 Ti 會沿著修補程式的邊緣進行平均，以取得該邊緣的鑲嵌式層級。</span><span class="sxs-lookup"><span data-stu-id="38a80-128">The Ti's for each vertex along an edge of a patch are averaged to obtain a tessellation level for that edge.</span></span> <span data-ttu-id="38a80-129">針對矩形修補程式、三角形修補程式和 N 修補程式計算 Ti 的演算法，在用來計算鑲嵌層級的控制項頂點上有所不同。</span><span class="sxs-lookup"><span data-stu-id="38a80-129">The algorithm for computing Ti for rectangle patches, triangle patches, and N-patches differs in what control vertices are used to compute the tessellation level.</span></span>

<span data-ttu-id="38a80-130">針對具有 B 曲線的矩形修補程式，會使用四個最外層的控制項頂點。</span><span class="sxs-lookup"><span data-stu-id="38a80-130">For the rectangle patches with a B-spline basis, the four outermost control vertices are used.</span></span> <span data-ttu-id="38a80-131">例如，使用 D3DORDER 的 \_ 三階順序：頂點 (1、1) 和 (1 寬度-2) 可搭配 pNumSegs \[ 0 \] 、頂點 (1、寬度-2) 和 (高度-2、高度-2) 搭配 pNumSegs \[ 1 \] 、頂點 (高度-2、寬度-2) 和 (1、寬度-2) 與 pNumSegs 2 搭配使用，而 \[ \] 頂點 (2，1) 和 (1，1) 用於 pNumSegs \[ 3 \] 。</span><span class="sxs-lookup"><span data-stu-id="38a80-131">For example, with D3DORDER\_CUBIC order: vertices (1,1) and (1,width-2) are used with pNumSegs\[0\], vertices (1,width-2) and (height-2,height-2) are used with pNumSegs\[1\], vertices (height-2,width-2) and (1,width-2) are used with pNumSegs\[2\], and vertices (2,1) and (1,1) are used with pNumSegs\[3\].</span></span>

<span data-ttu-id="38a80-132">針對三角形修補程式，會使用角落修補程式頂點。</span><span class="sxs-lookup"><span data-stu-id="38a80-132">For the triangle patches, the corner patch vertices are used.</span></span> <span data-ttu-id="38a80-133">使用 D3DORDER 的 \_ 三階順序：頂點 (0) 和 (9) 會搭配 pNumSegs \[ 0 使用 \] 、頂點 (9) 和 (6) 用於 pNumSegs \[ 1 \] 和頂點 (6) 和 (0) 用於 pNumSegs \[ 3 \] 。</span><span class="sxs-lookup"><span data-stu-id="38a80-133">With D3DORDER\_CUBIC order: vertices (0) and (9) are used with pNumSegs\[0\], vertices (9) and (6) are used with pNumSegs\[1\] and vertices (6) and (0) are used with pNumSegs\[3\].</span></span>

<span data-ttu-id="38a80-134">若是 N 個修補程式，則會使用三角形頂點。</span><span class="sxs-lookup"><span data-stu-id="38a80-134">For N-patches the triangle vertices are used.</span></span>

<span data-ttu-id="38a80-135">針對具有貝塞爾單位的矩形和三角形修補程式，會使用邊角控制頂點。</span><span class="sxs-lookup"><span data-stu-id="38a80-135">For the rectangle and triangle patches with a Bezier basis, the corner-control vertices are used.</span></span>

<span data-ttu-id="38a80-136">每個頂點的鑲嵌速率控制。</span><span class="sxs-lookup"><span data-stu-id="38a80-136">Per-vertex tessellation rate control.</span></span> <span data-ttu-id="38a80-137">應用程式可以選擇性地為每個頂點提供單一的固定點浮點值，可用來控制鑲嵌率。</span><span class="sxs-lookup"><span data-stu-id="38a80-137">An application can optionally supply a single positive floating-point value per vertex, which can be used to control the rate of tessellation.</span></span> <span data-ttu-id="38a80-138">這是使用 D3DDECLUSAGE TESSFACTOR 所提供 \_ ，其使用方式索引必須為0，而輸入類型必須是 D3DDECLTYPE \_ FLOAT1。</span><span class="sxs-lookup"><span data-stu-id="38a80-138">This is supplied using the D3DDECLUSAGE\_TESSFACTOR, for which usage index must be 0 and input type must be D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="38a80-139">這會乘以每個頂點的鑲嵌層級。</span><span class="sxs-lookup"><span data-stu-id="38a80-139">This is multiplied to the per-vertex tessellation level.</span></span>

### <a name="math"></a><span data-ttu-id="38a80-140">數學</span><span class="sxs-lookup"><span data-stu-id="38a80-140">Math</span></span>

<span data-ttu-id="38a80-141">以兩個控制頂點（ (Ve1，Ve2) ）表示的邊緣 e () Te 的鑲嵌層級，其計算方式如下所示：</span><span class="sxs-lookup"><span data-stu-id="38a80-141">The tessellation level (Te) for an edge e, represented by two control vertices (Ve1, Ve2), is computed as shown below :</span></span>


```
Vertex Vi: (Xi, Yi, Zi, TFactori (optional)). 
Ze1eye = Ve1 . Mdm 
Ze2eye = Ve2 . Mdm 
Te1 = MaxTessellationLevel * TFactore1 / Ze1eye 
Te2 = MaxTessellationLevel * TFactore2 / Ze2eye 
Te = ( Te1 + Te2 ) / 2; 
if Te > D3DRS_MAXTESSELLATIONLEVEL || Te < 0, then Te = D3DRS_MAXTESSELLATIONLEVEL 
if Te < D3DRS_MINTESSELLATIONLEVEL, then Te = D3DRS_MINTESSELLATIONLEVEL 
```



<span data-ttu-id="38a80-142">當 D3DRS \_ ENABLEADAPTIVETESSELLATION 為 **TRUE** 時，三角形 (三角形清單、風扇、條紋) 繪製為 N 修補程式， [**IDirect3DDevice9：： SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) 的設定值小於1.0。</span><span class="sxs-lookup"><span data-stu-id="38a80-142">When D3DRS\_ENABLEADAPTIVETESSELLATION is **TRUE**, triangle primitives (triangle lists, fans, strips) are drawn as N-patches, [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) has set value less than 1.0.</span></span>

### <a name="api-changes"></a><span data-ttu-id="38a80-143">API 變更</span><span class="sxs-lookup"><span data-stu-id="38a80-143">API Changes</span></span>

<span data-ttu-id="38a80-144">新的呈現狀態：</span><span class="sxs-lookup"><span data-stu-id="38a80-144">New render states:</span></span>


```
 D3DRS_ENABLEADAPTIVETESSELLATION // BOOL 
 D3DRS_MAXTESSELLATIONLEVEL       // Float 
 D3DRS_MINTESSELLATIONLEVEL       // Float 
 D3DRS_ADAPTIVETESS_X             // Float 
 D3DRS_ADAPTIVETESS_Y             // Float 
 D3DRS_ADAPTIVETESS_Z             // Float 
 D3DRS_ADAPTIVETESS_W             // Float 
 
 // D3DRS_MINTESSELLATIONLEVEL and D3DRS_MAXTESSELLATIONLEVEL 
 // cannot be less than 1 
```



<span data-ttu-id="38a80-145">和其預設值：</span><span class="sxs-lookup"><span data-stu-id="38a80-145">And their default values:</span></span>


```
D3DRS_MAXTESSELLATIONLEVEL = 1.0f 
D3DRS_MINTESSELLATIONLEVEL = 1.0f 
D3DRS_ADAPTIVETESS_X = 0.0f 
D3DRS_ADAPTIVETESS_Y = 0.0f 
D3DRS_ADAPTIVETESS_Z = 1.0f 
D3DRS_ADAPTIVETESS_W = 0.0f 
D3DRS_ENABLEADAPTIVETESSELLATION = FALSE 
```



<span data-ttu-id="38a80-146">新的硬體 cap：</span><span class="sxs-lookup"><span data-stu-id="38a80-146">New hardware caps:</span></span>


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a><span data-ttu-id="38a80-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="38a80-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38a80-148">頂點管線</span><span class="sxs-lookup"><span data-stu-id="38a80-148">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
