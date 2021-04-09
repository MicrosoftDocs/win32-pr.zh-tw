---
title: 'glNormal3d 函式 (Gl) '
description: '設定目前的一般向量。 |glNormal3d 函式 (Gl) '
ms.assetid: d256aef0-3ad5-4e70-b1c8-6402434b1e67
keywords:
- glNormal3d 函式 OpenGL
topic_type:
- apiref
api_name:
- glNormal3d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6ab158e298ff20cce635ab4002f38ca82fdaa2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035309"
---
# <a name="glnormal3d-function"></a><span data-ttu-id="02058-105">glNormal3d 函式</span><span class="sxs-lookup"><span data-stu-id="02058-105">glNormal3d function</span></span>

<span data-ttu-id="02058-106">設定目前的一般向量。</span><span class="sxs-lookup"><span data-stu-id="02058-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="02058-107">語法</span><span class="sxs-lookup"><span data-stu-id="02058-107">Syntax</span></span>


```C++
void WINAPI glNormal3d(
   GLdouble nx,
   GLdouble ny,
   GLdouble nz
);
```



## <a name="parameters"></a><span data-ttu-id="02058-108">參數</span><span class="sxs-lookup"><span data-stu-id="02058-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02058-109">*Nx*</span><span class="sxs-lookup"><span data-stu-id="02058-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="02058-110">指定新目前標準向量的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="02058-110">Specifies the x-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="02058-111">*紐約*</span><span class="sxs-lookup"><span data-stu-id="02058-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="02058-112">指定新目前標準向量的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="02058-112">Specifies the y-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="02058-113">*紐西蘭*</span><span class="sxs-lookup"><span data-stu-id="02058-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="02058-114">指定新目前標準向量的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="02058-114">Specifies the z-coordinate for the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02058-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="02058-115">Return value</span></span>

<span data-ttu-id="02058-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="02058-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02058-117">備註</span><span class="sxs-lookup"><span data-stu-id="02058-117">Remarks</span></span>

<span data-ttu-id="02058-118">當您呼叫 **glNormal3d** 函式時，目前的一般會設定為指定的座標。</span><span class="sxs-lookup"><span data-stu-id="02058-118">The current normal is set to the given coordinates whenever you call the **glNormal3d** function.</span></span>

<span data-ttu-id="02058-119">Byte、short 或 integer 引數會使用將最正面可表示的整數值對應至1.0 的線性對應，以及最大的負向-1.0 的可表示整數值，轉換為浮點格式。</span><span class="sxs-lookup"><span data-stu-id="02058-119">Byte, short, or integer arguments are converted to floating-point format by using a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="02058-120">使用 **glNormal3d** 指定的法線不需要單位長度。</span><span class="sxs-lookup"><span data-stu-id="02058-120">Normals specified by using **glNormal3d** need not have unit length.</span></span> <span data-ttu-id="02058-121">如果啟用正規化，則在轉換之後會正規化以 **glNormal3d** 指定的法線。</span><span class="sxs-lookup"><span data-stu-id="02058-121">If normalization is enabled, then normals specified with **glNormal3d** are normalized after transformation.</span></span> <span data-ttu-id="02058-122">您可以使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 搭配引數 GL 標準化來控制正規化 \_ 。</span><span class="sxs-lookup"><span data-stu-id="02058-122">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="02058-123">預設會停用正規化。</span><span class="sxs-lookup"><span data-stu-id="02058-123">By default, normalization is disabled.</span></span> <span data-ttu-id="02058-124">您可以隨時更新目前的正常情況。</span><span class="sxs-lookup"><span data-stu-id="02058-124">You can update the current normal at any time.</span></span> <span data-ttu-id="02058-125">尤其是，您可以呼叫 [**glBegin**](glbegin.md)的呼叫與 [**glEnd**](glend.md)的對應呼叫之間的 **glNormal3d**。</span><span class="sxs-lookup"><span data-stu-id="02058-125">In particular, you can call **glNormal3d** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="02058-126">下列函式會取出與 **glNormal3d** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="02058-126">The following functions retrieve information related to **glNormal3d**:</span></span>

<span data-ttu-id="02058-127">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 標準的 glGet</span><span class="sxs-lookup"><span data-stu-id="02058-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="02058-128">具有引數 GL 正規化的 [**glIsEnable**](glisenabled.md) \_</span><span class="sxs-lookup"><span data-stu-id="02058-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="02058-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="02058-129">Requirements</span></span>



| <span data-ttu-id="02058-130">需求</span><span class="sxs-lookup"><span data-stu-id="02058-130">Requirement</span></span> | <span data-ttu-id="02058-131">值</span><span class="sxs-lookup"><span data-stu-id="02058-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02058-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02058-132">Minimum supported client</span></span><br/> | <span data-ttu-id="02058-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02058-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="02058-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02058-134">Minimum supported server</span></span><br/> | <span data-ttu-id="02058-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02058-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02058-136">標頭</span><span class="sxs-lookup"><span data-stu-id="02058-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="02058-137"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="02058-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="02058-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="02058-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="02058-139"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="02058-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="02058-140">DLL</span><span class="sxs-lookup"><span data-stu-id="02058-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02058-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02058-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02058-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02058-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02058-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="02058-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="02058-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="02058-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="02058-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="02058-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="02058-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="02058-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="02058-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="02058-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="02058-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="02058-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





