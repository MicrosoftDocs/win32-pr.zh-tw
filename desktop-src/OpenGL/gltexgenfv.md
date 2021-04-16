---
title: 'glTexGenfv 函式 (Gl) '
description: '控制材質座標的產生。 |glTexGenfv 函式 (Gl) '
ms.assetid: d5454d6f-16bb-47d9-9c52-da2daf491224
keywords:
- glTexGenfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexGenfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4d5394b6385246f296a472ce51f2727e2738845
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104559128"
---
# <a name="gltexgenfv-function"></a><span data-ttu-id="d5f76-105">glTexGenfv 函式</span><span class="sxs-lookup"><span data-stu-id="d5f76-105">glTexGenfv function</span></span>

<span data-ttu-id="d5f76-106">控制材質座標的產生。</span><span class="sxs-lookup"><span data-stu-id="d5f76-106">Controls the generation of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f76-107">語法</span><span class="sxs-lookup"><span data-stu-id="d5f76-107">Syntax</span></span>


```C++
void WINAPI glTexGenfv(
         GLenum  coord,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="d5f76-108">參數</span><span class="sxs-lookup"><span data-stu-id="d5f76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5f76-109">*coord*</span><span class="sxs-lookup"><span data-stu-id="d5f76-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f76-110">材質座標。</span><span class="sxs-lookup"><span data-stu-id="d5f76-110">A texture coordinate.</span></span> <span data-ttu-id="d5f76-111">必須是下列其中一項： GL \_ S、gl \_ T、gl \_ R 或 GL \_ Q。</span><span class="sxs-lookup"><span data-stu-id="d5f76-111">Must be one of the following: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-112">**pname**</span><span class="sxs-lookup"><span data-stu-id="d5f76-112">**pname**</span></span> 
</dt> <dd>

<span data-ttu-id="d5f76-113">紋理座標產生函數的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="d5f76-113">The symbolic name of the texture coordinate generation function.</span></span>

</dd> <dt>

<span data-ttu-id="d5f76-114">*params*</span><span class="sxs-lookup"><span data-stu-id="d5f76-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f76-115">浮點數陣列，包含對應材質產生函數的係數。</span><span class="sxs-lookup"><span data-stu-id="d5f76-115">An array of floats that contains the coefficients for the corresponding texture generation function.</span></span>

``` syntax
GLfloat zPlane[] = { 0.0f, 0.0f, 1.0f, 0.0f };
```

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5f76-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5f76-116">Return value</span></span>

<span data-ttu-id="d5f76-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d5f76-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d5f76-118">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d5f76-118">Error codes</span></span>

<span data-ttu-id="d5f76-119">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d5f76-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d5f76-120">Name</span><span class="sxs-lookup"><span data-stu-id="d5f76-120">Name</span></span>                                                                                                  | <span data-ttu-id="d5f76-121">意義</span><span class="sxs-lookup"><span data-stu-id="d5f76-121">Meaning</span></span>                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d5f76-122"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f76-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d5f76-123">*coord* 或 *pname* 不是接受的定義值，或 *pname* 是 GL \_ 材質 \_ GEN \_ 模式，而 *params* 不是接受的定義值。</span><span class="sxs-lookup"><span data-stu-id="d5f76-123">*coord* or *pname* was not an accepted defined value, or *pname* was GL\_TEXTURE\_GEN\_MODE and *params* was not an accepted defined value.</span></span><br/> |
| <dl> <span data-ttu-id="d5f76-124"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f76-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d5f76-125">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="d5f76-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                 |



## <a name="remarks"></a><span data-ttu-id="d5f76-126">備註</span><span class="sxs-lookup"><span data-stu-id="d5f76-126">Remarks</span></span>

<span data-ttu-id="d5f76-127">**GlTexGen** 函式會選取材質座標產生函數或提供其中一個函數的係數。</span><span class="sxs-lookup"><span data-stu-id="d5f76-127">The **glTexGen** function selects a texture-coordinate generation function or supplies coefficients for one of the functions.</span></span> <span data-ttu-id="d5f76-128">*Coord* 參數會命名其中一個 (s、t、r、q) 材質座標，而且必須是下列其中一個符號： GL \_ s、GL \_ t、gl \_ r 或 gl \_ q。</span><span class="sxs-lookup"><span data-stu-id="d5f76-128">The *coord* parameter names one of the (s,t,r,q) texture coordinates, and it must be one of these symbols: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span> <span data-ttu-id="d5f76-129">*Pname* 參數必須是三個符號常數的其中一種： gl \_ 紋理內 \_ 代 \_ 模式、gl \_ 物件 \_ 平面或 gl \_ 眼 \_ 平面。</span><span class="sxs-lookup"><span data-stu-id="d5f76-129">The *pname* parameter must be one of three symbolic constants: GL\_TEXTURE\_GEN\_MODE, GL\_OBJECT\_PLANE, or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="d5f76-130">如果 *pname* 是 gl \_ 物件 \_ 平面或 gl \_ 眼 \_ 平面， *param* 就會包含對應材質產生函數的係數。</span><span class="sxs-lookup"><span data-stu-id="d5f76-130">If *pname* is either GL\_OBJECT\_PLANE or GL\_EYE\_PLANE, *param* contains coefficients for the corresponding texture generation function.</span></span>

<span data-ttu-id="d5f76-131">如果材質產生函數是 GL \_ 物件 \_ 線性，函式</span><span class="sxs-lookup"><span data-stu-id="d5f76-131">If the texture generation function is GL\_OBJECT\_LINEAR, the function</span></span>

<span data-ttu-id="d5f76-132">![當材質產生函數 GL_OBJECT_LINEAR 時，顯示 glTexGen 函式的方程式。]</span><span class="sxs-lookup"><span data-stu-id="d5f76-132">![Equation showing the glTexGen function when the texture generation function is GL_OBJECT_LINEAR.]</span></span>

<span data-ttu-id="d5f76-133">會使用，其中 g 是針對以 coord 命名的座標計算的值;p1、p2、p3 和 p4 是在 params 中提供的四個值;和 x？、y？、z？以及 w？是頂點的物件座標。</span><span class="sxs-lookup"><span data-stu-id="d5f76-133">is used, where g is the value computed for the coordinate named in coord; p1, p2, p3, and p4 are the four values supplied in params; and x?, y?, z?, and w? are the object coordinates of the vertex.</span></span> <span data-ttu-id="d5f76-134">您可以使用此函式來紋理對應地形，方法是使用海平面作為參考平面， (p1、p2、p3 和 p4) 所定義。</span><span class="sxs-lookup"><span data-stu-id="d5f76-134">You can use this function to texture-map terrain by using sea level as a reference plane (defined by p1, p2, p3, and p4).</span></span> <span data-ttu-id="d5f76-135">GL \_ 物件 \_ 線性座標產生函數會將地形頂點的高度計算為其與海平面之間的距離，而該海拔高度則是用來編制紋理影像的索引，以將白色的上階對應到尖峰，而將綠色草對應至 foothills。</span><span class="sxs-lookup"><span data-stu-id="d5f76-135">The GL\_OBJECT\_LINEAR coordinate generation function computes the altitude of a terrain vertex as its distance from sea level; that altitude is used to index the texture image to map white snow onto peaks and green grass onto foothills, for example.</span></span>

<span data-ttu-id="d5f76-136">如果材質產生函式為 GL \_ 眼 \_ 線性，則函式會</span><span class="sxs-lookup"><span data-stu-id="d5f76-136">If the texture generation function is GL\_EYE\_LINEAR, the function</span></span>

<span data-ttu-id="d5f76-137">![當材質產生函數 GL_EYE_LINEAR 時，顯示 glTexGen 函式的方程式。]</span><span class="sxs-lookup"><span data-stu-id="d5f76-137">![Equation showing the glTexGen function when the texture generation function is GL_EYE_LINEAR.]</span></span>

<span data-ttu-id="d5f76-138">使用</span><span class="sxs-lookup"><span data-stu-id="d5f76-138">is used, where</span></span>

![顯示頂點眼睛座標的方程式。](images/tex03.png)

<span data-ttu-id="d5f76-140">和 x？、y？、z？以及 w？頂點、p1、p2、p3 和 p4 的眼睛座標是在 *param* 中提供的值，而當您呼叫 **GlTexGen** 時，M 是模型矩陣。</span><span class="sxs-lookup"><span data-stu-id="d5f76-140">and x?, y?, z?, and w? are the eye coordinates of the vertex, p1, p2, p3, and p4 are the values supplied in *param*, and M is the modelview matrix when you call **glTexGen**.</span></span> <span data-ttu-id="d5f76-141">如果 M 的條件式或單數不佳，則產生的函式所產生的材質座標可能不正確或未定義。</span><span class="sxs-lookup"><span data-stu-id="d5f76-141">If M is poorly conditioned or singular, texture coordinates generated by the resulting function can be inaccurate or undefined.</span></span>

<span data-ttu-id="d5f76-142">請注意， *param* 中的值會以眼睛座標定義參考平面。</span><span class="sxs-lookup"><span data-stu-id="d5f76-142">Note that the values in *param* define a reference plane in eye coordinates.</span></span> <span data-ttu-id="d5f76-143">當多邊形頂點轉換時，套用至它們的模型矩陣可能不會是相同的結果。</span><span class="sxs-lookup"><span data-stu-id="d5f76-143">The modelview matrix that is applied to them may not be the same one in effect when the polygon vertices are transformed.</span></span> <span data-ttu-id="d5f76-144">此函式會建立可在移動物件上產生動態輪廓線的材質座標欄位。</span><span class="sxs-lookup"><span data-stu-id="d5f76-144">This function establishes a field of texture coordinates that can produce dynamic contour lines on moving objects.</span></span>

<span data-ttu-id="d5f76-145">如果 *pname* 為 gl \_ 球體 \_ 地圖，而 *COORD* 為 gl \_ S 或 gl \_ T，則會產生 S 和 T 紋理座標，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d5f76-145">If *pname* is GL\_SPHERE\_MAP and *coord* is either GL\_S or GL\_T, s and t texture coordinates are generated as follows.</span></span> <span data-ttu-id="d5f76-146">讓 u 成為從原點指向多邊形頂點的單位向量)  (眼睛座標。</span><span class="sxs-lookup"><span data-stu-id="d5f76-146">Let u be the unit vector pointing from the origin to the polygon vertex (in eye coordinates).</span></span> <span data-ttu-id="d5f76-147">在轉換為眼睛座標之後，讓 n 成為目前的正常情況。</span><span class="sxs-lookup"><span data-stu-id="d5f76-147">Let n  be the current normal, after transformation to eye coordinates.</span></span> <span data-ttu-id="d5f76-148">讓 f = (fx ( ) 年度 ( ) fz) T 是反映向量，</span><span class="sxs-lookup"><span data-stu-id="d5f76-148">Let f = (fx ( ) fy ( ) fz)T be the reflection vector such that</span></span>

![顯示反映向量作為單位向量和目前一般標準函式的方程式。](images/tex05.png)

<span data-ttu-id="d5f76-150">最後，讓我們</span><span class="sxs-lookup"><span data-stu-id="d5f76-150">Finally, let</span></span>

![顯示 m 的方程式，表示為反映向量的函式。](images/tex07.png)

<span data-ttu-id="d5f76-152">然後，指派給 i 和 t 紋理座標的值為</span><span class="sxs-lookup"><span data-stu-id="d5f76-152">Then the values assigned to the i and t texture coordinates are</span></span>

![顯示指派給 i 和 t 材質座標之值的方程式。](images/tex06.png)

<span data-ttu-id="d5f76-154">您可以使用 [**glEnable**](glenable.md) 或 [**glDisable**](gldisable.md) 搭配其中一個符號材質座標名稱 (GL \_ 材質 \_ gen \_ 、gl \_ 材質 \_ gen \_ T、GL \_ 材質 \_ gen \_ R 或 gl \_ 材質 \_ gen \_ Q) 作為引數，以啟用或停用材質座標產生函數。</span><span class="sxs-lookup"><span data-stu-id="d5f76-154">You can enable or disable a texture-coordinate generation function by using [**glEnable**](glenable.md) or [**glDisable**](gldisable.md) with one of the symbolic texture-coordinate names (GL\_TEXTURE\_GEN\_S, GL\_TEXTURE\_GEN\_T, GL\_TEXTURE\_GEN\_R, or GL\_TEXTURE\_GEN\_Q) as the argument.</span></span> <span data-ttu-id="d5f76-155">啟用此函式時，會根據與該座標相關聯的產生函數來計算指定的材質座標。</span><span class="sxs-lookup"><span data-stu-id="d5f76-155">When this function is enabled, the specified texture coordinate is computed according to the generating function associated with that coordinate.</span></span> <span data-ttu-id="d5f76-156">停用此函式時，後續頂點會從目前的材質座標集合取得指定的材質座標。</span><span class="sxs-lookup"><span data-stu-id="d5f76-156">When this function is disabled, subsequent vertices take the specified texture coordinate from the current set of texture coordinates.</span></span> <span data-ttu-id="d5f76-157">一開始，所有材質產生函數都會設定為 GL \_ 眼 \_ 線性，並停用。</span><span class="sxs-lookup"><span data-stu-id="d5f76-157">Initially, all texture generation functions are set to GL\_EYE\_LINEAR and are disabled.</span></span> <span data-ttu-id="d5f76-158">這兩個平面方能 (1、0、0、0) ;這兩個 t 平面方能 (0、1、0、0) ;和所有 r 和 q 平面方能 (0、0、0、0) 。</span><span class="sxs-lookup"><span data-stu-id="d5f76-158">Both s plane equations are (1,0,0,0); both t plane equations are (0,1,0,0); and all r and q plane equations are (0,0,0,0).</span></span>

<span data-ttu-id="d5f76-159">下列函式會取出與 glTexGen 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="d5f76-159">The following functions retrieve information related to glTexGen:</span></span>

<dl>

[<span data-ttu-id="d5f76-160">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="d5f76-160">**glGetTexGen**</span></span>](glgettexgen.md)  
<span data-ttu-id="d5f76-161">[](glisenabled.md)具有引數 GL \_ 材質 \_ GEN \_ S 的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="d5f76-161">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_S</span></span>  
<span data-ttu-id="d5f76-162">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ 材質 \_ GEN \_ T</span><span class="sxs-lookup"><span data-stu-id="d5f76-162">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_T</span></span>  
<span data-ttu-id="d5f76-163">[](glisenabled.md)具有引數 GL \_ 材質 \_ GEN \_ R 的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="d5f76-163">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_R</span></span>  
<span data-ttu-id="d5f76-164">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ 材質 \_ GEN 的 \_ Q</span><span class="sxs-lookup"><span data-stu-id="d5f76-164">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_Q</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="d5f76-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5f76-165">Requirements</span></span>



| <span data-ttu-id="d5f76-166">需求</span><span class="sxs-lookup"><span data-stu-id="d5f76-166">Requirement</span></span> | <span data-ttu-id="d5f76-167">值</span><span class="sxs-lookup"><span data-stu-id="d5f76-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f76-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5f76-168">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f76-169">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5f76-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d5f76-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5f76-170">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f76-171">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5f76-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d5f76-172">標頭</span><span class="sxs-lookup"><span data-stu-id="d5f76-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5f76-173"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="d5f76-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d5f76-174">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5f76-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5f76-175"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5f76-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d5f76-176">DLL</span><span class="sxs-lookup"><span data-stu-id="d5f76-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5f76-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5f76-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f76-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5f76-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f76-179">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d5f76-179">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d5f76-180">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d5f76-180">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d5f76-181">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="d5f76-181">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="d5f76-182">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="d5f76-182">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="d5f76-183">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="d5f76-183">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="d5f76-184">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="d5f76-184">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="d5f76-185">glTexEnv</span><span class="sxs-lookup"><span data-stu-id="d5f76-185">glTexEnv</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="d5f76-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="d5f76-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="d5f76-187">glTexParameter</span><span class="sxs-lookup"><span data-stu-id="d5f76-187">glTexParameter</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="d5f76-188">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="d5f76-188">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="d5f76-189">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="d5f76-189">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





