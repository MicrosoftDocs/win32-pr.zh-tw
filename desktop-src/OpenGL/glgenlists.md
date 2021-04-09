---
title: 'glGenLists 函式 (Gl) '
description: GlGenLists 函數會產生一組連續的空白顯示清單。
ms.assetid: 07a97e89-1fbe-4405-b1b0-c4c47b098633
keywords:
- glGenLists 函式 OpenGL
topic_type:
- apiref
api_name:
- glGenLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc556e789da9c768a7ed1aef6880ad48022a1ee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685652"
---
# <a name="glgenlists-function"></a><span data-ttu-id="91b6b-104">glGenLists 函式</span><span class="sxs-lookup"><span data-stu-id="91b6b-104">glGenLists function</span></span>

<span data-ttu-id="91b6b-105">**GlGenLists** 函數會產生一組連續的空白顯示清單。</span><span class="sxs-lookup"><span data-stu-id="91b6b-105">The **glGenLists** function generates a contiguous set of empty display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="91b6b-106">語法</span><span class="sxs-lookup"><span data-stu-id="91b6b-106">Syntax</span></span>


```C++
GLuint WINAPI glGenLists(
   GLsizei range
);
```



## <a name="parameters"></a><span data-ttu-id="91b6b-107">參數</span><span class="sxs-lookup"><span data-stu-id="91b6b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91b6b-108">*range*</span><span class="sxs-lookup"><span data-stu-id="91b6b-108">*range*</span></span> 
</dt> <dd>

<span data-ttu-id="91b6b-109">要產生的連續空白顯示清單數目。</span><span class="sxs-lookup"><span data-stu-id="91b6b-109">The number of contiguous empty display lists to be generated.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="91b6b-110">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="91b6b-110">Error codes</span></span>

<span data-ttu-id="91b6b-111">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="91b6b-111">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="91b6b-112">Name</span><span class="sxs-lookup"><span data-stu-id="91b6b-112">Name</span></span>                                                                                                  | <span data-ttu-id="91b6b-113">意義</span><span class="sxs-lookup"><span data-stu-id="91b6b-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="91b6b-114"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="91b6b-114"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="91b6b-115">*範圍* 為負數。</span><span class="sxs-lookup"><span data-stu-id="91b6b-115">*range* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="91b6b-116"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="91b6b-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="91b6b-117">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="91b6b-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="91b6b-118">備註</span><span class="sxs-lookup"><span data-stu-id="91b6b-118">Remarks</span></span>

<span data-ttu-id="91b6b-119">**GlGenLists** 函數有一個引數，*範圍*。</span><span class="sxs-lookup"><span data-stu-id="91b6b-119">The **glGenLists** function has one argument, *range*.</span></span> <span data-ttu-id="91b6b-120">它會傳回一個整數 *n* ，使 *範圍* 連續的空白顯示清單（名稱為 *n*， *n* + 1）。</span><span class="sxs-lookup"><span data-stu-id="91b6b-120">It returns an integer *n* such that *range* contiguous empty display lists, named *n*, *n* + 1, .</span></span> <span data-ttu-id="91b6b-121">.</span><span class="sxs-lookup"><span data-stu-id="91b6b-121">.</span></span> <span data-ttu-id="91b6b-122">.，會建立 *n* + (*範圍* -1) 。</span><span class="sxs-lookup"><span data-stu-id="91b6b-122">., *n* + (*range* - 1), are created.</span></span> <span data-ttu-id="91b6b-123">如果 [ *範圍* ] 為零，則表示沒有可用的 *範圍* 連續名稱群組，或是產生任何錯誤，則不會產生顯示清單，並傳回零。</span><span class="sxs-lookup"><span data-stu-id="91b6b-123">If *range* is zero, if there is no group of *range* contiguous names available, or if any error is generated, then no display lists are generated and zero is returned.</span></span>

<span data-ttu-id="91b6b-124">下列函式會抓取 **glGenLists** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="91b6b-124">The following function retrieves information related to **glGenLists**:</span></span>

[<span data-ttu-id="91b6b-125">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="91b6b-125">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="91b6b-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="91b6b-126">Requirements</span></span>



| <span data-ttu-id="91b6b-127">需求</span><span class="sxs-lookup"><span data-stu-id="91b6b-127">Requirement</span></span> | <span data-ttu-id="91b6b-128">值</span><span class="sxs-lookup"><span data-stu-id="91b6b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91b6b-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91b6b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="91b6b-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91b6b-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="91b6b-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91b6b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="91b6b-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91b6b-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="91b6b-133">標頭</span><span class="sxs-lookup"><span data-stu-id="91b6b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="91b6b-134"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="91b6b-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="91b6b-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="91b6b-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="91b6b-136"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="91b6b-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="91b6b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="91b6b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91b6b-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91b6b-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91b6b-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91b6b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91b6b-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="91b6b-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="91b6b-141">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="91b6b-141">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="91b6b-142">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="91b6b-142">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="91b6b-143">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="91b6b-143">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="91b6b-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="91b6b-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="91b6b-145">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="91b6b-145">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="91b6b-146">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="91b6b-146">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





