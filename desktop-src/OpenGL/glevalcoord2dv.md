---
title: 'glEvalCoord2dv 函式 (Gl) '
description: GlEvalCoord2dv 函數會評估啟用的二維地圖。
ms.assetid: 726a0c0c-d69e-46dc-b78e-a0d1e9ad97cd
keywords:
- glEvalCoord2dv 函式 OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a685606fb1445c6841efdf506a1f2d4747da838
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104561094"
---
# <a name="glevalcoord2dv-function"></a><span data-ttu-id="b18d1-104">glEvalCoord2dv 函式</span><span class="sxs-lookup"><span data-stu-id="b18d1-104">glEvalCoord2dv function</span></span>

<span data-ttu-id="b18d1-105">**GlEvalCoord2dv** 函數會評估啟用的二維地圖。</span><span class="sxs-lookup"><span data-stu-id="b18d1-105">The **glEvalCoord2dv** function evaluates enabled two-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="b18d1-106">語法</span><span class="sxs-lookup"><span data-stu-id="b18d1-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord2dv(
   const GLdouble *u
);
```



## <a name="parameters"></a><span data-ttu-id="b18d1-107">參數</span><span class="sxs-lookup"><span data-stu-id="b18d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b18d1-108">*u*</span><span class="sxs-lookup"><span data-stu-id="b18d1-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="b18d1-109">陣列的指標，該陣列包含網域座標 *u*。</span><span class="sxs-lookup"><span data-stu-id="b18d1-109">A pointer to an array containing the domain coordinate *u*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b18d1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b18d1-110">Return value</span></span>

<span data-ttu-id="b18d1-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b18d1-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b18d1-112">備註</span><span class="sxs-lookup"><span data-stu-id="b18d1-112">Remarks</span></span>

<span data-ttu-id="b18d1-113">**GlEvalCoord2dv** 函式會使用兩個定義域值（ *u* 和 *v*）來評估啟用的二維地圖。</span><span class="sxs-lookup"><span data-stu-id="b18d1-113">The **glEvalCoord2dv** function evaluates enabled two-dimensional maps using two domain values, *u* and *v*.</span></span> <span data-ttu-id="b18d1-114">使用 [**glMap1**](glmap1.md)定義對應。</span><span class="sxs-lookup"><span data-stu-id="b18d1-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="b18d1-115">使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md)來啟用或停用它們。</span><span class="sxs-lookup"><span data-stu-id="b18d1-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="b18d1-116">當發出其中一個 **glEvalCoord** 函式時，會評估指定維度目前啟用的所有對應。</span><span class="sxs-lookup"><span data-stu-id="b18d1-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="b18d1-117">然後，針對每個已啟用的對應，就像是以計算的值發出對應的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="b18d1-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="b18d1-118">也就是說，如果 \_ \_ 已啟用 GL MAP1 INDEX 或 gl \_ list.map2 \_ 索引，則會模擬 [**glIndex**](glindex-functions.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="b18d1-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="b18d1-119">如果 \_ \_ 已啟用 gl MAP1 color \_ 4 或 gl \_ list.map2 \_ color \_ 4，則會模擬 **glcolor** 函數。</span><span class="sxs-lookup"><span data-stu-id="b18d1-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="b18d1-120">如果 GL \_ MAP1 \_ NORMAL 或 gl \_ list.map2 \_ normal 已啟用，系統會產生一般向量，而且如果有任何 GL \_ MAP1 \_ 材質 \_ COORD \_ 1、gl \_ MAP1 \_ 材質 \_ COORD \_ 2、GL \_ MAP1 \_ 材質 \_ COORD \_ 3、GL \_ MAP1 \_ 材質 \_ COORD \_ 4、gl \_ list.map2 \_ 材質 \_ COORD \_ 1、gl \_ list.map2 \_ 材質 \_ COORD \_ 2、gl \_ list.map2 \_ 材質 \_ COORD \_ 3 和 gl \_ list.map2 \_ 材質 \_ COORD \_ 4 已啟用，則會模擬適當的 [**glTexCoord**](gltexcoord-functions.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="b18d1-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="b18d1-121">OpenGL 會針對已啟用的評估使用評估值（而非目前的值），而針對色彩、色彩索引、標準和材質座標使用目前的值。</span><span class="sxs-lookup"><span data-stu-id="b18d1-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="b18d1-122">不過，評估的值不會更新目前的值。</span><span class="sxs-lookup"><span data-stu-id="b18d1-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="b18d1-123">因此，如果 [**glVertex**](glvertex-functions.md) 函式與 **glEvalCoord** 函數交錯，則與 **glVertex** 函式相關聯的色彩、標準和材質座標不會受到 **glEvalCoord** 函式所產生之值的影響，但只能由最新的 [**glColor**](glcolor-functions.md)、 [**glIndex**](glindex-functions.md)、 [**glNormal**](glnormal-functions.md)和 [**glTexCoord**](gltexcoord-functions.md) 函數所影響。</span><span class="sxs-lookup"><span data-stu-id="b18d1-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="b18d1-124">如果啟用自動一般產生， **glEvalCoord2dv** 會使用引數 GL AUTO normal 來呼叫 [**glEnable**](glenable.md) ， \_ \_ 以產生介面法線 ANALYTICALLY，不論內容或啟用 GL \_ list.map2 \_ 一般地圖。</span><span class="sxs-lookup"><span data-stu-id="b18d1-124">If automatic normal generation is enabled, **glEvalCoord2dv** calls [**glEnable**](glenable.md) with argument GL\_AUTO\_NORMAL to generate surface normals analytically, regardless of the contents or enabling of the GL\_MAP2\_NORMAL map.</span></span> <span data-ttu-id="b18d1-125">Let</span><span class="sxs-lookup"><span data-stu-id="b18d1-125">Let</span></span>

![顯示地圖 m 之交叉乘積值的方程式。](images/evlcrd01.png)

<span data-ttu-id="b18d1-127">產生的一般 **n** 為</span><span class="sxs-lookup"><span data-stu-id="b18d1-127">The generated normal **n** is</span></span>

![顯示對應所產生之一般 n 的方程式。](images/evlcrd02.png)

<span data-ttu-id="b18d1-129">下列函式會取出與 **glEvalCoord2dv** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="b18d1-129">The following functions retrieve information related to the **glEvalCoord2dv** function:</span></span>

<span data-ttu-id="b18d1-130">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 頂點 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b18d1-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="b18d1-131">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 頂點 \_ 4</span><span class="sxs-lookup"><span data-stu-id="b18d1-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="b18d1-132">[](glisenabled.md)具有引數 GL \_ MAP1 \_ 索引的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="b18d1-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="b18d1-133">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 色彩 \_ 4</span><span class="sxs-lookup"><span data-stu-id="b18d1-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="b18d1-134">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="b18d1-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="b18d1-135">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 1</span><span class="sxs-lookup"><span data-stu-id="b18d1-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="b18d1-136">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 2</span><span class="sxs-lookup"><span data-stu-id="b18d1-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="b18d1-137">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 3</span><span class="sxs-lookup"><span data-stu-id="b18d1-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="b18d1-138">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 4</span><span class="sxs-lookup"><span data-stu-id="b18d1-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="b18d1-139">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 頂點 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b18d1-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="b18d1-140">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 頂點 \_ 4</span><span class="sxs-lookup"><span data-stu-id="b18d1-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="b18d1-141">[](glisenabled.md)具有引數 GL \_ List.map2 \_ 索引的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="b18d1-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="b18d1-142">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 色彩 \_ 4</span><span class="sxs-lookup"><span data-stu-id="b18d1-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="b18d1-143">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="b18d1-143">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="b18d1-144">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 1</span><span class="sxs-lookup"><span data-stu-id="b18d1-144">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="b18d1-145">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 2</span><span class="sxs-lookup"><span data-stu-id="b18d1-145">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="b18d1-146">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 3</span><span class="sxs-lookup"><span data-stu-id="b18d1-146">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="b18d1-147">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 4</span><span class="sxs-lookup"><span data-stu-id="b18d1-147">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="b18d1-148">具有引數 GL 的 [**glIsEnabled**](glisenabled.md) \_ 自動 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="b18d1-148">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="b18d1-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="b18d1-149">Requirements</span></span>



| <span data-ttu-id="b18d1-150">需求</span><span class="sxs-lookup"><span data-stu-id="b18d1-150">Requirement</span></span> | <span data-ttu-id="b18d1-151">值</span><span class="sxs-lookup"><span data-stu-id="b18d1-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b18d1-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b18d1-152">Minimum supported client</span></span><br/> | <span data-ttu-id="b18d1-153">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b18d1-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b18d1-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b18d1-154">Minimum supported server</span></span><br/> | <span data-ttu-id="b18d1-155">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b18d1-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b18d1-156">標頭</span><span class="sxs-lookup"><span data-stu-id="b18d1-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="b18d1-157"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="b18d1-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b18d1-158">程式庫</span><span class="sxs-lookup"><span data-stu-id="b18d1-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="b18d1-159"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b18d1-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b18d1-160">DLL</span><span class="sxs-lookup"><span data-stu-id="b18d1-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b18d1-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b18d1-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b18d1-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b18d1-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b18d1-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b18d1-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b18d1-164">**glColor**</span><span class="sxs-lookup"><span data-stu-id="b18d1-164">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="b18d1-165">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="b18d1-165">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="b18d1-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="b18d1-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="b18d1-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b18d1-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b18d1-168">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="b18d1-168">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="b18d1-169">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="b18d1-169">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="b18d1-170">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="b18d1-170">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="b18d1-171">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="b18d1-171">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="b18d1-172">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="b18d1-172">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="b18d1-173">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="b18d1-173">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="b18d1-174">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="b18d1-174">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="b18d1-175">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="b18d1-175">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="b18d1-176">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="b18d1-176">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="b18d1-177">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="b18d1-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="b18d1-178">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="b18d1-178">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





