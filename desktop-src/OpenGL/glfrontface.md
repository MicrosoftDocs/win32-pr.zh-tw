---
title: 'glFrontFace 函式 (Gl) '
description: GlFrontFace 函式會定義正面和背面的多邊形。
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- glFrontFace 函式 OpenGL
topic_type:
- apiref
api_name:
- glFrontFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106fa40989f21e50eb738f1a218394e8e7e9b4bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935067"
---
# <a name="glfrontface-function"></a><span data-ttu-id="3059d-104">glFrontFace 函式</span><span class="sxs-lookup"><span data-stu-id="3059d-104">glFrontFace function</span></span>

<span data-ttu-id="3059d-105">**GlFrontFace** 函式會定義正面和背面的多邊形。</span><span class="sxs-lookup"><span data-stu-id="3059d-105">The **glFrontFace** function defines front-facing and back-facing polygons.</span></span>

## <a name="syntax"></a><span data-ttu-id="3059d-106">語法</span><span class="sxs-lookup"><span data-stu-id="3059d-106">Syntax</span></span>


```C++
void WINAPI glFrontFace(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="3059d-107">參數</span><span class="sxs-lookup"><span data-stu-id="3059d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3059d-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="3059d-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="3059d-109">正面多邊形的方向。</span><span class="sxs-lookup"><span data-stu-id="3059d-109">The orientation of front-facing polygons.</span></span> <span data-ttu-id="3059d-110">\_已接受 gl CW 和 gl \_ CCW。</span><span class="sxs-lookup"><span data-stu-id="3059d-110">GL\_CW and GL\_CCW are accepted.</span></span> <span data-ttu-id="3059d-111">預設值為 GL \_ CCW。</span><span class="sxs-lookup"><span data-stu-id="3059d-111">The default value is GL\_CCW.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3059d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3059d-112">Return value</span></span>

<span data-ttu-id="3059d-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3059d-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3059d-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3059d-114">Error codes</span></span>

<span data-ttu-id="3059d-115">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3059d-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3059d-116">Name</span><span class="sxs-lookup"><span data-stu-id="3059d-116">Name</span></span>                                                                                                  | <span data-ttu-id="3059d-117">意義</span><span class="sxs-lookup"><span data-stu-id="3059d-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3059d-118"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="3059d-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3059d-119">*模式* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="3059d-119">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="3059d-120"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="3059d-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3059d-121">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="3059d-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3059d-122">備註</span><span class="sxs-lookup"><span data-stu-id="3059d-122">Remarks</span></span>

<span data-ttu-id="3059d-123">在完全由不透明封閉表面組成的場景中，永遠不會看到背面的多邊形。</span><span class="sxs-lookup"><span data-stu-id="3059d-123">In a scene composed entirely of opaque closed surfaces, back-facing polygons are never visible.</span></span> <span data-ttu-id="3059d-124">排除這些隱藏的多邊形具有加速影像呈現的明顯優點。</span><span class="sxs-lookup"><span data-stu-id="3059d-124">Eliminating these invisible polygons has the obvious benefit of speeding up the rendering of the image.</span></span> <span data-ttu-id="3059d-125">您可以使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) （使用引數 GL 剔除臉部）來啟用和停用後置多邊形 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="3059d-125">You enable and disable elimination of back-facing polygons with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) using argument GL\_CULL\_FACE.</span></span>

<span data-ttu-id="3059d-126">將多邊形的座標投射到視窗座標時，會被視為具有順向繞組，如果在路徑的第一個頂點、第二個頂點等之後，最後一個頂點，最後再回到第一個頂點，則會以順向方向與多邊形內部移動。</span><span class="sxs-lookup"><span data-stu-id="3059d-126">The projection of a polygon to window coordinates is said to have clockwise winding if an imaginary object following the path from its first vertex, its second vertex, and so on, to its last vertex, and finally back to its first vertex, moves in a clockwise direction about the interior of the polygon.</span></span> <span data-ttu-id="3059d-127">如果在相同路徑後面的虛數物件以逆時針方向移動多邊形內部的方向，則會將多邊形的纏繞視為逆時針。</span><span class="sxs-lookup"><span data-stu-id="3059d-127">The polygon's winding is said to be counterclockwise if the imaginary object following the same path moves in a counterclockwise direction about the interior of the polygon.</span></span> <span data-ttu-id="3059d-128">**GlFrontFace** 函式會指定在視窗座標中具有順時針繞組的多邊形，或在視窗座標中以逆時針方式纏繞的多邊形，會被正面朝上。</span><span class="sxs-lookup"><span data-stu-id="3059d-128">The **glFrontFace** function specifies whether polygons with clockwise winding in window coordinates, or counterclockwise winding in window coordinates, are taken to be front-facing.</span></span> <span data-ttu-id="3059d-129">將 GL \_ CCW 傳遞至 *模式* 時，會選取逆時針多邊形作為正面的多邊形;GL \_ CW 會選取順時針多邊形作為正面的多邊形。</span><span class="sxs-lookup"><span data-stu-id="3059d-129">Passing GL\_CCW to *mode* selects counterclockwise polygons as front-facing; GL\_CW selects clockwise polygons as front-facing.</span></span> <span data-ttu-id="3059d-130">依預設，會將逆時針多邊形視為正面朝上。</span><span class="sxs-lookup"><span data-stu-id="3059d-130">By default, counterclockwise polygons are taken to be front-facing.</span></span>

<span data-ttu-id="3059d-131">下列函數會抓取 **glFrontface** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="3059d-131">The following function retrieves information about **glFrontface**:</span></span>

<span data-ttu-id="3059d-132">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 正面 \_ 臉部的 glGet</span><span class="sxs-lookup"><span data-stu-id="3059d-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FRONT\_FACE</span></span>

## <a name="requirements"></a><span data-ttu-id="3059d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="3059d-133">Requirements</span></span>



| <span data-ttu-id="3059d-134">需求</span><span class="sxs-lookup"><span data-stu-id="3059d-134">Requirement</span></span> | <span data-ttu-id="3059d-135">值</span><span class="sxs-lookup"><span data-stu-id="3059d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3059d-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3059d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3059d-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3059d-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3059d-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3059d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3059d-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3059d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3059d-140">標頭</span><span class="sxs-lookup"><span data-stu-id="3059d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3059d-141"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="3059d-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3059d-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="3059d-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="3059d-143"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3059d-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3059d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3059d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3059d-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3059d-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3059d-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3059d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3059d-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3059d-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3059d-148">**glCullFace**</span><span class="sxs-lookup"><span data-stu-id="3059d-148">**glCullFace**</span></span>](glcullface.md)
</dt> <dt>

[<span data-ttu-id="3059d-149">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="3059d-149">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="3059d-150">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="3059d-150">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="3059d-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3059d-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3059d-152">**glGet**</span><span class="sxs-lookup"><span data-stu-id="3059d-152">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="3059d-153">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="3059d-153">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





