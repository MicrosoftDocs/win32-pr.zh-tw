---
title: 'glRects 函式 (Gl) '
description: GlRects 函式會繪製一個矩形。
ms.assetid: cf56352a-3396-4061-aa5e-dada986cf4ca
keywords:
- glRects 函式 OpenGL
topic_type:
- apiref
api_name:
- glRects
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcaa60d87c85001120da3a12005ca147b684b7a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106403"
---
# <a name="glrects-function"></a><span data-ttu-id="354ec-104">glRects 函式</span><span class="sxs-lookup"><span data-stu-id="354ec-104">glRects function</span></span>

<span data-ttu-id="354ec-105">**GlRects** 函式會繪製一個矩形。</span><span class="sxs-lookup"><span data-stu-id="354ec-105">The **glRects** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="354ec-106">語法</span><span class="sxs-lookup"><span data-stu-id="354ec-106">Syntax</span></span>


```C++
void WINAPI glRects(
   GLshort x1,
   GLshort y1,
   GLshort x2,
   GLshort y2
);
```



## <a name="parameters"></a><span data-ttu-id="354ec-107">參數</span><span class="sxs-lookup"><span data-stu-id="354ec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="354ec-108">*x1*</span><span class="sxs-lookup"><span data-stu-id="354ec-108">*x1*</span></span> 
</dt> <dd>

<span data-ttu-id="354ec-109">矩形頂點的 *x* 座標。</span><span class="sxs-lookup"><span data-stu-id="354ec-109">The *x* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="354ec-110">*y1*</span><span class="sxs-lookup"><span data-stu-id="354ec-110">*y1*</span></span> 
</dt> <dd>

<span data-ttu-id="354ec-111">矩形頂點的 *y* 座標。</span><span class="sxs-lookup"><span data-stu-id="354ec-111">The *y* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="354ec-112">*x2*</span><span class="sxs-lookup"><span data-stu-id="354ec-112">*x2*</span></span> 
</dt> <dd>

<span data-ttu-id="354ec-113">矩形相對頂點的 *x* 座標。</span><span class="sxs-lookup"><span data-stu-id="354ec-113">The *x* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="354ec-114">*y2*</span><span class="sxs-lookup"><span data-stu-id="354ec-114">*y2*</span></span> 
</dt> <dd>

<span data-ttu-id="354ec-115">矩形相對頂點的 *y* 座標。</span><span class="sxs-lookup"><span data-stu-id="354ec-115">The *y* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="354ec-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="354ec-116">Return value</span></span>

<span data-ttu-id="354ec-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="354ec-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="354ec-118">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="354ec-118">Error codes</span></span>

<span data-ttu-id="354ec-119">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="354ec-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="354ec-120">Name</span><span class="sxs-lookup"><span data-stu-id="354ec-120">Name</span></span>                                                                                                  | <span data-ttu-id="354ec-121">意義</span><span class="sxs-lookup"><span data-stu-id="354ec-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="354ec-122"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="354ec-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="354ec-123">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="354ec-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="354ec-124">備註</span><span class="sxs-lookup"><span data-stu-id="354ec-124">Remarks</span></span>

<span data-ttu-id="354ec-125">**GlRects** 函式支援以有效的矩形規格作為兩個角落點。</span><span class="sxs-lookup"><span data-stu-id="354ec-125">The **glRects** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="354ec-126">每個矩形命令都採用四個引數，並以兩個連續的 (x、 *y*) 座標，或作為陣列的兩個指標（每個都包含 (*x*、 *y*) 組）進行組織。</span><span class="sxs-lookup"><span data-stu-id="354ec-126">Each rectangle command takes four arguments, organized either as two consecutive pairs of (x, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="354ec-127">產生的矩形是在 *z* = 0 平面中定義。</span><span class="sxs-lookup"><span data-stu-id="354ec-127">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="354ec-128">**GlRects** (*x1、* *y1、* *x2、* *y2*) 函數完全等同于下列順序：</span><span class="sxs-lookup"><span data-stu-id="354ec-128">The **glRects**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="354ec-129">**glBegin** (GL \_ 多邊形) ;</span><span class="sxs-lookup"><span data-stu-id="354ec-129">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="354ec-130">**glVertex2** ( *x1，* *y1* ) ;</span><span class="sxs-lookup"><span data-stu-id="354ec-130">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="354ec-131">**glVertex2** ( *x2，* *y1* ) ;</span><span class="sxs-lookup"><span data-stu-id="354ec-131">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="354ec-132">**glVertex2** ( *x2，* *y2* ) ;</span><span class="sxs-lookup"><span data-stu-id="354ec-132">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="354ec-133">**glVertex2** ( *x1，* *y2* ) ;</span><span class="sxs-lookup"><span data-stu-id="354ec-133">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="354ec-134">**glEnd** ( ) ;</span><span class="sxs-lookup"><span data-stu-id="354ec-134">**glEnd**( );</span></span>

<span data-ttu-id="354ec-135">請注意，如果第二個頂點在第一個頂點的上方和右邊，則會以逆時針繞組來構成矩形。</span><span class="sxs-lookup"><span data-stu-id="354ec-135">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="354ec-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="354ec-136">Requirements</span></span>



| <span data-ttu-id="354ec-137">需求</span><span class="sxs-lookup"><span data-stu-id="354ec-137">Requirement</span></span> | <span data-ttu-id="354ec-138">值</span><span class="sxs-lookup"><span data-stu-id="354ec-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="354ec-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="354ec-139">Minimum supported client</span></span><br/> | <span data-ttu-id="354ec-140">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="354ec-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="354ec-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="354ec-141">Minimum supported server</span></span><br/> | <span data-ttu-id="354ec-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="354ec-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="354ec-143">標頭</span><span class="sxs-lookup"><span data-stu-id="354ec-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="354ec-144"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="354ec-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="354ec-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="354ec-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="354ec-146"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="354ec-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="354ec-147">DLL</span><span class="sxs-lookup"><span data-stu-id="354ec-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="354ec-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="354ec-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="354ec-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="354ec-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="354ec-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="354ec-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="354ec-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="354ec-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="354ec-152">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="354ec-152">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





