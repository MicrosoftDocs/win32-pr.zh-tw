---
title: 'glNormal3bv 函式 (Gl) '
description: '設定目前的一般向量。 |glNormal3bv 函式 (Gl) '
ms.assetid: 1d9be974-93c9-45ac-89f1-92c14ff1c242
keywords:
- glNormal3bv 函式 OpenGL
topic_type:
- apiref
api_name:
- glNormal3bv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d758c1768425ecb736096d59a49133ff4c8918c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986479"
---
# <a name="glnormal3bv-function"></a><span data-ttu-id="0e713-105">glNormal3bv 函式</span><span class="sxs-lookup"><span data-stu-id="0e713-105">glNormal3bv function</span></span>

<span data-ttu-id="0e713-106">設定目前的一般向量。</span><span class="sxs-lookup"><span data-stu-id="0e713-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e713-107">語法</span><span class="sxs-lookup"><span data-stu-id="0e713-107">Syntax</span></span>


```C++
void WINAPI glNormal3bv(
   const GLbyte *v
);
```



## <a name="parameters"></a><span data-ttu-id="0e713-108">參數</span><span class="sxs-lookup"><span data-stu-id="0e713-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e713-109">*V*</span><span class="sxs-lookup"><span data-stu-id="0e713-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="0e713-110">三個元素的陣列指標：新的目前一般標準的 x、y 和 z 座標。</span><span class="sxs-lookup"><span data-stu-id="0e713-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e713-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e713-111">Return value</span></span>

<span data-ttu-id="0e713-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0e713-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e713-113">備註</span><span class="sxs-lookup"><span data-stu-id="0e713-113">Remarks</span></span>

<span data-ttu-id="0e713-114">當您呼叫 **glNormal3bv** 函式時，目前的一般會設定為指定的座標。</span><span class="sxs-lookup"><span data-stu-id="0e713-114">The current normal is set to the given coordinates whenever you call the **glNormal3bv** function.</span></span>

<span data-ttu-id="0e713-115">Byte、short 或 integer 引數會使用將最正面可表示的整數值對應至1.0 的線性對應，以及最大的負向-1.0 的可表示整數值，轉換為浮點格式。</span><span class="sxs-lookup"><span data-stu-id="0e713-115">Byte, short, or integer arguments are converted to floating-point format by using a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="0e713-116">使用 **glNormal3bv** 指定的法線不需要單位長度。</span><span class="sxs-lookup"><span data-stu-id="0e713-116">Normals specified by using **glNormal3bv** need not have unit length.</span></span> <span data-ttu-id="0e713-117">如果啟用正規化，則在轉換之後，會將使用 **glNormal3bv** 所指定的法線正規化。</span><span class="sxs-lookup"><span data-stu-id="0e713-117">If normalization is enabled, then normals specified by using **glNormal3bv** are normalized after transformation.</span></span> <span data-ttu-id="0e713-118">您可以使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 搭配引數 GL 標準化來控制正規化 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0e713-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="0e713-119">預設會停用正規化。</span><span class="sxs-lookup"><span data-stu-id="0e713-119">By default, normalization is disabled.</span></span> <span data-ttu-id="0e713-120">您可以隨時更新目前的正常情況。</span><span class="sxs-lookup"><span data-stu-id="0e713-120">You can update the current normal any time.</span></span> <span data-ttu-id="0e713-121">尤其是，您可以呼叫 [**glBegin**](glbegin.md)的呼叫與 [**glEnd**](glend.md)的對應呼叫之間的 **glNormal3bv**。</span><span class="sxs-lookup"><span data-stu-id="0e713-121">In particular, you can call **glNormal3bv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="0e713-122">下列函式會取出與 **glNormal3bv** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="0e713-122">The following functions retrieve information related to **glNormal3bv**:</span></span>

<span data-ttu-id="0e713-123">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 標準的 glGet</span><span class="sxs-lookup"><span data-stu-id="0e713-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="0e713-124">具有引數 GL 正規化的 [**glIsEnable**](glisenabled.md) \_</span><span class="sxs-lookup"><span data-stu-id="0e713-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="0e713-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e713-125">Requirements</span></span>



| <span data-ttu-id="0e713-126">需求</span><span class="sxs-lookup"><span data-stu-id="0e713-126">Requirement</span></span> | <span data-ttu-id="0e713-127">值</span><span class="sxs-lookup"><span data-stu-id="0e713-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e713-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e713-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0e713-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e713-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0e713-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e713-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0e713-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e713-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e713-132">標頭</span><span class="sxs-lookup"><span data-stu-id="0e713-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e713-133"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="0e713-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0e713-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="0e713-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e713-135"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e713-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0e713-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0e713-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e713-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e713-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e713-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e713-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e713-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0e713-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0e713-140">**glColor**</span><span class="sxs-lookup"><span data-stu-id="0e713-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="0e713-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0e713-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0e713-142">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="0e713-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="0e713-143">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="0e713-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="0e713-144">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="0e713-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





