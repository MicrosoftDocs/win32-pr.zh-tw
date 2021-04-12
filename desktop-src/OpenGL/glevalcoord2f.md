---
title: 'glEvalCoord2f 函式 (Gl) '
description: GlEvalCoord2f 函數會評估啟用的二維地圖。
ms.assetid: feb2a324-9148-4e3f-8e6e-c545e36962c6
keywords:
- glEvalCoord2f 函式 OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e586991b319e047957ae53362534c1bb0c90590
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104321340"
---
# <a name="glevalcoord2f-function"></a><span data-ttu-id="02063-104">glEvalCoord2f 函式</span><span class="sxs-lookup"><span data-stu-id="02063-104">glEvalCoord2f function</span></span>

<span data-ttu-id="02063-105">[**GlEvalCoord2f**](glevalcoord2d.md)函數會評估啟用的二維地圖。</span><span class="sxs-lookup"><span data-stu-id="02063-105">The [**glEvalCoord2f**](glevalcoord2d.md) function evaluates enabled two-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="02063-106">語法</span><span class="sxs-lookup"><span data-stu-id="02063-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord2f(
   GLfloat u,
   GLfloat v
);
```



## <a name="parameters"></a><span data-ttu-id="02063-107">參數</span><span class="sxs-lookup"><span data-stu-id="02063-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02063-108">*u*</span><span class="sxs-lookup"><span data-stu-id="02063-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="02063-109">值，這個值是在上一個 [**glMap2**](glmap2.md)函式中定義之基礎函數的域座標 *u* 。</span><span class="sxs-lookup"><span data-stu-id="02063-109">A value that is the domain coordinate *u* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="02063-110">*V*</span><span class="sxs-lookup"><span data-stu-id="02063-110">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="02063-111">值，這個值是在上一個 [**glMap2**](glmap2.md)函式中定義之基礎函數的域座標 *v* 。</span><span class="sxs-lookup"><span data-stu-id="02063-111">A value that is the domain coordinate *v* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02063-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="02063-112">Return value</span></span>

<span data-ttu-id="02063-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="02063-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02063-114">備註</span><span class="sxs-lookup"><span data-stu-id="02063-114">Remarks</span></span>

<span data-ttu-id="02063-115">[**GlEvalCoord2f**](glevalcoord2d.md)函式會使用兩個定義域值（ *u* 和 *v*）來評估啟用的二維地圖。</span><span class="sxs-lookup"><span data-stu-id="02063-115">The [**glEvalCoord2f**](glevalcoord2d.md) function evaluates enabled two-dimensional maps using two domain values, *u* and *v*.</span></span> <span data-ttu-id="02063-116">使用 [**glMap2**](glmap2.md)定義對應。</span><span class="sxs-lookup"><span data-stu-id="02063-116">Define maps with [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="02063-117">使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md)來啟用或停用它們。</span><span class="sxs-lookup"><span data-stu-id="02063-117">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="02063-118">當發出其中一個 **glEvalCoord** 函式時，會評估指定維度目前啟用的所有對應。</span><span class="sxs-lookup"><span data-stu-id="02063-118">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="02063-119">然後，針對每個已啟用的對應，就像是以計算的值發出對應的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="02063-119">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="02063-120">也就是說，如果 \_ \_ 已啟用 GL MAP1 INDEX 或 gl \_ list.map2 \_ 索引，則會模擬 [**glIndex**](glindex-functions.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="02063-120">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="02063-121">如果 \_ \_ 已啟用 gl MAP1 color \_ 4 或 gl \_ list.map2 \_ color \_ 4，則會模擬 **glcolor** 函數。</span><span class="sxs-lookup"><span data-stu-id="02063-121">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="02063-122">如果 GL \_ MAP1 \_ NORMAL 或 gl \_ list.map2 \_ normal 已啟用，系統會產生一般向量，而且如果有任何 GL \_ MAP1 \_ 材質 \_ COORD \_ 1、gl \_ MAP1 \_ 材質 \_ COORD \_ 2、GL \_ MAP1 \_ 材質 \_ COORD \_ 3、GL \_ MAP1 \_ 材質 \_ COORD \_ 4、gl \_ list.map2 \_ 材質 \_ COORD \_ 1、gl \_ list.map2 \_ 材質 \_ COORD \_ 2、gl \_ list.map2 \_ 材質 \_ COORD \_ 3 和 gl \_ list.map2 \_ 材質 \_ COORD \_ 4 已啟用，則會模擬適當的 [**glTexCoord**](gltexcoord-functions.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="02063-122">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="02063-123">OpenGL 會針對已啟用的評估使用評估值（而非目前的值），而針對色彩、色彩索引、標準和材質座標使用目前的值。</span><span class="sxs-lookup"><span data-stu-id="02063-123">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="02063-124">不過，評估的值不會更新目前的值。</span><span class="sxs-lookup"><span data-stu-id="02063-124">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="02063-125">因此，如果 [**glVertex**](glvertex-functions.md) 函式與 **glEvalCoord** 函數交錯，則與 **glVertex** 函式相關聯的色彩、標準和材質座標不會受到 **glEvalCoord** 函式所產生之值的影響，但只能由最新的 [**glColor**](glcolor-functions.md)、 [**glIndex**](glindex-functions.md)、 [**glNormal**](glnormal-functions.md)和 [**glTexCoord**](gltexcoord-functions.md) 函數所影響。</span><span class="sxs-lookup"><span data-stu-id="02063-125">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="02063-126">如果啟用自動一般產生， [**glEvalCoord2f**](glevalcoord2d.md) 會使用引數 GL AUTO normal 來呼叫 [**glEnable**](glenable.md) ， \_ \_ 以產生介面法線 ANALYTICALLY，不論內容或啟用 GL \_ list.map2 \_ 一般地圖。</span><span class="sxs-lookup"><span data-stu-id="02063-126">If automatic normal generation is enabled, [**glEvalCoord2f**](glevalcoord2d.md) calls [**glEnable**](glenable.md) with argument GL\_AUTO\_NORMAL to generate surface normals analytically, regardless of the contents or enabling of the GL\_MAP2\_NORMAL map.</span></span> <span data-ttu-id="02063-127">Let</span><span class="sxs-lookup"><span data-stu-id="02063-127">Let</span></span>

![顯示地圖 m 之交叉乘積值的方程式。](images/evlcrd01.png)

<span data-ttu-id="02063-129">產生的一般 **n** 為</span><span class="sxs-lookup"><span data-stu-id="02063-129">The generated normal **n** is</span></span>

![顯示對應所產生之一般 n 的方程式。](images/evlcrd02.png)

<span data-ttu-id="02063-131">下列函式會取出與 [**glEvalCoord2f**](glevalcoord2d.md) 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="02063-131">The following functions retrieve information related to the [**glEvalCoord2f**](glevalcoord2d.md) function:</span></span>

<span data-ttu-id="02063-132">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 頂點 \_ 3</span><span class="sxs-lookup"><span data-stu-id="02063-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="02063-133">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 頂點 \_ 4</span><span class="sxs-lookup"><span data-stu-id="02063-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="02063-134">[](glisenabled.md)具有引數 GL \_ MAP1 \_ 索引的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="02063-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="02063-135">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 色彩 \_ 4</span><span class="sxs-lookup"><span data-stu-id="02063-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="02063-136">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="02063-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="02063-137">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 1</span><span class="sxs-lookup"><span data-stu-id="02063-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="02063-138">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 2</span><span class="sxs-lookup"><span data-stu-id="02063-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="02063-139">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 3</span><span class="sxs-lookup"><span data-stu-id="02063-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="02063-140">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 4</span><span class="sxs-lookup"><span data-stu-id="02063-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="02063-141">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 頂點 \_ 3</span><span class="sxs-lookup"><span data-stu-id="02063-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="02063-142">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 頂點 \_ 4</span><span class="sxs-lookup"><span data-stu-id="02063-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="02063-143">[](glisenabled.md)具有引數 GL \_ List.map2 \_ 索引的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="02063-143">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="02063-144">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 色彩 \_ 4</span><span class="sxs-lookup"><span data-stu-id="02063-144">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="02063-145">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="02063-145">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="02063-146">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 1</span><span class="sxs-lookup"><span data-stu-id="02063-146">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="02063-147">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 2</span><span class="sxs-lookup"><span data-stu-id="02063-147">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="02063-148">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 3</span><span class="sxs-lookup"><span data-stu-id="02063-148">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="02063-149">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 4</span><span class="sxs-lookup"><span data-stu-id="02063-149">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="02063-150">具有引數 GL 的 [**glIsEnabled**](glisenabled.md) \_ 自動 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="02063-150">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="02063-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="02063-151">Requirements</span></span>



| <span data-ttu-id="02063-152">需求</span><span class="sxs-lookup"><span data-stu-id="02063-152">Requirement</span></span> | <span data-ttu-id="02063-153">值</span><span class="sxs-lookup"><span data-stu-id="02063-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02063-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02063-154">Minimum supported client</span></span><br/> | <span data-ttu-id="02063-155">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02063-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="02063-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02063-156">Minimum supported server</span></span><br/> | <span data-ttu-id="02063-157">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02063-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02063-158">標頭</span><span class="sxs-lookup"><span data-stu-id="02063-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="02063-159"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="02063-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="02063-160">程式庫</span><span class="sxs-lookup"><span data-stu-id="02063-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="02063-161"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="02063-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="02063-162">DLL</span><span class="sxs-lookup"><span data-stu-id="02063-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02063-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02063-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02063-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02063-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02063-165">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="02063-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="02063-166">**glColor**</span><span class="sxs-lookup"><span data-stu-id="02063-166">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="02063-167">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="02063-167">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="02063-168">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="02063-168">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="02063-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="02063-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="02063-170">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="02063-170">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="02063-171">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="02063-171">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="02063-172">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="02063-172">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="02063-173">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="02063-173">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="02063-174">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="02063-174">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="02063-175">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="02063-175">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="02063-176">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="02063-176">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="02063-177">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="02063-177">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="02063-178">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="02063-178">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="02063-179">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="02063-179">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="02063-180">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="02063-180">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





