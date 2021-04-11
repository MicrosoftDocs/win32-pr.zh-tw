---
description: 定義材質座標轉換值。
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: 'D3DTEXTURETRANSFORMFLAGS 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 63426c0d57dee02823ee2f37327ba7c66d421b24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196199"
---
# <a name="d3dtexturetransformflags-enumeration"></a><span data-ttu-id="df611-103">D3DTEXTURETRANSFORMFLAGS 列舉</span><span class="sxs-lookup"><span data-stu-id="df611-103">D3DTEXTURETRANSFORMFLAGS enumeration</span></span>

<span data-ttu-id="df611-104">定義材質座標轉換值。</span><span class="sxs-lookup"><span data-stu-id="df611-104">Defines texture coordinate transformation values.</span></span>

## <a name="syntax"></a><span data-ttu-id="df611-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df611-105">Syntax</span></span>


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a><span data-ttu-id="df611-106">常數</span><span class="sxs-lookup"><span data-stu-id="df611-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="df611-107"><span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**D3DTTFF \_ DISABLE**</span><span class="sxs-lookup"><span data-stu-id="df611-107"><span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**D3DTTFF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="df611-108">材質座標會直接傳遞至轉譯器。</span><span class="sxs-lookup"><span data-stu-id="df611-108">Texture coordinates are passed directly to the rasterizer.</span></span>

</dd> <dt>

<span data-ttu-id="df611-109"><span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF \_ COUNT1**</span><span class="sxs-lookup"><span data-stu-id="df611-109"><span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF\_COUNT1**</span></span>
</dt> <dd>

<span data-ttu-id="df611-110">轉譯器應該預期是1D 材質座標。</span><span class="sxs-lookup"><span data-stu-id="df611-110">The rasterizer should expect 1D texture coordinates.</span></span> <span data-ttu-id="df611-111">Fixed 函式頂點處理會使用這個值;使用可程式化的頂點著色器時，應該設定為0。</span><span class="sxs-lookup"><span data-stu-id="df611-111">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="df611-112"><span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF \_ COUNT2**</span><span class="sxs-lookup"><span data-stu-id="df611-112"><span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF\_COUNT2**</span></span>
</dt> <dd>

<span data-ttu-id="df611-113">轉譯器應預期2D 材質座標。</span><span class="sxs-lookup"><span data-stu-id="df611-113">The rasterizer should expect 2D texture coordinates.</span></span> <span data-ttu-id="df611-114">Fixed 函式頂點處理會使用這個值;使用可程式化的頂點著色器時，應該設定為0。</span><span class="sxs-lookup"><span data-stu-id="df611-114">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="df611-115"><span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF \_ COUNT3**</span><span class="sxs-lookup"><span data-stu-id="df611-115"><span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF\_COUNT3**</span></span>
</dt> <dd>

<span data-ttu-id="df611-116">轉譯器應預期3D 紋理座標。</span><span class="sxs-lookup"><span data-stu-id="df611-116">The rasterizer should expect 3D texture coordinates.</span></span> <span data-ttu-id="df611-117">Fixed 函式頂點處理會使用這個值;使用可程式化的頂點著色器時，應該設定為0。</span><span class="sxs-lookup"><span data-stu-id="df611-117">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="df611-118"><span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF \_ COUNT4**</span><span class="sxs-lookup"><span data-stu-id="df611-118"><span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF\_COUNT4**</span></span>
</dt> <dd>

<span data-ttu-id="df611-119">轉譯器應預期為4D 材質座標。</span><span class="sxs-lookup"><span data-stu-id="df611-119">The rasterizer should expect 4D texture coordinates.</span></span> <span data-ttu-id="df611-120">Fixed 函式頂點處理會使用這個值;使用可程式化的頂點著色器時，應該設定為0。</span><span class="sxs-lookup"><span data-stu-id="df611-120">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="df611-121"><span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ 投射**</span><span class="sxs-lookup"><span data-stu-id="df611-121"><span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF\_PROJECTED**</span></span>
</dt> <dd>

<span data-ttu-id="df611-122">固定函式圖元管線會採用此旗標，以及將 ps 1 1 版本中的可程式化圖元管線視為 \_ \_ ps \_ 1 \_ 3。</span><span class="sxs-lookup"><span data-stu-id="df611-122">This flag is honored by the fixed function pixel pipeline, as well as the programmable pixel pipeline in versions ps\_1\_1 to ps\_1\_3.</span></span> <span data-ttu-id="df611-123">針對材質階段啟用紋理投影時，全部四個浮點值都必須寫入對應的材質暫存器。</span><span class="sxs-lookup"><span data-stu-id="df611-123">When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register.</span></span> <span data-ttu-id="df611-124">每個材質座標都會先除以最後一個元素，然後再傳遞給轉譯器。</span><span class="sxs-lookup"><span data-stu-id="df611-124">Each texture coordinate is divided by the last element before being passed to the rasterizer.</span></span> <span data-ttu-id="df611-125">例如，如果使用 D3DTTFF COUNT3 旗標來指定此旗標 \_ ，則第一個和第二個材質座標會先除以第三個座標，再傳遞給轉譯器。</span><span class="sxs-lookup"><span data-stu-id="df611-125">For example, if this flag is specified with the D3DTTFF\_COUNT3 flag, the first and second texture coordinates are divided by the third coordinate before being passed to the rasterizer.</span></span>

</dd> <dt>

<span data-ttu-id="df611-126"><span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="df611-126"><span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="df611-127">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="df611-127">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="df611-128">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="df611-128">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="df611-129">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="df611-129">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df611-130">備註</span><span class="sxs-lookup"><span data-stu-id="df611-130">Remarks</span></span>

<span data-ttu-id="df611-131">您可以使用 4 x 4 矩陣來轉換材質座標，然後將結果傳遞給轉譯器。</span><span class="sxs-lookup"><span data-stu-id="df611-131">Texture coordinates can be transformed using a 4 x 4 matrix before the results are passed to the rasterizer.</span></span> <span data-ttu-id="df611-132">紋理座標轉換的設定方式是呼叫 [**IDirect3DDevice9：： SetTextureStageState**](/windows/desktop/api)，並傳入 D3DTSS \_ TEXTURETRANSFORMFLAGS 材質階段狀態和 **D3DTEXTURETRANSFORMFLAGS** 中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="df611-132">The texture coordinate transforms are set by calling [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api), and by passing in the D3DTSS\_TEXTURETRANSFORMFLAGS texture stage state and one of the values from **D3DTEXTURETRANSFORMFLAGS**.</span></span> <span data-ttu-id="df611-133">如需紋理轉換的詳細資訊，請參閱 [ (Direct3D 9) 的材質座標轉換 ](texture-coordinate-transformations.md)。</span><span class="sxs-lookup"><span data-stu-id="df611-133">For more information about texture transforms, see [Texture Coordinate Transformations (Direct3D 9)](texture-coordinate-transformations.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df611-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="df611-134">Requirements</span></span>



| <span data-ttu-id="df611-135">需求</span><span class="sxs-lookup"><span data-stu-id="df611-135">Requirement</span></span> | <span data-ttu-id="df611-136">值</span><span class="sxs-lookup"><span data-stu-id="df611-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df611-137">標頭</span><span class="sxs-lookup"><span data-stu-id="df611-137">Header</span></span><br/> | <dl> <span data-ttu-id="df611-138"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="df611-138"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df611-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df611-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df611-140">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="df611-140">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="df611-141">**D3DTEXTURESTAGESTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="df611-141">**D3DTEXTURESTAGESTATETYPE**</span></span>](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
