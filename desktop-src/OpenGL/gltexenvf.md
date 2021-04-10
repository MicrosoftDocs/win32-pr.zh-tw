---
title: 'glTexEnvf 函式 (Gl) '
description: GlTexEnvf 函式會設定紋理環境參數。
ms.assetid: 1b203240-a963-4dfe-96bc-735720e16122
keywords:
- glTexEnvf 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexEnvf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1566378b6dcd2f91a2e2cd445f0ec39c0f6f6a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685814"
---
# <a name="gltexenvf-function"></a><span data-ttu-id="a3dc3-104">glTexEnvf 函式</span><span class="sxs-lookup"><span data-stu-id="a3dc3-104">glTexEnvf function</span></span>

<span data-ttu-id="a3dc3-105">**GlTexEnvf** 函式會設定紋理環境參數。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-105">The **glTexEnvf** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3dc3-106">語法</span><span class="sxs-lookup"><span data-stu-id="a3dc3-106">Syntax</span></span>


```C++
void WINAPI glTexEnvf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="a3dc3-107">參數</span><span class="sxs-lookup"><span data-stu-id="a3dc3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3dc3-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="a3dc3-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="a3dc3-109">紋理環境。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-109">A texture environment.</span></span> <span data-ttu-id="a3dc3-110">必須是 GL \_ 紋理 \_ 環境。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="a3dc3-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="a3dc3-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="a3dc3-112">單一值紋理環境參數的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="a3dc3-113">必須是 GL \_ 紋理 \_ 環境 \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-113">Must be GL\_TEXTURE\_ENV\_MODE.</span></span>

</dd> <dt>

<span data-ttu-id="a3dc3-114">*param*</span><span class="sxs-lookup"><span data-stu-id="a3dc3-114">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="a3dc3-115">單一符號常數，其中一個 GL \_ lambert、gl \_ DECAL、gl \_ BLEND 或 gl \_ 取代。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-115">A single symbolic constant, one of GL\_MODULATE, GL\_DECAL, GL\_BLEND, or GL\_REPLACE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3dc3-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3dc3-116">Return value</span></span>

<span data-ttu-id="a3dc3-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a3dc3-118">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="a3dc3-118">Error codes</span></span>

<span data-ttu-id="a3dc3-119">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a3dc3-120">Name</span><span class="sxs-lookup"><span data-stu-id="a3dc3-120">Name</span></span>                                                                                                  | <span data-ttu-id="a3dc3-121">意義</span><span class="sxs-lookup"><span data-stu-id="a3dc3-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a3dc3-122"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="a3dc3-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a3dc3-123">*target* 或 *pname* 不是其中一個可接受的定義值，或當 *params* 應該有定義的常數值 (根據 *pname*) 的值而不是時。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="a3dc3-124"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="a3dc3-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a3dc3-125">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="a3dc3-126">備註</span><span class="sxs-lookup"><span data-stu-id="a3dc3-126">Remarks</span></span>

<span data-ttu-id="a3dc3-127">材質環境指定當片段有紋理時，材質值的轉譯方式。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="a3dc3-128">*目標* 參數必須是 GL \_ 紋理 \_ 環境。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="a3dc3-129">*Pname* 參數為 GL \_ 紋理 \_ 環境 \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-129">The *pname* parameter is GL\_TEXTURE\_ENV\_MODE.</span></span> <span data-ttu-id="a3dc3-130">已定義三個材質函數： GL \_ lambert、gl \_ DECAL 和 GL \_ BLEND。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-130">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="a3dc3-131">材質函式會使用適用于片段的材質影像值，在片段上作用 (查看 [**glTexParameter**](gltexparameter-functions.md)) 並產生該片段的 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-131">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="a3dc3-132">下表顯示如何為每個可選擇的材質函數產生 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-132">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="a3dc3-133">*C* 是三倍的色彩值 (RGB) ，而 *a* 是相關聯的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-133">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="a3dc3-134">從材質影像解壓縮的 RGBA 值位於 \[ 0、1的範圍內 \] 。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-134">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="a3dc3-135">注標 *f* 指的是傳入片段、紋理影像的注標 *t* 、紋理環境色彩的注標 *c* ，以及注標 *v* 表示紋理函式所產生的值。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-135">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="a3dc3-136">材質影像的每個材質元素最多可有四個元件 (查看 [**glTexImage1D**](glteximage1d.md) 和 [**glTexImage2D**](glteximage2d.md)) 。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-136">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="a3dc3-137">在一個元件的影像中，Lt 表示單一元件。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-137">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="a3dc3-138">雙元件映射使用 *L？*</span><span class="sxs-lookup"><span data-stu-id="a3dc3-138">A two-component image uses *L?*</span></span>  <span data-ttu-id="a3dc3-139">和 *答？*</span><span class="sxs-lookup"><span data-stu-id="a3dc3-139">and *A?*</span></span> <span data-ttu-id="a3dc3-140">.</span><span class="sxs-lookup"><span data-stu-id="a3dc3-140">.</span></span> <span data-ttu-id="a3dc3-141">三個元件的影像只有一個色彩值 *C？*</span><span class="sxs-lookup"><span data-stu-id="a3dc3-141">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="a3dc3-142">.</span><span class="sxs-lookup"><span data-stu-id="a3dc3-142">.</span></span> <span data-ttu-id="a3dc3-143">四個元件的影像同時具有色彩值 *C？*</span><span class="sxs-lookup"><span data-stu-id="a3dc3-143">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="a3dc3-144">和 Alpha 值 *A？*</span><span class="sxs-lookup"><span data-stu-id="a3dc3-144">and an alpha value *A?*</span></span> <span data-ttu-id="a3dc3-145">.</span><span class="sxs-lookup"><span data-stu-id="a3dc3-145">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a3dc3-146">元件數目</span><span class="sxs-lookup"><span data-stu-id="a3dc3-146">Number of components</span></span></th>
<th><span data-ttu-id="a3dc3-147">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="a3dc3-147">GL_MODULATE</span></span></th>
<th><span data-ttu-id="a3dc3-148">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="a3dc3-148">GL_DECAL</span></span></th>
<th><span data-ttu-id="a3dc3-149">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="a3dc3-149">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="a3dc3-150">1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="a3dc3-150">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a3dc3-151"><em>C<sub>v</sub> </em>  = <em>L？</em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-151"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="a3dc3-152"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-152"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="a3dc3-153">未定義 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="a3dc3-153">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a3dc3-154"><em>C</em> <em><sub>v</sub></em>  =  <em> (1</em> - <em>L？</em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-154"><em>C</em> <em><sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="a3dc3-155"><em>) C<sub>f</sub> </em> + <em>L？</em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-155"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="a3dc3-156"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-156"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3dc3-157"><em>A<sub>v</sub> </em>  = <em> <sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-157"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="a3dc3-158"><em>A<sub>v</sub> </em>  = <em> <sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-158"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="a3dc3-159">2 $ {移除} $</span><span class="sxs-lookup"><span data-stu-id="a3dc3-159">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a3dc3-160"><em>C<sub>v</sub> </em>  = <em>L？</em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-160"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="a3dc3-161"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-161"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="a3dc3-162">未定義 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="a3dc3-162">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a3dc3-163"><em>C<sub>v</sub> </em>  = <em> (1</em> - <em>L？</em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-163"><em>C<sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="a3dc3-164"><em>) C<sub>f</sub> </em> + <em>L？</em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-164"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="a3dc3-165"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-165"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3dc3-166"><em>A<sub>v</sub> </em>  = <em> <sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-166"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="a3dc3-167"><em>A<sub>v</sub> </em>  = <em> <sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-167"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="a3dc3-168">3 $ {移除} $</span><span class="sxs-lookup"><span data-stu-id="a3dc3-168">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a3dc3-169"><em>C<sub>v</sub> </em>  = <em>C？</em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-169"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="a3dc3-170"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-170"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="a3dc3-171"><em>C<sub>v</sub> </em>  = <em>C？</em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-171"><em>C<sub>v</sub></em> = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="a3dc3-172">未定義 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="a3dc3-172">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3dc3-173"><em>A<sub>v</sub> </em>  = <em> <sub>F</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="a3dc3-173"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="a3dc3-174"><em>A<sub>v</sub> </em>  = <em> <sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-174"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="a3dc3-175">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="a3dc3-175">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a3dc3-176"><em>C<sub>v</sub> </em>  = <em>C？</em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-176"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="a3dc3-177"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-177"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="a3dc3-178"><em>C<sub>v</sub> </em> = (1- <em>A？</em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-178"><em>C<sub>v</sub></em> = (1 - <em>A?</em></span></span> <span data-ttu-id="a3dc3-179"><em>) C<sub>f</sub> </em> + <em>A？</em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-179"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="a3dc3-180"><em>C？</em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-180"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="a3dc3-181">未定義 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="a3dc3-181">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3dc3-182"><em>A<sub>v</sub> </em>  = <em>答：</em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-182"><em>A<sub>v</sub></em> = <em>A?</em></span></span> <span data-ttu-id="a3dc3-183"><em><sub>F</sub></em> </span><span class="sxs-lookup"><span data-stu-id="a3dc3-183"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="a3dc3-184"><em>A<sub>v</sub> </em>  = <em> <sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="a3dc3-184"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="a3dc3-185">GL \_ 紋理 \_ ENV \_ 模式預設為 gl \_ lambert。</span><span class="sxs-lookup"><span data-stu-id="a3dc3-185">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE.</span></span>

<span data-ttu-id="a3dc3-186">下列函式會抓取 **glTexEnvf** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="a3dc3-186">The following function retrieves information related to **glTexEnvf**:</span></span>

[<span data-ttu-id="a3dc3-187">**glTexGetEnvfv**</span><span class="sxs-lookup"><span data-stu-id="a3dc3-187">**glTexGetEnvfv**</span></span>](glgettexenvfv.md)

## <a name="requirements"></a><span data-ttu-id="a3dc3-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3dc3-188">Requirements</span></span>



| <span data-ttu-id="a3dc3-189">需求</span><span class="sxs-lookup"><span data-stu-id="a3dc3-189">Requirement</span></span> | <span data-ttu-id="a3dc3-190">值</span><span class="sxs-lookup"><span data-stu-id="a3dc3-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3dc3-191">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3dc3-191">Minimum supported client</span></span><br/> | <span data-ttu-id="a3dc3-192">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3dc3-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a3dc3-193">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3dc3-193">Minimum supported server</span></span><br/> | <span data-ttu-id="a3dc3-194">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3dc3-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a3dc3-195">標頭</span><span class="sxs-lookup"><span data-stu-id="a3dc3-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3dc3-196"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="a3dc3-196"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a3dc3-197">程式庫</span><span class="sxs-lookup"><span data-stu-id="a3dc3-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3dc3-198"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3dc3-198"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a3dc3-199">DLL</span><span class="sxs-lookup"><span data-stu-id="a3dc3-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3dc3-200"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3dc3-200"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3dc3-201">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3dc3-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3dc3-202">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a3dc3-202">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a3dc3-203">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a3dc3-203">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a3dc3-204">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="a3dc3-204">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="a3dc3-205">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="a3dc3-205">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="a3dc3-206">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="a3dc3-206">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





