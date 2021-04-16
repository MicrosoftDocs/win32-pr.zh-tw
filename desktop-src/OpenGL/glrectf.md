---
title: 'glRectf 函式 (Gl) '
description: GlRectf 函式會繪製一個矩形。
ms.assetid: 3fb55382-6041-4d9a-83cb-09a5170cc95a
keywords:
- glRectf 函式 OpenGL
topic_type:
- apiref
api_name:
- glRectf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0c7036ae7395dce66d88f52c30631be801c4af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464332"
---
# <a name="glrectf-function"></a><span data-ttu-id="0bf8a-104">glRectf 函式</span><span class="sxs-lookup"><span data-stu-id="0bf8a-104">glRectf function</span></span>

<span data-ttu-id="0bf8a-105">[**GlRectf**](glrectd.md)函式會繪製一個矩形。</span><span class="sxs-lookup"><span data-stu-id="0bf8a-105">The [**glRectf**](glrectd.md) function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bf8a-106">語法</span><span class="sxs-lookup"><span data-stu-id="0bf8a-106">Syntax</span></span>


```C++
void WINAPI glRectf(
   GLfloat x1,
   GLfloat y1,
   GLfloat x2,
   GLfloat y2
);
```



## <a name="parameters"></a><span data-ttu-id="0bf8a-107">參數</span><span class="sxs-lookup"><span data-stu-id="0bf8a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bf8a-108">*x1*</span><span class="sxs-lookup"><span data-stu-id="0bf8a-108">*x1*</span></span> 
</dt> <dd>

<span data-ttu-id="0bf8a-109">矩形頂點的 *x* 座標。</span><span class="sxs-lookup"><span data-stu-id="0bf8a-109">The *x* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="0bf8a-110">*y1*</span><span class="sxs-lookup"><span data-stu-id="0bf8a-110">*y1*</span></span> 
</dt> <dd>

<span data-ttu-id="0bf8a-111">矩形頂點的 *y* 座標。</span><span class="sxs-lookup"><span data-stu-id="0bf8a-111">The *y* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="0bf8a-112">*x2*</span><span class="sxs-lookup"><span data-stu-id="0bf8a-112">*x2*</span></span> 
</dt> <dd>

<span data-ttu-id="0bf8a-113">矩形相對頂點的 *x* 座標。</span><span class="sxs-lookup"><span data-stu-id="0bf8a-113">The *x* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="0bf8a-114">*y2*</span><span class="sxs-lookup"><span data-stu-id="0bf8a-114">*y2*</span></span> 
</dt> <dd>

<span data-ttu-id="0bf8a-115">矩形相對頂點的 *y* 座標。</span><span class="sxs-lookup"><span data-stu-id="0bf8a-115">The *y* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bf8a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="0bf8a-116">Return value</span></span>

<span data-ttu-id="0bf8a-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0bf8a-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0bf8a-118">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0bf8a-118">Error codes</span></span>

<span data-ttu-id="0bf8a-119">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0bf8a-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0bf8a-120">Name</span><span class="sxs-lookup"><span data-stu-id="0bf8a-120">Name</span></span>                                                                                                  | <span data-ttu-id="0bf8a-121">意義</span><span class="sxs-lookup"><span data-stu-id="0bf8a-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0bf8a-122"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="0bf8a-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0bf8a-123">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="0bf8a-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0bf8a-124">備註</span><span class="sxs-lookup"><span data-stu-id="0bf8a-124">Remarks</span></span>

<span data-ttu-id="0bf8a-125">**GlRectf** 函式支援以有效的矩形規格作為兩個角落點。</span><span class="sxs-lookup"><span data-stu-id="0bf8a-125">The **glRectf** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="0bf8a-126">每個矩形命令都採用四個引數，並以兩個連續的 (*x*、 *y*) 座標，或作為陣列的兩個指標（每個都包含 (*x*、 *y*) 組）進行組織。</span><span class="sxs-lookup"><span data-stu-id="0bf8a-126">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="0bf8a-127">產生的矩形是在 *z* = 0 平面中定義。</span><span class="sxs-lookup"><span data-stu-id="0bf8a-127">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="0bf8a-128">**GlRectf** (*x1、* *y1、* *x2、* *y2*) 函數完全等同于下列順序：</span><span class="sxs-lookup"><span data-stu-id="0bf8a-128">The **glRectf**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="0bf8a-129">**glBegin** (GL \_ 多邊形) ;</span><span class="sxs-lookup"><span data-stu-id="0bf8a-129">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="0bf8a-130">**glVertex2** ( *x1，* *y1* ) ;</span><span class="sxs-lookup"><span data-stu-id="0bf8a-130">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="0bf8a-131">**glVertex2** ( *x2，* *y1* ) ;</span><span class="sxs-lookup"><span data-stu-id="0bf8a-131">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="0bf8a-132">**glVertex2** ( *x2，* *y2* ) ;</span><span class="sxs-lookup"><span data-stu-id="0bf8a-132">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="0bf8a-133">**glVertex2** ( *x1，* *y2* ) ;</span><span class="sxs-lookup"><span data-stu-id="0bf8a-133">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="0bf8a-134">**glEnd** ( ) ;</span><span class="sxs-lookup"><span data-stu-id="0bf8a-134">**glEnd**( );</span></span>

<span data-ttu-id="0bf8a-135">請注意，如果第二個頂點在第一個頂點的上方和右邊，則會以逆時針繞組來構成矩形。</span><span class="sxs-lookup"><span data-stu-id="0bf8a-135">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bf8a-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="0bf8a-136">Requirements</span></span>



| <span data-ttu-id="0bf8a-137">需求</span><span class="sxs-lookup"><span data-stu-id="0bf8a-137">Requirement</span></span> | <span data-ttu-id="0bf8a-138">值</span><span class="sxs-lookup"><span data-stu-id="0bf8a-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf8a-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0bf8a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0bf8a-140">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0bf8a-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0bf8a-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0bf8a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0bf8a-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0bf8a-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0bf8a-143">標頭</span><span class="sxs-lookup"><span data-stu-id="0bf8a-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bf8a-144"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="0bf8a-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0bf8a-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="0bf8a-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="0bf8a-146"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bf8a-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0bf8a-147">DLL</span><span class="sxs-lookup"><span data-stu-id="0bf8a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bf8a-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bf8a-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bf8a-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0bf8a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bf8a-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0bf8a-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0bf8a-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0bf8a-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0bf8a-152">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="0bf8a-152">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





