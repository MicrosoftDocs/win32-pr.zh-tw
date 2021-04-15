---
title: 'glMultMatrixf 函式 (Gl) '
description: 'GlMultMatrixf 函式會將目前的矩陣乘以任意矩陣。 |glMultMatrixf 函式 (Gl) '
ms.assetid: fea5e557-09bd-4c45-89cc-9f3739b577bb
keywords:
- glMultMatrixf 函式 OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f981b78dc2d9f152a4a7d1f40c4a2d1f120944b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104554727"
---
# <a name="glmultmatrixf-function"></a><span data-ttu-id="f3faf-105">glMultMatrixf 函式</span><span class="sxs-lookup"><span data-stu-id="f3faf-105">glMultMatrixf function</span></span>

<span data-ttu-id="f3faf-106">[**GlMultMatrixd**](glmultmatrixd.md)和 **glMultMatrixf** 函數會將目前的矩陣乘以任意矩陣。</span><span class="sxs-lookup"><span data-stu-id="f3faf-106">The [**glMultMatrixd**](glmultmatrixd.md) and **glMultMatrixf** functions multiply the current matrix by an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3faf-107">語法</span><span class="sxs-lookup"><span data-stu-id="f3faf-107">Syntax</span></span>


```C++
void WINAPI glMultMatrixf(
   const GLfloat *m
);
```



## <a name="parameters"></a><span data-ttu-id="f3faf-108">參數</span><span class="sxs-lookup"><span data-stu-id="f3faf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3faf-109">*m*</span><span class="sxs-lookup"><span data-stu-id="f3faf-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="f3faf-110">以資料行主要順序儲存為16個連續值之4x4 矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="f3faf-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3faf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3faf-111">Return value</span></span>

<span data-ttu-id="f3faf-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f3faf-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f3faf-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f3faf-113">Error codes</span></span>

<span data-ttu-id="f3faf-114">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f3faf-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f3faf-115">Name</span><span class="sxs-lookup"><span data-stu-id="f3faf-115">Name</span></span>                                                                                                  | <span data-ttu-id="f3faf-116">意義</span><span class="sxs-lookup"><span data-stu-id="f3faf-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f3faf-117"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="f3faf-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f3faf-118">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="f3faf-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f3faf-119">備註</span><span class="sxs-lookup"><span data-stu-id="f3faf-119">Remarks</span></span>

<span data-ttu-id="f3faf-120">**GlMultMatrix** 函式會將目前的矩陣乘以 *m* 中指定的矩陣。</span><span class="sxs-lookup"><span data-stu-id="f3faf-120">The **glMultMatrix** function multiplies the current matrix by the one specified in *m*.</span></span> <span data-ttu-id="f3faf-121">也就是說，如果 M 是目前的矩陣，而 T 是傳遞給 **glMultMatrix** 的矩陣，則 m 會取代為 m T。</span><span class="sxs-lookup"><span data-stu-id="f3faf-121">That is, if M is the current matrix and T is the matrix passed to **glMultMatrix**, then M is replaced with M   T.</span></span>

<span data-ttu-id="f3faf-122">目前的矩陣是投射矩陣、模型矩陣或紋理矩陣，由目前的矩陣模式決定 (查看 [**glMatrixMode**](glmatrixmode.md)) 。</span><span class="sxs-lookup"><span data-stu-id="f3faf-122">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="f3faf-123">*M* 參數指向以資料行主要順序儲存之單精確度或雙精確度浮點值的4x4 矩陣。</span><span class="sxs-lookup"><span data-stu-id="f3faf-123">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="f3faf-124">也就是說，矩陣的儲存方式如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="f3faf-124">That is, the matrix is stored as shown in the following image.</span></span>

![![顯示 m 參數所指向之4x4 矩陣的圖表]。](images/multi01.png)

<span data-ttu-id="f3faf-126">下列函式會取出與 **glMultMatrix** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="f3faf-126">The following functions retrieve information related to **glMultMatrix**:</span></span>

<span data-ttu-id="f3faf-127">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="f3faf-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="f3faf-128">具有引數 GL \_ 模型 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="f3faf-128">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="f3faf-129">具有引數 GL \_ 投射 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="f3faf-129">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="f3faf-130">具有引數 GL \_ 材質 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="f3faf-130">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="f3faf-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3faf-131">Requirements</span></span>



| <span data-ttu-id="f3faf-132">需求</span><span class="sxs-lookup"><span data-stu-id="f3faf-132">Requirement</span></span> | <span data-ttu-id="f3faf-133">值</span><span class="sxs-lookup"><span data-stu-id="f3faf-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3faf-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3faf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f3faf-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3faf-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f3faf-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3faf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f3faf-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3faf-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f3faf-138">標頭</span><span class="sxs-lookup"><span data-stu-id="f3faf-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3faf-139"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="f3faf-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f3faf-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="f3faf-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="f3faf-141"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3faf-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f3faf-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f3faf-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3faf-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3faf-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3faf-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3faf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3faf-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f3faf-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f3faf-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f3faf-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f3faf-147">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="f3faf-147">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="f3faf-148">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="f3faf-148">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="f3faf-149">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="f3faf-149">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="f3faf-150">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="f3faf-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





