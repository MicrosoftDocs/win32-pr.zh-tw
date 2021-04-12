---
title: 'glIsList 函式 (Gl) '
description: GllsList 函數會測試顯示清單是否存在。
ms.assetid: 86ef3684-8047-4ee4-befd-ec26bcd036c3
keywords:
- glIsList 函式 OpenGL
topic_type:
- apiref
api_name:
- glIsList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fdc67d0a7dad18f8850c283f0d5eb224ff9ebbd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317391"
---
# <a name="glislist-function"></a><span data-ttu-id="da19c-104">glIsList 函式</span><span class="sxs-lookup"><span data-stu-id="da19c-104">glIsList function</span></span>

<span data-ttu-id="da19c-105">**GllsList** 函數會測試顯示清單是否存在。</span><span class="sxs-lookup"><span data-stu-id="da19c-105">The **gllsList** function tests for display list existence.</span></span>

## <a name="syntax"></a><span data-ttu-id="da19c-106">語法</span><span class="sxs-lookup"><span data-stu-id="da19c-106">Syntax</span></span>


```C++
GLboolean WINAPI glIsList(
   GLuint list
);
```



## <a name="parameters"></a><span data-ttu-id="da19c-107">參數</span><span class="sxs-lookup"><span data-stu-id="da19c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da19c-108">*list*</span><span class="sxs-lookup"><span data-stu-id="da19c-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="da19c-109">可能的顯示清單名稱。</span><span class="sxs-lookup"><span data-stu-id="da19c-109">A potential display list name.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="da19c-110">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="da19c-110">Error codes</span></span>

<span data-ttu-id="da19c-111">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="da19c-111">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="da19c-112">Name</span><span class="sxs-lookup"><span data-stu-id="da19c-112">Name</span></span>                                                                                                  | <span data-ttu-id="da19c-113">意義</span><span class="sxs-lookup"><span data-stu-id="da19c-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="da19c-114"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="da19c-114"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="da19c-115">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="da19c-115">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="da19c-116">備註</span><span class="sxs-lookup"><span data-stu-id="da19c-116">Remarks</span></span>

<span data-ttu-id="da19c-117"> \_ 如果 *list* 是顯示清單的名稱，則 gllsList 函數會傳回 gl TRUE，否則會傳回 gl \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="da19c-117">The **gllsList** function returns GL\_TRUE if *list* is the name of a display list and returns GL\_FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="da19c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="da19c-118">Requirements</span></span>



| <span data-ttu-id="da19c-119">需求</span><span class="sxs-lookup"><span data-stu-id="da19c-119">Requirement</span></span> | <span data-ttu-id="da19c-120">值</span><span class="sxs-lookup"><span data-stu-id="da19c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da19c-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da19c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="da19c-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da19c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="da19c-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da19c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="da19c-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da19c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="da19c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="da19c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="da19c-126"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="da19c-126"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="da19c-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="da19c-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="da19c-128"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="da19c-128"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="da19c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="da19c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da19c-130"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da19c-130"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da19c-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da19c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da19c-132">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="da19c-132">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="da19c-133">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="da19c-133">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="da19c-134">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="da19c-134">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="da19c-135">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="da19c-135">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="da19c-136">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="da19c-136">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="da19c-137">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="da19c-137">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="da19c-138">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="da19c-138">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





