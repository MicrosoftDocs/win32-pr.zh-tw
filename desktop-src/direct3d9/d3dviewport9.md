---
description: 定義3D 磁片區專案的呈現目標表面的視窗維度。
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: 'D3DVIEWPORT9 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVIEWPORT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3d96000de50934ebdc893ffc3866dd3252703bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975690"
---
# <a name="d3dviewport9-structure"></a><span data-ttu-id="2581d-103">D3DVIEWPORT9 結構</span><span class="sxs-lookup"><span data-stu-id="2581d-103">D3DVIEWPORT9 structure</span></span>

<span data-ttu-id="2581d-104">定義3D 磁片區專案的呈現目標表面的視窗維度。</span><span class="sxs-lookup"><span data-stu-id="2581d-104">Defines the window dimensions of a render-target surface onto which a 3D volume projects.</span></span>

## <a name="syntax"></a><span data-ttu-id="2581d-105">語法</span><span class="sxs-lookup"><span data-stu-id="2581d-105">Syntax</span></span>


```C++
typedef struct D3DVIEWPORT9 {
  DWORD X;
  DWORD Y;
  DWORD Width;
  DWORD Height;
  float MinZ;
  float MaxZ;
} D3DVIEWPORT9, *LPD3DVIEWPORT9;
```



## <a name="members"></a><span data-ttu-id="2581d-106">成員</span><span class="sxs-lookup"><span data-stu-id="2581d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2581d-107">**X**</span><span class="sxs-lookup"><span data-stu-id="2581d-107">**X**</span></span>
</dt> <dd>

<span data-ttu-id="2581d-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2581d-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2581d-109">轉譯目標介面上，視口左上角的圖元座標。</span><span class="sxs-lookup"><span data-stu-id="2581d-109">Pixel coordinate of the upper-left corner of the viewport on the render-target surface.</span></span> <span data-ttu-id="2581d-110">除非您想要轉譯為介面的子集，否則這個成員可以設定為0。</span><span class="sxs-lookup"><span data-stu-id="2581d-110">Unless you want to render to a subset of the surface, this member can be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="2581d-111">**Y**</span><span class="sxs-lookup"><span data-stu-id="2581d-111">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="2581d-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2581d-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2581d-113">轉譯目標介面上，視口左上角的圖元座標。</span><span class="sxs-lookup"><span data-stu-id="2581d-113">Pixel coordinate of the upper-left corner of the viewport on the render-target surface.</span></span> <span data-ttu-id="2581d-114">除非您想要轉譯為介面的子集，否則這個成員可以設定為0。</span><span class="sxs-lookup"><span data-stu-id="2581d-114">Unless you want to render to a subset of the surface, this member can be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="2581d-115">**寬度**</span><span class="sxs-lookup"><span data-stu-id="2581d-115">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="2581d-116">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2581d-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2581d-117">剪輯音量的寬度維度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2581d-117">Width dimension of the clip volume, in pixels.</span></span> <span data-ttu-id="2581d-118">除非您只轉譯為介面的子集，否則這個成員應設定為呈現目標介面的寬度維度。</span><span class="sxs-lookup"><span data-stu-id="2581d-118">Unless you are rendering only to a subset of the surface, this member should be set to the width dimension of the render-target surface.</span></span>

</dd> <dt>

<span data-ttu-id="2581d-119">**高度**</span><span class="sxs-lookup"><span data-stu-id="2581d-119">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="2581d-120">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2581d-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2581d-121">剪輯音量的高度維度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2581d-121">Height dimension of the clip volume, in pixels.</span></span> <span data-ttu-id="2581d-122">除非您只轉譯為介面的子集，否則這個成員應設定為轉譯目標介面的高度維度。</span><span class="sxs-lookup"><span data-stu-id="2581d-122">Unless you are rendering only to a subset of the surface, this member should be set to the height dimension of the render-target surface.</span></span>

</dd> <dt>

<span data-ttu-id="2581d-123">**MinZ**</span><span class="sxs-lookup"><span data-stu-id="2581d-123">**MinZ**</span></span>
</dt> <dd>

<span data-ttu-id="2581d-124">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="2581d-124">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="2581d-125">搭配 MaxZ，描述要轉譯場景的深度值範圍的值，也就是剪輯音量的最小值和最大值。</span><span class="sxs-lookup"><span data-stu-id="2581d-125">Together with MaxZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume.</span></span> <span data-ttu-id="2581d-126">大部分的應用程式會將此值設定為0.0。</span><span class="sxs-lookup"><span data-stu-id="2581d-126">Most applications set this value to 0.0.</span></span> <span data-ttu-id="2581d-127">套用投射矩陣之後，會執行裁剪。</span><span class="sxs-lookup"><span data-stu-id="2581d-127">Clipping is performed after applying the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="2581d-128">**MaxZ**</span><span class="sxs-lookup"><span data-stu-id="2581d-128">**MaxZ**</span></span>
</dt> <dd>

<span data-ttu-id="2581d-129">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="2581d-129">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="2581d-130">搭配 MinZ，描述要轉譯場景的深度值範圍的值，也就是剪輯音量的最小值和最大值。</span><span class="sxs-lookup"><span data-stu-id="2581d-130">Together with MinZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume.</span></span> <span data-ttu-id="2581d-131">大部分的應用程式會將此值設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="2581d-131">Most applications set this value to 1.0.</span></span> <span data-ttu-id="2581d-132">套用投射矩陣之後，會執行裁剪。</span><span class="sxs-lookup"><span data-stu-id="2581d-132">Clipping is performed after applying the projection matrix.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2581d-133">備註</span><span class="sxs-lookup"><span data-stu-id="2581d-133">Remarks</span></span>

<span data-ttu-id="2581d-134">X、Y、寬度和高度成員描述轉譯目標介面上的視口位置和維度。</span><span class="sxs-lookup"><span data-stu-id="2581d-134">The X, Y, Width, and Height members describe the position and dimensions of the viewport on the render-target surface.</span></span> <span data-ttu-id="2581d-135">通常，應用程式會轉譯成整個目標介面;在 640 x 480 介面上轉譯時，這些成員應分別為0、0、640和480。</span><span class="sxs-lookup"><span data-stu-id="2581d-135">Usually, applications render to the entire target surface; when rendering on a 640 x 480 surface, these members should be 0, 0, 640, and 480, respectively.</span></span> <span data-ttu-id="2581d-136">MinZ 和 MaxZ 通常會設定為0.0 和1.0，但是可以設定為其他值，以達成特定效果。</span><span class="sxs-lookup"><span data-stu-id="2581d-136">The MinZ and MaxZ are typically set to 0.0 and 1.0 but can be set to other values to achieve specific effects.</span></span> <span data-ttu-id="2581d-137">例如，您可以將它們設定為0.0，強制系統將物件轉譯為場景的前景，或同時設定為1.0 以強制物件進入背景。</span><span class="sxs-lookup"><span data-stu-id="2581d-137">For example, you might set them both to 0.0 to force the system to render objects to the foreground of a scene, or both to 1.0 to force the objects into the background.</span></span>

<span data-ttu-id="2581d-138">當裝置的視口參數變更 (因為) 呼叫 [**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) 方法時，驅動程式會建立新的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="2581d-138">When the viewport parameters for a device change (because of a call to the [**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) method), the driver builds a new transformation matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="2581d-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="2581d-139">Requirements</span></span>



| <span data-ttu-id="2581d-140">需求</span><span class="sxs-lookup"><span data-stu-id="2581d-140">Requirement</span></span> | <span data-ttu-id="2581d-141">值</span><span class="sxs-lookup"><span data-stu-id="2581d-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2581d-142">標頭</span><span class="sxs-lookup"><span data-stu-id="2581d-142">Header</span></span><br/> | <dl> <span data-ttu-id="2581d-143"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="2581d-143"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2581d-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2581d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2581d-145">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="2581d-145">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="2581d-146">**GetViewport**</span><span class="sxs-lookup"><span data-stu-id="2581d-146">**GetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[<span data-ttu-id="2581d-147">**SetViewport**</span><span class="sxs-lookup"><span data-stu-id="2581d-147">**SetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
