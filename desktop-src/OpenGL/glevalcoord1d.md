---
title: 'glEvalCoord1d 函式 (Gl) '
description: GlEvalCoord1d 函數會評估啟用的一維對應。
ms.assetid: 5e884f11-fb3f-4158-8041-6c71509bf7d5
keywords:
- glEvalCoord1d 函式 OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239d0cc6267989bfd4ae020f1f8935c0cca1c192
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968331"
---
# <a name="glevalcoord1d-function"></a><span data-ttu-id="97371-104">glEvalCoord1d 函式</span><span class="sxs-lookup"><span data-stu-id="97371-104">glEvalCoord1d function</span></span>

<span data-ttu-id="97371-105">**GlEvalCoord1d** 函數會評估啟用的一維對應。</span><span class="sxs-lookup"><span data-stu-id="97371-105">The **glEvalCoord1d** function evaluates enabled one-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="97371-106">語法</span><span class="sxs-lookup"><span data-stu-id="97371-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord1d(
   GLdouble u
);
```



## <a name="parameters"></a><span data-ttu-id="97371-107">參數</span><span class="sxs-lookup"><span data-stu-id="97371-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97371-108">*u*</span><span class="sxs-lookup"><span data-stu-id="97371-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="97371-109">值，這個值是在上一個 [**glMap1**](glmap1.md)函式中定義之基礎函數的域座標 *u* 。</span><span class="sxs-lookup"><span data-stu-id="97371-109">A value that is the domain coordinate *u* to the basis function defined in a previous [**glMap1**](glmap1.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97371-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="97371-110">Return value</span></span>

<span data-ttu-id="97371-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="97371-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="97371-112">備註</span><span class="sxs-lookup"><span data-stu-id="97371-112">Remarks</span></span>

<span data-ttu-id="97371-113">**GlEvalCoord1d** 函式會評估在引數 *u* 啟用一維的地圖。</span><span class="sxs-lookup"><span data-stu-id="97371-113">The **glEvalCoord1d** function evaluates enabled one-dimensional maps at argument *u*.</span></span> <span data-ttu-id="97371-114">使用 [**glMap1**](glmap1.md)定義對應。</span><span class="sxs-lookup"><span data-stu-id="97371-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="97371-115">使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md)來啟用或停用它們。</span><span class="sxs-lookup"><span data-stu-id="97371-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="97371-116">當發出其中一個 **glEvalCoord** 函式時，會評估指定維度目前啟用的所有對應。</span><span class="sxs-lookup"><span data-stu-id="97371-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="97371-117">然後，針對每個已啟用的對應，就像是以計算的值發出對應的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="97371-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="97371-118">也就是說，如果 \_ \_ 已啟用 GL MAP1 INDEX 或 gl \_ list.map2 \_ 索引，則會模擬 [**glIndex**](glindex-functions.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="97371-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="97371-119">如果 \_ \_ 已啟用 gl MAP1 color \_ 4 或 gl \_ list.map2 \_ color \_ 4，則會模擬 **glcolor** 函數。</span><span class="sxs-lookup"><span data-stu-id="97371-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="97371-120">如果 GL \_ MAP1 \_ NORMAL 或 gl \_ list.map2 \_ normal 已啟用，系統會產生一般向量，而且如果有任何 GL \_ MAP1 \_ 材質 \_ COORD \_ 1、gl \_ MAP1 \_ 材質 \_ COORD \_ 2、GL \_ MAP1 \_ 材質 \_ COORD \_ 3、GL \_ MAP1 \_ 材質 \_ COORD \_ 4、gl \_ list.map2 \_ 材質 \_ COORD \_ 1、gl \_ list.map2 \_ 材質 \_ COORD \_ 2、gl \_ list.map2 \_ 材質 \_ COORD \_ 3 和 gl \_ list.map2 \_ 材質 \_ COORD \_ 4 已啟用，則會模擬適當的 [**glTexCoord**](gltexcoord-functions.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="97371-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="97371-121">OpenGL 會針對已啟用的評估使用評估值（而非目前的值），而針對色彩、色彩索引、標準和材質座標使用目前的值。</span><span class="sxs-lookup"><span data-stu-id="97371-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="97371-122">不過，評估的值不會更新目前的值。</span><span class="sxs-lookup"><span data-stu-id="97371-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="97371-123">因此，如果 [**glVertex**](glvertex-functions.md) 函式與 **glEvalCoord** 函數交錯，則與 **glVertex** 函式相關聯的色彩、標準和材質座標不會受到 **glEvalCoord** 函式所產生之值的影響，但只能由最新的 [**glColor**](glcolor-functions.md)、 [**glIndex**](glindex-functions.md)、 [**glNormal**](glnormal-functions.md)和 [**glTexCoord**](gltexcoord-functions.md) 函數所影響。</span><span class="sxs-lookup"><span data-stu-id="97371-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="97371-124">下列函式會取出與 **glEvalCoord1d** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="97371-124">The following functions retrieve information related to the **glEvalCoord1d** function:</span></span>

<span data-ttu-id="97371-125">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 頂點 \_ 3</span><span class="sxs-lookup"><span data-stu-id="97371-125">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="97371-126">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 頂點 \_ 4</span><span class="sxs-lookup"><span data-stu-id="97371-126">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="97371-127">[](glisenabled.md)具有引數 GL \_ MAP1 \_ 索引的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="97371-127">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="97371-128">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 色彩 \_ 4</span><span class="sxs-lookup"><span data-stu-id="97371-128">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="97371-129">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="97371-129">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="97371-130">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 1</span><span class="sxs-lookup"><span data-stu-id="97371-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="97371-131">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 2</span><span class="sxs-lookup"><span data-stu-id="97371-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="97371-132">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 3</span><span class="sxs-lookup"><span data-stu-id="97371-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="97371-133">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 4</span><span class="sxs-lookup"><span data-stu-id="97371-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="97371-134">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 頂點 \_ 3</span><span class="sxs-lookup"><span data-stu-id="97371-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="97371-135">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 頂點 \_ 4</span><span class="sxs-lookup"><span data-stu-id="97371-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="97371-136">[](glisenabled.md)具有引數 GL \_ List.map2 \_ 索引的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="97371-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="97371-137">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 色彩 \_ 4</span><span class="sxs-lookup"><span data-stu-id="97371-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="97371-138">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="97371-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="97371-139">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 1</span><span class="sxs-lookup"><span data-stu-id="97371-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="97371-140">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 2</span><span class="sxs-lookup"><span data-stu-id="97371-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="97371-141">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 3</span><span class="sxs-lookup"><span data-stu-id="97371-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="97371-142">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 4</span><span class="sxs-lookup"><span data-stu-id="97371-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="97371-143">具有引數 GL 的 [**glIsEnabled**](glisenabled.md) \_ 自動 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="97371-143">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="97371-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="97371-144">Requirements</span></span>



| <span data-ttu-id="97371-145">需求</span><span class="sxs-lookup"><span data-stu-id="97371-145">Requirement</span></span> | <span data-ttu-id="97371-146">值</span><span class="sxs-lookup"><span data-stu-id="97371-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97371-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97371-147">Minimum supported client</span></span><br/> | <span data-ttu-id="97371-148">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97371-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="97371-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97371-149">Minimum supported server</span></span><br/> | <span data-ttu-id="97371-150">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97371-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="97371-151">標頭</span><span class="sxs-lookup"><span data-stu-id="97371-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="97371-152"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="97371-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="97371-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="97371-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="97371-154"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="97371-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="97371-155">DLL</span><span class="sxs-lookup"><span data-stu-id="97371-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97371-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97371-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97371-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97371-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97371-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="97371-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="97371-159">**glColor**</span><span class="sxs-lookup"><span data-stu-id="97371-159">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="97371-160">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="97371-160">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="97371-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="97371-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="97371-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="97371-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="97371-163">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="97371-163">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="97371-164">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="97371-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="97371-165">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="97371-165">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="97371-166">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="97371-166">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="97371-167">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="97371-167">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="97371-168">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="97371-168">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="97371-169">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="97371-169">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="97371-170">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="97371-170">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="97371-171">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="97371-171">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="97371-172">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="97371-172">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="97371-173">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="97371-173">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





