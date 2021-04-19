---
title: 'glVertex2f 函式 (Gl) '
description: '指定頂點。 |glVertex2f 函式 (Gl) '
ms.assetid: d351cdc1-efaa-4c06-96d9-c4ef613c64df
keywords:
- glVertex2f 函式 OpenGL
topic_type:
- apiref
api_name:
- glVertex2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b2610b4d0498a5a623372ba5f28ee4feea7b40d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981959"
---
# <a name="glvertex2f-function"></a><span data-ttu-id="8afb6-105">glVertex2f 函式</span><span class="sxs-lookup"><span data-stu-id="8afb6-105">glVertex2f function</span></span>

<span data-ttu-id="8afb6-106">指定頂點。</span><span class="sxs-lookup"><span data-stu-id="8afb6-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="8afb6-107">語法</span><span class="sxs-lookup"><span data-stu-id="8afb6-107">Syntax</span></span>


```C++
void WINAPI glVertex2f(
   GLfloat x,
   GLfloat y
);
```



## <a name="parameters"></a><span data-ttu-id="8afb6-108">參數</span><span class="sxs-lookup"><span data-stu-id="8afb6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8afb6-109">*x*</span><span class="sxs-lookup"><span data-stu-id="8afb6-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="8afb6-110">指定頂點的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="8afb6-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="8afb6-111">*y*</span><span class="sxs-lookup"><span data-stu-id="8afb6-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="8afb6-112">指定頂點的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="8afb6-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8afb6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8afb6-113">Return value</span></span>

<span data-ttu-id="8afb6-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8afb6-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8afb6-115">備註</span><span class="sxs-lookup"><span data-stu-id="8afb6-115">Remarks</span></span>

<span data-ttu-id="8afb6-116">GlVertex 函數命令會在 [**glBegin**](glbegin.md) / [**glEnd**](glend.md)配對中用來指定點、線條和多邊形頂點。</span><span class="sxs-lookup"><span data-stu-id="8afb6-116">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="8afb6-117">當呼叫 glVertex 時，目前的色彩、標準和材質座標會與頂點相關聯。</span><span class="sxs-lookup"><span data-stu-id="8afb6-117">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="8afb6-118">當僅指定 *x* 和 *y* 時， *z* 的預設值為0.0， *w* 預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="8afb6-118">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="8afb6-119">當指定 *x*、 *y* 和 *z* 時， *w* 預設為1.0。</span><span class="sxs-lookup"><span data-stu-id="8afb6-119">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="8afb6-120">在 **glBegin** / **glEnd** 配對之外叫用 glVertex 會導致未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="8afb6-120">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="8afb6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8afb6-121">Requirements</span></span>



| <span data-ttu-id="8afb6-122">需求</span><span class="sxs-lookup"><span data-stu-id="8afb6-122">Requirement</span></span> | <span data-ttu-id="8afb6-123">值</span><span class="sxs-lookup"><span data-stu-id="8afb6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8afb6-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8afb6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8afb6-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8afb6-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8afb6-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8afb6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8afb6-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8afb6-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8afb6-128">標頭</span><span class="sxs-lookup"><span data-stu-id="8afb6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8afb6-129"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="8afb6-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8afb6-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="8afb6-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="8afb6-131"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8afb6-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8afb6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8afb6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8afb6-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8afb6-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8afb6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8afb6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8afb6-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8afb6-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8afb6-136">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="8afb6-136">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="8afb6-137">**glColor**</span><span class="sxs-lookup"><span data-stu-id="8afb6-137">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="8afb6-138">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="8afb6-138">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="8afb6-139">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8afb6-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8afb6-140">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="8afb6-140">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="8afb6-141">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="8afb6-141">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="8afb6-142">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="8afb6-142">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="8afb6-143">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="8afb6-143">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="8afb6-144">**glRect**</span><span class="sxs-lookup"><span data-stu-id="8afb6-144">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="8afb6-145">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="8afb6-145">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





