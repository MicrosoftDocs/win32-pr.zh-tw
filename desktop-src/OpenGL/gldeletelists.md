---
title: 'glDeleteLists 函式 (Gl) '
description: GlDeleteLists 函式會刪除連續的顯示清單群組。
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- glDeleteLists 函式 OpenGL
topic_type:
- apiref
api_name:
- glDeleteLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11ae41273cba5bd050a62ea330cef9da0647769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106998014"
---
# <a name="gldeletelists-function"></a><span data-ttu-id="8ceff-104">glDeleteLists 函式</span><span class="sxs-lookup"><span data-stu-id="8ceff-104">glDeleteLists function</span></span>

<span data-ttu-id="8ceff-105">**GlDeleteLists** 函式會刪除連續的顯示清單群組。</span><span class="sxs-lookup"><span data-stu-id="8ceff-105">The **glDeleteLists** function deletes a contiguous group of display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ceff-106">語法</span><span class="sxs-lookup"><span data-stu-id="8ceff-106">Syntax</span></span>


```C++
void WINAPI glDeleteLists(
   GLuint  list,
   GLsizei range
);
```



## <a name="parameters"></a><span data-ttu-id="8ceff-107">參數</span><span class="sxs-lookup"><span data-stu-id="8ceff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ceff-108">*list*</span><span class="sxs-lookup"><span data-stu-id="8ceff-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="8ceff-109">要刪除的第一個顯示清單的整數名稱。</span><span class="sxs-lookup"><span data-stu-id="8ceff-109">The integer name of the first display list to delete.</span></span>

</dd> <dt>

<span data-ttu-id="8ceff-110">*range*</span><span class="sxs-lookup"><span data-stu-id="8ceff-110">*range*</span></span> 
</dt> <dd>

<span data-ttu-id="8ceff-111">要刪除的顯示清單數目。</span><span class="sxs-lookup"><span data-stu-id="8ceff-111">The number of display lists to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ceff-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ceff-112">Return value</span></span>

<span data-ttu-id="8ceff-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8ceff-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8ceff-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="8ceff-114">Error codes</span></span>

<span data-ttu-id="8ceff-115">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8ceff-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8ceff-116">Name</span><span class="sxs-lookup"><span data-stu-id="8ceff-116">Name</span></span>                                                                                                  | <span data-ttu-id="8ceff-117">意義</span><span class="sxs-lookup"><span data-stu-id="8ceff-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ceff-118"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="8ceff-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="8ceff-119">*範圍* 為負數。</span><span class="sxs-lookup"><span data-stu-id="8ceff-119">*range* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="8ceff-120"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="8ceff-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8ceff-121">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="8ceff-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8ceff-122">備註</span><span class="sxs-lookup"><span data-stu-id="8ceff-122">Remarks</span></span>

<span data-ttu-id="8ceff-123">**GlDeleteLists** 函式會刪除連續的顯示清單群組。</span><span class="sxs-lookup"><span data-stu-id="8ceff-123">The **glDeleteLists** function causes a contiguous group of display lists to be deleted.</span></span> <span data-ttu-id="8ceff-124">*清單* 參數是要刪除之第一個顯示清單的名稱，而 *範圍* 是要刪除的顯示清單數目。</span><span class="sxs-lookup"><span data-stu-id="8ceff-124">The *list* parameter is the name of the first display list to be deleted, and *range* is the number of display lists to delete.</span></span> <span data-ttu-id="8ceff-125">系統會刪除 *清單*  =  *d*  =  *清單*  +  *範圍*-1 的所有顯示清單 d。</span><span class="sxs-lookup"><span data-stu-id="8ceff-125">All display lists *d* with *list* = *d* = *list* + *range* - 1 are deleted.</span></span>

<span data-ttu-id="8ceff-126">配置給指定之顯示清單的所有儲存位置會釋出，且名稱可供稍後重複使用。</span><span class="sxs-lookup"><span data-stu-id="8ceff-126">All storage locations allocated to the specified display lists are freed, and the names are available for reuse at a later time.</span></span> <span data-ttu-id="8ceff-127">系統會忽略範圍內沒有相關聯顯示清單的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ceff-127">Names within the range that do not have an associated display list are ignored.</span></span> <span data-ttu-id="8ceff-128">如果 *範圍* 為零，則不會發生任何事。</span><span class="sxs-lookup"><span data-stu-id="8ceff-128">If *range* is zero, nothing happens.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ceff-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ceff-129">Requirements</span></span>



| <span data-ttu-id="8ceff-130">需求</span><span class="sxs-lookup"><span data-stu-id="8ceff-130">Requirement</span></span> | <span data-ttu-id="8ceff-131">值</span><span class="sxs-lookup"><span data-stu-id="8ceff-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ceff-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ceff-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8ceff-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ceff-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8ceff-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ceff-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8ceff-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ceff-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8ceff-136">標頭</span><span class="sxs-lookup"><span data-stu-id="8ceff-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ceff-137"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="8ceff-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8ceff-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="8ceff-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="8ceff-139"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ceff-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8ceff-140">DLL</span><span class="sxs-lookup"><span data-stu-id="8ceff-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ceff-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ceff-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ceff-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ceff-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ceff-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8ceff-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8ceff-144">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="8ceff-144">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="8ceff-145">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="8ceff-145">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="8ceff-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8ceff-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8ceff-147">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="8ceff-147">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="8ceff-148">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="8ceff-148">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="8ceff-149">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="8ceff-149">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





