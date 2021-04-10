---
title: 'glStencilMask 函式 (Gl) '
description: GlStencilMask 函數控制樣板平面中個別位的寫入。
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- glStencilMask 函式 OpenGL
topic_type:
- apiref
api_name:
- glStencilMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63790fa30e88abbde6e1ba47e624c6caf2dcfc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106398"
---
# <a name="glstencilmask-function"></a><span data-ttu-id="1a640-104">glStencilMask 函式</span><span class="sxs-lookup"><span data-stu-id="1a640-104">glStencilMask function</span></span>

<span data-ttu-id="1a640-105">**GlStencilMask** 函數控制樣板平面中個別位的寫入。</span><span class="sxs-lookup"><span data-stu-id="1a640-105">The **glStencilMask** function controls the writing of individual bits in the stencil planes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a640-106">語法</span><span class="sxs-lookup"><span data-stu-id="1a640-106">Syntax</span></span>


```C++
void WINAPI glStencilMask(
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="1a640-107">參數</span><span class="sxs-lookup"><span data-stu-id="1a640-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a640-108">*面具*</span><span class="sxs-lookup"><span data-stu-id="1a640-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="1a640-109">用來啟用和停用在樣板平面中寫入個別位的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="1a640-109">A bit mask to enable and disable writing of individual bits in the stencil planes.</span></span> <span data-ttu-id="1a640-110">一開始，遮罩就是所有的遮罩。</span><span class="sxs-lookup"><span data-stu-id="1a640-110">Initially, the mask is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a640-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a640-111">Return value</span></span>

<span data-ttu-id="1a640-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1a640-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1a640-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1a640-113">Error codes</span></span>

<span data-ttu-id="1a640-114">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1a640-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1a640-115">Name</span><span class="sxs-lookup"><span data-stu-id="1a640-115">Name</span></span>                                                                                                  | <span data-ttu-id="1a640-116">意義</span><span class="sxs-lookup"><span data-stu-id="1a640-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1a640-117"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="1a640-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1a640-118">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="1a640-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1a640-119">備註</span><span class="sxs-lookup"><span data-stu-id="1a640-119">Remarks</span></span>

<span data-ttu-id="1a640-120">**GlStencilMask** 函數控制樣板平面中個別位的寫入。</span><span class="sxs-lookup"><span data-stu-id="1a640-120">The **glStencilMask** function controls the writing of individual bits in the stencil planes.</span></span> <span data-ttu-id="1a640-121">最不重要的 *n* 位 *遮罩*，其中 *n* 是樣板緩衝區中的位數，指定遮罩。</span><span class="sxs-lookup"><span data-stu-id="1a640-121">The least significant *n* bits of *mask*, where *n* is the number of bits in the stencil buffer, specify a mask.</span></span> <span data-ttu-id="1a640-122">當遮罩中出現一個時，會讓樣板緩衝區中的對應位成為可寫入的位置。</span><span class="sxs-lookup"><span data-stu-id="1a640-122">Wherever a one appears in the mask, the corresponding bit in the stencil buffer is made writable.</span></span> <span data-ttu-id="1a640-123">如果出現零，則位為寫入保護。</span><span class="sxs-lookup"><span data-stu-id="1a640-123">Where a zero appears, the bit is write-protected.</span></span> <span data-ttu-id="1a640-124">一開始，所有位都會啟用寫入。</span><span class="sxs-lookup"><span data-stu-id="1a640-124">Initially, all bits are enabled for writing.</span></span>

<span data-ttu-id="1a640-125">下列函式會取出與 **glStencilMask** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="1a640-125">The following functions retrieve information related to **glStencilMask**:</span></span>

<span data-ttu-id="1a640-126">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 樣板 \_ WRITEMASK 的 glGet</span><span class="sxs-lookup"><span data-stu-id="1a640-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_WRITEMASK</span></span>

<span data-ttu-id="1a640-127">具有引數 GL 樣板位的 glGet \_ \_</span><span class="sxs-lookup"><span data-stu-id="1a640-127">glGet with argument GL\_STENCIL\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="1a640-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a640-128">Requirements</span></span>



| <span data-ttu-id="1a640-129">需求</span><span class="sxs-lookup"><span data-stu-id="1a640-129">Requirement</span></span> | <span data-ttu-id="1a640-130">值</span><span class="sxs-lookup"><span data-stu-id="1a640-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a640-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a640-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1a640-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a640-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1a640-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a640-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1a640-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a640-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1a640-135">標頭</span><span class="sxs-lookup"><span data-stu-id="1a640-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a640-136"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="1a640-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1a640-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="1a640-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a640-138"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a640-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1a640-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1a640-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a640-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a640-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a640-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a640-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a640-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1a640-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1a640-143">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="1a640-143">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="1a640-144">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="1a640-144">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="1a640-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1a640-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1a640-146">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="1a640-146">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="1a640-147">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="1a640-147">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> <dt>

[<span data-ttu-id="1a640-148">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="1a640-148">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





