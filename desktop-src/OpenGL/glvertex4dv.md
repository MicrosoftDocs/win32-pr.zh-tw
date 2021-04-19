---
title: 'glVertex4dv 函式 (Gl) '
description: '指定頂點。 |glVertex4dv 函式 (Gl) '
ms.assetid: af0a3c69-0d71-4cbb-9494-561033d99ac1
keywords:
- glVertex4dv 函式 OpenGL
topic_type:
- apiref
api_name:
- glVertex4dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 532a71c576ca0b49dd645afe8b501f0e718a827b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992261"
---
# <a name="glvertex4dv-function"></a><span data-ttu-id="3ec1b-105">glVertex4dv 函式</span><span class="sxs-lookup"><span data-stu-id="3ec1b-105">glVertex4dv function</span></span>

<span data-ttu-id="3ec1b-106">指定頂點。</span><span class="sxs-lookup"><span data-stu-id="3ec1b-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ec1b-107">語法</span><span class="sxs-lookup"><span data-stu-id="3ec1b-107">Syntax</span></span>


```C++
void WINAPI glVertex4dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="3ec1b-108">參數</span><span class="sxs-lookup"><span data-stu-id="3ec1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ec1b-109">*V*</span><span class="sxs-lookup"><span data-stu-id="3ec1b-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="3ec1b-110">四個元素的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="3ec1b-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="3ec1b-111">元素是頂點的 x、y、z 和 w 座標。</span><span class="sxs-lookup"><span data-stu-id="3ec1b-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ec1b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ec1b-112">Return value</span></span>

<span data-ttu-id="3ec1b-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3ec1b-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ec1b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ec1b-114">Requirements</span></span>



| <span data-ttu-id="3ec1b-115">需求</span><span class="sxs-lookup"><span data-stu-id="3ec1b-115">Requirement</span></span> | <span data-ttu-id="3ec1b-116">值</span><span class="sxs-lookup"><span data-stu-id="3ec1b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec1b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ec1b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec1b-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ec1b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3ec1b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ec1b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec1b-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ec1b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ec1b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="3ec1b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ec1b-122"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="3ec1b-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3ec1b-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="3ec1b-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ec1b-124"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ec1b-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3ec1b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3ec1b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ec1b-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ec1b-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ec1b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ec1b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec1b-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3ec1b-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3ec1b-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="3ec1b-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="3ec1b-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="3ec1b-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="3ec1b-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="3ec1b-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="3ec1b-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3ec1b-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3ec1b-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="3ec1b-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="3ec1b-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="3ec1b-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="3ec1b-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="3ec1b-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="3ec1b-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="3ec1b-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="3ec1b-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="3ec1b-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="3ec1b-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="3ec1b-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





