---
title: 'glPixelZoom 函式 (Gl) '
description: GlPixelZoom 函式會指定圖元縮放因數。
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
keywords:
- glPixelZoom 函式 OpenGL
topic_type:
- apiref
api_name:
- glPixelZoom
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 065e1735ca0228046cfb08e2fb441d3cdc02af74
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106986006"
---
# <a name="glpixelzoom-function"></a><span data-ttu-id="ac782-104">glPixelZoom 函式</span><span class="sxs-lookup"><span data-stu-id="ac782-104">glPixelZoom function</span></span>

<span data-ttu-id="ac782-105">**GlPixelZoom** 函式會指定圖元縮放因數。</span><span class="sxs-lookup"><span data-stu-id="ac782-105">The **glPixelZoom** function specifies the pixel zoom factors.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac782-106">語法</span><span class="sxs-lookup"><span data-stu-id="ac782-106">Syntax</span></span>


```C++
void WINAPI glPixelZoom(
   GLfloat xfactor,
   GLfloat yfactor
);
```



## <a name="parameters"></a><span data-ttu-id="ac782-107">參數</span><span class="sxs-lookup"><span data-stu-id="ac782-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac782-108">*xfactor*</span><span class="sxs-lookup"><span data-stu-id="ac782-108">*xfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="ac782-109">圖元寫入作業的 *x* 縮放比例。</span><span class="sxs-lookup"><span data-stu-id="ac782-109">The *x* zoom factor for pixel write operations.</span></span>

</dd> <dt>

<span data-ttu-id="ac782-110">*yfactor*</span><span class="sxs-lookup"><span data-stu-id="ac782-110">*yfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="ac782-111">圖元寫入作業的 *y* 縮放係數。</span><span class="sxs-lookup"><span data-stu-id="ac782-111">The *y* zoom factor for pixel write operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac782-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac782-112">Return value</span></span>

<span data-ttu-id="ac782-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ac782-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ac782-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ac782-114">Error codes</span></span>

<span data-ttu-id="ac782-115">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ac782-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ac782-116">Name</span><span class="sxs-lookup"><span data-stu-id="ac782-116">Name</span></span>                                                                                                  | <span data-ttu-id="ac782-117">意義</span><span class="sxs-lookup"><span data-stu-id="ac782-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ac782-118"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="ac782-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ac782-119">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="ac782-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ac782-120">備註</span><span class="sxs-lookup"><span data-stu-id="ac782-120">Remarks</span></span>

<span data-ttu-id="ac782-121">**GlPixelZoom** 函式會指定 *x* 和 *y* 縮放因數的值。</span><span class="sxs-lookup"><span data-stu-id="ac782-121">The **glPixelZoom** function specifies values for the *x* and *y* zoom factors.</span></span> <span data-ttu-id="ac782-122">執行 [**glDrawPixels**](gldrawpixels.md) 或 [**glCopyPixels**](glcopypixels.md)時，如果 (*x*<sub>r</sub> ，*y*<sub>r</sub> ) 是目前的點陣位置，而指定的元素位於圖元矩形的第 *n* 個數據列和第 *m* 個數據行中，則其中心位於矩形中的圖元，而矩形的邊角為</span><span class="sxs-lookup"><span data-stu-id="ac782-122">During the execution of [**glDrawPixels**](gldrawpixels.md) or [**glCopyPixels**](glcopypixels.md), if (*x*<sub>r</sub> ,*y*<sub>r</sub> ) is the current raster position, and a given element is in the *n* th row and *m* th column of the pixel rectangle, then pixels whose centers are in the rectangle with corners at</span></span>

![顯示要取代之圖元位置的方程式。](images/pix05.png)

<span data-ttu-id="ac782-124">是取代的候選項目。</span><span class="sxs-lookup"><span data-stu-id="ac782-124">are candidates for replacement.</span></span> <span data-ttu-id="ac782-125">中心位於這個矩形區域底部或左邊緣的任何圖元也會一併修改。</span><span class="sxs-lookup"><span data-stu-id="ac782-125">Any pixel whose center lies on the bottom or left edge of this rectangular region is also modified.</span></span>

<span data-ttu-id="ac782-126">圖元縮放因數不限於正值。</span><span class="sxs-lookup"><span data-stu-id="ac782-126">Pixel zoom factors are not limited to positive values.</span></span> <span data-ttu-id="ac782-127">負縮放因數會反映目前點陣位置的結果影像。</span><span class="sxs-lookup"><span data-stu-id="ac782-127">Negative zoom factors reflect the resulting image about the current raster position.</span></span>

<span data-ttu-id="ac782-128">下列函式會取出與 **glPixelZoom** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="ac782-128">The following functions retrieve information related to **glPixelZoom**:</span></span>

<span data-ttu-id="ac782-129">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ ZOOM \_ X 的 glGet</span><span class="sxs-lookup"><span data-stu-id="ac782-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ZOOM\_X</span></span>

<span data-ttu-id="ac782-130">具有引數 GL \_ ZOOM \_ Y 的 glGet</span><span class="sxs-lookup"><span data-stu-id="ac782-130">**glGet** with argument GL\_ZOOM\_Y</span></span>

## <a name="requirements"></a><span data-ttu-id="ac782-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac782-131">Requirements</span></span>



| <span data-ttu-id="ac782-132">需求</span><span class="sxs-lookup"><span data-stu-id="ac782-132">Requirement</span></span> | <span data-ttu-id="ac782-133">值</span><span class="sxs-lookup"><span data-stu-id="ac782-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac782-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac782-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ac782-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac782-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ac782-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac782-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ac782-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac782-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ac782-138">標頭</span><span class="sxs-lookup"><span data-stu-id="ac782-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac782-139"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="ac782-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ac782-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="ac782-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac782-141"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac782-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ac782-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ac782-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac782-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac782-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac782-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac782-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac782-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ac782-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ac782-146">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="ac782-146">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="ac782-147">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="ac782-147">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="ac782-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ac782-148">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





