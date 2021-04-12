---
title: 'gluNextContour 函式 (X.glu 隊) '
description: GluNextContour 函式會將另一個輪廓的開頭標示為開頭。
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- gluNextContour 函式 OpenGL
topic_type:
- apiref
api_name:
- gluNextContour
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b798eba50205053c019e3e8d1708c9ed834e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384250"
---
# <a name="glunextcontour-function"></a><span data-ttu-id="f612d-104">gluNextContour 函式</span><span class="sxs-lookup"><span data-stu-id="f612d-104">gluNextContour function</span></span>

<span data-ttu-id="f612d-105">\[**GluNextContour** 函式已過時，而且只為了回溯相容性而提供。</span><span class="sxs-lookup"><span data-stu-id="f612d-105">\[The **gluNextContour** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="f612d-106">**GluNextContour** 函式會對應到 [**gluTessEndContour**](glutessendcontour.md) ，後面接著 [**gluTessBeginContour**](glutessbegincontour.md)。\]</span><span class="sxs-lookup"><span data-stu-id="f612d-106">The **gluNextContour** function is mapped to [**gluTessEndContour**](glutessendcontour.md) followed by [**gluTessBeginContour**](glutessbegincontour.md).\]</span></span>

<span data-ttu-id="f612d-107">**GluNextContour** 函式會將另一個輪廓的開頭標示為開頭。</span><span class="sxs-lookup"><span data-stu-id="f612d-107">The **gluNextContour** function marks the beginning of another contour.</span></span>

## <a name="syntax"></a><span data-ttu-id="f612d-108">語法</span><span class="sxs-lookup"><span data-stu-id="f612d-108">Syntax</span></span>


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a><span data-ttu-id="f612d-109">參數</span><span class="sxs-lookup"><span data-stu-id="f612d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f612d-110">*苔 絲*</span><span class="sxs-lookup"><span data-stu-id="f612d-110">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="f612d-111">使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。</span><span class="sxs-lookup"><span data-stu-id="f612d-111">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="f612d-112">*type*</span><span class="sxs-lookup"><span data-stu-id="f612d-112">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="f612d-113">要定義的輪廓類型。</span><span class="sxs-lookup"><span data-stu-id="f612d-113">The type of the contour being defined.</span></span> <span data-ttu-id="f612d-114">下列是有效的值。</span><span class="sxs-lookup"><span data-stu-id="f612d-114">The following values are valid.</span></span>



| <span data-ttu-id="f612d-115">值</span><span class="sxs-lookup"><span data-stu-id="f612d-115">Value</span></span>                                                                                                                                                                | <span data-ttu-id="f612d-116">意義</span><span class="sxs-lookup"><span data-stu-id="f612d-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <span data-ttu-id="f612d-117"><dt>**X.GLU 隊 \_ 外部**</dt></span><span class="sxs-lookup"><span data-stu-id="f612d-117"><dt>**GLU\_EXTERIOR**</dt></span></span> </dl>           | <span data-ttu-id="f612d-118">外輪廓定義多邊形的外部界限。</span><span class="sxs-lookup"><span data-stu-id="f612d-118">An exterior contour defines an exterior boundary of the polygon.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <span data-ttu-id="f612d-119"><dt>**X.GLU 隊 \_ 內部**</dt></span><span class="sxs-lookup"><span data-stu-id="f612d-119"><dt>**GLU\_INTERIOR**</dt></span></span> </dl>           | <span data-ttu-id="f612d-120">內部輪廓會定義多邊形 (的內部界限，例如洞) 。</span><span class="sxs-lookup"><span data-stu-id="f612d-120">An interior contour defines an interior boundary of the polygon (such as a hole).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <span data-ttu-id="f612d-121"><dt>**X.GLU 隊 \_ 不明**</dt></span><span class="sxs-lookup"><span data-stu-id="f612d-121"><dt>**GLU\_UNKNOWN**</dt></span></span> </dl>              | <span data-ttu-id="f612d-122">程式庫會分析未知的輪廓，以判斷其是否為內部或外部。</span><span class="sxs-lookup"><span data-stu-id="f612d-122">An unknown contour is analyzed by the library to determine whether it is interior or exterior.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <span data-ttu-id="f612d-123"><dt>**X.GLU 隊 \_ CCW，X.GLU 隊 \_ CW**</dt></span><span class="sxs-lookup"><span data-stu-id="f612d-123"><dt>**GLU\_CCW, GLU\_CW**</dt></span></span> </dl> | <span data-ttu-id="f612d-124">第一個定義的 X.GLU 隊 \_ CCW 或 X.glu 隊 \_ CW 分布圖會視為外部。</span><span class="sxs-lookup"><span data-stu-id="f612d-124">The first GLU\_CCW or GLU\_CW contour defined is considered to be exterior.</span></span> <span data-ttu-id="f612d-125">如果所有其他的輪廓都是以相同方向進行導向， (順時針或逆時針) 作為第一個輪廓，如果不是，則會被視為外部。</span><span class="sxs-lookup"><span data-stu-id="f612d-125">All other contours are considered to be exterior if they are oriented in the same direction (clockwise or counterclockwise) as the first contour, and interior if they are not.</span></span><br/> <span data-ttu-id="f612d-126">如果某個輪廓的類型為 X.GLU 隊 \_ CCW 或 X.glu 隊 \_ CW，則所有的輪廓都必須是相同類型 (如果不是，則所有 x.glu 隊 \_ CCW 和 x.glu 隊 \_ 的 CW 分佈將會變更為 x.glu 隊 \_ 未知) 。</span><span class="sxs-lookup"><span data-stu-id="f612d-126">If one contour is of type GLU\_CCW or GLU\_CW, then all contours must be of the same type (if they are not, then all GLU\_CCW and GLU\_CW contours will be changed to GLU\_UNKNOWN).</span></span> <span data-ttu-id="f612d-127">請注意，X.GLU 隊 \_ CCW 和 x.glu 隊的 CW 分佈類型之間沒有真正的差異 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f612d-127">Note that there is no real difference between the GLU\_CCW and GLU\_CW contour types.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f612d-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="f612d-128">Return value</span></span>

<span data-ttu-id="f612d-129">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f612d-129">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f612d-130">備註</span><span class="sxs-lookup"><span data-stu-id="f612d-130">Remarks</span></span>

<span data-ttu-id="f612d-131">您可以使用 **gluNextContour** 函數來描述具有多個分佈的多邊形。</span><span class="sxs-lookup"><span data-stu-id="f612d-131">Use the **gluNextContour** function to describe polygons with multiple contours.</span></span> <span data-ttu-id="f612d-132">當您透過一連串的 [**gluTessVertex**](glutessvertex.md) 呼叫來描述第一個輪廓之後， **gluNextContour** 呼叫會指出先前的輪廓已完成，而且下一個輪廓即將開始。</span><span class="sxs-lookup"><span data-stu-id="f612d-132">After you describe the first contour through a series of [**gluTessVertex**](glutessvertex.md) calls, a **gluNextContour** call indicates that the previous contour is complete and that the next contour is about to begin.</span></span> <span data-ttu-id="f612d-133">執行另一系列的 **gluTessVertex** 呼叫來描述新的輪廓。</span><span class="sxs-lookup"><span data-stu-id="f612d-133">Perform another series of **gluTessVertex** calls to describe the new contour.</span></span> <span data-ttu-id="f612d-134">重複此程式，直到描述所有的輪廓為止。</span><span class="sxs-lookup"><span data-stu-id="f612d-134">Repeat this process until all contours have been described.</span></span>

<span data-ttu-id="f612d-135">*Type* 參數會定義其後的輪廓類型。</span><span class="sxs-lookup"><span data-stu-id="f612d-135">The *type* parameter defines what type of contour follows.</span></span>

<span data-ttu-id="f612d-136">若要定義第一個輪廓的型別，您可以在描述第一個輪廓之前呼叫 **gluNextContour** 。</span><span class="sxs-lookup"><span data-stu-id="f612d-136">To define the type of the first contour, you can call **gluNextContour** before describing the first contour.</span></span> <span data-ttu-id="f612d-137">如果您未在第一個輪廓之前呼叫 **gluNextContour** ，則會將第一個輪廓標示為 x.glu 隊 \_ 外部。</span><span class="sxs-lookup"><span data-stu-id="f612d-137">If you do not call **gluNextContour** before the first contour, the first contour is marked GLU\_EXTERIOR.</span></span>

## <a name="examples"></a><span data-ttu-id="f612d-138">範例</span><span class="sxs-lookup"><span data-stu-id="f612d-138">Examples</span></span>

<span data-ttu-id="f612d-139">您可以在其中描述具有三角形孔的四邊形，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f612d-139">You can describe a quadrilateral with a triangular hole in it as follows:</span></span>

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4);  
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7);  
gluEndPolygon(tess);
```

## <a name="requirements"></a><span data-ttu-id="f612d-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="f612d-140">Requirements</span></span>



| <span data-ttu-id="f612d-141">需求</span><span class="sxs-lookup"><span data-stu-id="f612d-141">Requirement</span></span> | <span data-ttu-id="f612d-142">值</span><span class="sxs-lookup"><span data-stu-id="f612d-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f612d-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f612d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f612d-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f612d-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f612d-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f612d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f612d-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f612d-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f612d-147">標頭</span><span class="sxs-lookup"><span data-stu-id="f612d-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="f612d-148"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="f612d-148"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f612d-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="f612d-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="f612d-150"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f612d-150"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f612d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f612d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f612d-152"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f612d-152"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f612d-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f612d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f612d-154">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="f612d-154">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="f612d-155">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="f612d-155">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="f612d-156">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="f612d-156">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="f612d-157">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="f612d-157">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="f612d-158">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="f612d-158">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="f612d-159">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="f612d-159">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





