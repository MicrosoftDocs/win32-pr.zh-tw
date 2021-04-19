---
title: 'glVertex3fv 函式 (Gl) '
description: '指定頂點。 |glVertex3fv 函式 (Gl) '
ms.assetid: d8790ffe-73b1-49d8-a7f5-2117177573ac
keywords:
- glVertex3fv 函式 OpenGL
topic_type:
- apiref
api_name:
- glVertex3fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f3bcbe73d071bc18e3a1a58ef2f505fa9bd6a3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976431"
---
# <a name="glvertex3fv-function"></a><span data-ttu-id="e3bdf-105">glVertex3fv 函式</span><span class="sxs-lookup"><span data-stu-id="e3bdf-105">glVertex3fv function</span></span>

<span data-ttu-id="e3bdf-106">指定頂點。</span><span class="sxs-lookup"><span data-stu-id="e3bdf-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3bdf-107">語法</span><span class="sxs-lookup"><span data-stu-id="e3bdf-107">Syntax</span></span>


```C++
void WINAPI glVertex3fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="e3bdf-108">參數</span><span class="sxs-lookup"><span data-stu-id="e3bdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3bdf-109">*V*</span><span class="sxs-lookup"><span data-stu-id="e3bdf-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="e3bdf-110">三個元素的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="e3bdf-110">A pointer to an array of three elements.</span></span> <span data-ttu-id="e3bdf-111">元素是頂點的 x、y 和 z 座標。</span><span class="sxs-lookup"><span data-stu-id="e3bdf-111">The elements are the x, y, and z coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3bdf-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3bdf-112">Return value</span></span>

<span data-ttu-id="e3bdf-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e3bdf-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3bdf-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3bdf-114">Requirements</span></span>



| <span data-ttu-id="e3bdf-115">需求</span><span class="sxs-lookup"><span data-stu-id="e3bdf-115">Requirement</span></span> | <span data-ttu-id="e3bdf-116">值</span><span class="sxs-lookup"><span data-stu-id="e3bdf-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3bdf-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3bdf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e3bdf-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3bdf-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e3bdf-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3bdf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e3bdf-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3bdf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3bdf-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e3bdf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3bdf-122"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="e3bdf-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e3bdf-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="e3bdf-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3bdf-124"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3bdf-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e3bdf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e3bdf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3bdf-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3bdf-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3bdf-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3bdf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3bdf-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e3bdf-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e3bdf-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="e3bdf-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="e3bdf-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="e3bdf-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="e3bdf-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="e3bdf-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="e3bdf-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e3bdf-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e3bdf-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="e3bdf-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="e3bdf-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="e3bdf-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="e3bdf-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="e3bdf-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="e3bdf-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="e3bdf-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="e3bdf-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="e3bdf-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="e3bdf-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="e3bdf-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





