---
title: 'gluPickMatrix 函式 (X.glu 隊) '
description: GluPickMatrix 函式會定義挑選區域。
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- gluPickMatrix 函式 OpenGL
topic_type:
- apiref
api_name:
- gluPickMatrix
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c54e62f82f52fedc7de7c7c4af1cd3ed1ccdf149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933889"
---
# <a name="glupickmatrix-function"></a><span data-ttu-id="b1808-104">gluPickMatrix 函式</span><span class="sxs-lookup"><span data-stu-id="b1808-104">gluPickMatrix function</span></span>

<span data-ttu-id="b1808-105">**GluPickMatrix** 函式會定義挑選區域。</span><span class="sxs-lookup"><span data-stu-id="b1808-105">The **gluPickMatrix** function defines a picking region.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1808-106">語法</span><span class="sxs-lookup"><span data-stu-id="b1808-106">Syntax</span></span>


```C++
void WINAPI gluPickMatrix(
   GLdouble x,
   GLdouble y,
   GLdouble height,
   GLdouble width,
   GLint    viewport[4]
);
```



## <a name="parameters"></a><span data-ttu-id="b1808-107">參數</span><span class="sxs-lookup"><span data-stu-id="b1808-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1808-108">*x*</span><span class="sxs-lookup"><span data-stu-id="b1808-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="b1808-109">挑選區域的 x 視窗座標。</span><span class="sxs-lookup"><span data-stu-id="b1808-109">The x window coordinate of a picking region.</span></span>

</dd> <dt>

<span data-ttu-id="b1808-110">*y*</span><span class="sxs-lookup"><span data-stu-id="b1808-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="b1808-111">挑選區域的 y 視窗座標。</span><span class="sxs-lookup"><span data-stu-id="b1808-111">The y window coordinate of a picking region.</span></span>

</dd> <dt>

<span data-ttu-id="b1808-112">*height* (高度)</span><span class="sxs-lookup"><span data-stu-id="b1808-112">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="b1808-113">視窗座標中挑選區域的高度。</span><span class="sxs-lookup"><span data-stu-id="b1808-113">The height of the picking region in window coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="b1808-114">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="b1808-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="b1808-115">視窗座標中挑選區域的寬度。</span><span class="sxs-lookup"><span data-stu-id="b1808-115">The width of the picking region in window coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="b1808-116">*視窗*</span><span class="sxs-lookup"><span data-stu-id="b1808-116">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="b1808-117">目前的視口 (為來自 [**glGetIntegerv**](glgetintegerv.md) 呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="b1808-117">The current viewport (as from a [**glGetIntegerv**](glgetintegerv.md) call).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1808-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1808-118">Return value</span></span>

<span data-ttu-id="b1808-119">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b1808-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1808-120">備註</span><span class="sxs-lookup"><span data-stu-id="b1808-120">Remarks</span></span>

<span data-ttu-id="b1808-121">**GluPickMatrix** 函式會建立一個投射矩陣，您可以用來將繪圖限制在一個社區域的區域。</span><span class="sxs-lookup"><span data-stu-id="b1808-121">The **gluPickMatrix** function creates a projection matrix you can use to restrict drawing to a small region of the viewport.</span></span>

1.  <span data-ttu-id="b1808-122">使用 **gluPickMatrix** 將繪圖限制在游標周圍的社區域。</span><span class="sxs-lookup"><span data-stu-id="b1808-122">Use **gluPickMatrix** to restrict drawing to a small region around the cursor.</span></span>
2.  <span data-ttu-id="b1808-123">使用 [**glRenderMode**](glrendermode.md)) 進入選取模式 (，然後 rerender 場景。</span><span class="sxs-lookup"><span data-stu-id="b1808-123">Enter selection mode (with [**glRenderMode**](glrendermode.md)), and then rerender the scene.</span></span>

    <span data-ttu-id="b1808-124">所有會在資料指標附近繪製的基本專案都會被識別並儲存在選取範圍緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="b1808-124">All primitives that would have been drawn near the cursor are identified and stored in the selection buffer.</span></span>

<span data-ttu-id="b1808-125">**GluPickMatrix** 所建立的矩陣會乘以目前的矩陣，就如同使用產生的矩陣來呼叫 [**glMultMatrix**](glmultmatrix.md)一樣。</span><span class="sxs-lookup"><span data-stu-id="b1808-125">The matrix created by **gluPickMatrix** is multiplied by the current matrix just as if [**glMultMatrix**](glmultmatrix.md) were called with the generated matrix.</span></span>

1.  <span data-ttu-id="b1808-126">呼叫 [**glLoadIdentity**](glloadidentity.md) 將識別矩陣載入至透視圖矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="b1808-126">Call [**glLoadIdentity**](glloadidentity.md) to load an identity matrix onto the perspective matrix stack.</span></span>
2.  <span data-ttu-id="b1808-127">呼叫 **gluPickMatrix**。</span><span class="sxs-lookup"><span data-stu-id="b1808-127">Call **gluPickMatrix**.</span></span>
3.  <span data-ttu-id="b1808-128">呼叫函數 (例如 [**gluPerspective**](gluperspective.md)) ，以將透視圖矩陣乘以挑選矩陣。</span><span class="sxs-lookup"><span data-stu-id="b1808-128">Call a function (such as [**gluPerspective**](gluperspective.md)) to multiply the perspective matrix by the pick matrix.</span></span>

<span data-ttu-id="b1808-129">使用 **gluPickMatrix** 挑選非統一的有理 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 時，請小心關閉 NURBS 屬性，x.glu 隊 \_ 自動 \_ 載入 \_ 矩陣。</span><span class="sxs-lookup"><span data-stu-id="b1808-129">When using **gluPickMatrix** to pick Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)), be careful to turn off the NURBS property, GLU\_AUTO\_LOAD\_MATRIX.</span></span> <span data-ttu-id="b1808-130">如果未關閉 X.GLU 隊 \_ 自動 \_ 載入 \_ 矩陣，任何轉譯的 NURBS 介面都會與挑選矩陣的細分方式不同，而不需要挑選矩陣。</span><span class="sxs-lookup"><span data-stu-id="b1808-130">If GLU\_AUTO\_LOAD\_MATRIX is not turned off, any NURBS surface rendered is subdivided differently with the pick matrix from how it was subdivided without the pick matrix.</span></span>

## <a name="examples"></a><span data-ttu-id="b1808-131">範例</span><span class="sxs-lookup"><span data-stu-id="b1808-131">Examples</span></span>

<span data-ttu-id="b1808-132">轉譯場景時，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b1808-132">When rendering a scene as follows:</span></span>


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



<span data-ttu-id="b1808-133">下列程式碼會選取部分的部分區：</span><span class="sxs-lookup"><span data-stu-id="b1808-133">the following code selects a portion of the viewport:</span></span>


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPickMatrix(x, y, width, height, viewport);  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



## <a name="requirements"></a><span data-ttu-id="b1808-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1808-134">Requirements</span></span>



| <span data-ttu-id="b1808-135">需求</span><span class="sxs-lookup"><span data-stu-id="b1808-135">Requirement</span></span> | <span data-ttu-id="b1808-136">值</span><span class="sxs-lookup"><span data-stu-id="b1808-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b1808-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1808-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b1808-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1808-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b1808-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1808-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b1808-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1808-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b1808-141">標頭</span><span class="sxs-lookup"><span data-stu-id="b1808-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1808-142"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1808-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="b1808-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="b1808-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="b1808-144"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1808-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b1808-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b1808-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1808-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1808-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1808-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1808-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1808-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b1808-148">**glGetIntegerv**</span></span>](glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="b1808-149">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="b1808-149">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="b1808-150">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="b1808-150">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="b1808-151">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="b1808-151">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="b1808-152">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="b1808-152">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





