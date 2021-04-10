---
description: 將 DWORD 值寫入至指定的資料庫。
ms.assetid: 2ecbfcac-5bb1-4129-9501-79210672aa1b
title: SdbWriteDWORDTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5b549a91037aa308b5b88d0e3e2a51e153002bd5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187665"
---
# <a name="sdbwritedwordtag-function"></a><span data-ttu-id="6825d-103">SdbWriteDWORDTag 函式</span><span class="sxs-lookup"><span data-stu-id="6825d-103">SdbWriteDWORDTag function</span></span>

<span data-ttu-id="6825d-104">將 **DWORD** 值寫入至指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="6825d-104">Writes a **DWORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="6825d-105">語法</span><span class="sxs-lookup"><span data-stu-id="6825d-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteDWORDTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ DWORD dwData
);
```



## <a name="parameters"></a><span data-ttu-id="6825d-106">參數</span><span class="sxs-lookup"><span data-stu-id="6825d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6825d-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6825d-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6825d-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6825d-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="6825d-109">*tTag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6825d-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6825d-110">專案的標記。</span><span class="sxs-lookup"><span data-stu-id="6825d-110">The TAG for the entry.</span></span> <span data-ttu-id="6825d-111">這個標記必須是類型 **標記 \_ 類型 \_ DWORD**。</span><span class="sxs-lookup"><span data-stu-id="6825d-111">This TAG must be of type **TAG\_TYPE\_DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="6825d-112">*dwData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6825d-112">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6825d-113">數值。</span><span class="sxs-lookup"><span data-stu-id="6825d-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6825d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6825d-114">Return value</span></span>

<span data-ttu-id="6825d-115">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="6825d-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6825d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6825d-116">Requirements</span></span>



| <span data-ttu-id="6825d-117">需求</span><span class="sxs-lookup"><span data-stu-id="6825d-117">Requirement</span></span> | <span data-ttu-id="6825d-118">值</span><span class="sxs-lookup"><span data-stu-id="6825d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6825d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6825d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6825d-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6825d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6825d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6825d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6825d-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6825d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6825d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6825d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6825d-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6825d-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6825d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6825d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6825d-126">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="6825d-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="6825d-127">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="6825d-127">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="6825d-128">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="6825d-128">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="6825d-129">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="6825d-129">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




