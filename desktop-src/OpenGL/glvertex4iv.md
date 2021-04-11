---
title: 'glVertex4iv 函式 (Gl) '
description: '指定頂點。 |glVertex4iv 函式 (Gl) '
ms.assetid: 7b56777a-f904-4a9d-8d3d-84a38cbf0b45
keywords:
- glVertex4iv 函式 OpenGL
topic_type:
- apiref
api_name:
- glVertex4iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff55c5534245843d5caa8797b2b529c7cfe00f9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853948"
---
# <a name="glvertex4iv-function"></a><span data-ttu-id="7ecec-105">glVertex4iv 函式</span><span class="sxs-lookup"><span data-stu-id="7ecec-105">glVertex4iv function</span></span>

<span data-ttu-id="7ecec-106">指定頂點。</span><span class="sxs-lookup"><span data-stu-id="7ecec-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ecec-107">語法</span><span class="sxs-lookup"><span data-stu-id="7ecec-107">Syntax</span></span>


```C++
void WINAPI glVertex4iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="7ecec-108">參數</span><span class="sxs-lookup"><span data-stu-id="7ecec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ecec-109">*V*</span><span class="sxs-lookup"><span data-stu-id="7ecec-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="7ecec-110">四個元素的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="7ecec-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="7ecec-111">元素是頂點的 x、y、z 和 w 座標。</span><span class="sxs-lookup"><span data-stu-id="7ecec-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ecec-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ecec-112">Return value</span></span>

<span data-ttu-id="7ecec-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7ecec-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ecec-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ecec-114">Requirements</span></span>



| <span data-ttu-id="7ecec-115">需求</span><span class="sxs-lookup"><span data-stu-id="7ecec-115">Requirement</span></span> | <span data-ttu-id="7ecec-116">值</span><span class="sxs-lookup"><span data-stu-id="7ecec-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ecec-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ecec-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7ecec-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ecec-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7ecec-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ecec-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7ecec-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ecec-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7ecec-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7ecec-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ecec-122"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="7ecec-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7ecec-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="7ecec-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ecec-124"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ecec-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7ecec-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7ecec-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ecec-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ecec-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ecec-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ecec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ecec-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7ecec-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7ecec-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="7ecec-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="7ecec-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="7ecec-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="7ecec-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="7ecec-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="7ecec-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7ecec-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7ecec-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="7ecec-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="7ecec-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="7ecec-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="7ecec-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="7ecec-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="7ecec-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="7ecec-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="7ecec-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="7ecec-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="7ecec-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="7ecec-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





