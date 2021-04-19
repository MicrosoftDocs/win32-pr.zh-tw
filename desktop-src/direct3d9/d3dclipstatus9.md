---
description: 描述目前的剪輯狀態。
ms.assetid: 3ea8631c-a967-4d24-a49a-1751b3ee6077
title: 'D3DCLIPSTATUS9 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPSTATUS9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3b22fdfcc136c05ec8fe03ae491612606b2df62f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986501"
---
# <a name="d3dclipstatus9-structure"></a><span data-ttu-id="e7e32-103">D3DCLIPSTATUS9 結構</span><span class="sxs-lookup"><span data-stu-id="e7e32-103">D3DCLIPSTATUS9 structure</span></span>

<span data-ttu-id="e7e32-104">描述目前的剪輯狀態。</span><span class="sxs-lookup"><span data-stu-id="e7e32-104">Describes the current clip status.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e32-105">語法</span><span class="sxs-lookup"><span data-stu-id="e7e32-105">Syntax</span></span>


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a><span data-ttu-id="e7e32-106">成員</span><span class="sxs-lookup"><span data-stu-id="e7e32-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e7e32-107">**ClipUnion**</span><span class="sxs-lookup"><span data-stu-id="e7e32-107">**ClipUnion**</span></span>
</dt> <dd>

<span data-ttu-id="e7e32-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7e32-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e7e32-109">描述目前剪輯狀態的剪輯聯集旗標。</span><span class="sxs-lookup"><span data-stu-id="e7e32-109">Clip union flags that describe the current clip status.</span></span> <span data-ttu-id="e7e32-110">這個成員可以是下列其中一個或多個旗標：</span><span class="sxs-lookup"><span data-stu-id="e7e32-110">This member can be one or more of the following flags:</span></span>



| <span data-ttu-id="e7e32-111">值</span><span class="sxs-lookup"><span data-stu-id="e7e32-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="e7e32-112">意義</span><span class="sxs-lookup"><span data-stu-id="e7e32-112">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <span data-ttu-id="e7e32-113"><dt>**D3DCS \_ 全部**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e32-113"><dt>**D3DCS\_ALL**</dt></span></span> </dl>          | <span data-ttu-id="e7e32-114">所有剪輯旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="e7e32-114">Combination of all clip flags.</span></span><br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <span data-ttu-id="e7e32-115"><dt>**\_左 D3DCS**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e32-115"><dt>**D3DCS\_LEFT**</dt></span></span> </dl>       | <span data-ttu-id="e7e32-116">所有頂點都會由 [視圖] 的左平面裁剪。</span><span class="sxs-lookup"><span data-stu-id="e7e32-116">All vertices are clipped by the left plane of the viewing frustum.</span></span><br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <span data-ttu-id="e7e32-117"><dt>**D3DCS \_ RIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e32-117"><dt>**D3DCS\_RIGHT**</dt></span></span> </dl>    | <span data-ttu-id="e7e32-118">所有頂點都會由「視圖」分隔的右平面裁剪。</span><span class="sxs-lookup"><span data-stu-id="e7e32-118">All vertices are clipped by the right plane of the viewing frustum.</span></span><br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <span data-ttu-id="e7e32-119"><dt>**D3DCS \_ TOP**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e32-119"><dt>**D3DCS\_TOP**</dt></span></span> </dl>          | <span data-ttu-id="e7e32-120">所有頂點都是由「視圖」截斷的最上層平面所修剪。</span><span class="sxs-lookup"><span data-stu-id="e7e32-120">All vertices are clipped by the top plane of the viewing frustum.</span></span><br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <span data-ttu-id="e7e32-121"><dt>**D3DCS \_ 底部**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e32-121"><dt>**D3DCS\_BOTTOM**</dt></span></span> </dl> | <span data-ttu-id="e7e32-122">所有頂點都會由「視圖」分隔的下平面裁剪。</span><span class="sxs-lookup"><span data-stu-id="e7e32-122">All vertices are clipped by the bottom plane of the viewing frustum.</span></span><br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <span data-ttu-id="e7e32-123"><dt>**D3DCS \_ FRONT**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e32-123"><dt>**D3DCS\_FRONT**</dt></span></span> </dl>    | <span data-ttu-id="e7e32-124">所有頂點都是由「視圖」分隔的前平面所修剪。</span><span class="sxs-lookup"><span data-stu-id="e7e32-124">All vertices are clipped by the front plane of the viewing frustum.</span></span><br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <span data-ttu-id="e7e32-125"><dt>**D3DCS \_ 回來**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e32-125"><dt>**D3DCS\_BACK**</dt></span></span> </dl>       | <span data-ttu-id="e7e32-126">所有頂點都是由「視圖」分隔的背面平面所修剪。</span><span class="sxs-lookup"><span data-stu-id="e7e32-126">All vertices are clipped by the back plane of the viewing frustum.</span></span><br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <span data-ttu-id="e7e32-127"><dt>**D3DCS \_ PLANE0**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e32-127"><dt>**D3DCS\_PLANE0**</dt></span></span> </dl> | <span data-ttu-id="e7e32-128">應用程式定義的裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="e7e32-128">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <span data-ttu-id="e7e32-129"><dt>**D3DCS \_ PLANE1**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e32-129"><dt>**D3DCS\_PLANE1**</dt></span></span> </dl> | <span data-ttu-id="e7e32-130">應用程式定義的裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="e7e32-130">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <span data-ttu-id="e7e32-131"><dt>**D3DCS \_ PLANE2**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e32-131"><dt>**D3DCS\_PLANE2**</dt></span></span> </dl> | <span data-ttu-id="e7e32-132">應用程式定義的裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="e7e32-132">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <span data-ttu-id="e7e32-133"><dt>**D3DCS \_ PLANE3**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e32-133"><dt>**D3DCS\_PLANE3**</dt></span></span> </dl> | <span data-ttu-id="e7e32-134">應用程式定義的裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="e7e32-134">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <span data-ttu-id="e7e32-135"><dt>**D3DCS \_ PLANE4**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e32-135"><dt>**D3DCS\_PLANE4**</dt></span></span> </dl> | <span data-ttu-id="e7e32-136">應用程式定義的裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="e7e32-136">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <span data-ttu-id="e7e32-137"><dt>**D3DCS \_ PLANE5**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e32-137"><dt>**D3DCS\_PLANE5**</dt></span></span> </dl> | <span data-ttu-id="e7e32-138">應用程式定義的裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="e7e32-138">Application-defined clipping planes.</span></span><br/>                                 |



 

</dd> <dt>

<span data-ttu-id="e7e32-139">**ClipIntersection**</span><span class="sxs-lookup"><span data-stu-id="e7e32-139">**ClipIntersection**</span></span>
</dt> <dd>

<span data-ttu-id="e7e32-140">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7e32-140">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e7e32-141">描述目前剪輯狀態的剪輯交集旗標。</span><span class="sxs-lookup"><span data-stu-id="e7e32-141">Clip intersection flags that describe the current clip status.</span></span> <span data-ttu-id="e7e32-142">這個成員可以採用與 ClipUnion 相同的旗標。</span><span class="sxs-lookup"><span data-stu-id="e7e32-142">This member can take the same flags as ClipUnion.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7e32-143">備註</span><span class="sxs-lookup"><span data-stu-id="e7e32-143">Remarks</span></span>

<span data-ttu-id="e7e32-144">當 [**ProcessVertices**](/windows/desktop/api)、 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)或其他) 繪圖函式 (頂點處理期間啟用裁剪時，Direct3D 會計算每個頂點的剪輯代碼。</span><span class="sxs-lookup"><span data-stu-id="e7e32-144">When clipping is enabled during vertex processing (by [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), or other drawing functions), Direct3D computes a clip code for every vertex.</span></span> <span data-ttu-id="e7e32-145">剪輯程式碼是 D3DCS 位的組合 \_ \* 。</span><span class="sxs-lookup"><span data-stu-id="e7e32-145">The clip code is a combination of D3DCS\_\* bits.</span></span> <span data-ttu-id="e7e32-146">當頂點在特定裁剪平面之外時，會在裁剪程式碼中設定對應的位。</span><span class="sxs-lookup"><span data-stu-id="e7e32-146">When a vertex is outside a particular clipping plane, the corresponding bit is set in the clipping code.</span></span> <span data-ttu-id="e7e32-147">Direct3D 會使用具有 ClipUnion 和 ClipIntersection 成員的 **D3DCLIPSTATUS9** 來維護剪輯狀態。</span><span class="sxs-lookup"><span data-stu-id="e7e32-147">Direct3D maintains the clip status using **D3DCLIPSTATUS9**, which has ClipUnion and ClipIntersection members.</span></span> <span data-ttu-id="e7e32-148">ClipUnion 是所有頂點剪輯代碼的位 OR，而 ClipIntersection 是所有頂點剪輯代碼的位 AND。</span><span class="sxs-lookup"><span data-stu-id="e7e32-148">ClipUnion is a bitwise OR of all vertex clip codes and ClipIntersection is a bitwise AND of all vertex clip codes.</span></span> <span data-ttu-id="e7e32-149">ClipUnion 的初始值為零，而 ClipIntersection 的值為0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="e7e32-149">Initial values are zero for ClipUnion and 0xFFFFFFFF for ClipIntersection.</span></span> <span data-ttu-id="e7e32-150">當 D3DRS \_ 剪切設定為 **FALSE** 時，ClipUnion 和 ClipIntersection 會設定為零。</span><span class="sxs-lookup"><span data-stu-id="e7e32-150">When D3DRS\_CLIPPING is set to **FALSE**, ClipUnion and ClipIntersection are set to zero.</span></span> <span data-ttu-id="e7e32-151">Direct3D 會在繪製呼叫期間更新剪輯狀態。</span><span class="sxs-lookup"><span data-stu-id="e7e32-151">Direct3D updates the clip status during drawing calls.</span></span> <span data-ttu-id="e7e32-152">若要計算特定物件的剪輯狀態，請將 ClipUnion 和 ClipIntersection 設定為初始值並繼續繪製。</span><span class="sxs-lookup"><span data-stu-id="e7e32-152">To compute clip status for a particular object, set ClipUnion and ClipIntersection to their initial value and continue drawing.</span></span>

<span data-ttu-id="e7e32-153">[**DrawRectPatch**](/windows/desktop/api)和 [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)不會更新剪輯狀態，因為它們沒有軟體模擬。</span><span class="sxs-lookup"><span data-stu-id="e7e32-153">Clip status is not updated by [**DrawRectPatch**](/windows/desktop/api) and [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) because there is no software emulation for them.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7e32-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7e32-154">Requirements</span></span>



| <span data-ttu-id="e7e32-155">需求</span><span class="sxs-lookup"><span data-stu-id="e7e32-155">Requirement</span></span> | <span data-ttu-id="e7e32-156">值</span><span class="sxs-lookup"><span data-stu-id="e7e32-156">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e32-157">標頭</span><span class="sxs-lookup"><span data-stu-id="e7e32-157">Header</span></span><br/> | <dl> <span data-ttu-id="e7e32-158"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7e32-158"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7e32-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7e32-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e32-160">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="e7e32-160">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="e7e32-161">**GetClipStatus**</span><span class="sxs-lookup"><span data-stu-id="e7e32-161">**GetClipStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[<span data-ttu-id="e7e32-162">**SetClipStatus**</span><span class="sxs-lookup"><span data-stu-id="e7e32-162">**SetClipStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
