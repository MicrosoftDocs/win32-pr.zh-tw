---
title: 'glColorMask 函式 (Gl) '
description: GlColorMask 函式會啟用和停用框架緩衝區色彩元件的寫入功能。
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- glColorMask 函式 OpenGL
topic_type:
- apiref
api_name:
- glColorMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9aa36eeceeae4aaa9373d73b50fda09663edb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843276"
---
# <a name="glcolormask-function"></a><span data-ttu-id="35f96-104">glColorMask 函式</span><span class="sxs-lookup"><span data-stu-id="35f96-104">glColorMask function</span></span>

<span data-ttu-id="35f96-105">**GlColorMask** 函式會啟用和停用框架緩衝區色彩元件的寫入功能。</span><span class="sxs-lookup"><span data-stu-id="35f96-105">The **glColorMask** function enables and disables writing of frame-buffer color components.</span></span>

## <a name="syntax"></a><span data-ttu-id="35f96-106">語法</span><span class="sxs-lookup"><span data-stu-id="35f96-106">Syntax</span></span>


```C++
void WINAPI glColorMask(
   GLboolean red,
   GLboolean green,
   GLboolean blue,
   GLboolean alpha
);
```



## <a name="parameters"></a><span data-ttu-id="35f96-107">參數</span><span class="sxs-lookup"><span data-stu-id="35f96-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35f96-108">*紅*</span><span class="sxs-lookup"><span data-stu-id="35f96-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="35f96-109">指定紅色是否可寫入至畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="35f96-109">Specify whether red can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="35f96-110">預設值為 GL \_ TRUE，表示可以寫入色彩元件。</span><span class="sxs-lookup"><span data-stu-id="35f96-110">The default values is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="35f96-111">*綠色*</span><span class="sxs-lookup"><span data-stu-id="35f96-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="35f96-112">指定綠色是否可以或無法寫入至畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="35f96-112">Specify whether green can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="35f96-113">預設值為 GL \_ TRUE，表示可以寫入色彩元件。</span><span class="sxs-lookup"><span data-stu-id="35f96-113">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="35f96-114">*藍色*</span><span class="sxs-lookup"><span data-stu-id="35f96-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="35f96-115">指定 blue 是否可以或無法寫入至畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="35f96-115">Specify whether blue can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="35f96-116">預設值為 GL \_ TRUE，表示可以寫入色彩元件。</span><span class="sxs-lookup"><span data-stu-id="35f96-116">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="35f96-117">*阿 爾 法*</span><span class="sxs-lookup"><span data-stu-id="35f96-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="35f96-118">指定是否可以或不能將 Alpha 寫入至畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="35f96-118">Specify whether alpha can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="35f96-119">預設值為 GL \_ TRUE，表示可以寫入色彩元件。</span><span class="sxs-lookup"><span data-stu-id="35f96-119">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35f96-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="35f96-120">Return value</span></span>

<span data-ttu-id="35f96-121">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="35f96-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="35f96-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="35f96-122">Error codes</span></span>

<span data-ttu-id="35f96-123">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="35f96-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="35f96-124">Name</span><span class="sxs-lookup"><span data-stu-id="35f96-124">Name</span></span>                                                                                                  | <span data-ttu-id="35f96-125">意義</span><span class="sxs-lookup"><span data-stu-id="35f96-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35f96-126"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="35f96-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="35f96-127">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="35f96-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="35f96-128">備註</span><span class="sxs-lookup"><span data-stu-id="35f96-128">Remarks</span></span>

<span data-ttu-id="35f96-129">**GlColorMask** 函式會指定畫面格緩衝區中的個別色彩元件是否可以或無法寫入。</span><span class="sxs-lookup"><span data-stu-id="35f96-129">The **glColorMask** function specifies whether the individual color components in the framebuffer can or cannot be written.</span></span> <span data-ttu-id="35f96-130">如果 *red* 為 GL \_ FALSE，則不會對任何色彩緩衝區中任何圖元的紅色元件進行任何變更，不論嘗試進行的繪圖操作為何。</span><span class="sxs-lookup"><span data-stu-id="35f96-130">If *red* is GL\_FALSE, for example, no change is made to the red component of any pixel in any of the color buffers, regardless of the drawing operation attempted.</span></span>

<span data-ttu-id="35f96-131">無法控制個別元件元件的變更。</span><span class="sxs-lookup"><span data-stu-id="35f96-131">Changes to individual bits of components cannot be controlled.</span></span> <span data-ttu-id="35f96-132">相反地，會針對整個色彩元件啟用或停用變更。</span><span class="sxs-lookup"><span data-stu-id="35f96-132">Rather, changes are either enabled or disabled for entire color components.</span></span>

<span data-ttu-id="35f96-133">下列函式會取出與 **glColorMask** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="35f96-133">The following functions retrieve information related to **glColorMask**:</span></span>

<span data-ttu-id="35f96-134">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 色彩 \_ WRITEMASK 的 glGet</span><span class="sxs-lookup"><span data-stu-id="35f96-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_WRITEMASK</span></span>

<span data-ttu-id="35f96-135">具有引數 GL \_ RGBA \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="35f96-135">**glGet** with argument GL\_RGBA\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="35f96-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="35f96-136">Requirements</span></span>



| <span data-ttu-id="35f96-137">需求</span><span class="sxs-lookup"><span data-stu-id="35f96-137">Requirement</span></span> | <span data-ttu-id="35f96-138">值</span><span class="sxs-lookup"><span data-stu-id="35f96-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35f96-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35f96-139">Minimum supported client</span></span><br/> | <span data-ttu-id="35f96-140">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35f96-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="35f96-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35f96-141">Minimum supported server</span></span><br/> | <span data-ttu-id="35f96-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35f96-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35f96-143">標頭</span><span class="sxs-lookup"><span data-stu-id="35f96-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="35f96-144"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="35f96-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="35f96-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="35f96-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="35f96-146"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="35f96-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="35f96-147">DLL</span><span class="sxs-lookup"><span data-stu-id="35f96-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35f96-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35f96-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35f96-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35f96-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35f96-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="35f96-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="35f96-151">**glColor**</span><span class="sxs-lookup"><span data-stu-id="35f96-151">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="35f96-152">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="35f96-152">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="35f96-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="35f96-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="35f96-154">**glGet**</span><span class="sxs-lookup"><span data-stu-id="35f96-154">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="35f96-155">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="35f96-155">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="35f96-156">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="35f96-156">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="35f96-157">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="35f96-157">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





