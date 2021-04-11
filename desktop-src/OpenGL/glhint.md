---
title: 'glHint 函式 (Gl) '
description: GlHint 函式會指定實作為特定的提示。
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- glHint 函式 OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2772c76868c741660486184e5ab51bd193d3667a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094147"
---
# <a name="glhint-function"></a><span data-ttu-id="6de74-104">glHint 函式</span><span class="sxs-lookup"><span data-stu-id="6de74-104">glHint function</span></span>

<span data-ttu-id="6de74-105">**GlHint** 函式會指定實作為特定的提示。</span><span class="sxs-lookup"><span data-stu-id="6de74-105">The **glHint** function specifies implementation-specific hints.</span></span>

## <a name="syntax"></a><span data-ttu-id="6de74-106">語法</span><span class="sxs-lookup"><span data-stu-id="6de74-106">Syntax</span></span>


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="6de74-107">參數</span><span class="sxs-lookup"><span data-stu-id="6de74-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6de74-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="6de74-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="6de74-109">指出要控制之行為的符號常數。</span><span class="sxs-lookup"><span data-stu-id="6de74-109">A symbolic constant indicating the behavior to be controlled.</span></span> <span data-ttu-id="6de74-110">接受下列符號常數以及建議的語法。</span><span class="sxs-lookup"><span data-stu-id="6de74-110">The following symbolic constants, along with suggested semantics, are accepted.</span></span>



| <span data-ttu-id="6de74-111">值</span><span class="sxs-lookup"><span data-stu-id="6de74-111">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="6de74-112">意義</span><span class="sxs-lookup"><span data-stu-id="6de74-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <span data-ttu-id="6de74-113"><dt>**GL \_ 霧化 \_ 提示**</dt></span><span class="sxs-lookup"><span data-stu-id="6de74-113"><dt>**GL\_FOG\_HINT**</dt></span></span> </dl>                                                           | <span data-ttu-id="6de74-114">表示霧化計算的精確度。</span><span class="sxs-lookup"><span data-stu-id="6de74-114">Indicates the accuracy of fog calculation.</span></span> <span data-ttu-id="6de74-115">如果 OpenGL 執行不能有效率地支援每個圖元的霧化計算，則提示 GL 不 \_ \_ 在意或 GL \_ 最快可能會導致每個頂點的霧化效果計算。</span><span class="sxs-lookup"><span data-stu-id="6de74-115">If per-pixel fog calculation is not efficiently supported by the OpenGL implementation, hinting GL\_DONT\_CARE or GL\_FASTEST can result in per-vertex calculation of fog effects.</span></span><br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <span data-ttu-id="6de74-116"><dt>**GL \_ 行 \_ 平滑 \_ 提示**</dt></span><span class="sxs-lookup"><span data-stu-id="6de74-116"><dt>**GL\_LINE\_SMOOTH\_HINT**</dt></span></span> </dl>                                  | <span data-ttu-id="6de74-117">指出反鋸齒線條的取樣品質。</span><span class="sxs-lookup"><span data-stu-id="6de74-117">Indicates the sampling quality of antialiased lines.</span></span> <span data-ttu-id="6de74-118">如果套用 \_ 較大的篩選函式，提示 GL 最好可能會導致在點陣化期間產生更多圖元片段。</span><span class="sxs-lookup"><span data-stu-id="6de74-118">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <span data-ttu-id="6de74-119"><dt>**GL \_ 透視圖 \_ 校正 \_ 提示**</dt></span><span class="sxs-lookup"><span data-stu-id="6de74-119"><dt>**GL\_PERSPECTIVE\_CORRECTION\_HINT**</dt></span></span> </dl> | <span data-ttu-id="6de74-120">指出色彩和材質座標插補的品質。</span><span class="sxs-lookup"><span data-stu-id="6de74-120">Indicates the quality of color and texture coordinate interpolation.</span></span> <span data-ttu-id="6de74-121">如果 OpenGL 修正程式未有效率地支援以觀點校正的參數插補，則提示 GL 不 \_ \_ 在意或 GL 最快的方式， \_ 會導致色彩和/或紋理座標的簡單線性插補。</span><span class="sxs-lookup"><span data-stu-id="6de74-121">If perspective-corrected parameter interpolation is not efficiently supported by the OpenGL implementation, hinting GL\_DONT\_CARE or GL\_FASTEST can result in simple linear interpolation of colors and/or texture coordinates.</span></span><br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <span data-ttu-id="6de74-122"><dt>**GL \_ 點 \_ 平滑 \_ 提示**</dt></span><span class="sxs-lookup"><span data-stu-id="6de74-122"><dt>**GL\_POINT\_SMOOTH\_HINT**</dt></span></span> </dl>                               | <span data-ttu-id="6de74-123">指出反鋸齒點的取樣品質。</span><span class="sxs-lookup"><span data-stu-id="6de74-123">Indicates the sampling quality of antialiased points.</span></span> <span data-ttu-id="6de74-124">如果套用 \_ 較大的篩選函式，提示 GL 最好可能會導致在點陣化期間產生更多圖元片段。</span><span class="sxs-lookup"><span data-stu-id="6de74-124">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <span data-ttu-id="6de74-125"><dt>**GL \_ 多邊形 \_ 平滑 \_ 提示**</dt></span><span class="sxs-lookup"><span data-stu-id="6de74-125"><dt>**GL\_POLYGON\_SMOOTH\_HINT**</dt></span></span> </dl>                         | <span data-ttu-id="6de74-126">指出反鋸齒多邊形的取樣品質。</span><span class="sxs-lookup"><span data-stu-id="6de74-126">Indicates the sampling quality of antialiased polygons.</span></span> <span data-ttu-id="6de74-127">如果套用 \_ 較大的篩選函式，提示 GL 最好可能會導致在點陣化期間產生更多圖元片段。</span><span class="sxs-lookup"><span data-stu-id="6de74-127">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="6de74-128">*mode*</span><span class="sxs-lookup"><span data-stu-id="6de74-128">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="6de74-129">表示所需行為的符號常數。</span><span class="sxs-lookup"><span data-stu-id="6de74-129">A symbolic constant indicating the desired behavior.</span></span> <span data-ttu-id="6de74-130">接受下列符號常數。</span><span class="sxs-lookup"><span data-stu-id="6de74-130">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="6de74-131">值</span><span class="sxs-lookup"><span data-stu-id="6de74-131">Value</span></span>                                                                                                                                                       | <span data-ttu-id="6de74-132">意義</span><span class="sxs-lookup"><span data-stu-id="6de74-132">Meaning</span></span>                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <span data-ttu-id="6de74-133"><dt>**GL \_ 最快**</dt></span><span class="sxs-lookup"><span data-stu-id="6de74-133"><dt>**GL\_FASTEST**</dt></span></span> </dl>        | <span data-ttu-id="6de74-134">您應該選擇最有效率的選項。</span><span class="sxs-lookup"><span data-stu-id="6de74-134">The most efficient option should be chosen.</span></span><br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <span data-ttu-id="6de74-135"><dt>**GL \_ 最好**</dt></span><span class="sxs-lookup"><span data-stu-id="6de74-135"><dt>**GL\_NICEST**</dt></span></span> </dl>           | <span data-ttu-id="6de74-136">您應該選擇最正確或最高品質的選項。</span><span class="sxs-lookup"><span data-stu-id="6de74-136">The most correct, or highest quality, option should be chosen.</span></span><br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <span data-ttu-id="6de74-137"><dt>**GL \_ 別 \_ 在意**</dt></span><span class="sxs-lookup"><span data-stu-id="6de74-137"><dt>**GL\_DONT\_CARE**</dt></span></span> </dl> | <span data-ttu-id="6de74-138">用戶端沒有喜好設定。</span><span class="sxs-lookup"><span data-stu-id="6de74-138">The client doesn't have a preference.</span></span><br/>                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6de74-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="6de74-139">Return value</span></span>

<span data-ttu-id="6de74-140">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6de74-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6de74-141">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="6de74-141">Error codes</span></span>

<span data-ttu-id="6de74-142">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6de74-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6de74-143">Name</span><span class="sxs-lookup"><span data-stu-id="6de74-143">Name</span></span>                                                                                                  | <span data-ttu-id="6de74-144">意義</span><span class="sxs-lookup"><span data-stu-id="6de74-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6de74-145"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="6de74-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="6de74-146">*目標* 或 *模式* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="6de74-146">*target* or *mode* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="6de74-147"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="6de74-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6de74-148">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="6de74-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6de74-149">備註</span><span class="sxs-lookup"><span data-stu-id="6de74-149">Remarks</span></span>

<span data-ttu-id="6de74-150">當有足夠的解讀空間時，您可以使用提示來控制 OpenGL 行為的特定層面。</span><span class="sxs-lookup"><span data-stu-id="6de74-150">When there is room for interpretation, you can control certain aspects of OpenGL behavior with hints.</span></span> <span data-ttu-id="6de74-151">您可以指定具有兩個引數的提示。</span><span class="sxs-lookup"><span data-stu-id="6de74-151">You specify a hint with two arguments.</span></span> <span data-ttu-id="6de74-152">*目標* 參數是指出要控制之行為的符號常數，而 *模式* 則是另一個指出所需行為的符號常數。</span><span class="sxs-lookup"><span data-stu-id="6de74-152">The *target* parameter is a symbolic constant indicating the behavior to be controlled, and *mode* is another symbolic constant indicating the desired behavior.</span></span>

<span data-ttu-id="6de74-153">雖然可以提示的實方面是妥善定義的，但提示的解讀取決於執行。</span><span class="sxs-lookup"><span data-stu-id="6de74-153">Though the implementation aspects that can be hinted are well defined, the interpretation of the hints depends on the implementation.</span></span>

<span data-ttu-id="6de74-154">可以忽略 **glHint** 函數。</span><span class="sxs-lookup"><span data-stu-id="6de74-154">The **glHint** function can be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="6de74-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="6de74-155">Requirements</span></span>



| <span data-ttu-id="6de74-156">需求</span><span class="sxs-lookup"><span data-stu-id="6de74-156">Requirement</span></span> | <span data-ttu-id="6de74-157">值</span><span class="sxs-lookup"><span data-stu-id="6de74-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6de74-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6de74-158">Minimum supported client</span></span><br/> | <span data-ttu-id="6de74-159">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6de74-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6de74-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6de74-160">Minimum supported server</span></span><br/> | <span data-ttu-id="6de74-161">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6de74-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6de74-162">標頭</span><span class="sxs-lookup"><span data-stu-id="6de74-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="6de74-163"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="6de74-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6de74-164">程式庫</span><span class="sxs-lookup"><span data-stu-id="6de74-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="6de74-165"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6de74-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6de74-166">DLL</span><span class="sxs-lookup"><span data-stu-id="6de74-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6de74-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6de74-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de74-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6de74-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de74-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6de74-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6de74-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6de74-170">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





