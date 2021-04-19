---
title: 'glLoadMatrixf 函式 (Gl) '
description: 'GlLoadMatrixf 函數會以任意矩陣取代目前的矩陣。 |glLoadMatrixf 函式 (Gl) '
ms.assetid: 6e1337b0-d1e7-4002-a561-d959d7f70942
keywords:
- glLoadMatrixf 函式 OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0c54f4f7f7255b2dde724cf018d57fab6cf3e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976419"
---
# <a name="glloadmatrixf-function"></a><span data-ttu-id="a08c8-105">glLoadMatrixf 函式</span><span class="sxs-lookup"><span data-stu-id="a08c8-105">glLoadMatrixf function</span></span>

<span data-ttu-id="a08c8-106">[**GlLoadMatrixd**](glloadmatrixd.md)和 **glLoadMatrixf** 函數會將目前的矩陣取代為任意矩陣。</span><span class="sxs-lookup"><span data-stu-id="a08c8-106">The [**glLoadMatrixd**](glloadmatrixd.md) and **glLoadMatrixf** functions replace the current matrix with an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a08c8-107">語法</span><span class="sxs-lookup"><span data-stu-id="a08c8-107">Syntax</span></span>


```C++
void WINAPI glLoadMatrixf(
   const GLfloat *m
);
```



## <a name="parameters"></a><span data-ttu-id="a08c8-108">參數</span><span class="sxs-lookup"><span data-stu-id="a08c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a08c8-109">*m*</span><span class="sxs-lookup"><span data-stu-id="a08c8-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="a08c8-110">以資料行主要順序儲存為16個連續值之4x4 矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="a08c8-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a08c8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a08c8-111">Return value</span></span>

<span data-ttu-id="a08c8-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a08c8-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a08c8-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="a08c8-113">Error codes</span></span>

<span data-ttu-id="a08c8-114">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a08c8-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a08c8-115">Name</span><span class="sxs-lookup"><span data-stu-id="a08c8-115">Name</span></span>                                                                                                  | <span data-ttu-id="a08c8-116">意義</span><span class="sxs-lookup"><span data-stu-id="a08c8-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a08c8-117"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="a08c8-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a08c8-118">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="a08c8-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a08c8-119">備註</span><span class="sxs-lookup"><span data-stu-id="a08c8-119">Remarks</span></span>

<span data-ttu-id="a08c8-120">**GlLoadMatrix** 函式會將目前的矩陣取代為在 *m* 中指定的矩陣。</span><span class="sxs-lookup"><span data-stu-id="a08c8-120">The **glLoadMatrix** function replaces the current matrix with the one specified in *m*.</span></span> <span data-ttu-id="a08c8-121">目前的矩陣是投射矩陣、模型矩陣或紋理矩陣，由目前的矩陣模式決定 (查看 [**glMatrixMode**](glmatrixmode.md)) 。</span><span class="sxs-lookup"><span data-stu-id="a08c8-121">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="a08c8-122">*M* 參數指向以資料行主要順序儲存之單精確度或雙精確度浮點值的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="a08c8-122">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="a08c8-123">也就是說，矩陣的儲存方式如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="a08c8-123">That is, the matrix is stored as shown in the following image.</span></span>

![顯示 m 參數所指向之4x4 矩陣的圖表。](images/load02.png)

<span data-ttu-id="a08c8-125">下列函式會取出與 **glLoadMatrix** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="a08c8-125">The following functions retrieve information related to **glLoadMatrix**:</span></span>

<span data-ttu-id="a08c8-126">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="a08c8-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="a08c8-127">具有引數 GL \_ 模型 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="a08c8-127">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="a08c8-128">具有引數 GL \_ 投射 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="a08c8-128">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="a08c8-129">具有引數 GL \_ 材質 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="a08c8-129">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="a08c8-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="a08c8-130">Requirements</span></span>



| <span data-ttu-id="a08c8-131">需求</span><span class="sxs-lookup"><span data-stu-id="a08c8-131">Requirement</span></span> | <span data-ttu-id="a08c8-132">值</span><span class="sxs-lookup"><span data-stu-id="a08c8-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a08c8-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a08c8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a08c8-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a08c8-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a08c8-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a08c8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a08c8-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a08c8-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a08c8-137">標頭</span><span class="sxs-lookup"><span data-stu-id="a08c8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a08c8-138"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="a08c8-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a08c8-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="a08c8-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="a08c8-140"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a08c8-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a08c8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a08c8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a08c8-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a08c8-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a08c8-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a08c8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08c8-144">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a08c8-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a08c8-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a08c8-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a08c8-146">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="a08c8-146">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="a08c8-147">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="a08c8-147">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="a08c8-148">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="a08c8-148">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="a08c8-149">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="a08c8-149">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





