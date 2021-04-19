---
title: 'gluUnProject 函式 (X.glu 隊) '
description: GluUnProject 函式會將視窗座標組應到物件座標。
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
keywords:
- gluUnProject 函式 OpenGL
topic_type:
- apiref
api_name:
- gluUnProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45311171dd3d71c9e699953c049e0813f2df361
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969621"
---
# <a name="gluunproject-function"></a><span data-ttu-id="4d8b1-104">gluUnProject 函式</span><span class="sxs-lookup"><span data-stu-id="4d8b1-104">gluUnProject function</span></span>

<span data-ttu-id="4d8b1-105">**GluUnProject** 函式會將視窗座標組應到物件座標。</span><span class="sxs-lookup"><span data-stu-id="4d8b1-105">The **gluUnProject** function maps window coordinates to object coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d8b1-106">語法</span><span class="sxs-lookup"><span data-stu-id="4d8b1-106">Syntax</span></span>


```C++
int WINAPI gluUnProject(
         GLdouble winx,
         GLdouble winy,
         GLdouble winz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *objx,
         GLdouble *objy,
         GLdouble *objz
);
```



## <a name="parameters"></a><span data-ttu-id="4d8b1-107">參數</span><span class="sxs-lookup"><span data-stu-id="4d8b1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d8b1-108">*winx*</span><span class="sxs-lookup"><span data-stu-id="4d8b1-108">*winx*</span></span> 
</dt> <dd>

<span data-ttu-id="4d8b1-109">要對應的 x 視窗座標。</span><span class="sxs-lookup"><span data-stu-id="4d8b1-109">The x window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="4d8b1-110">*winy*</span><span class="sxs-lookup"><span data-stu-id="4d8b1-110">*winy*</span></span> 
</dt> <dd>

<span data-ttu-id="4d8b1-111">要對應的 y 視窗座標。</span><span class="sxs-lookup"><span data-stu-id="4d8b1-111">The y window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="4d8b1-112">*winz*</span><span class="sxs-lookup"><span data-stu-id="4d8b1-112">*winz*</span></span> 
</dt> <dd>

<span data-ttu-id="4d8b1-113">要對應的 z 視窗座標。</span><span class="sxs-lookup"><span data-stu-id="4d8b1-113">The z window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="4d8b1-114">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="4d8b1-114">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="4d8b1-115">模型矩陣 (為 [**glGetDoublev**](glgetdoublev.md) 呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="4d8b1-115">The modelview matrix (as from a [**glGetDoublev**](glgetdoublev.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="4d8b1-116">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="4d8b1-116">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="4d8b1-117">投射矩陣 (從 **glGetDoublev** 呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="4d8b1-117">The projection matrix (as from a **glGetDoublev** call).</span></span>

</dd> <dt>

<span data-ttu-id="4d8b1-118">*視窗*</span><span class="sxs-lookup"><span data-stu-id="4d8b1-118">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="4d8b1-119">從 [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 呼叫)  (的區。</span><span class="sxs-lookup"><span data-stu-id="4d8b1-119">The viewport (as from a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="4d8b1-120">*objx*</span><span class="sxs-lookup"><span data-stu-id="4d8b1-120">*objx*</span></span> 
</dt> <dd>

<span data-ttu-id="4d8b1-121">計算的 x 物件座標。</span><span class="sxs-lookup"><span data-stu-id="4d8b1-121">The computed x object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="4d8b1-122">*objy*</span><span class="sxs-lookup"><span data-stu-id="4d8b1-122">*objy*</span></span> 
</dt> <dd>

<span data-ttu-id="4d8b1-123">計算的 y 物件座標。</span><span class="sxs-lookup"><span data-stu-id="4d8b1-123">The computed y object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="4d8b1-124">*objz*</span><span class="sxs-lookup"><span data-stu-id="4d8b1-124">*objz*</span></span> 
</dt> <dd>

<span data-ttu-id="4d8b1-125">計算的 z 物件座標。</span><span class="sxs-lookup"><span data-stu-id="4d8b1-125">The computed z object coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d8b1-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d8b1-126">Return value</span></span>

<span data-ttu-id="4d8b1-127">如果函式成功，則傳回值為 GL \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="4d8b1-127">If the function succeeds, the return value is GL\_TRUE.</span></span>

<span data-ttu-id="4d8b1-128">如果函式失敗，則傳回值為 GL \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="4d8b1-128">If the function fails, the return value is GL\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d8b1-129">備註</span><span class="sxs-lookup"><span data-stu-id="4d8b1-129">Remarks</span></span>

<span data-ttu-id="4d8b1-130">**GluUnProject** 函式會使用 *modelMatrix*、 *projMatrix* 和 *視窗* 圖將指定的視窗座標組應到物件座標。</span><span class="sxs-lookup"><span data-stu-id="4d8b1-130">The **gluUnProject** function maps the specified window coordinates into object coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="4d8b1-131">結果會儲存在 *objx*、 *objy* 和 *objz* 中。</span><span class="sxs-lookup"><span data-stu-id="4d8b1-131">The result is stored in *objx*, *objy*, and *objz*.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d8b1-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d8b1-132">Requirements</span></span>



| <span data-ttu-id="4d8b1-133">需求</span><span class="sxs-lookup"><span data-stu-id="4d8b1-133">Requirement</span></span> | <span data-ttu-id="4d8b1-134">值</span><span class="sxs-lookup"><span data-stu-id="4d8b1-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4d8b1-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d8b1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4d8b1-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d8b1-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4d8b1-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d8b1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4d8b1-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d8b1-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4d8b1-139">標頭</span><span class="sxs-lookup"><span data-stu-id="4d8b1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d8b1-140"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="4d8b1-140"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="4d8b1-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="4d8b1-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d8b1-142"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d8b1-142"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4d8b1-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4d8b1-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d8b1-144"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d8b1-144"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d8b1-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d8b1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d8b1-146">**glGet**</span><span class="sxs-lookup"><span data-stu-id="4d8b1-146">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="4d8b1-147">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="4d8b1-147">**glGetDoublev**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="4d8b1-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="4d8b1-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="4d8b1-149">**gluProject**</span><span class="sxs-lookup"><span data-stu-id="4d8b1-149">**gluProject**</span></span>](gluproject.md)
</dt> </dl>

 

 





