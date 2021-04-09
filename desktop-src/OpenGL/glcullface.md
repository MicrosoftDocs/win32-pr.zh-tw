---
title: 'glCullFace 函式 (Gl) '
description: GlCullFace 函式會指定是否可以挑選正面或後端面向的 facet。
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- glCullFace 函式 OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c20370e0fa8bcf746d1b835ee45725f76158fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934027"
---
# <a name="glcullface-function"></a><span data-ttu-id="418d2-104">glCullFace 函式</span><span class="sxs-lookup"><span data-stu-id="418d2-104">glCullFace function</span></span>

<span data-ttu-id="418d2-105">**GlCullFace** 函式會指定是否可以挑選正面或後端面向的 facet。</span><span class="sxs-lookup"><span data-stu-id="418d2-105">The **glCullFace** function specifies whether front-facing or back-facing facets can be culled.</span></span>

## <a name="syntax"></a><span data-ttu-id="418d2-106">語法</span><span class="sxs-lookup"><span data-stu-id="418d2-106">Syntax</span></span>


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="418d2-107">參數</span><span class="sxs-lookup"><span data-stu-id="418d2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="418d2-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="418d2-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="418d2-109">指定正面或後端面向是否為剔除的候選項目。</span><span class="sxs-lookup"><span data-stu-id="418d2-109">Specifies whether front-facing or back-facing facets are candidates for culling.</span></span> <span data-ttu-id="418d2-110">接受符號常數 GL \_ 前端、gl \_ 背面和 gl \_ 前端 \_ 和 \_ 後端。</span><span class="sxs-lookup"><span data-stu-id="418d2-110">The symbolic constants GL\_FRONT, GL\_BACK, and GL\_FRONT\_AND\_BACK are accepted.</span></span> <span data-ttu-id="418d2-111">預設值為 [GL \_ 回]。</span><span class="sxs-lookup"><span data-stu-id="418d2-111">The default value is GL\_BACK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="418d2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="418d2-112">Return value</span></span>

<span data-ttu-id="418d2-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="418d2-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="418d2-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="418d2-114">Error codes</span></span>

<span data-ttu-id="418d2-115">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="418d2-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="418d2-116">Name</span><span class="sxs-lookup"><span data-stu-id="418d2-116">Name</span></span>                                                                                                  | <span data-ttu-id="418d2-117">意義</span><span class="sxs-lookup"><span data-stu-id="418d2-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="418d2-118"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="418d2-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="418d2-119">*模式* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="418d2-119">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="418d2-120"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="418d2-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="418d2-121">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="418d2-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="418d2-122">備註</span><span class="sxs-lookup"><span data-stu-id="418d2-122">Remarks</span></span>

<span data-ttu-id="418d2-123">**GlCullFace** 函式會指定在啟用 Facet 剔除時，) 由 *模式* 所指定 (的正面或後端 facet 是否為挑選。</span><span class="sxs-lookup"><span data-stu-id="418d2-123">The **glCullFace** function specifies whether front-facing or back-facing facets are culled (as specified by *mode*) when facet culling is enabled.</span></span> <span data-ttu-id="418d2-124">您可以使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 搭配引數 GL 剔除臉部來啟用和停用 facet 剔除 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="418d2-124">You enable and disable facet culling using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_CULL\_FACE.</span></span> <span data-ttu-id="418d2-125">Facet 包括三角形、quadrilaterals、多邊形和矩形。</span><span class="sxs-lookup"><span data-stu-id="418d2-125">Facets include triangles, quadrilaterals, polygons, and rectangles.</span></span>

<span data-ttu-id="418d2-126">[**GlFrontFace**](glfrontface.md)函式會指定順向和逆時針的 facet 為正面和反向的面向。</span><span class="sxs-lookup"><span data-stu-id="418d2-126">The [**glFrontFace**](glfrontface.md) function specifies which of the clockwise and counterclockwise facets are front-facing and back-facing.</span></span>

<span data-ttu-id="418d2-127">如果 *模式* 是 GL \_ 前端 \_ 和 \_ 後端，則不會繪製任何 facet，但會繪製其他基本專案，例如點和線條。</span><span class="sxs-lookup"><span data-stu-id="418d2-127">If *mode* is GL\_FRONT\_AND\_BACK, no facets are drawn, but other primitives, such as points and lines, are drawn.</span></span>

<span data-ttu-id="418d2-128">下列函式會取出與 **glCullFace** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="418d2-128">The following functions retrieve information related to **glCullFace**:</span></span>

<span data-ttu-id="418d2-129">具有引數 GL 的 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)會 \_ 挑選 \_ 臉部 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="418d2-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CULL\_FACE\_MODE</span></span>

<span data-ttu-id="418d2-130">[**glIsEnabled**](glisenabled.md) 與引數 GL \_ 挑選 \_ 臉部</span><span class="sxs-lookup"><span data-stu-id="418d2-130">[**glIsEnabled**](glisenabled.md) with argument GL\_CULL\_FACE</span></span>

## <a name="requirements"></a><span data-ttu-id="418d2-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="418d2-131">Requirements</span></span>



| <span data-ttu-id="418d2-132">需求</span><span class="sxs-lookup"><span data-stu-id="418d2-132">Requirement</span></span> | <span data-ttu-id="418d2-133">值</span><span class="sxs-lookup"><span data-stu-id="418d2-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="418d2-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="418d2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="418d2-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="418d2-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="418d2-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="418d2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="418d2-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="418d2-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="418d2-138">標頭</span><span class="sxs-lookup"><span data-stu-id="418d2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="418d2-139"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="418d2-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="418d2-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="418d2-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="418d2-141"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="418d2-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="418d2-142">DLL</span><span class="sxs-lookup"><span data-stu-id="418d2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="418d2-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="418d2-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="418d2-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="418d2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="418d2-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="418d2-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="418d2-146">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="418d2-146">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="418d2-147">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="418d2-147">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="418d2-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="418d2-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="418d2-149">**glFrontFace**</span><span class="sxs-lookup"><span data-stu-id="418d2-149">**glFrontFace**</span></span>](glfrontface.md)
</dt> <dt>

[<span data-ttu-id="418d2-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="418d2-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="418d2-151">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="418d2-151">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





