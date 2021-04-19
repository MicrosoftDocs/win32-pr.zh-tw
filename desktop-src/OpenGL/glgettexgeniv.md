---
title: 'glGetTexGeniv 函式 (Gl) '
description: 'GlGetTexGendv、glGetTexGenfv 和 glGetTexGeniv 函數會傳回材質座標產生參數。 |glGetTexGeniv 函式 (Gl) '
ms.assetid: 62c481d1-4862-43bb-9319-5a282c4e47d3
keywords:
- glGetTexGeniv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetTexGeniv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29569c84d21dbb2cd69579c78747e844cfd23ba4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981956"
---
# <a name="glgettexgeniv-function"></a><span data-ttu-id="89866-105">glGetTexGeniv 函式</span><span class="sxs-lookup"><span data-stu-id="89866-105">glGetTexGeniv function</span></span>

<span data-ttu-id="89866-106">[**GlGetTexGendv**](glgettexgendv.md)、 [**glGetTexGenfv**](glgettexgenfv.md)和 **glGetTexGeniv** 函數會傳回材質座標產生參數。</span><span class="sxs-lookup"><span data-stu-id="89866-106">The [**glGetTexGendv**](glgettexgendv.md), [**glGetTexGenfv**](glgettexgenfv.md), and **glGetTexGeniv** functions return texture coordinate generation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="89866-107">語法</span><span class="sxs-lookup"><span data-stu-id="89866-107">Syntax</span></span>


```C++
void WINAPI glGetTexGeniv(
   GLenum coord,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="89866-108">參數</span><span class="sxs-lookup"><span data-stu-id="89866-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89866-109">*coord*</span><span class="sxs-lookup"><span data-stu-id="89866-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="89866-110">材質座標。</span><span class="sxs-lookup"><span data-stu-id="89866-110">A texture coordinate.</span></span> <span data-ttu-id="89866-111">必須是 GL \_ S、gl \_ T、gl \_ R 或 gl \_ Q。</span><span class="sxs-lookup"><span data-stu-id="89866-111">Must be GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="89866-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="89866-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="89866-113">值 (s 的符號名稱，) 要傳回的值。</span><span class="sxs-lookup"><span data-stu-id="89866-113">The symbolic name of the value(s) to be returned.</span></span> <span data-ttu-id="89866-114">必須是 GL \_ 材質 \_ \_ 產生模式或其中一個材質產生平面方程式的名稱： GL \_ 物件 \_ 平面或 gl \_ 眼 \_ 平面。</span><span class="sxs-lookup"><span data-stu-id="89866-114">Must be either GL\_TEXTURE\_GEN\_MODE or the name of one of the texture generation plane equations: GL\_OBJECT\_PLANE or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="89866-115">這些值如下所示。</span><span class="sxs-lookup"><span data-stu-id="89866-115">These values are as follows.</span></span>



| <span data-ttu-id="89866-116">值</span><span class="sxs-lookup"><span data-stu-id="89866-116">Value</span></span>                                                                                                                                                                             | <span data-ttu-id="89866-117">意義</span><span class="sxs-lookup"><span data-stu-id="89866-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <span data-ttu-id="89866-118"><dt>**GL \_ 材質 \_ 產生 \_ 模式**</dt></span><span class="sxs-lookup"><span data-stu-id="89866-118"><dt>**GL\_TEXTURE\_GEN\_MODE**</dt></span></span> </dl> | <span data-ttu-id="89866-119">*Params* 參數會傳回單一值紋理產生函數（符號常數）。</span><span class="sxs-lookup"><span data-stu-id="89866-119">The *params* parameter returns the single-valued texture generation function, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <span data-ttu-id="89866-120"><dt>**GL \_ 物件 \_ 平面**</dt></span><span class="sxs-lookup"><span data-stu-id="89866-120"><dt>**GL\_OBJECT\_PLANE**</dt></span></span> </dl>              | <span data-ttu-id="89866-121">*Params* 參數會傳回四個平面方程式係數，以指定物件線性座標產生。</span><span class="sxs-lookup"><span data-stu-id="89866-121">The *params* parameter returns the four plane equation coefficients that specify object linear-coordinate generation.</span></span> <span data-ttu-id="89866-122">整數值在要求時，會直接從內部浮點標記法對應。</span><span class="sxs-lookup"><span data-stu-id="89866-122">Integer values, when requested, are mapped directly from the internal floating-point representation.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <span data-ttu-id="89866-123"><dt>**GL \_ 眼 \_ 平面**</dt></span><span class="sxs-lookup"><span data-stu-id="89866-123"><dt>**GL\_EYE\_PLANE**</dt></span></span> </dl>                       | <span data-ttu-id="89866-124">*Params* 參數會傳回四個平面方程式係數，以指定眼睛線性座標產生。</span><span class="sxs-lookup"><span data-stu-id="89866-124">The *params* parameter returns the four plane equation coefficients that specify eye linear-coordinate generation.</span></span> <span data-ttu-id="89866-125">整數值在要求時，會直接從內部浮點標記法對應。</span><span class="sxs-lookup"><span data-stu-id="89866-125">Integer values, when requested, are mapped directly from the internal floating-point representation.</span></span> <span data-ttu-id="89866-126">傳回的值是以眼睛座標維持的值。</span><span class="sxs-lookup"><span data-stu-id="89866-126">The returned values are those maintained in eye coordinates.</span></span> <span data-ttu-id="89866-127">除非模型矩陣是在呼叫 **glTexGen** 時所識別，否則它們不等於使用 [**glTexGen**](gltexgen-functions.md)所指定的值。</span><span class="sxs-lookup"><span data-stu-id="89866-127">They are not equal to the values specified using [**glTexGen**](gltexgen-functions.md), unless the modelview matrix was identified at the time **glTexGen** was called.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="89866-128">*params*</span><span class="sxs-lookup"><span data-stu-id="89866-128">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="89866-129">傳回要求的資料。</span><span class="sxs-lookup"><span data-stu-id="89866-129">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89866-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="89866-130">Return value</span></span>

<span data-ttu-id="89866-131">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="89866-131">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="89866-132">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="89866-132">Error codes</span></span>

<span data-ttu-id="89866-133">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="89866-133">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="89866-134">Name</span><span class="sxs-lookup"><span data-stu-id="89866-134">Name</span></span>                                                                                                  | <span data-ttu-id="89866-135">意義</span><span class="sxs-lookup"><span data-stu-id="89866-135">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89866-136"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="89866-136"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="89866-137">*coord* 或 *pname* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="89866-137">*coord* or *pname* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="89866-138"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="89866-138"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="89866-139">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="89866-139">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="89866-140">備註</span><span class="sxs-lookup"><span data-stu-id="89866-140">Remarks</span></span>

<span data-ttu-id="89866-141">**GlGetTexGen** 函式會傳回您使用 **glTexGen** 指定之材質座標產生函數的 *params* 選取參數。</span><span class="sxs-lookup"><span data-stu-id="89866-141">The **glGetTexGen** function returns in *params* selected parameters of a texture-coordinate generation function that you specified with **glTexGen**.</span></span> <span data-ttu-id="89866-142">*Coord* 參數會使用符號常數 GL、 \*\* gl t \*\*、   \_ \_ gl \_ r 或 gl q 來命名其中一個 (s、t、r、q) 材質座標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="89866-142">The *coord* parameter names one of the (*s*, *t*, *r*, *q*) texture coordinates, using the symbolic constant GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

<span data-ttu-id="89866-143">如果產生錯誤，則不會對 *參數* 的內容進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="89866-143">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="89866-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="89866-144">Requirements</span></span>



| <span data-ttu-id="89866-145">需求</span><span class="sxs-lookup"><span data-stu-id="89866-145">Requirement</span></span> | <span data-ttu-id="89866-146">值</span><span class="sxs-lookup"><span data-stu-id="89866-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89866-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89866-147">Minimum supported client</span></span><br/> | <span data-ttu-id="89866-148">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89866-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="89866-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89866-149">Minimum supported server</span></span><br/> | <span data-ttu-id="89866-150">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89866-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="89866-151">標頭</span><span class="sxs-lookup"><span data-stu-id="89866-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="89866-152"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="89866-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="89866-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="89866-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="89866-154"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="89866-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="89866-155">DLL</span><span class="sxs-lookup"><span data-stu-id="89866-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89866-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89866-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89866-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89866-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89866-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="89866-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="89866-159">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="89866-159">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="89866-160">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="89866-160">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> </dl>

 

 





