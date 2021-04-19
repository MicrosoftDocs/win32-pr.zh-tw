---
title: 'glVertex2i 函式 (Gl) '
description: '指定頂點。 |glVertex2i 函式 (Gl) '
ms.assetid: 13dc175b-9382-4266-962d-6dcf23ff5949
keywords:
- glVertex2i 函式 OpenGL
topic_type:
- apiref
api_name:
- glVertex2i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f810083c61fbd04d1c61349d57e7abd72ab95a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106982184"
---
# <a name="glvertex2i-function"></a><span data-ttu-id="41534-105">glVertex2i 函式</span><span class="sxs-lookup"><span data-stu-id="41534-105">glVertex2i function</span></span>

<span data-ttu-id="41534-106">指定頂點。</span><span class="sxs-lookup"><span data-stu-id="41534-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="41534-107">語法</span><span class="sxs-lookup"><span data-stu-id="41534-107">Syntax</span></span>


```C++
void WINAPI glVertex2i(
   GLint x,
   GLint y
);
```



## <a name="parameters"></a><span data-ttu-id="41534-108">參數</span><span class="sxs-lookup"><span data-stu-id="41534-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41534-109">*x*</span><span class="sxs-lookup"><span data-stu-id="41534-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="41534-110">指定頂點的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="41534-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="41534-111">*y*</span><span class="sxs-lookup"><span data-stu-id="41534-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="41534-112">指定頂點的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="41534-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41534-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="41534-113">Return value</span></span>

<span data-ttu-id="41534-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="41534-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41534-115">備註</span><span class="sxs-lookup"><span data-stu-id="41534-115">Remarks</span></span>

<span data-ttu-id="41534-116">GlVertex 函數命令會在 [**glBegin**](glbegin.md) / [**glEnd**](glend.md)配對中用來指定點、線條和多邊形頂點。</span><span class="sxs-lookup"><span data-stu-id="41534-116">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="41534-117">當呼叫 glVertex 時，目前的色彩、標準和材質座標會與頂點相關聯。</span><span class="sxs-lookup"><span data-stu-id="41534-117">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="41534-118">當僅指定 *x* 和 *y* 時， *z* 的預設值為0.0， *w* 預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="41534-118">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="41534-119">當指定 *x*、 *y* 和 *z* 時， *w* 預設為1.0。</span><span class="sxs-lookup"><span data-stu-id="41534-119">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="41534-120">在 **glBegin** / **glEnd** 配對之外叫用 glVertex 會導致未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="41534-120">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="41534-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="41534-121">Requirements</span></span>



| <span data-ttu-id="41534-122">需求</span><span class="sxs-lookup"><span data-stu-id="41534-122">Requirement</span></span> | <span data-ttu-id="41534-123">值</span><span class="sxs-lookup"><span data-stu-id="41534-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41534-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41534-124">Minimum supported client</span></span><br/> | <span data-ttu-id="41534-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41534-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="41534-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41534-126">Minimum supported server</span></span><br/> | <span data-ttu-id="41534-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41534-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="41534-128">標頭</span><span class="sxs-lookup"><span data-stu-id="41534-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="41534-129"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="41534-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="41534-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="41534-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="41534-131"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="41534-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="41534-132">DLL</span><span class="sxs-lookup"><span data-stu-id="41534-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41534-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41534-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41534-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41534-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41534-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="41534-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="41534-136">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="41534-136">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="41534-137">**glColor**</span><span class="sxs-lookup"><span data-stu-id="41534-137">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="41534-138">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="41534-138">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="41534-139">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="41534-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="41534-140">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="41534-140">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="41534-141">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="41534-141">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="41534-142">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="41534-142">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="41534-143">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="41534-143">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="41534-144">**glRect**</span><span class="sxs-lookup"><span data-stu-id="41534-144">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="41534-145">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="41534-145">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





