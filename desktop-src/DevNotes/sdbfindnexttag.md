---
description: 在指定的父系內搜尋下一個標記相符，並傳回相符的 TAGID。
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: SdbFindNextTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a5baf728a75e4c02c20ed4207b7d6b9a968af1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847178"
---
# <a name="sdbfindnexttag-function"></a><span data-ttu-id="285ff-103">SdbFindNextTag 函式</span><span class="sxs-lookup"><span data-stu-id="285ff-103">SdbFindNextTag function</span></span>

<span data-ttu-id="285ff-104">在指定的父系內搜尋下一個標記相符，並傳回相符的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="285ff-104">Searches for the next TAG match within the specified parent and returns the **TAGID** of the match.</span></span>

## <a name="syntax"></a><span data-ttu-id="285ff-105">語法</span><span class="sxs-lookup"><span data-stu-id="285ff-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindNextTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a><span data-ttu-id="285ff-106">參數</span><span class="sxs-lookup"><span data-stu-id="285ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="285ff-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="285ff-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="285ff-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="285ff-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="285ff-109">*tiParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="285ff-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="285ff-110">搜尋的 **TAGID** 開始。</span><span class="sxs-lookup"><span data-stu-id="285ff-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="285ff-111">此參數可以是 **TAGID \_ 根** 或 **標記 \_ 類型 \_ 清單**。</span><span class="sxs-lookup"><span data-stu-id="285ff-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="285ff-112">*tiPrev* \[在\]</span><span class="sxs-lookup"><span data-stu-id="285ff-112">*tiPrev* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="285ff-113">上一個相符項的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="285ff-113">The **TAGID** of the previous match.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="285ff-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="285ff-114">Return value</span></span>

<span data-ttu-id="285ff-115">相符的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="285ff-115">The **TAGID** of the match.</span></span>

## <a name="remarks"></a><span data-ttu-id="285ff-116">備註</span><span class="sxs-lookup"><span data-stu-id="285ff-116">Remarks</span></span>

<span data-ttu-id="285ff-117">呼叫此函式之前，請先呼叫 [**SdbFindFirstTag**](sdbfindfirsttag.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="285ff-117">Before calling this function, call the [**SdbFindFirstTag**](sdbfindfirsttag.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="285ff-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="285ff-118">Requirements</span></span>



| <span data-ttu-id="285ff-119">需求</span><span class="sxs-lookup"><span data-stu-id="285ff-119">Requirement</span></span> | <span data-ttu-id="285ff-120">值</span><span class="sxs-lookup"><span data-stu-id="285ff-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="285ff-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="285ff-121">Minimum supported client</span></span><br/> | <span data-ttu-id="285ff-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="285ff-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="285ff-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="285ff-123">Minimum supported server</span></span><br/> | <span data-ttu-id="285ff-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="285ff-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="285ff-125">DLL</span><span class="sxs-lookup"><span data-stu-id="285ff-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="285ff-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="285ff-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="285ff-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="285ff-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="285ff-128">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="285ff-128">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="285ff-129">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="285ff-129">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




