---
title: 'glRectiv 函式 (Gl) '
description: GlRectiv 函式會繪製一個矩形。
ms.assetid: 24db6fc0-9b53-4e72-9b12-18ea65409f12
keywords:
- glRectiv 函式 OpenGL
topic_type:
- apiref
api_name:
- glRectiv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 668e1f253a44833ee7b1e0210327e93536bb850f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843116"
---
# <a name="glrectiv-function"></a><span data-ttu-id="cae9c-104">glRectiv 函式</span><span class="sxs-lookup"><span data-stu-id="cae9c-104">glRectiv function</span></span>

<span data-ttu-id="cae9c-105">**GlRectiv** 函式會繪製一個矩形。</span><span class="sxs-lookup"><span data-stu-id="cae9c-105">The **glRectiv** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae9c-106">語法</span><span class="sxs-lookup"><span data-stu-id="cae9c-106">Syntax</span></span>


```C++
void WINAPI glRectiv(
   const GLint *v1,
   const GLint *v2
);
```



## <a name="parameters"></a><span data-ttu-id="cae9c-107">參數</span><span class="sxs-lookup"><span data-stu-id="cae9c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cae9c-108">*v1*</span><span class="sxs-lookup"><span data-stu-id="cae9c-108">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="cae9c-109">矩形的一個頂點指標。</span><span class="sxs-lookup"><span data-stu-id="cae9c-109">A pointer to one vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="cae9c-110">*v2*</span><span class="sxs-lookup"><span data-stu-id="cae9c-110">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="cae9c-111">矩形相對頂點的指標。</span><span class="sxs-lookup"><span data-stu-id="cae9c-111">a pointer to the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cae9c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cae9c-112">Return value</span></span>

<span data-ttu-id="cae9c-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cae9c-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cae9c-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="cae9c-114">Error codes</span></span>

<span data-ttu-id="cae9c-115">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cae9c-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cae9c-116">Name</span><span class="sxs-lookup"><span data-stu-id="cae9c-116">Name</span></span>                                                                                                  | <span data-ttu-id="cae9c-117">意義</span><span class="sxs-lookup"><span data-stu-id="cae9c-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cae9c-118"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="cae9c-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cae9c-119">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="cae9c-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cae9c-120">備註</span><span class="sxs-lookup"><span data-stu-id="cae9c-120">Remarks</span></span>

<span data-ttu-id="cae9c-121">**GlRecti** 函式支援以有效的矩形規格作為兩個角落點。</span><span class="sxs-lookup"><span data-stu-id="cae9c-121">The **glRecti** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="cae9c-122">每個矩形命令都採用四個引數，並以兩個連續的 (*x*、 *y*) 座標，或作為陣列的兩個指標（每個都包含 (*x*、 *y*) 組）進行組織。</span><span class="sxs-lookup"><span data-stu-id="cae9c-122">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="cae9c-123">產生的矩形是在 *z* = 0 平面中定義。</span><span class="sxs-lookup"><span data-stu-id="cae9c-123">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="cae9c-124">**GlRecti** (*x1、* *y1、* *x2、* *y2*) 函數完全等同于下列順序：</span><span class="sxs-lookup"><span data-stu-id="cae9c-124">The **glRecti**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="cae9c-125">**glBegin** (GL \_ 多邊形) ;</span><span class="sxs-lookup"><span data-stu-id="cae9c-125">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="cae9c-126">**glVertex2** ( *x1，* *y1* ) ;</span><span class="sxs-lookup"><span data-stu-id="cae9c-126">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="cae9c-127">**glVertex2** ( *x2，* *y1* ) ;</span><span class="sxs-lookup"><span data-stu-id="cae9c-127">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="cae9c-128">**glVertex2** ( *x2，* *y2* ) ;</span><span class="sxs-lookup"><span data-stu-id="cae9c-128">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="cae9c-129">**glVertex2** ( *x1，* *y2* ) ;</span><span class="sxs-lookup"><span data-stu-id="cae9c-129">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="cae9c-130">**glEnd** ( ) ;</span><span class="sxs-lookup"><span data-stu-id="cae9c-130">**glEnd**( );</span></span>

<span data-ttu-id="cae9c-131">請注意，如果第二個頂點在第一個頂點的上方和右邊，則會以逆時針繞組來構成矩形。</span><span class="sxs-lookup"><span data-stu-id="cae9c-131">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="cae9c-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="cae9c-132">Requirements</span></span>



| <span data-ttu-id="cae9c-133">需求</span><span class="sxs-lookup"><span data-stu-id="cae9c-133">Requirement</span></span> | <span data-ttu-id="cae9c-134">值</span><span class="sxs-lookup"><span data-stu-id="cae9c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cae9c-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cae9c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cae9c-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cae9c-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cae9c-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cae9c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cae9c-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cae9c-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cae9c-139">標頭</span><span class="sxs-lookup"><span data-stu-id="cae9c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cae9c-140"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="cae9c-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cae9c-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="cae9c-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="cae9c-142"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cae9c-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cae9c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cae9c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cae9c-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cae9c-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cae9c-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cae9c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae9c-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cae9c-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cae9c-147">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="cae9c-147">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cae9c-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="cae9c-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





