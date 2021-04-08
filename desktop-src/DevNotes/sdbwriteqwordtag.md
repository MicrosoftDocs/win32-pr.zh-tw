---
description: 將 QWORD 值寫入至指定的資料庫。
ms.assetid: 8ce566ea-a941-45fa-b031-26c3144ca02c
title: SdbWriteQWORDTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 58dcaad3487bb1f59a75dd6a671ecb43c9cf1751
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688723"
---
# <a name="sdbwriteqwordtag-function"></a><span data-ttu-id="3f193-103">SdbWriteQWORDTag 函式</span><span class="sxs-lookup"><span data-stu-id="3f193-103">SdbWriteQWORDTag function</span></span>

<span data-ttu-id="3f193-104">將 **QWORD** 值寫入至指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="3f193-104">Writes a **QWORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f193-105">語法</span><span class="sxs-lookup"><span data-stu-id="3f193-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteQWORDTag(
  _In_ PDB       pdb,
  _In_ TAG       tTag,
  _In_ ULONGLONG qwData
);
```



## <a name="parameters"></a><span data-ttu-id="3f193-106">參數</span><span class="sxs-lookup"><span data-stu-id="3f193-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f193-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3f193-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f193-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3f193-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="3f193-109">*tTag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3f193-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f193-110">專案的標記。</span><span class="sxs-lookup"><span data-stu-id="3f193-110">The TAG for the entry.</span></span> <span data-ttu-id="3f193-111">這個標記必須是類型為 **\_ \_ QWORD 的標記類型**。</span><span class="sxs-lookup"><span data-stu-id="3f193-111">This TAG must be of type **TAG\_TYPE\_QWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="3f193-112">*qwData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3f193-112">*qwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f193-113">數值。</span><span class="sxs-lookup"><span data-stu-id="3f193-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f193-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3f193-114">Return value</span></span>

<span data-ttu-id="3f193-115">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3f193-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f193-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f193-116">Requirements</span></span>



| <span data-ttu-id="3f193-117">需求</span><span class="sxs-lookup"><span data-stu-id="3f193-117">Requirement</span></span> | <span data-ttu-id="3f193-118">值</span><span class="sxs-lookup"><span data-stu-id="3f193-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f193-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f193-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3f193-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f193-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3f193-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f193-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3f193-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f193-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3f193-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3f193-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f193-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f193-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f193-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f193-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f193-126">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="3f193-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="3f193-127">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3f193-127">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="3f193-128">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="3f193-128">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="3f193-129">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3f193-129">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




