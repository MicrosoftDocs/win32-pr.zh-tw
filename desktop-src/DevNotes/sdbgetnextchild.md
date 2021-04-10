---
description: 搜尋指定父系內的下一個子標記，並傳回下一個子系的 TAGID。
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: SdbGetNextChild 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f2943eaf0baec84a9473b679743b9eafad3b7fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847256"
---
# <a name="sdbgetnextchild-function"></a><span data-ttu-id="8f9c2-103">SdbGetNextChild 函式</span><span class="sxs-lookup"><span data-stu-id="8f9c2-103">SdbGetNextChild function</span></span>

<span data-ttu-id="8f9c2-104">搜尋指定父系內的下一個子標記，並傳回下一個子系的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="8f9c2-104">Searches for the next child TAG within the specified parent and returns the **TAGID** of the next child.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f9c2-105">語法</span><span class="sxs-lookup"><span data-stu-id="8f9c2-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetNextChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a><span data-ttu-id="8f9c2-106">參數</span><span class="sxs-lookup"><span data-stu-id="8f9c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f9c2-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f9c2-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9c2-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8f9c2-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="8f9c2-109">*tiParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f9c2-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9c2-110">搜尋的 **TAGID** 開始。</span><span class="sxs-lookup"><span data-stu-id="8f9c2-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="8f9c2-111">此參數可以是 **TAGID \_ 根** 或 **標記 \_ 類型 \_ 清單**。</span><span class="sxs-lookup"><span data-stu-id="8f9c2-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="8f9c2-112">*tiPrev* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f9c2-112">*tiPrev* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9c2-113">上一個子系的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="8f9c2-113">The **TAGID** of the previous child.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f9c2-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f9c2-114">Return value</span></span>

<span data-ttu-id="8f9c2-115">如果找不到子系，則為子系的 **TAGID** 或 **TAGID \_ Null** 。</span><span class="sxs-lookup"><span data-stu-id="8f9c2-115">The **TAGID** of the child or **TAGID\_NULL** if no child is found.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f9c2-116">備註</span><span class="sxs-lookup"><span data-stu-id="8f9c2-116">Remarks</span></span>

<span data-ttu-id="8f9c2-117">呼叫此函式之前，請先呼叫 [**SdbGetFirstChild**](sdbgetfirstchild.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="8f9c2-117">Before calling this function, call the [**SdbGetFirstChild**](sdbgetfirstchild.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f9c2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f9c2-118">Requirements</span></span>



| <span data-ttu-id="8f9c2-119">需求</span><span class="sxs-lookup"><span data-stu-id="8f9c2-119">Requirement</span></span> | <span data-ttu-id="8f9c2-120">值</span><span class="sxs-lookup"><span data-stu-id="8f9c2-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9c2-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f9c2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8f9c2-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f9c2-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8f9c2-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f9c2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8f9c2-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f9c2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8f9c2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8f9c2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f9c2-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f9c2-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f9c2-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f9c2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f9c2-128">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="8f9c2-128">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="8f9c2-129">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="8f9c2-129">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="8f9c2-130">**SdbGetFirstChild**</span><span class="sxs-lookup"><span data-stu-id="8f9c2-130">**SdbGetFirstChild**</span></span>](sdbgetfirstchild.md)
</dt> </dl>

 

 




