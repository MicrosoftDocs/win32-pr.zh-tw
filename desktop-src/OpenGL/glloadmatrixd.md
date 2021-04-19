---
title: 'glLoadMatrixd 函式 (Gl) '
description: 'GlLoadMatrixd 函數會以任意矩陣取代目前的矩陣。 |glLoadMatrixd 函式 (Gl) '
ms.assetid: 66c499f7-3f55-4de2-b67b-5b775b5854e0
keywords:
- glLoadMatrixd 函式 OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4715da159dff60024adb3c7331cbf03c7c3759ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106982166"
---
# <a name="glloadmatrixd-function"></a><span data-ttu-id="e4c0a-105">glLoadMatrixd 函式</span><span class="sxs-lookup"><span data-stu-id="e4c0a-105">glLoadMatrixd function</span></span>

<span data-ttu-id="e4c0a-106">**GlLoadMatrixd** 和 [**glLoadMatrixf**](glloadmatrixf.md)函數會將目前的矩陣取代為任意矩陣。</span><span class="sxs-lookup"><span data-stu-id="e4c0a-106">The **glLoadMatrixd** and [**glLoadMatrixf**](glloadmatrixf.md) functions replace the current matrix with an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c0a-107">語法</span><span class="sxs-lookup"><span data-stu-id="e4c0a-107">Syntax</span></span>


```C++
void WINAPI glLoadMatrixd(
   const GLdouble *m
);
```



## <a name="parameters"></a><span data-ttu-id="e4c0a-108">參數</span><span class="sxs-lookup"><span data-stu-id="e4c0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4c0a-109">*m*</span><span class="sxs-lookup"><span data-stu-id="e4c0a-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="e4c0a-110">以資料行主要順序儲存為16個連續值之4x4 矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="e4c0a-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4c0a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4c0a-111">Return value</span></span>

<span data-ttu-id="e4c0a-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e4c0a-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e4c0a-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e4c0a-113">Error codes</span></span>

<span data-ttu-id="e4c0a-114">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e4c0a-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e4c0a-115">Name</span><span class="sxs-lookup"><span data-stu-id="e4c0a-115">Name</span></span>                                                                                                  | <span data-ttu-id="e4c0a-116">意義</span><span class="sxs-lookup"><span data-stu-id="e4c0a-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4c0a-117"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="e4c0a-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e4c0a-118">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="e4c0a-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e4c0a-119">備註</span><span class="sxs-lookup"><span data-stu-id="e4c0a-119">Remarks</span></span>

<span data-ttu-id="e4c0a-120">**GlLoadMatrix** 函式會將目前的矩陣取代為在 *m* 中指定的矩陣。</span><span class="sxs-lookup"><span data-stu-id="e4c0a-120">The **glLoadMatrix** function replaces the current matrix with the one specified in *m*.</span></span> <span data-ttu-id="e4c0a-121">目前的矩陣是投射矩陣、模型矩陣或紋理矩陣，由目前的矩陣模式決定 (查看 [**glMatrixMode**](glmatrixmode.md)) 。</span><span class="sxs-lookup"><span data-stu-id="e4c0a-121">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="e4c0a-122">*M* 參數指向以資料行主要順序儲存之單精確度或雙精確度浮點值的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="e4c0a-122">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="e4c0a-123">也就是說，矩陣的儲存方式如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="e4c0a-123">That is, the matrix is stored as shown in the following image.</span></span>

![顯示 m 參數所指向之4x4 矩陣的圖表。](images/load02.png)

<span data-ttu-id="e4c0a-125">下列函式會取出與 **glLoadMatrix** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="e4c0a-125">The following functions retrieve information related to **glLoadMatrix**:</span></span>

<span data-ttu-id="e4c0a-126">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="e4c0a-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="e4c0a-127">具有引數 GL \_ 模型 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="e4c0a-127">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="e4c0a-128">具有引數 GL \_ 投射 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="e4c0a-128">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="e4c0a-129">具有引數 GL \_ 材質 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="e4c0a-129">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="e4c0a-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4c0a-130">Requirements</span></span>



| <span data-ttu-id="e4c0a-131">需求</span><span class="sxs-lookup"><span data-stu-id="e4c0a-131">Requirement</span></span> | <span data-ttu-id="e4c0a-132">值</span><span class="sxs-lookup"><span data-stu-id="e4c0a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c0a-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4c0a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e4c0a-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4c0a-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e4c0a-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4c0a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e4c0a-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4c0a-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e4c0a-137">標頭</span><span class="sxs-lookup"><span data-stu-id="e4c0a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4c0a-138"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="e4c0a-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e4c0a-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="e4c0a-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4c0a-140"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4c0a-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e4c0a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e4c0a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4c0a-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4c0a-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4c0a-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4c0a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4c0a-144">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e4c0a-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e4c0a-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e4c0a-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e4c0a-146">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="e4c0a-146">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="e4c0a-147">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="e4c0a-147">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="e4c0a-148">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="e4c0a-148">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="e4c0a-149">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="e4c0a-149">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





