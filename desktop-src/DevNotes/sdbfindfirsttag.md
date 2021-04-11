---
description: 在指定的父系內搜尋標記相符，並傳回第一個相符項的 TAGID。
ms.assetid: ecbe216c-1e46-4472-b1d1-e2ac7ace82ab
title: SdbFindFirstTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: dc8b752d536be83d90ded55474166d14521f0f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936029"
---
# <a name="sdbfindfirsttag-function"></a><span data-ttu-id="cdfa9-103">SdbFindFirstTag 函式</span><span class="sxs-lookup"><span data-stu-id="cdfa9-103">SdbFindFirstTag function</span></span>

<span data-ttu-id="cdfa9-104">在指定的父系內搜尋標記相符，並傳回第一個相符項的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="cdfa9-104">Searches for a TAG match within the specified parent and returns the **TAGID** of the first match.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdfa9-105">語法</span><span class="sxs-lookup"><span data-stu-id="cdfa9-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindFirstTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAG   tTag
);
```



## <a name="parameters"></a><span data-ttu-id="cdfa9-106">參數</span><span class="sxs-lookup"><span data-stu-id="cdfa9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdfa9-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdfa9-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdfa9-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cdfa9-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="cdfa9-109">*tiParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdfa9-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdfa9-110">搜尋的 **TAGID** 開始。</span><span class="sxs-lookup"><span data-stu-id="cdfa9-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="cdfa9-111">此參數可以是 **TAGID \_ 根** 或 **標記 \_ 類型 \_ 清單**。</span><span class="sxs-lookup"><span data-stu-id="cdfa9-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="cdfa9-112">*tTag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdfa9-112">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdfa9-113">要比對的標記。</span><span class="sxs-lookup"><span data-stu-id="cdfa9-113">The TAG to be matched.</span></span> <span data-ttu-id="cdfa9-114">如需可能值的清單，請參閱 [標記](tag.md) 。</span><span class="sxs-lookup"><span data-stu-id="cdfa9-114">See [TAG](tag.md) for a list of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdfa9-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="cdfa9-115">Return value</span></span>

<span data-ttu-id="cdfa9-116">第一個相符項的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="cdfa9-116">The **TAGID** of the first match.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdfa9-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdfa9-117">Requirements</span></span>



| <span data-ttu-id="cdfa9-118">需求</span><span class="sxs-lookup"><span data-stu-id="cdfa9-118">Requirement</span></span> | <span data-ttu-id="cdfa9-119">值</span><span class="sxs-lookup"><span data-stu-id="cdfa9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdfa9-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cdfa9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cdfa9-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdfa9-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cdfa9-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cdfa9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cdfa9-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdfa9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cdfa9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cdfa9-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdfa9-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdfa9-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdfa9-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdfa9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdfa9-127">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="cdfa9-127">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="cdfa9-128">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="cdfa9-128">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




