---
description: 狀態欄塊所使用的預先定義管線狀態組合 (請參閱 (Direct3D 9) ) 的狀態欄塊儲存和還原狀態。
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: 'D3DSTATEBLOCKTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTATEBLOCKTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 03b1834a2bd8e1b5f89922d908a558aa97e58f76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104560695"
---
# <a name="d3dstateblocktype-enumeration"></a><span data-ttu-id="31abc-103">D3DSTATEBLOCKTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="31abc-103">D3DSTATEBLOCKTYPE enumeration</span></span>

<span data-ttu-id="31abc-104">狀態欄塊所使用的預先定義管線狀態組合 (請參閱 [ (Direct3D 9) ) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md) 。</span><span class="sxs-lookup"><span data-stu-id="31abc-104">Predefined sets of pipeline state used by state blocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="31abc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31abc-105">Syntax</span></span>


```C++
typedef enum _D3DSTATEBLOCKTYPE { 
  D3DSBT_ALL          = 1,
  D3DSBT_PIXELSTATE   = 2,
  D3DSBT_VERTEXSTATE  = 3,
  D3DSBT_FORCE_DWORD  = 0x7fffffff
} D3DSTATEBLOCKTYPE;
```



## <a name="constants"></a><span data-ttu-id="31abc-106">常數</span><span class="sxs-lookup"><span data-stu-id="31abc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="31abc-107"><span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ 全部**</span><span class="sxs-lookup"><span data-stu-id="31abc-107"><span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="31abc-108">捕捉目前的 [裝置狀態](saving-all-device-states-with-a-stateblock.md)。</span><span class="sxs-lookup"><span data-stu-id="31abc-108">Capture the current [device state](saving-all-device-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="31abc-109"><span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ PIXELSTATE**</span><span class="sxs-lookup"><span data-stu-id="31abc-109"><span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT\_PIXELSTATE**</span></span>
</dt> <dd>

<span data-ttu-id="31abc-110">捕捉目前的 [圖元狀態](saving-pixel-states-with-a-stateblock.md)。</span><span class="sxs-lookup"><span data-stu-id="31abc-110">Capture the current [pixel state](saving-pixel-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="31abc-111"><span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ VERTEXSTATE**</span><span class="sxs-lookup"><span data-stu-id="31abc-111"><span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT\_VERTEXSTATE**</span></span>
</dt> <dd>

<span data-ttu-id="31abc-112">捕捉目前的 [頂點狀態](saving-vertex-states-with-a-stateblock.md)。</span><span class="sxs-lookup"><span data-stu-id="31abc-112">Capture the current [vertex state](saving-vertex-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="31abc-113"><span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="31abc-113"><span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="31abc-114">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="31abc-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="31abc-115">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="31abc-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="31abc-116">請勿使用此值。</span><span class="sxs-lookup"><span data-stu-id="31abc-116">Do not use this value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31abc-117">備註</span><span class="sxs-lookup"><span data-stu-id="31abc-117">Remarks</span></span>

<span data-ttu-id="31abc-118">如下圖所示，頂點和圖元狀態都是裝置狀態的子集。</span><span class="sxs-lookup"><span data-stu-id="31abc-118">As the following diagram shows, vertex and pixel state are both subsets of device state.</span></span>

![裝置狀態的圖表，其頂點狀態和圖元狀態為子集](images/statesets.png)

<span data-ttu-id="31abc-120">只有幾個狀態會視為頂點和圖元狀態。</span><span class="sxs-lookup"><span data-stu-id="31abc-120">There are only a few states that are considered both vertex and pixel state.</span></span> <span data-ttu-id="31abc-121">這些狀態包括：</span><span class="sxs-lookup"><span data-stu-id="31abc-121">These states are:</span></span>

-   <span data-ttu-id="31abc-122">轉譯狀態： D3DRS \_ FOGDENSITY</span><span class="sxs-lookup"><span data-stu-id="31abc-122">Render state: D3DRS\_FOGDENSITY</span></span>
-   <span data-ttu-id="31abc-123">轉譯狀態： D3DRS \_ FOGSTART</span><span class="sxs-lookup"><span data-stu-id="31abc-123">Render state: D3DRS\_FOGSTART</span></span>
-   <span data-ttu-id="31abc-124">轉譯狀態： D3DRS \_ FOGEND</span><span class="sxs-lookup"><span data-stu-id="31abc-124">Render state: D3DRS\_FOGEND</span></span>
-   <span data-ttu-id="31abc-125">材質狀態： D3DTSS \_ TEXCOORDINDEX</span><span class="sxs-lookup"><span data-stu-id="31abc-125">Texture state: D3DTSS\_TEXCOORDINDEX</span></span>
-   <span data-ttu-id="31abc-126">材質狀態： D3DTSS \_ TEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="31abc-126">Texture state: D3DTSS\_TEXTURETRANSFORMFLAGS</span></span>

## <a name="requirements"></a><span data-ttu-id="31abc-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="31abc-127">Requirements</span></span>



| <span data-ttu-id="31abc-128">需求</span><span class="sxs-lookup"><span data-stu-id="31abc-128">Requirement</span></span> | <span data-ttu-id="31abc-129">值</span><span class="sxs-lookup"><span data-stu-id="31abc-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31abc-130">標頭</span><span class="sxs-lookup"><span data-stu-id="31abc-130">Header</span></span><br/> | <dl> <span data-ttu-id="31abc-131"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="31abc-131"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31abc-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31abc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31abc-133">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="31abc-133">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="31abc-134">**IDirect3DDevice9::CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="31abc-134">**IDirect3DDevice9::CreateStateBlock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

<span data-ttu-id="31abc-135">**IDirect3DDevice9::CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="31abc-135">**IDirect3DDevice9::CreateStateBlock**</span></span>
</dt> </dl>

 

 
