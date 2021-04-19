---
title: 'glEnd 函式 (Gl) '
description: 'GlBegin 和 glend 函式會分隔基本或類似基本類型群組的頂點。 |glEnd 函式 (Gl) '
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
keywords:
- glEnd 函式 OpenGL
topic_type:
- apiref
api_name:
- glEnd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bb41395b3ed2e38a64094506e07e2a69ad1d52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986466"
---
# <a name="glend-function"></a><span data-ttu-id="0a510-105">glEnd 函式</span><span class="sxs-lookup"><span data-stu-id="0a510-105">glEnd function</span></span>

<span data-ttu-id="0a510-106">[**GlBegin**](glbegin.md)和 **glend** 函式會分隔基本或類似基本類型群組的頂點。</span><span class="sxs-lookup"><span data-stu-id="0a510-106">The [**glBegin**](glbegin.md) and **glend** functions delimit the vertices of a primitive or a group of like primitives.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a510-107">語法</span><span class="sxs-lookup"><span data-stu-id="0a510-107">Syntax</span></span>


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a><span data-ttu-id="0a510-108">參數</span><span class="sxs-lookup"><span data-stu-id="0a510-108">Parameters</span></span>

<span data-ttu-id="0a510-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="0a510-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a510-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a510-110">Return value</span></span>

<span data-ttu-id="0a510-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0a510-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0a510-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0a510-112">Error codes</span></span>

<span data-ttu-id="0a510-113">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0a510-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0a510-114">Name</span><span class="sxs-lookup"><span data-stu-id="0a510-114">Name</span></span>                                                                                                  | <span data-ttu-id="0a510-115">意義</span><span class="sxs-lookup"><span data-stu-id="0a510-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a510-116"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="0a510-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0a510-117">**GlVertex**、 **glColor**、 **glIndex**、 **glNormal**、 **glTexCoord**、 **glEvalCoord**、 **glEvalPoint**、 **glMaterial**、 **glEdgeFlag**、 **glCallList** 或 **glCallLists** 以外的函式會在 **glBegin** 與對應的 **glEnd** 之間呼叫。</span><span class="sxs-lookup"><span data-stu-id="0a510-117">A function other than **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **glEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList**, or **glCallLists** was called between **glBegin** and the corresponding **glEnd**.</span></span> <span data-ttu-id="0a510-118">函數 **glEnd** 是在呼叫對應的 **glBegin** 之前呼叫，或在 **glBegin** / **glEnd** 序列內呼叫 glBegin。</span><span class="sxs-lookup"><span data-stu-id="0a510-118">The function **glEnd** was called before the corresponding **glBegin** was called, or **glBegin** was called within a **glBegin**/**glEnd** sequence.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="0a510-119">備註</span><span class="sxs-lookup"><span data-stu-id="0a510-119">Remarks</span></span>

<span data-ttu-id="0a510-120">[**GlBegin**](glbegin.md)和 **glend** 函式會分隔定義基本或類似基本類型群組的頂點。</span><span class="sxs-lookup"><span data-stu-id="0a510-120">The [**glBegin**](glbegin.md) and **glend** functions delimit the vertices that define a primitive or a group of like primitives.</span></span> <span data-ttu-id="0a510-121">**GlBegin** 函式會接受單一引數，以指定頂點所組成的10個基本類型。</span><span class="sxs-lookup"><span data-stu-id="0a510-121">The **glBegin** function accepts a single argument that specifies which of ten primitives the vertices compose.</span></span> <span data-ttu-id="0a510-122">從1開始，將 *n* 做為整數計數，而 *n* 則是指定的頂點總數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0a510-122">Taking *n* as an integer count starting at one, and *N* as the total number of vertices specified, the interpretations are as follows:</span></span>

-   <span data-ttu-id="0a510-123">您只能在 **glBegin** 與 **GlEnd** 之間使用 OpenGL 函數的子集。</span><span class="sxs-lookup"><span data-stu-id="0a510-123">You can use only a subset of OpenGL functions between **glBegin** and **glEnd**.</span></span> <span data-ttu-id="0a510-124">您可以使用的函數如下：</span><span class="sxs-lookup"><span data-stu-id="0a510-124">The functions you can use are:</span></span>

    -   [<span data-ttu-id="0a510-125">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="0a510-125">**glVertex**</span></span>](glvertex-functions.md)
    -   [<span data-ttu-id="0a510-126">**glColor**</span><span class="sxs-lookup"><span data-stu-id="0a510-126">**glColor**</span></span>](glcolor-functions.md)
    -   [<span data-ttu-id="0a510-127">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="0a510-127">**glIndex**</span></span>](glindex-functions.md)
    -   [<span data-ttu-id="0a510-128">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="0a510-128">**glNormal**</span></span>](glnormal-functions.md)
    -   [<span data-ttu-id="0a510-129">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="0a510-129">**glTexCoord**</span></span>](gltexcoord-functions.md)
    -   [<span data-ttu-id="0a510-130">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="0a510-130">**glEvalCoord**</span></span>](glevalcoord-functions.md)
    -   [<span data-ttu-id="0a510-131">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="0a510-131">**glEvalPoint**</span></span>](glevalpoint.md)
    -   [<span data-ttu-id="0a510-132">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="0a510-132">**glMaterial**</span></span>](glmaterial-functions.md)
    -   [<span data-ttu-id="0a510-133">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="0a510-133">**glEdgeFlag**</span></span>](gledgeflag-functions.md)

    <span data-ttu-id="0a510-134">您也可以使用 [**glCallList**](glcalllist.md) 或 [**glCallLists**](glcalllists.md) 來執行只包含上述函式的顯示清單。</span><span class="sxs-lookup"><span data-stu-id="0a510-134">You can also use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) to execute display lists that include only the preceding functions.</span></span> <span data-ttu-id="0a510-135">如果在 **glBegin** 和 **glEnd** 之間呼叫任何其他 OpenGL 函數，則會設定錯誤旗標，並忽略函式。</span><span class="sxs-lookup"><span data-stu-id="0a510-135">If any other OpenGL function is called between **glBegin** and **glEnd**, the error flag is set and the function is ignored.</span></span>

-   <span data-ttu-id="0a510-136">無論在 **glBegin** 中為 *模式* 選擇的值為何，您可以在 **glBegin** 和 **glEnd** 之間定義的頂點數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="0a510-136">Regardless of the value chosen for *mode* in **glBegin**, there is no limit to the number of vertices you can define between **glBegin** and **glEnd**.</span></span> <span data-ttu-id="0a510-137">未完整指定的線條、三角形、quadrilaterals 和多邊形都不會繪製。</span><span class="sxs-lookup"><span data-stu-id="0a510-137">Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn.</span></span> <span data-ttu-id="0a510-138">當提供的頂點太少以指定單一基本或指定了不正確的頂點倍數時，不完整的規格結果。</span><span class="sxs-lookup"><span data-stu-id="0a510-138">Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified.</span></span> <span data-ttu-id="0a510-139">忽略不完整的基本類型;繪製完整的基本專案。</span><span class="sxs-lookup"><span data-stu-id="0a510-139">The incomplete primitive is ignored; the complete primitives are drawn.</span></span>
-   <span data-ttu-id="0a510-140">每個基本類型頂點的最小規格為：</span><span class="sxs-lookup"><span data-stu-id="0a510-140">The minimum specification of vertices for each primitive is:</span></span> 

    | <span data-ttu-id="0a510-141">頂點的最小數目</span><span class="sxs-lookup"><span data-stu-id="0a510-141">Minimum number of vertices</span></span> | <span data-ttu-id="0a510-142">基本類型</span><span class="sxs-lookup"><span data-stu-id="0a510-142">Type of primitive</span></span> |
    |----------------------------|-------------------|
    | <span data-ttu-id="0a510-143">1</span><span class="sxs-lookup"><span data-stu-id="0a510-143">1</span></span>                          | <span data-ttu-id="0a510-144">點</span><span class="sxs-lookup"><span data-stu-id="0a510-144">point</span></span>             |
    | <span data-ttu-id="0a510-145">2</span><span class="sxs-lookup"><span data-stu-id="0a510-145">2</span></span>                          | <span data-ttu-id="0a510-146">line</span><span class="sxs-lookup"><span data-stu-id="0a510-146">line</span></span>              |
    | <span data-ttu-id="0a510-147">3</span><span class="sxs-lookup"><span data-stu-id="0a510-147">3</span></span>                          | <span data-ttu-id="0a510-148">三角形</span><span class="sxs-lookup"><span data-stu-id="0a510-148">triangle</span></span>          |
    | <span data-ttu-id="0a510-149">4</span><span class="sxs-lookup"><span data-stu-id="0a510-149">4</span></span>                          | <span data-ttu-id="0a510-150">四邊形</span><span class="sxs-lookup"><span data-stu-id="0a510-150">quadrilateral</span></span>     |
    | <span data-ttu-id="0a510-151">3</span><span class="sxs-lookup"><span data-stu-id="0a510-151">3</span></span>                          | <span data-ttu-id="0a510-152">多邊形</span><span class="sxs-lookup"><span data-stu-id="0a510-152">polygon</span></span>           |

    

     

-   <span data-ttu-id="0a510-153">需要特定多個頂點的模式為 GL \_ 行 (2) 、gl \_ 三角形 (3) 、gl \_ 四邊形 (4) 和 GL 四 \_ \_ 個 () 。</span><span class="sxs-lookup"><span data-stu-id="0a510-153">Modes that require a certain multiple of vertices are GL\_LINES (2), GL\_TRIANGLES (3), GL\_QUADS (4), and GL\_QUAD\_STRIP (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a510-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a510-154">Requirements</span></span>



| <span data-ttu-id="0a510-155">需求</span><span class="sxs-lookup"><span data-stu-id="0a510-155">Requirement</span></span> | <span data-ttu-id="0a510-156">值</span><span class="sxs-lookup"><span data-stu-id="0a510-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a510-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a510-157">Minimum supported client</span></span><br/> | <span data-ttu-id="0a510-158">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a510-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0a510-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a510-159">Minimum supported server</span></span><br/> | <span data-ttu-id="0a510-160">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a510-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0a510-161">標頭</span><span class="sxs-lookup"><span data-stu-id="0a510-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a510-162"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="0a510-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0a510-163">程式庫</span><span class="sxs-lookup"><span data-stu-id="0a510-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a510-164"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a510-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0a510-165">DLL</span><span class="sxs-lookup"><span data-stu-id="0a510-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a510-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a510-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a510-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a510-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a510-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0a510-168">**glBegin**</span></span>](/windows/desktop/OpenGL/glbegin)
</dt> <dt>

[<span data-ttu-id="0a510-169">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="0a510-169">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="0a510-170">**glColor**</span><span class="sxs-lookup"><span data-stu-id="0a510-170">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="0a510-171">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="0a510-171">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="0a510-172">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="0a510-172">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="0a510-173">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="0a510-173">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="0a510-174">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="0a510-174">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="0a510-175">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="0a510-175">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="0a510-176">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="0a510-176">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="0a510-177">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="0a510-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="0a510-178">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="0a510-178">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

