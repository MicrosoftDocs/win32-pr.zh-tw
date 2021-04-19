---
title: 'glVertex3d 函式 (Gl) '
description: '指定頂點。 |glVertex3d 函式 (Gl) '
ms.assetid: 531a552d-7979-4994-ad28-73c2d3987bae
keywords:
- glVertex3d 函式 OpenGL
topic_type:
- apiref
api_name:
- glVertex3d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 608ab02bf2cd41b7f2ffcc8fa3fe8cb2dea0ca89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106988150"
---
# <a name="glvertex3d-function"></a><span data-ttu-id="a300b-105">glVertex3d 函式</span><span class="sxs-lookup"><span data-stu-id="a300b-105">glVertex3d function</span></span>

<span data-ttu-id="a300b-106">指定頂點。</span><span class="sxs-lookup"><span data-stu-id="a300b-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="a300b-107">語法</span><span class="sxs-lookup"><span data-stu-id="a300b-107">Syntax</span></span>


```C++
void WINAPI glVertex3d(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="a300b-108">參數</span><span class="sxs-lookup"><span data-stu-id="a300b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a300b-109">*x*</span><span class="sxs-lookup"><span data-stu-id="a300b-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="a300b-110">指定頂點的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="a300b-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="a300b-111">*y*</span><span class="sxs-lookup"><span data-stu-id="a300b-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="a300b-112">指定頂點的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="a300b-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="a300b-113">*Z*</span><span class="sxs-lookup"><span data-stu-id="a300b-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="a300b-114">指定頂點的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="a300b-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a300b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a300b-115">Return value</span></span>

<span data-ttu-id="a300b-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a300b-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a300b-117">備註</span><span class="sxs-lookup"><span data-stu-id="a300b-117">Remarks</span></span>

<span data-ttu-id="a300b-118">GlVertex 函數命令會在 [**glBegin**](glbegin.md) / [**glEnd**](glend.md)配對中用來指定點、線條和多邊形頂點。</span><span class="sxs-lookup"><span data-stu-id="a300b-118">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="a300b-119">當呼叫 glVertex 時，目前的色彩、標準和材質座標會與頂點相關聯。</span><span class="sxs-lookup"><span data-stu-id="a300b-119">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="a300b-120">當僅指定 *x* 和 *y* 時， *z* 的預設值為0.0， *w* 預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="a300b-120">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="a300b-121">當指定 *x*、 *y* 和 *z* 時， *w* 預設為1.0。</span><span class="sxs-lookup"><span data-stu-id="a300b-121">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="a300b-122">在 **glBegin** / **glEnd** 配對之外叫用 glVertex 會導致未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="a300b-122">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="a300b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a300b-123">Requirements</span></span>



| <span data-ttu-id="a300b-124">需求</span><span class="sxs-lookup"><span data-stu-id="a300b-124">Requirement</span></span> | <span data-ttu-id="a300b-125">值</span><span class="sxs-lookup"><span data-stu-id="a300b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a300b-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a300b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a300b-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a300b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a300b-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a300b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a300b-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a300b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a300b-130">標頭</span><span class="sxs-lookup"><span data-stu-id="a300b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a300b-131"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="a300b-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a300b-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="a300b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="a300b-133"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a300b-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a300b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a300b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a300b-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a300b-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a300b-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a300b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a300b-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a300b-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a300b-138">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="a300b-138">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="a300b-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="a300b-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="a300b-140">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="a300b-140">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="a300b-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a300b-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a300b-142">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="a300b-142">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="a300b-143">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="a300b-143">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="a300b-144">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="a300b-144">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="a300b-145">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="a300b-145">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="a300b-146">**glRect**</span><span class="sxs-lookup"><span data-stu-id="a300b-146">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="a300b-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="a300b-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





