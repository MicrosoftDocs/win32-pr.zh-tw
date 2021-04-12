---
title: 'glNormal3b 函式 (Gl) '
description: '設定目前的一般向量。 |glNormal3b 函式 (Gl) '
ms.assetid: b6976143-bc9a-4766-9f7e-5380c3a24173
keywords:
- glNormal3b 函式 OpenGL
topic_type:
- apiref
api_name:
- glNormal3b
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a09a92b718881670ed5625fd5aa94a23193cdd6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853592"
---
# <a name="glnormal3b-function"></a><span data-ttu-id="ce680-105">glNormal3b 函式</span><span class="sxs-lookup"><span data-stu-id="ce680-105">glNormal3b function</span></span>

<span data-ttu-id="ce680-106">設定目前的一般向量。</span><span class="sxs-lookup"><span data-stu-id="ce680-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce680-107">語法</span><span class="sxs-lookup"><span data-stu-id="ce680-107">Syntax</span></span>


```C++
void WINAPI glNormal3b(
   GLbyte nx,
   GLbyte ny,
   GLbyte nz
);
```



## <a name="parameters"></a><span data-ttu-id="ce680-108">參數</span><span class="sxs-lookup"><span data-stu-id="ce680-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce680-109">*Nx*</span><span class="sxs-lookup"><span data-stu-id="ce680-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="ce680-110">指定新目前標準向量的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="ce680-110">Specifies the x-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="ce680-111">*紐約*</span><span class="sxs-lookup"><span data-stu-id="ce680-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="ce680-112">指定新目前標準向量的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="ce680-112">Specifies the y-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="ce680-113">*紐西蘭*</span><span class="sxs-lookup"><span data-stu-id="ce680-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="ce680-114">指定新目前標準向量的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="ce680-114">Specifies the z-coordinate for the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce680-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce680-115">Return value</span></span>

<span data-ttu-id="ce680-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ce680-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce680-117">備註</span><span class="sxs-lookup"><span data-stu-id="ce680-117">Remarks</span></span>

<span data-ttu-id="ce680-118">當您呼叫 **glNormal3b** 函式時，目前的一般會設定為指定的座標。</span><span class="sxs-lookup"><span data-stu-id="ce680-118">The current normal is set to the given coordinates whenever you call the **glNormal3b** function.</span></span>

<span data-ttu-id="ce680-119">Byte、short 或 integer 引數會使用將最正面可表示的整數值對應至1.0 的線性對應，以及最大的負向-1.0 的可表示整數值，轉換為浮點格式。</span><span class="sxs-lookup"><span data-stu-id="ce680-119">Byte, short, or integer arguments are converted to floating-point format by using a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="ce680-120">使用 **glNormal3b** 指定的法線不需要單位長度。</span><span class="sxs-lookup"><span data-stu-id="ce680-120">Normals specified with **glNormal3b** need not have unit length.</span></span> <span data-ttu-id="ce680-121">如果啟用正規化，則在轉換之後會正規化以 **glNormal3b** 指定的法線。</span><span class="sxs-lookup"><span data-stu-id="ce680-121">If normalization is enabled, then normals specified with **glNormal3b** are normalized after transformation.</span></span> <span data-ttu-id="ce680-122">您可以使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 搭配引數 GL 標準化來控制正規化 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ce680-122">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="ce680-123">預設會停用正規化。</span><span class="sxs-lookup"><span data-stu-id="ce680-123">By default, normalization is disabled.</span></span> <span data-ttu-id="ce680-124">您可以隨時更新目前的正常情況。</span><span class="sxs-lookup"><span data-stu-id="ce680-124">You can update the current normal at any time.</span></span> <span data-ttu-id="ce680-125">尤其是，您可以呼叫 [**glBegin**](glbegin.md)的呼叫與 [**glEnd**](glend.md)的對應呼叫之間的 **glNormal3b**。</span><span class="sxs-lookup"><span data-stu-id="ce680-125">In particular, you can call **glNormal3b** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="ce680-126">下列函式會取出與 **glNormal3b** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="ce680-126">The following functions retrieve information related to **glNormal3b**:</span></span>

<span data-ttu-id="ce680-127">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 標準的 glGet</span><span class="sxs-lookup"><span data-stu-id="ce680-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="ce680-128">具有引數 GL 正規化的 [**glIsEnable**](glisenabled.md) \_</span><span class="sxs-lookup"><span data-stu-id="ce680-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="ce680-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce680-129">Requirements</span></span>



| <span data-ttu-id="ce680-130">需求</span><span class="sxs-lookup"><span data-stu-id="ce680-130">Requirement</span></span> | <span data-ttu-id="ce680-131">值</span><span class="sxs-lookup"><span data-stu-id="ce680-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce680-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce680-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ce680-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce680-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ce680-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce680-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ce680-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce680-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce680-136">標頭</span><span class="sxs-lookup"><span data-stu-id="ce680-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce680-137"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="ce680-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ce680-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="ce680-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce680-139"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce680-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ce680-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ce680-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce680-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce680-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce680-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce680-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce680-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ce680-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ce680-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="ce680-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="ce680-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ce680-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ce680-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="ce680-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="ce680-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="ce680-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="ce680-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="ce680-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





