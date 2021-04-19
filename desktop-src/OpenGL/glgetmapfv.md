---
title: 'glGetMapfv 函式 (Gl) '
description: 'GlGetMapdv、glGetMapfv 和 glGetMapiv 函數會傳回評估工具參數。 |glGetMapfv 函式 (Gl) '
ms.assetid: dc93e468-7b76-4b5d-a46c-63920ed05568
keywords:
- glGetMapfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02129e9637333fb36265ce9f7b631d6cb3377d0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981777"
---
# <a name="glgetmapfv-function"></a><span data-ttu-id="d38fb-105">glGetMapfv 函式</span><span class="sxs-lookup"><span data-stu-id="d38fb-105">glGetMapfv function</span></span>

<span data-ttu-id="d38fb-106">[**GlGetMapdv**](glgetmapdv.md)、 **glGetMapfv** 和 [**glGetMapiv**](glgetmapiv.md)函數會傳回評估工具參數。</span><span class="sxs-lookup"><span data-stu-id="d38fb-106">The [**glGetMapdv**](glgetmapdv.md), **glGetMapfv**, and [**glGetMapiv**](glgetmapiv.md) functions return evaluator parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="d38fb-107">語法</span><span class="sxs-lookup"><span data-stu-id="d38fb-107">Syntax</span></span>


```C++
void WINAPI glGetMapfv(
   GLenum  target,
   GLenum  query,
   GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="d38fb-108">參數</span><span class="sxs-lookup"><span data-stu-id="d38fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d38fb-109">*目標*</span><span class="sxs-lookup"><span data-stu-id="d38fb-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="d38fb-110">地圖的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="d38fb-110">The symbolic name of a map.</span></span> <span data-ttu-id="d38fb-111">以下是接受的值： GL \_ MAP1 \_ COLOR \_ 4、gl \_ MAP1 \_ INDEX、gl \_ MAP1 \_ NORMAL、gl \_ MAP1 \_ 材質 \_ COORD \_ 1、gl \_ MAP1 \_ 材質 \_ COORD \_ 2、gl \_ MAP1 \_ 材質 \_ COORD \_ 3、gl \_ MAP1 \_ 材質 \_ COORD \_ 4、GL \_ MAP1 \_ 頂點 \_ 3、gl \_ MAP1 \_ 頂點 \_ 4、gl \_ LIST.MAP2 \_ COLOR \_ 4、GL \_ List.map2 \_ INDEX、gl \_ list.map2 \_ NORMAL、gl \_ list.map2 \_ 材質 \_ COORD \_ 1、gl \_ list.map2 \_ 材質 \_ COORD \_ 2、gl \_ list.map2 \_ 材質 \_ COORD \_ 3、gl list.map2 材質 COORD \_ \_ \_ \_ 4、gl \_ list.map2 \_ 頂點 \_ 3 和 gl \_ list.map2 \_ 頂點 \_ 4。</span><span class="sxs-lookup"><span data-stu-id="d38fb-111">The following are accepted values: GL\_MAP1\_COLOR\_4, GL\_MAP1\_INDEX, GL\_MAP1\_NORMAL, GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP1\_VERTEX\_3, GL\_MAP1\_VERTEX\_4, GL\_MAP2\_COLOR\_4, GL\_MAP2\_INDEX, GL\_MAP2\_NORMAL, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, GL\_MAP2\_TEXTURE\_COORD\_4, GL\_MAP2\_VERTEX\_3, and GL\_MAP2\_VERTEX\_4.</span></span>

</dd> <dt>

<span data-ttu-id="d38fb-112">*查詢*</span><span class="sxs-lookup"><span data-stu-id="d38fb-112">*query*</span></span> 
</dt> <dd>

<span data-ttu-id="d38fb-113">指定要傳回的參數。</span><span class="sxs-lookup"><span data-stu-id="d38fb-113">Specifies which parameter to return.</span></span> <span data-ttu-id="d38fb-114">接受下列符號名稱。</span><span class="sxs-lookup"><span data-stu-id="d38fb-114">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="d38fb-115">值</span><span class="sxs-lookup"><span data-stu-id="d38fb-115">Value</span></span>                                                                                                                                             | <span data-ttu-id="d38fb-116">意義</span><span class="sxs-lookup"><span data-stu-id="d38fb-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <span data-ttu-id="d38fb-117"><dt>**GL \_ COEFF**</dt></span><span class="sxs-lookup"><span data-stu-id="d38fb-117"><dt>**GL\_COEFF**</dt></span></span> </dl>    | <span data-ttu-id="d38fb-118">*V* 參數會傳回評估工具函數的控制點。</span><span class="sxs-lookup"><span data-stu-id="d38fb-118">The *v* parameter returns the control points for the evaluator function.</span></span> <span data-ttu-id="d38fb-119">一維評估工具會傳回 *順序* 控制點，而二維評估工具會傳回 *uorder* *x* *vorder* 控制點。</span><span class="sxs-lookup"><span data-stu-id="d38fb-119">One-dimensional evaluators return *order* control points, and two-dimensional evaluators return *uorder* *x* *vorder* control points.</span></span> <span data-ttu-id="d38fb-120">每個控制點都包含一個、兩個、三個或四個整數、單精確度浮點數或雙精確度浮點值（視評估工具的類型而定）。</span><span class="sxs-lookup"><span data-stu-id="d38fb-120">Each control point consists of one, two, three, or four integer, single-precision floating-point, or double-precision floating-point values, depending on the type of the evaluator.</span></span> <span data-ttu-id="d38fb-121">二維控制點會以資料列主要順序傳回、快速遞增 *uorder* 索引，以及每個資料列之後的 *vorder* 索引。</span><span class="sxs-lookup"><span data-stu-id="d38fb-121">Two-dimensional control points are returned in row-major order, incrementing the *uorder* index quickly, and the *vorder* index after each row.</span></span> <span data-ttu-id="d38fb-122">在要求時，整數值會藉由將內部浮點值四捨五入為最接近的整數值來計算。</span><span class="sxs-lookup"><span data-stu-id="d38fb-122">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <span data-ttu-id="d38fb-123"><dt>**GL \_ 訂單**</dt></span><span class="sxs-lookup"><span data-stu-id="d38fb-123"><dt>**GL\_ORDER**</dt></span></span> </dl>    | <span data-ttu-id="d38fb-124">*V* 參數會傳回評估工具函數的順序。</span><span class="sxs-lookup"><span data-stu-id="d38fb-124">The *v* parameter returns the order of the evaluator function.</span></span> <span data-ttu-id="d38fb-125">一維評估工具會傳回單一值、 *order*。</span><span class="sxs-lookup"><span data-stu-id="d38fb-125">One-dimensional evaluators return a single value, *order*.</span></span> <span data-ttu-id="d38fb-126">二維評估工具會傳回兩個值： *uorder* 和 *vorder*。</span><span class="sxs-lookup"><span data-stu-id="d38fb-126">Two-dimensional evaluators return two values, *uorder* and *vorder*.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <span data-ttu-id="d38fb-127"><dt>**GL \_ 網域**</dt></span><span class="sxs-lookup"><span data-stu-id="d38fb-127"><dt>**GL\_DOMAIN**</dt></span></span> </dl> | <span data-ttu-id="d38fb-128">*V* 參數會傳回線性 *u* 和 *v* 對應參數。</span><span class="sxs-lookup"><span data-stu-id="d38fb-128">The *v* parameter returns the linear *u* and *v* mapping parameters.</span></span> <span data-ttu-id="d38fb-129">一維評估工具會傳回兩個值，例如 *u* 1 和 *u* 2，如 [**glMap1**](glmap1.md)所指定。</span><span class="sxs-lookup"><span data-stu-id="d38fb-129">One-dimensional evaluators return two values, *u* 1 and *u* 2, as specified by [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="d38fb-130">二維評估工具會傳回四個值 (*u1*、 *u2*、 *V1* 和 *v2*) 如 [**glMap2**](glmap2.md)所指定。</span><span class="sxs-lookup"><span data-stu-id="d38fb-130">Two-dimensional evaluators return four values (*u1*, *u2*, *v1*, and *v2*) as specified by [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="d38fb-131">在要求時，整數值會藉由將內部浮點值四捨五入為最接近的整數值來計算。</span><span class="sxs-lookup"><span data-stu-id="d38fb-131">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="d38fb-132">*V*</span><span class="sxs-lookup"><span data-stu-id="d38fb-132">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="d38fb-133">傳回要求的資料。</span><span class="sxs-lookup"><span data-stu-id="d38fb-133">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d38fb-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="d38fb-134">Return value</span></span>

<span data-ttu-id="d38fb-135">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d38fb-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d38fb-136">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d38fb-136">Error codes</span></span>

<span data-ttu-id="d38fb-137">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d38fb-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d38fb-138">Name</span><span class="sxs-lookup"><span data-stu-id="d38fb-138">Name</span></span>                                                                                                  | <span data-ttu-id="d38fb-139">意義</span><span class="sxs-lookup"><span data-stu-id="d38fb-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d38fb-140"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="d38fb-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d38fb-141">*目標* 或 *查詢* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="d38fb-141">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="d38fb-142"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="d38fb-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d38fb-143">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="d38fb-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d38fb-144">備註</span><span class="sxs-lookup"><span data-stu-id="d38fb-144">Remarks</span></span>

<span data-ttu-id="d38fb-145">**GlGetMap** 函數會傳回評估工具參數。</span><span class="sxs-lookup"><span data-stu-id="d38fb-145">The **glGetMap** function returns evaluator parameters.</span></span> <span data-ttu-id="d38fb-146"> (**glMap1** 和 **glMap2** 函式定義評估工具。 ) *target* 參數指定對應， *查詢* 會選取特定的參數，而 *v* 指向將傳回值的儲存區。</span><span class="sxs-lookup"><span data-stu-id="d38fb-146">(The **glMap1** and **glMap2** functions define evaluators.) The *target* parameter specifies a map, *query* selects a specific parameter, and *v* points to storage where the values will be returned.</span></span>

<span data-ttu-id="d38fb-147">[**GlMap1**](glmap1.md)和 [**glMap2**](glmap2.md)會說明 *目標* 參數可接受的值。</span><span class="sxs-lookup"><span data-stu-id="d38fb-147">The acceptable values for the *target* parameter are described in [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="d38fb-148">如果產生錯誤，則不會對 *v* 內容進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="d38fb-148">If an error is generated, no change is made to the contents of *v*.</span></span>

## <a name="requirements"></a><span data-ttu-id="d38fb-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="d38fb-149">Requirements</span></span>



| <span data-ttu-id="d38fb-150">需求</span><span class="sxs-lookup"><span data-stu-id="d38fb-150">Requirement</span></span> | <span data-ttu-id="d38fb-151">值</span><span class="sxs-lookup"><span data-stu-id="d38fb-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d38fb-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d38fb-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d38fb-153">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d38fb-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d38fb-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d38fb-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d38fb-155">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d38fb-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d38fb-156">標頭</span><span class="sxs-lookup"><span data-stu-id="d38fb-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="d38fb-157"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="d38fb-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d38fb-158">程式庫</span><span class="sxs-lookup"><span data-stu-id="d38fb-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="d38fb-159"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d38fb-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d38fb-160">DLL</span><span class="sxs-lookup"><span data-stu-id="d38fb-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d38fb-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d38fb-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d38fb-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d38fb-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d38fb-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d38fb-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d38fb-164">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d38fb-164">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d38fb-165">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="d38fb-165">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="d38fb-166">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="d38fb-166">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="d38fb-167">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="d38fb-167">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





