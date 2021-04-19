---
title: 'glVertex2sv 函式 (Gl) '
description: '指定頂點。 |glVertex2sv 函式 (Gl) '
ms.assetid: 4e13356a-a74b-4fb6-a001-1fffc28dd7a1
keywords:
- glVertex2sv 函式 OpenGL
topic_type:
- apiref
api_name:
- glVertex2sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e865ab8999e08f9c13ad46443ba039be1cda9e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106974804"
---
# <a name="glvertex2sv-function"></a><span data-ttu-id="c2e5a-105">glVertex2sv 函式</span><span class="sxs-lookup"><span data-stu-id="c2e5a-105">glVertex2sv function</span></span>

<span data-ttu-id="c2e5a-106">指定頂點。</span><span class="sxs-lookup"><span data-stu-id="c2e5a-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e5a-107">語法</span><span class="sxs-lookup"><span data-stu-id="c2e5a-107">Syntax</span></span>


```C++
void WINAPI glVertex2sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="c2e5a-108">參數</span><span class="sxs-lookup"><span data-stu-id="c2e5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e5a-109">*V*</span><span class="sxs-lookup"><span data-stu-id="c2e5a-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="c2e5a-110">兩個元素的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="c2e5a-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="c2e5a-111">元素是頂點的 x 和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="c2e5a-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2e5a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2e5a-112">Return value</span></span>

<span data-ttu-id="c2e5a-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c2e5a-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e5a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2e5a-114">Requirements</span></span>



| <span data-ttu-id="c2e5a-115">需求</span><span class="sxs-lookup"><span data-stu-id="c2e5a-115">Requirement</span></span> | <span data-ttu-id="c2e5a-116">值</span><span class="sxs-lookup"><span data-stu-id="c2e5a-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e5a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2e5a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c2e5a-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2e5a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c2e5a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2e5a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c2e5a-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2e5a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2e5a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c2e5a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2e5a-122"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="c2e5a-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c2e5a-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="c2e5a-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2e5a-124"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2e5a-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c2e5a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c2e5a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2e5a-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2e5a-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2e5a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2e5a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e5a-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c2e5a-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c2e5a-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="c2e5a-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="c2e5a-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="c2e5a-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="c2e5a-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="c2e5a-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="c2e5a-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c2e5a-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c2e5a-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="c2e5a-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="c2e5a-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="c2e5a-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="c2e5a-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="c2e5a-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="c2e5a-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="c2e5a-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="c2e5a-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="c2e5a-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="c2e5a-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="c2e5a-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





