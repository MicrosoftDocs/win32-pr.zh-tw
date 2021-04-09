---
title: 'gluErrorString 函式 (X.glu 隊) '
description: GluErrorString 函式會從 OpenGL 或 X.GLU 隊錯誤碼產生錯誤字串。 錯誤字串僅為 ANSI。
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- gluErrorString 函式 OpenGL
topic_type:
- apiref
api_name:
- gluErrorString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cdcfad0e2a943bf3a475317f32d37921878a8f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685812"
---
# <a name="gluerrorstring-function"></a><span data-ttu-id="a0918-105">gluErrorString 函式</span><span class="sxs-lookup"><span data-stu-id="a0918-105">gluErrorString function</span></span>

<span data-ttu-id="a0918-106">**GluErrorString** 函式會從 OPENGL 或 x.glu 隊錯誤碼產生錯誤字串。</span><span class="sxs-lookup"><span data-stu-id="a0918-106">The **gluErrorString** function produces an error string from an OpenGL or GLU error code.</span></span> <span data-ttu-id="a0918-107">錯誤字串僅為 ANSI。</span><span class="sxs-lookup"><span data-stu-id="a0918-107">The error string is ANSI only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0918-108">語法</span><span class="sxs-lookup"><span data-stu-id="a0918-108">Syntax</span></span>


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a><span data-ttu-id="a0918-109">參數</span><span class="sxs-lookup"><span data-stu-id="a0918-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0918-110">*errCode*</span><span class="sxs-lookup"><span data-stu-id="a0918-110">*errCode*</span></span> 
</dt> <dd>

<span data-ttu-id="a0918-111">OpenGL 或 X.GLU 隊錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a0918-111">An OpenGL or GLU error code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0918-112">備註</span><span class="sxs-lookup"><span data-stu-id="a0918-112">Remarks</span></span>

<span data-ttu-id="a0918-113">**GluErrorString** 函式會從 OPENGL 或 x.glu 隊錯誤碼產生錯誤字串。</span><span class="sxs-lookup"><span data-stu-id="a0918-113">The **gluErrorString** function produces an error string from an OpenGL or GLU error code.</span></span> <span data-ttu-id="a0918-114">字串採用 ISO 拉丁1格式。</span><span class="sxs-lookup"><span data-stu-id="a0918-114">The string is in an ISO Latin 1 format.</span></span> <span data-ttu-id="a0918-115">例如， **gluErrorString** (GL \_ 記憶體不足) 會傳回「 \_ \_ 記憶體不足」字串。</span><span class="sxs-lookup"><span data-stu-id="a0918-115">For example, **gluErrorString**(GL\_OUT\_OF\_MEMORY) returns the string "out of memory".</span></span>

<span data-ttu-id="a0918-116">標準 X.GLU 隊錯誤碼為 X.GLU 隊 \_ 無效 \_ 的列舉、X.glu 隊 \_ 無效 \_ 的值，以及 x.glu 隊 \_ \_ 記憶體不足 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a0918-116">The standard GLU error codes are GLU\_INVALID\_ENUM, GLU\_INVALID\_VALUE, and GLU\_OUT\_OF\_MEMORY.</span></span> <span data-ttu-id="a0918-117">某些其他 X.GLU 隊函數可以透過回呼傳回特製化的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a0918-117">Certain other GLU functions can return specialized error codes through callbacks.</span></span> <span data-ttu-id="a0918-118">如需 OpenGL 錯誤碼清單，請參閱 [**glGetError**](glgeterror.md)。</span><span class="sxs-lookup"><span data-stu-id="a0918-118">For the list of OpenGL error codes, see [**glGetError**](glgeterror.md).</span></span>

<span data-ttu-id="a0918-119">**GluErrorString** 函式只會產生 ANSI 的錯誤字串。</span><span class="sxs-lookup"><span data-stu-id="a0918-119">The **gluErrorString** function produces error strings in ANSI only.</span></span> <span data-ttu-id="a0918-120">可能的話，請使用 **gluErrorStringWIN**，允許 ANSI 或 Unicode 錯誤字串。</span><span class="sxs-lookup"><span data-stu-id="a0918-120">Whenever possible, use **gluErrorStringWIN**, which allows ANSI or Unicode error strings.</span></span> <span data-ttu-id="a0918-121">這可讓您更輕鬆地將程式當地語系化以與其他語言搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a0918-121">This makes it easier to localize your program for use with another language.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0918-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0918-122">Requirements</span></span>



| <span data-ttu-id="a0918-123">需求</span><span class="sxs-lookup"><span data-stu-id="a0918-123">Requirement</span></span> | <span data-ttu-id="a0918-124">值</span><span class="sxs-lookup"><span data-stu-id="a0918-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a0918-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0918-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a0918-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0918-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a0918-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0918-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a0918-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0918-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a0918-129">標頭</span><span class="sxs-lookup"><span data-stu-id="a0918-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0918-130"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0918-130"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="a0918-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="a0918-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="a0918-132"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0918-132"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a0918-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a0918-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0918-134"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0918-134"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0918-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0918-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0918-136">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="a0918-136">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="a0918-137">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="a0918-137">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="a0918-138">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="a0918-138">*gluQuadricCallback*</span></span>](gluquadric.md)
</dt> <dt>

[<span data-ttu-id="a0918-139">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="a0918-139">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





