---
title: 'glMatrixMode 函式 (Gl) '
description: GlMatrixMode 函數會指定哪一個矩陣是目前的矩陣。
ms.assetid: f1006ea3-322a-42a9-b33c-6c7181985ef9
keywords:
- glMatrixMode 函式 OpenGL
topic_type:
- apiref
api_name:
- glMatrixMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9877d62fc6e721cc6757206c7c2d07d24f3e879b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104681"
---
# <a name="glmatrixmode-function"></a><span data-ttu-id="4ccaa-104">glMatrixMode 函式</span><span class="sxs-lookup"><span data-stu-id="4ccaa-104">glMatrixMode function</span></span>

<span data-ttu-id="4ccaa-105">**GlMatrixMode** 函數會指定哪一個矩陣是目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-105">The **glMatrixMode** function specifies which matrix is the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ccaa-106">語法</span><span class="sxs-lookup"><span data-stu-id="4ccaa-106">Syntax</span></span>


```C++
void WINAPI glMatrixMode(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="4ccaa-107">參數</span><span class="sxs-lookup"><span data-stu-id="4ccaa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ccaa-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="4ccaa-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="4ccaa-109">矩陣堆疊，也就是後續矩陣作業的目標。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-109">The matrix stack that is the target for subsequent matrix operations.</span></span> <span data-ttu-id="4ccaa-110">*Mode* 參數可以採用三個值的其中一個。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-110">The *mode* parameter can assume one of three values.</span></span>



| <span data-ttu-id="4ccaa-111">值</span><span class="sxs-lookup"><span data-stu-id="4ccaa-111">Value</span></span>                                                                                                                                                         | <span data-ttu-id="4ccaa-112">意義</span><span class="sxs-lookup"><span data-stu-id="4ccaa-112">Meaning</span></span>                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="GL_MODELVIEW"></span><span id="gl_modelview"></span><dl> <span data-ttu-id="4ccaa-113"><dt>**GL \_ 模型**</dt></span><span class="sxs-lookup"><span data-stu-id="4ccaa-113"><dt>**GL\_MODELVIEW**</dt></span></span> </dl>    | <span data-ttu-id="4ccaa-114">將後續矩陣作業套用至模型矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-114">Applies subsequent matrix operations to the modelview matrix stack.</span></span><br/>  |
| <span id="GL_PROJECTION"></span><span id="gl_projection"></span><dl> <span data-ttu-id="4ccaa-115"><dt>**GL \_ 投射**</dt></span><span class="sxs-lookup"><span data-stu-id="4ccaa-115"><dt>**GL\_PROJECTION**</dt></span></span> </dl> | <span data-ttu-id="4ccaa-116">將後續矩陣作業套用至投射矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-116">Applies subsequent matrix operations to the projection matrix stack.</span></span><br/> |
| <span id="GL_TEXTURE"></span><span id="gl_texture"></span><dl> <span data-ttu-id="4ccaa-117"><dt>**GL \_ 材質**</dt></span><span class="sxs-lookup"><span data-stu-id="4ccaa-117"><dt>**GL\_TEXTURE**</dt></span></span> </dl>          | <span data-ttu-id="4ccaa-118">將後續矩陣作業套用至材質矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-118">Applies subsequent matrix operations to the texture matrix stack.</span></span><br/>    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ccaa-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ccaa-119">Return value</span></span>

<span data-ttu-id="4ccaa-120">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4ccaa-121">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="4ccaa-121">Error codes</span></span>

<span data-ttu-id="4ccaa-122">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4ccaa-123">Name</span><span class="sxs-lookup"><span data-stu-id="4ccaa-123">Name</span></span>                                                                                                  | <span data-ttu-id="4ccaa-124">意義</span><span class="sxs-lookup"><span data-stu-id="4ccaa-124">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4ccaa-125"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="4ccaa-125"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="4ccaa-126">*模式* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-126">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="4ccaa-127"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="4ccaa-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4ccaa-128">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4ccaa-129">備註</span><span class="sxs-lookup"><span data-stu-id="4ccaa-129">Remarks</span></span>

<span data-ttu-id="4ccaa-130">**GlMatrixMode** 函數會設定目前的矩陣模式。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-130">The **glMatrixMode** function sets the current matrix mode.</span></span>

<span data-ttu-id="4ccaa-131">下列函式會抓取 **glMatrixMode** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="4ccaa-131">The following function retrieves information related to **glMatrixMode**:</span></span>

<span data-ttu-id="4ccaa-132">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="4ccaa-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="4ccaa-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ccaa-133">Requirements</span></span>



| <span data-ttu-id="4ccaa-134">需求</span><span class="sxs-lookup"><span data-stu-id="4ccaa-134">Requirement</span></span> | <span data-ttu-id="4ccaa-135">值</span><span class="sxs-lookup"><span data-stu-id="4ccaa-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ccaa-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ccaa-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4ccaa-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ccaa-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4ccaa-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ccaa-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4ccaa-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ccaa-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4ccaa-140">標頭</span><span class="sxs-lookup"><span data-stu-id="4ccaa-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ccaa-141"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="4ccaa-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4ccaa-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="4ccaa-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="4ccaa-143"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ccaa-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4ccaa-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4ccaa-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ccaa-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ccaa-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ccaa-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ccaa-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ccaa-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4ccaa-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4ccaa-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4ccaa-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4ccaa-149">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="4ccaa-149">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="4ccaa-150">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="4ccaa-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





