---
title: 'glVertex4f 函式 (Gl) '
description: '指定頂點。 |glVertex4f 函式 (Gl) '
ms.assetid: 877fce8c-095e-4ae4-8633-7c84659ee8a6
keywords:
- glVertex4f 函式 OpenGL
topic_type:
- apiref
api_name:
- glVertex4f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b07852c1199338917ca1f29c54923ba6a904f30f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945859"
---
# <a name="glvertex4f-function"></a><span data-ttu-id="32f4d-105">glVertex4f 函式</span><span class="sxs-lookup"><span data-stu-id="32f4d-105">glVertex4f function</span></span>

<span data-ttu-id="32f4d-106">指定頂點。</span><span class="sxs-lookup"><span data-stu-id="32f4d-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="32f4d-107">語法</span><span class="sxs-lookup"><span data-stu-id="32f4d-107">Syntax</span></span>


```C++
void WINAPI glVertex4f(
   GLfloat x,
   GLfloat y,
   GLfloat z,
   GLfloat w
);
```



## <a name="parameters"></a><span data-ttu-id="32f4d-108">參數</span><span class="sxs-lookup"><span data-stu-id="32f4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32f4d-109">*x*</span><span class="sxs-lookup"><span data-stu-id="32f4d-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="32f4d-110">指定頂點的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="32f4d-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="32f4d-111">*y*</span><span class="sxs-lookup"><span data-stu-id="32f4d-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="32f4d-112">指定頂點的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="32f4d-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="32f4d-113">*Z*</span><span class="sxs-lookup"><span data-stu-id="32f4d-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="32f4d-114">指定頂點的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="32f4d-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="32f4d-115">*w*</span><span class="sxs-lookup"><span data-stu-id="32f4d-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="32f4d-116">指定頂點的 w 座標。</span><span class="sxs-lookup"><span data-stu-id="32f4d-116">Specifies the w-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32f4d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="32f4d-117">Return value</span></span>

<span data-ttu-id="32f4d-118">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="32f4d-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32f4d-119">備註</span><span class="sxs-lookup"><span data-stu-id="32f4d-119">Remarks</span></span>

<span data-ttu-id="32f4d-120">GlVertex 函數命令會在 [**glBegin**](glbegin.md) / [**glEnd**](glend.md)配對中用來指定點、線條和多邊形頂點。</span><span class="sxs-lookup"><span data-stu-id="32f4d-120">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="32f4d-121">當呼叫 glVertex 時，目前的色彩、標準和材質座標會與頂點相關聯。</span><span class="sxs-lookup"><span data-stu-id="32f4d-121">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="32f4d-122">當僅指定 *x* 和 *y* 時， *z* 的預設值為0.0， *w* 預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="32f4d-122">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="32f4d-123">當指定 *x*、 *y* 和 *z* 時， *w* 預設為1.0。</span><span class="sxs-lookup"><span data-stu-id="32f4d-123">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="32f4d-124">在 **glBegin** / **glEnd** 配對之外叫用 glVertex 會導致未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="32f4d-124">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="32f4d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="32f4d-125">Requirements</span></span>



| <span data-ttu-id="32f4d-126">需求</span><span class="sxs-lookup"><span data-stu-id="32f4d-126">Requirement</span></span> | <span data-ttu-id="32f4d-127">值</span><span class="sxs-lookup"><span data-stu-id="32f4d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32f4d-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32f4d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="32f4d-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32f4d-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="32f4d-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32f4d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="32f4d-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32f4d-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="32f4d-132">標頭</span><span class="sxs-lookup"><span data-stu-id="32f4d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="32f4d-133"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="32f4d-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="32f4d-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="32f4d-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="32f4d-135"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="32f4d-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="32f4d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="32f4d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32f4d-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32f4d-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32f4d-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32f4d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32f4d-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="32f4d-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="32f4d-140">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="32f4d-140">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="32f4d-141">**glColor**</span><span class="sxs-lookup"><span data-stu-id="32f4d-141">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="32f4d-142">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="32f4d-142">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="32f4d-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="32f4d-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="32f4d-144">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="32f4d-144">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="32f4d-145">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="32f4d-145">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="32f4d-146">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="32f4d-146">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="32f4d-147">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="32f4d-147">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="32f4d-148">**glRect**</span><span class="sxs-lookup"><span data-stu-id="32f4d-148">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="32f4d-149">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="32f4d-149">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





