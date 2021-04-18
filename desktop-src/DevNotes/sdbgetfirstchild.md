---
description: 在指定的父系內搜尋子標記，並傳回第一個子系的 TAGID。
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: SdbGetFirstChild 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: abc06ae0e4b5d842a968d0f3fbeb7a15702660b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510362"
---
# <a name="sdbgetfirstchild-function"></a><span data-ttu-id="08b9d-103">SdbGetFirstChild 函式</span><span class="sxs-lookup"><span data-stu-id="08b9d-103">SdbGetFirstChild function</span></span>

<span data-ttu-id="08b9d-104">在指定的父系內搜尋子標記，並傳回第一個子系的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="08b9d-104">Searches for a child TAG within the specified parent and returns the **TAGID** of the first child.</span></span>

## <a name="syntax"></a><span data-ttu-id="08b9d-105">語法</span><span class="sxs-lookup"><span data-stu-id="08b9d-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
);
```



## <a name="parameters"></a><span data-ttu-id="08b9d-106">參數</span><span class="sxs-lookup"><span data-stu-id="08b9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08b9d-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="08b9d-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08b9d-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="08b9d-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="08b9d-109">*tiParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="08b9d-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08b9d-110">搜尋的 **TAGID** 開始。</span><span class="sxs-lookup"><span data-stu-id="08b9d-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="08b9d-111">此參數可以是 **TAGID \_ 根** 或 **標記 \_ 類型 \_ 清單**。</span><span class="sxs-lookup"><span data-stu-id="08b9d-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08b9d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="08b9d-112">Return value</span></span>

<span data-ttu-id="08b9d-113">第一個子系或 **TAGID \_ Null** 的 **TAGID** ，找不到子系。</span><span class="sxs-lookup"><span data-stu-id="08b9d-113">The **TAGID** of the first child or **TAGID\_NULL** is no child is found.</span></span>

## <a name="requirements"></a><span data-ttu-id="08b9d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="08b9d-114">Requirements</span></span>



| <span data-ttu-id="08b9d-115">需求</span><span class="sxs-lookup"><span data-stu-id="08b9d-115">Requirement</span></span> | <span data-ttu-id="08b9d-116">值</span><span class="sxs-lookup"><span data-stu-id="08b9d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08b9d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="08b9d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="08b9d-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08b9d-118">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="08b9d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="08b9d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="08b9d-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08b9d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="08b9d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="08b9d-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08b9d-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08b9d-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08b9d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08b9d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08b9d-124">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="08b9d-124">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="08b9d-125">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="08b9d-125">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="08b9d-126">**SdbGetNextChild**</span><span class="sxs-lookup"><span data-stu-id="08b9d-126">**SdbGetNextChild**</span></span>](sdbgetnextchild.md)
</dt> </dl>

 

 




