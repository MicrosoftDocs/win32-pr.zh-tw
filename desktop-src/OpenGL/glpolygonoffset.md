---
title: 'glPolygonOffset 函式 (Gl) '
description: GlPolygonOffset 函式會設定 OpenGL 用來計算深度值的小數位數和單位數。
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- glPolygonOffset 函式 OpenGL
topic_type:
- apiref
api_name:
- glPolygonOffset
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84fa7d130fcc300fc1ebe33d091253e33f2d1e03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384813"
---
# <a name="glpolygonoffset-function"></a><span data-ttu-id="d52a3-104">glPolygonOffset 函式</span><span class="sxs-lookup"><span data-stu-id="d52a3-104">glPolygonOffset function</span></span>

<span data-ttu-id="d52a3-105">**GlPolygonOffset** 函式會設定 OpenGL 用來計算深度值的小數位數和單位數。</span><span class="sxs-lookup"><span data-stu-id="d52a3-105">The **glPolygonOffset** function sets the scale and units OpenGL uses to calculate depth values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d52a3-106">語法</span><span class="sxs-lookup"><span data-stu-id="d52a3-106">Syntax</span></span>


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a><span data-ttu-id="d52a3-107">參數</span><span class="sxs-lookup"><span data-stu-id="d52a3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d52a3-108">*因素*</span><span class="sxs-lookup"><span data-stu-id="d52a3-108">*factor*</span></span> 
</dt> <dd>

<span data-ttu-id="d52a3-109">指定用來為每個多邊形建立可變深度位移的比例因數。</span><span class="sxs-lookup"><span data-stu-id="d52a3-109">Specifies a scale factor that is used to create a variable depth offset for each polygon.</span></span> <span data-ttu-id="d52a3-110">初始值為零。</span><span class="sxs-lookup"><span data-stu-id="d52a3-110">The initial value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="d52a3-111">*單位*</span><span class="sxs-lookup"><span data-stu-id="d52a3-111">*units*</span></span> 
</dt> <dd>

<span data-ttu-id="d52a3-112">指定乘以實值指定值的值，以建立常數深度位移。</span><span class="sxs-lookup"><span data-stu-id="d52a3-112">Specifies a value that is multiplied by an implementation-specific value to create a constant depth offset.</span></span> <span data-ttu-id="d52a3-113">初始值為0。</span><span class="sxs-lookup"><span data-stu-id="d52a3-113">The initial value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d52a3-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d52a3-114">Return value</span></span>

<span data-ttu-id="d52a3-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d52a3-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d52a3-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d52a3-116">Error codes</span></span>

<span data-ttu-id="d52a3-117">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d52a3-117">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d52a3-118">Name</span><span class="sxs-lookup"><span data-stu-id="d52a3-118">Name</span></span>                                                                                                  | <span data-ttu-id="d52a3-119">意義</span><span class="sxs-lookup"><span data-stu-id="d52a3-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d52a3-120"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="d52a3-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d52a3-121">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="d52a3-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d52a3-122">備註</span><span class="sxs-lookup"><span data-stu-id="d52a3-122">Remarks</span></span>

<span data-ttu-id="d52a3-123">當 \_ 啟用 GL 多邊形 \_ 位移時，每個片段的深度值將會在從適當頂點的深度值中插補之後位移。</span><span class="sxs-lookup"><span data-stu-id="d52a3-123">When GL\_POLYGON\_OFFSET is enabled, each fragment's depth value will be offset after it is interpolated from the depth values of the appropriate vertices.</span></span> <span data-ttu-id="d52a3-124">位移的值是 *係數* \* ？ z + r \* *單位*，其中？ z 是相對於多邊形螢幕區域的變更深度度量，而 r 是保證為指定的執行產生可解析位移的最小值。</span><span class="sxs-lookup"><span data-stu-id="d52a3-124">The value of the offset is *factor* \* ?z + r \**units*, where ?z is a measurement of the change in depth relative to the screen area of the polygon, and r is the smallest value that is guaranteed to produce a resolvable offset for a given implementation.</span></span> <span data-ttu-id="d52a3-125">在執行深度測試之前，以及將值寫入深度緩衝區之前，會加入位移。</span><span class="sxs-lookup"><span data-stu-id="d52a3-125">The offset is added before the depth test is performed and before the value is written into the depth buffer.</span></span>

<span data-ttu-id="d52a3-126">**GlPolygonOffset** 函式適用于轉譯隱藏行影像、將 decals 套用至表面，以及用來呈現具有反白顯示邊緣的純色。</span><span class="sxs-lookup"><span data-stu-id="d52a3-126">The **glPolygonOffset** function is useful for rendering hidden-line images, for applying decals to surfaces, and for rendering solids with highlighted edges.</span></span>

<span data-ttu-id="d52a3-127">**GlPolygonOffset** 函式對在意見緩衝區中放置的深度座標沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="d52a3-127">The **glPolygonOffset** function has no effect on depth coordinates placed in the feedback buffer.</span></span> <span data-ttu-id="d52a3-128">它也不會影響選取專案。</span><span class="sxs-lookup"><span data-stu-id="d52a3-128">It also has no effect on selection.</span></span>

<span data-ttu-id="d52a3-129">下列函式會取出與 **glPolygonOffset** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="d52a3-129">The following functions retrieve information related to **glPolygonOffset**:</span></span>

-   <span data-ttu-id="d52a3-130">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 多邊形 \_ 位移 \_ 因數的 glGet</span><span class="sxs-lookup"><span data-stu-id="d52a3-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_OFFSET\_FACTOR</span></span>
-   <span data-ttu-id="d52a3-131">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 多邊形 \_ 位移 \_ 單位的 glGet</span><span class="sxs-lookup"><span data-stu-id="d52a3-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_OFFSET\_UNITS</span></span>
-   <span data-ttu-id="d52a3-132">[](glisenabled.md)具有引數 GL \_ 多邊形 \_ 位移 \_ 填滿的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="d52a3-132">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_FILL</span></span>
-   <span data-ttu-id="d52a3-133">[](glisenabled.md)具有引數 GL \_ 多邊形 \_ 位移 \_ 線的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="d52a3-133">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_LINE</span></span>
-   <span data-ttu-id="d52a3-134">[](glisenabled.md)具有引數 GL \_ 多邊形 \_ 位移 \_ 點的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="d52a3-134">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_POINT</span></span>

> [!Note]  
> <span data-ttu-id="d52a3-135">**GlPolygonOffset** 函式僅適用于 OpenGl 1.1 版或更高版本。</span><span class="sxs-lookup"><span data-stu-id="d52a3-135">The **glPolygonOffset** function is only available in OpenGl version 1.1 or greater.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d52a3-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="d52a3-136">Requirements</span></span>



| <span data-ttu-id="d52a3-137">需求</span><span class="sxs-lookup"><span data-stu-id="d52a3-137">Requirement</span></span> | <span data-ttu-id="d52a3-138">值</span><span class="sxs-lookup"><span data-stu-id="d52a3-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d52a3-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d52a3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d52a3-140">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d52a3-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d52a3-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d52a3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d52a3-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d52a3-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d52a3-143">標頭</span><span class="sxs-lookup"><span data-stu-id="d52a3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="d52a3-144"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="d52a3-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d52a3-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="d52a3-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="d52a3-146"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d52a3-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d52a3-147">DLL</span><span class="sxs-lookup"><span data-stu-id="d52a3-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d52a3-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d52a3-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d52a3-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d52a3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d52a3-150">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="d52a3-150">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="d52a3-151">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="d52a3-151">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="d52a3-152">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="d52a3-152">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="d52a3-153">**glGet**</span><span class="sxs-lookup"><span data-stu-id="d52a3-153">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="d52a3-154">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="d52a3-154">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="d52a3-155">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="d52a3-155">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="d52a3-156">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="d52a3-156">**glStencilOp**</span></span>](glstencilop.md)
</dt> <dt>

[<span data-ttu-id="d52a3-157">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="d52a3-157">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





