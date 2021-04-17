---
title: 'gluProject 函式 (X.glu 隊) '
description: GluProject 函式會將物件座標組應至視窗座標。
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- gluProject 函式 OpenGL
topic_type:
- apiref
api_name:
- gluProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84972d95d381a630bf6caf7f0099ce740a4f2741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466180"
---
# <a name="gluproject-function"></a><span data-ttu-id="4c21a-104">gluProject 函式</span><span class="sxs-lookup"><span data-stu-id="4c21a-104">gluProject function</span></span>

<span data-ttu-id="4c21a-105">**GluProject** 函式會將物件座標組應至視窗座標。</span><span class="sxs-lookup"><span data-stu-id="4c21a-105">The **gluProject** function maps object coordinates to window coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c21a-106">語法</span><span class="sxs-lookup"><span data-stu-id="4c21a-106">Syntax</span></span>


```C++
int WINAPI gluProject(
         GLdouble objx,
         GLdouble objy,
         GLdouble objz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *winx,
         GLdouble *winy,
         GLdouble *winz
);
```



## <a name="parameters"></a><span data-ttu-id="4c21a-107">參數</span><span class="sxs-lookup"><span data-stu-id="4c21a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c21a-108">*objx*</span><span class="sxs-lookup"><span data-stu-id="4c21a-108">*objx*</span></span> 
</dt> <dd>

<span data-ttu-id="4c21a-109">X 物件座標。</span><span class="sxs-lookup"><span data-stu-id="4c21a-109">The x object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="4c21a-110">*objy*</span><span class="sxs-lookup"><span data-stu-id="4c21a-110">*objy*</span></span> 
</dt> <dd>

<span data-ttu-id="4c21a-111">Y 物件座標。</span><span class="sxs-lookup"><span data-stu-id="4c21a-111">The y object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="4c21a-112">*objz*</span><span class="sxs-lookup"><span data-stu-id="4c21a-112">*objz*</span></span> 
</dt> <dd>

<span data-ttu-id="4c21a-113">Z 物件座標。</span><span class="sxs-lookup"><span data-stu-id="4c21a-113">The z object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="4c21a-114">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="4c21a-114">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="4c21a-115">目前的模型矩陣 (為 [**glGetDoublev**](glgetdoublev.md) 呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="4c21a-115">The current modelview matrix (as from a [**glGetDoublev**](glgetdoublev.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="4c21a-116">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="4c21a-116">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="4c21a-117">目前的投射矩陣 (從 **glGetDoublev** 呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="4c21a-117">The current projection matrix (as from a **glGetDoublev** call).</span></span>

</dd> <dt>

<span data-ttu-id="4c21a-118">*視窗*</span><span class="sxs-lookup"><span data-stu-id="4c21a-118">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="4c21a-119">目前的視口 (為來自 [**glGetIntegerv**](glgetintegerv.md) 呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="4c21a-119">The current viewport (as from a [**glGetIntegerv**](glgetintegerv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="4c21a-120">*winx*</span><span class="sxs-lookup"><span data-stu-id="4c21a-120">*winx*</span></span> 
</dt> <dd>

<span data-ttu-id="4c21a-121">計算的 x 視窗座標。</span><span class="sxs-lookup"><span data-stu-id="4c21a-121">The computed x window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="4c21a-122">*winy*</span><span class="sxs-lookup"><span data-stu-id="4c21a-122">*winy*</span></span> 
</dt> <dd>

<span data-ttu-id="4c21a-123">計算的 y 視窗座標。</span><span class="sxs-lookup"><span data-stu-id="4c21a-123">The computed y window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="4c21a-124">*winz*</span><span class="sxs-lookup"><span data-stu-id="4c21a-124">*winz*</span></span> 
</dt> <dd>

<span data-ttu-id="4c21a-125">計算的 z 視窗座標。</span><span class="sxs-lookup"><span data-stu-id="4c21a-125">The computed z window coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c21a-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c21a-126">Return value</span></span>

<span data-ttu-id="4c21a-127">如果函式成功，則傳回值為 GL \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="4c21a-127">If the function succeeds, the return value is GL\_TRUE.</span></span>

<span data-ttu-id="4c21a-128">如果函式失敗，則傳回值為 GL \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="4c21a-128">If the function fails, the return value is GL\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c21a-129">備註</span><span class="sxs-lookup"><span data-stu-id="4c21a-129">Remarks</span></span>

<span data-ttu-id="4c21a-130">**GluProject** 函式會使用 *modelMatrix*、 *projMatrix* 和 *視口*，將指定的物件座標轉換成視窗座標。</span><span class="sxs-lookup"><span data-stu-id="4c21a-130">The **gluProject** function transforms the specified object coordinates into window coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="4c21a-131">結果會儲存在 *winx*、 *winy* 和 *winz* 中。</span><span class="sxs-lookup"><span data-stu-id="4c21a-131">The result is stored in *winx*, *winy*, and *winz*.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c21a-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c21a-132">Requirements</span></span>



| <span data-ttu-id="4c21a-133">需求</span><span class="sxs-lookup"><span data-stu-id="4c21a-133">Requirement</span></span> | <span data-ttu-id="4c21a-134">值</span><span class="sxs-lookup"><span data-stu-id="4c21a-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4c21a-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c21a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4c21a-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c21a-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4c21a-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c21a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4c21a-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c21a-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4c21a-139">標頭</span><span class="sxs-lookup"><span data-stu-id="4c21a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c21a-140"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c21a-140"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="4c21a-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="4c21a-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c21a-142"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c21a-142"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4c21a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4c21a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c21a-144"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c21a-144"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c21a-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c21a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c21a-146">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="4c21a-146">**glGetDoublev**</span></span>](glgetdoublev.md)
</dt> <dt>

[<span data-ttu-id="4c21a-147">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="4c21a-147">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="4c21a-148">**gluUnProject**</span><span class="sxs-lookup"><span data-stu-id="4c21a-148">**gluUnProject**</span></span>](gluunproject.md)
</dt> </dl>

 

 





