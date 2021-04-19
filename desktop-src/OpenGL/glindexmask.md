---
title: 'glIndexMask 函式 (Gl) '
description: GlIndexMask 函式會控制如何在色彩索引緩衝區中寫入個別位。
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- glIndexMask 函式 OpenGL
topic_type:
- apiref
api_name:
- glIndexMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d426cb1f4bb2e794bef53853d0336db1d64b263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966911"
---
# <a name="glindexmask-function"></a><span data-ttu-id="e85ac-104">glIndexMask 函式</span><span class="sxs-lookup"><span data-stu-id="e85ac-104">glIndexMask function</span></span>

<span data-ttu-id="e85ac-105">**GlIndexMask** 函式會控制如何在色彩索引緩衝區中寫入個別位。</span><span class="sxs-lookup"><span data-stu-id="e85ac-105">The **glIndexMask** function controls the writing of individual bits in the color-index buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e85ac-106">語法</span><span class="sxs-lookup"><span data-stu-id="e85ac-106">Syntax</span></span>


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="e85ac-107">參數</span><span class="sxs-lookup"><span data-stu-id="e85ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e85ac-108">*面具*</span><span class="sxs-lookup"><span data-stu-id="e85ac-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="e85ac-109">用來啟用和停用在色彩索引緩衝區中寫入個別位的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="e85ac-109">A bit mask to enable and disable the writing of individual bits in the color-index buffers.</span></span> <span data-ttu-id="e85ac-110">一開始，遮罩就是所有的遮罩。</span><span class="sxs-lookup"><span data-stu-id="e85ac-110">Initially, the mask is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e85ac-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e85ac-111">Return value</span></span>

<span data-ttu-id="e85ac-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e85ac-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e85ac-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e85ac-113">Error codes</span></span>

<span data-ttu-id="e85ac-114">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e85ac-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e85ac-115">Name</span><span class="sxs-lookup"><span data-stu-id="e85ac-115">Name</span></span>                                                                                                  | <span data-ttu-id="e85ac-116">意義</span><span class="sxs-lookup"><span data-stu-id="e85ac-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e85ac-117"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="e85ac-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e85ac-118">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="e85ac-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e85ac-119">備註</span><span class="sxs-lookup"><span data-stu-id="e85ac-119">Remarks</span></span>

<span data-ttu-id="e85ac-120">**GlIndexMask** 函式會控制如何在色彩索引緩衝區中寫入個別位。</span><span class="sxs-lookup"><span data-stu-id="e85ac-120">The **glIndexMask** function controls the writing of individual bits in the color-index buffers.</span></span> <span data-ttu-id="e85ac-121">最小的 *n* 位 *遮罩*，其中 *1* 是色彩索引緩衝區中的位數，指定遮罩。</span><span class="sxs-lookup"><span data-stu-id="e85ac-121">The least significant *n* bits of *mask*, where *1* is the number of bits in a color-index buffer, specify a mask.</span></span> <span data-ttu-id="e85ac-122">當遮罩中出現一個時，會將色彩索引緩衝區 (或) 緩衝區中的對應位設為可寫入。</span><span class="sxs-lookup"><span data-stu-id="e85ac-122">Wherever a one appears in the mask, the corresponding bit in the color-index buffer (or buffers) is made writable.</span></span> <span data-ttu-id="e85ac-123">如果出現零，則位為寫入保護。</span><span class="sxs-lookup"><span data-stu-id="e85ac-123">Where a zero appears, the bit is write-protected.</span></span>

<span data-ttu-id="e85ac-124">這個遮罩只會在色彩索引模式中使用，它只會影響目前為寫入所選取的緩衝區 (請參閱 [**glDrawBuffer**](gldrawbuffer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="e85ac-124">This mask is used only in color-index mode, and it affects only the buffers currently selected for writing (see [**glDrawBuffer**](gldrawbuffer.md)).</span></span> <span data-ttu-id="e85ac-125">一開始，所有位都會啟用寫入。</span><span class="sxs-lookup"><span data-stu-id="e85ac-125">Initially, all bits are enabled for writing.</span></span>

<span data-ttu-id="e85ac-126">下列函式會抓取 **glIndexMask** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="e85ac-126">The following function retrieves information related to **glIndexMask**:</span></span>

<span data-ttu-id="e85ac-127">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 索引 \_ WRITEMASK 的 glGet</span><span class="sxs-lookup"><span data-stu-id="e85ac-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_WRITEMASK</span></span>

## <a name="requirements"></a><span data-ttu-id="e85ac-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="e85ac-128">Requirements</span></span>



| <span data-ttu-id="e85ac-129">需求</span><span class="sxs-lookup"><span data-stu-id="e85ac-129">Requirement</span></span> | <span data-ttu-id="e85ac-130">值</span><span class="sxs-lookup"><span data-stu-id="e85ac-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e85ac-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e85ac-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e85ac-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e85ac-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e85ac-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e85ac-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e85ac-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e85ac-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e85ac-135">標頭</span><span class="sxs-lookup"><span data-stu-id="e85ac-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e85ac-136"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="e85ac-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e85ac-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="e85ac-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="e85ac-138"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e85ac-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e85ac-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e85ac-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e85ac-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e85ac-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e85ac-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e85ac-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e85ac-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e85ac-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e85ac-143">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="e85ac-143">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="e85ac-144">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="e85ac-144">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="e85ac-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e85ac-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e85ac-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="e85ac-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="e85ac-147">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="e85ac-147">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





