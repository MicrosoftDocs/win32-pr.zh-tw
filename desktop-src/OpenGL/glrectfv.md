---
title: 'glRectfv 函式 (Gl) '
description: GlRectfv 函式會繪製一個矩形。
ms.assetid: 2053890e-bae7-4c06-98e7-5ce4314fe95c
keywords:
- glRectfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glRectfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 871cd3edc44598ba66fb686d9957af7322d77730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383906"
---
# <a name="glrectfv-function"></a><span data-ttu-id="48a94-104">glRectfv 函式</span><span class="sxs-lookup"><span data-stu-id="48a94-104">glRectfv function</span></span>

<span data-ttu-id="48a94-105">[**GlRectfv**](glrectdv.md)函式會繪製一個矩形。</span><span class="sxs-lookup"><span data-stu-id="48a94-105">The [**glRectfv**](glrectdv.md) function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a94-106">語法</span><span class="sxs-lookup"><span data-stu-id="48a94-106">Syntax</span></span>


```C++
void WINAPI glRectfv(
   const GLfloat *v1,
   const GLfloat *v2
);
```



## <a name="parameters"></a><span data-ttu-id="48a94-107">參數</span><span class="sxs-lookup"><span data-stu-id="48a94-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a94-108">*v1*</span><span class="sxs-lookup"><span data-stu-id="48a94-108">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="48a94-109">矩形的一個頂點指標。</span><span class="sxs-lookup"><span data-stu-id="48a94-109">A pointer to one vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="48a94-110">*v2*</span><span class="sxs-lookup"><span data-stu-id="48a94-110">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="48a94-111">矩形相對頂點的指標。</span><span class="sxs-lookup"><span data-stu-id="48a94-111">a pointer to the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a94-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="48a94-112">Return value</span></span>

<span data-ttu-id="48a94-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="48a94-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="48a94-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="48a94-114">Error codes</span></span>

<span data-ttu-id="48a94-115">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="48a94-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="48a94-116">Name</span><span class="sxs-lookup"><span data-stu-id="48a94-116">Name</span></span>                                                                                                  | <span data-ttu-id="48a94-117">意義</span><span class="sxs-lookup"><span data-stu-id="48a94-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48a94-118"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="48a94-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="48a94-119">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="48a94-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="48a94-120">備註</span><span class="sxs-lookup"><span data-stu-id="48a94-120">Remarks</span></span>

<span data-ttu-id="48a94-121">**GlRectf** 函式支援以有效的矩形規格作為兩個角落點。</span><span class="sxs-lookup"><span data-stu-id="48a94-121">The **glRectf** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="48a94-122">每個矩形命令都採用四個引數，並以兩個連續的 (*x*、 *y*) 座標，或作為陣列的兩個指標（每個都包含 (*x*、 *y*) 組）進行組織。</span><span class="sxs-lookup"><span data-stu-id="48a94-122">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="48a94-123">產生的矩形是在 *z* = 0 平面中定義。</span><span class="sxs-lookup"><span data-stu-id="48a94-123">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="48a94-124">**GlRectf** (*x1、* *y1、* *x2、* *y2*) 函數完全等同于下列順序：</span><span class="sxs-lookup"><span data-stu-id="48a94-124">The **glRectf**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="48a94-125">**glBegin** (GL \_ 多邊形) ;</span><span class="sxs-lookup"><span data-stu-id="48a94-125">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="48a94-126">**glVertex2** ( *x1，* *y1* ) ;</span><span class="sxs-lookup"><span data-stu-id="48a94-126">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="48a94-127">**glVertex2** ( *x2，* *y1* ) ;</span><span class="sxs-lookup"><span data-stu-id="48a94-127">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="48a94-128">**glVertex2** ( *x2，* *y2* ) ;</span><span class="sxs-lookup"><span data-stu-id="48a94-128">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="48a94-129">**glVertex2** ( *x1，* *y2* ) ;</span><span class="sxs-lookup"><span data-stu-id="48a94-129">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="48a94-130">**glEnd** ( ) ;</span><span class="sxs-lookup"><span data-stu-id="48a94-130">**glEnd**( );</span></span>

<span data-ttu-id="48a94-131">請注意，如果第二個頂點在第一個頂點的上方和右邊，則會以逆時針繞組來構成矩形。</span><span class="sxs-lookup"><span data-stu-id="48a94-131">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="48a94-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="48a94-132">Requirements</span></span>



| <span data-ttu-id="48a94-133">需求</span><span class="sxs-lookup"><span data-stu-id="48a94-133">Requirement</span></span> | <span data-ttu-id="48a94-134">值</span><span class="sxs-lookup"><span data-stu-id="48a94-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48a94-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48a94-135">Minimum supported client</span></span><br/> | <span data-ttu-id="48a94-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48a94-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="48a94-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48a94-137">Minimum supported server</span></span><br/> | <span data-ttu-id="48a94-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48a94-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="48a94-139">標頭</span><span class="sxs-lookup"><span data-stu-id="48a94-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="48a94-140"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="48a94-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="48a94-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="48a94-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="48a94-142"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="48a94-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="48a94-143">DLL</span><span class="sxs-lookup"><span data-stu-id="48a94-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48a94-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48a94-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48a94-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48a94-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a94-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="48a94-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="48a94-147">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="48a94-147">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="48a94-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="48a94-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





