---
description: 將字串寫入至指定的資料庫。
ms.assetid: 72c62d91-0c1c-4ff8-8829-1c3ec1fa8648
title: SdbWriteStringTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4ac588d99408d0d7f13bc0fd13d8abe8a6580e69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847175"
---
# <a name="sdbwritestringtag-function"></a><span data-ttu-id="01285-103">SdbWriteStringTag 函式</span><span class="sxs-lookup"><span data-stu-id="01285-103">SdbWriteStringTag function</span></span>

<span data-ttu-id="01285-104">將字串寫入至指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="01285-104">Writes a string to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="01285-105">語法</span><span class="sxs-lookup"><span data-stu-id="01285-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteStringTag(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszData
);
```



## <a name="parameters"></a><span data-ttu-id="01285-106">參數</span><span class="sxs-lookup"><span data-stu-id="01285-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01285-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01285-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01285-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="01285-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="01285-109">*tTag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01285-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01285-110">專案的標記。</span><span class="sxs-lookup"><span data-stu-id="01285-110">The TAG for the entry.</span></span> <span data-ttu-id="01285-111">此標記的類型必須是 **標記 \_ 類型 \_ STRINGREF**。</span><span class="sxs-lookup"><span data-stu-id="01285-111">This TAG must be of type **TAG\_TYPE\_STRINGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="01285-112">*pwszData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01285-112">*pwszData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01285-113">以 null 結束的字串。</span><span class="sxs-lookup"><span data-stu-id="01285-113">The null-terminated string.</span></span> <span data-ttu-id="01285-114">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="01285-114">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01285-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="01285-115">Return value</span></span>

<span data-ttu-id="01285-116">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="01285-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="01285-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="01285-117">Requirements</span></span>



| <span data-ttu-id="01285-118">需求</span><span class="sxs-lookup"><span data-stu-id="01285-118">Requirement</span></span> | <span data-ttu-id="01285-119">值</span><span class="sxs-lookup"><span data-stu-id="01285-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01285-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01285-120">Minimum supported client</span></span><br/> | <span data-ttu-id="01285-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01285-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="01285-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01285-122">Minimum supported server</span></span><br/> | <span data-ttu-id="01285-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01285-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="01285-124">DLL</span><span class="sxs-lookup"><span data-stu-id="01285-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01285-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01285-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01285-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01285-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01285-127">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="01285-127">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="01285-128">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="01285-128">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="01285-129">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="01285-129">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="01285-130">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="01285-130">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




