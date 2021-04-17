---
title: 'glTexGend 函式 (Gl) '
description: '控制材質座標的產生。 |glTexGend 函式 (Gl) '
ms.assetid: 75ab3468-281d-4c8d-95cc-138d75646cdf
keywords:
- glTexGend 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexGend
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45854eb1e2070f334bfc906c249fbb4341ab74d0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104566518"
---
# <a name="gltexgend-function"></a><span data-ttu-id="bf9d5-105">glTexGend 函式</span><span class="sxs-lookup"><span data-stu-id="bf9d5-105">glTexGend function</span></span>

<span data-ttu-id="bf9d5-106">控制材質座標的產生。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-106">Controls the generation of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf9d5-107">語法</span><span class="sxs-lookup"><span data-stu-id="bf9d5-107">Syntax</span></span>


```C++
void WINAPI glTexGend(
   GLenum   coord,
   GLenum   pname,
   GLdouble param
);
```



## <a name="parameters"></a><span data-ttu-id="bf9d5-108">參數</span><span class="sxs-lookup"><span data-stu-id="bf9d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf9d5-109">*coord*</span><span class="sxs-lookup"><span data-stu-id="bf9d5-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="bf9d5-110">材質座標。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-110">A texture coordinate.</span></span> <span data-ttu-id="bf9d5-111">必須是下列其中一項： GL \_ S、gl \_ T、gl \_ R 或 GL \_ Q。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-111">Must be one of the following: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="bf9d5-112">**pname**</span><span class="sxs-lookup"><span data-stu-id="bf9d5-112">**pname**</span></span> 
</dt> <dd>

<span data-ttu-id="bf9d5-113">紋理座標產生函數的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-113">The symbolic name of the texture coordinate generation function.</span></span>

</dd> <dt>

<span data-ttu-id="bf9d5-114">*param*</span><span class="sxs-lookup"><span data-stu-id="bf9d5-114">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="bf9d5-115">單一值材質產生參數、GL \_ 物件 \_ 線性、gl \_ 眼 \_ 線性或 gl \_ 球體 \_ 圖的其中一個。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-115">A single valued texture generation parameter, one of GL\_OBJECT\_LINEAR, GL\_EYE\_LINEAR, or GL\_SPHERE\_MAP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf9d5-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf9d5-116">Return value</span></span>

<span data-ttu-id="bf9d5-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bf9d5-118">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bf9d5-118">Error codes</span></span>

<span data-ttu-id="bf9d5-119">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="bf9d5-120">Name</span><span class="sxs-lookup"><span data-stu-id="bf9d5-120">Name</span></span>                                                                                                  | <span data-ttu-id="bf9d5-121">意義</span><span class="sxs-lookup"><span data-stu-id="bf9d5-121">Meaning</span></span>                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf9d5-122"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="bf9d5-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="bf9d5-123">*coord* 或 *pname* 不是接受的定義值，或 *pname* 是 GL \_ 材質 \_ GEN \_ 模式，而 *params* 不是接受的定義值。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-123">*coord* or *pname* was not an accepted defined value, or *pname* was GL\_TEXTURE\_GEN\_MODE and *params* was not an accepted defined value.</span></span><br/> |
| <dl> <span data-ttu-id="bf9d5-124"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="bf9d5-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="bf9d5-125">*pname* 是 gl \_ 材質 \_ GEN \_ 模式、 *params* 是 GL \_ 球體 \_ 地圖，而 *coord* 是 gl \_ R 或 gl \_ Q</span><span class="sxs-lookup"><span data-stu-id="bf9d5-125">*pname* was GL\_TEXTURE\_GEN\_MODE, *params* was GL\_SPHERE\_MAP, and *coord* was either GL\_R or GL\_Q</span></span><br/>                                     |
| <dl> <span data-ttu-id="bf9d5-126"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="bf9d5-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="bf9d5-127">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                 |



## <a name="remarks"></a><span data-ttu-id="bf9d5-128">備註</span><span class="sxs-lookup"><span data-stu-id="bf9d5-128">Remarks</span></span>

<span data-ttu-id="bf9d5-129">**GlTexGen** 函式會選取材質座標產生函數或提供其中一個函數的係數。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-129">The **glTexGen** function selects a texture-coordinate generation function or supplies coefficients for one of the functions.</span></span> <span data-ttu-id="bf9d5-130">*Coord* 參數會命名其中一個 (s、t、r、q) 材質座標，而且必須是下列其中一個符號： GL \_ s、GL \_ t、gl \_ r 或 gl \_ q。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-130">The *coord* parameter names one of the (s,t,r,q) texture coordinates, and it must be one of these symbols: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span> <span data-ttu-id="bf9d5-131">*Pname* 參數必須是三個符號常數的其中一種： gl \_ 紋理內 \_ 代 \_ 模式、gl \_ 物件 \_ 平面或 gl \_ 眼 \_ 平面。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-131">The *pname* parameter must be one of three symbolic constants: GL\_TEXTURE\_GEN\_MODE, GL\_OBJECT\_PLANE, or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="bf9d5-132">如果 *pname* 是 gl \_ 材質 \_ 產生 \_ 模式，則 *param* 會指定一個模式，也就是 gl \_ 物件 \_ 線性、gl \_ 眼 \_ 線性或 gl \_ 球體 \_ 地圖。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-132">If *pname* is GL\_TEXTURE\_GEN\_MODE, then *param* specifies a mode, one of GL\_OBJECT\_LINEAR, GL\_EYE\_LINEAR, or GL\_SPHERE\_MAP.</span></span> <span data-ttu-id="bf9d5-133">如果 *pname* 是 gl \_ 物件 \_ 平面或 gl \_ 眼 \_ 平面， *param* 就會包含對應材質產生函數的係數。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-133">If *pname* is either GL\_OBJECT\_PLANE or GL\_EYE\_PLANE, *param* contains coefficients for the corresponding texture generation function.</span></span>

<span data-ttu-id="bf9d5-134">如果材質產生函數是 GL \_ 物件 \_ 線性，函式</span><span class="sxs-lookup"><span data-stu-id="bf9d5-134">If the texture generation function is GL\_OBJECT\_LINEAR, the function</span></span>

![當材質產生函數 GL_OBJECT_LINEAR 時，顯示 glTexGen 函式的方程式。](images/tex02.png)

<span data-ttu-id="bf9d5-136">會使用，其中 g 是針對以 coord 命名的座標計算的值;p1、p2、p3 和 p4 是在 params 中提供的四個值;和 x？、y？、z？以及 w？是頂點的物件座標。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-136">is used, where g is the value computed for the coordinate named in coord; p1, p2, p3, and p4 are the four values supplied in params; and x?, y?, z?, and w? are the object coordinates of the vertex.</span></span> <span data-ttu-id="bf9d5-137">您可以使用此函式來紋理對應地形，方法是使用海平面作為參考平面， (p1、p2、p3 和 p4) 所定義。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-137">You can use this function to texture-map terrain by using sea level as a reference plane (defined by p1, p2, p3, and p4).</span></span> <span data-ttu-id="bf9d5-138">GL \_ 物件 \_ 線性座標產生函數會將地形頂點的高度計算為其與海平面之間的距離，而該海拔高度則是用來編制紋理影像的索引，以將白色的上階對應到尖峰，而將綠色草對應至 foothills。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-138">The GL\_OBJECT\_LINEAR coordinate generation function computes the altitude of a terrain vertex as its distance from sea level; that altitude is used to index the texture image to map white snow onto peaks and green grass onto foothills, for example.</span></span>

<span data-ttu-id="bf9d5-139">如果材質產生函式為 GL \_ 眼 \_ 線性，則函式會</span><span class="sxs-lookup"><span data-stu-id="bf9d5-139">If the texture generation function is GL\_EYE\_LINEAR, the function</span></span>

![當材質產生函數 GL_EYE_LINEAR 時，顯示 glTexGen 函式的方程式。](images/tex02.png)

<span data-ttu-id="bf9d5-141">使用</span><span class="sxs-lookup"><span data-stu-id="bf9d5-141">is used, where</span></span>

![顯示頂點眼睛座標的方程式。](images/tex03.png)

<span data-ttu-id="bf9d5-143">和 x？、y？、z？以及 w？頂點、p1、p2、p3 和 p4 的眼睛座標是在 *param* 中提供的值，而當您呼叫 **GlTexGen** 時，M 是模型矩陣。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-143">and x?, y?, z?, and w? are the eye coordinates of the vertex, p1, p2, p3, and p4 are the values supplied in *param*, and M is the modelview matrix when you call **glTexGen**.</span></span> <span data-ttu-id="bf9d5-144">如果 M 的條件式或單數不佳，則產生的函式所產生的材質座標可能不正確或未定義。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-144">If M is poorly conditioned or singular, texture coordinates generated by the resulting function can be inaccurate or undefined.</span></span>

<span data-ttu-id="bf9d5-145">*Param* 中的值會以眼睛座標定義參考平面。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-145">The values in *param* define a reference plane in eye coordinates.</span></span> <span data-ttu-id="bf9d5-146">套用至這些專案的模型矩陣，在轉換多邊形頂點時，不能是同一個效果。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-146">The modelview matrix that is applied to them cannot be the same one in effect when the polygon vertices are transformed.</span></span> <span data-ttu-id="bf9d5-147">此函式會建立可在移動物件上產生動態輪廓線的材質座標欄位。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-147">This function establishes a field of texture coordinates that can produce dynamic contour lines on moving objects.</span></span>

<span data-ttu-id="bf9d5-148">如果 *pname* 為 gl \_ 球體 \_ 地圖，而 *COORD* 為 gl \_ S 或 gl \_ T，則會產生 S 和 T 紋理座標，如下所示。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-148">If *pname* is GL\_SPHERE\_MAP and *coord* is either GL\_S or GL\_T, s and t texture coordinates are generated as follows.</span></span> <span data-ttu-id="bf9d5-149">讓 u 成為從原點指向多邊形頂點的單位向量)  (眼睛座標。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-149">Let u be the unit vector pointing from the origin to the polygon vertex (in eye coordinates).</span></span> <span data-ttu-id="bf9d5-150">在轉換為眼睛座標之後，讓 n 成為目前的正常情況。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-150">Let n  be the current normal, after transformation to eye coordinates.</span></span> <span data-ttu-id="bf9d5-151">讓 f = (fx ( ) 年度 ( ) fz) T 是反映向量，</span><span class="sxs-lookup"><span data-stu-id="bf9d5-151">Let f = (fx ( ) fy ( ) fz)T be the reflection vector such that</span></span>

![顯示反映向量作為單位向量和目前一般標準函式的方程式。](images/tex05.png)

<span data-ttu-id="bf9d5-153">最後，讓我們</span><span class="sxs-lookup"><span data-stu-id="bf9d5-153">Finally, let</span></span>

![顯示 m 的方程式，表示為反映向量的函式。](images/tex07.png)

<span data-ttu-id="bf9d5-155">然後，指派給 i 和 t 紋理座標的值為</span><span class="sxs-lookup"><span data-stu-id="bf9d5-155">Then the values assigned to the i and t texture coordinates are</span></span>

![顯示指派給 i 和 t 材質座標之值的方程式。](images/tex06.png)

<span data-ttu-id="bf9d5-157">您可以使用 [**glEnable**](glenable.md) 或 [**glDisable**](gldisable.md) 搭配其中一個符號材質座標名稱 (GL \_ 材質 \_ gen \_ 、gl \_ 材質 \_ gen \_ T、GL \_ 材質 \_ gen \_ R 或 gl \_ 材質 \_ gen \_ Q) 作為引數，以啟用或停用材質座標產生函數。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-157">You can enable or disable a texture-coordinate generation function by using [**glEnable**](glenable.md) or [**glDisable**](gldisable.md) with one of the symbolic texture-coordinate names (GL\_TEXTURE\_GEN\_S, GL\_TEXTURE\_GEN\_T, GL\_TEXTURE\_GEN\_R, or GL\_TEXTURE\_GEN\_Q) as the argument.</span></span> <span data-ttu-id="bf9d5-158">啟用此函式時，會根據與該座標相關聯的產生函數來計算指定的材質座標。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-158">When this function is enabled, the specified texture coordinate is computed according to the generating function associated with that coordinate.</span></span> <span data-ttu-id="bf9d5-159">當停用函式時，後續頂點會從目前的材質座標集合取得指定的材質座標。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-159">When the function is disabled, subsequent vertices take the specified texture coordinate from the current set of texture coordinates.</span></span> <span data-ttu-id="bf9d5-160">一開始，所有材質產生函數都會設定為 GL \_ 眼 \_ 線性，並停用。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-160">Initially, all texture generation functions are set to GL\_EYE\_LINEAR and are disabled.</span></span> <span data-ttu-id="bf9d5-161">這兩個平面方能 (1、0、0、0) ;這兩個 t 平面方能 (0、1、0、0) ;和所有 r 和 q 平面方能 (0、0、0、0) 。</span><span class="sxs-lookup"><span data-stu-id="bf9d5-161">Both s plane equations are (1,0,0,0); both t plane equations are (0,1,0,0); and all r and q plane equations are (0,0,0,0).</span></span>

<span data-ttu-id="bf9d5-162">下列函式會取出與 glTexGen 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="bf9d5-162">The following functions retrieve information related to glTexGen:</span></span>

<dl>

[<span data-ttu-id="bf9d5-163">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="bf9d5-163">**glGetTexGen**</span></span>](glgettexgen.md)  
<span data-ttu-id="bf9d5-164">[](glisenabled.md)具有引數 GL \_ 材質 \_ GEN \_ S 的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="bf9d5-164">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_S</span></span>  
<span data-ttu-id="bf9d5-165">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ 材質 \_ GEN \_ T</span><span class="sxs-lookup"><span data-stu-id="bf9d5-165">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_T</span></span>  
<span data-ttu-id="bf9d5-166">[](glisenabled.md)具有引數 GL \_ 材質 \_ GEN \_ R 的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="bf9d5-166">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_R</span></span>  
<span data-ttu-id="bf9d5-167">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ 材質 \_ GEN 的 \_ Q</span><span class="sxs-lookup"><span data-stu-id="bf9d5-167">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_Q</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="bf9d5-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf9d5-168">Requirements</span></span>



| <span data-ttu-id="bf9d5-169">需求</span><span class="sxs-lookup"><span data-stu-id="bf9d5-169">Requirement</span></span> | <span data-ttu-id="bf9d5-170">值</span><span class="sxs-lookup"><span data-stu-id="bf9d5-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf9d5-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf9d5-171">Minimum supported client</span></span><br/> | <span data-ttu-id="bf9d5-172">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf9d5-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bf9d5-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf9d5-173">Minimum supported server</span></span><br/> | <span data-ttu-id="bf9d5-174">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf9d5-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf9d5-175">標頭</span><span class="sxs-lookup"><span data-stu-id="bf9d5-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf9d5-176"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="bf9d5-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bf9d5-177">程式庫</span><span class="sxs-lookup"><span data-stu-id="bf9d5-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf9d5-178"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf9d5-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bf9d5-179">DLL</span><span class="sxs-lookup"><span data-stu-id="bf9d5-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf9d5-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf9d5-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf9d5-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf9d5-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf9d5-182">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bf9d5-182">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bf9d5-183">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bf9d5-183">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bf9d5-184">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="bf9d5-184">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="bf9d5-185">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="bf9d5-185">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="bf9d5-186">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="bf9d5-186">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="bf9d5-187">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="bf9d5-187">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="bf9d5-188">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="bf9d5-188">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="bf9d5-189">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="bf9d5-189">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="bf9d5-190">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="bf9d5-190">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="bf9d5-191">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="bf9d5-191">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="bf9d5-192">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="bf9d5-192">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





