---
description: 將文字值寫入至指定的資料庫。
ms.assetid: 8f921e14-4a82-4d8e-83fa-beb78118ecb8
title: SdbWriteWORDTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75a5b3eb430901de36d5aca325f928aae266bc39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510490"
---
# <a name="sdbwritewordtag-function"></a><span data-ttu-id="381d0-103">SdbWriteWORDTag 函式</span><span class="sxs-lookup"><span data-stu-id="381d0-103">SdbWriteWORDTag function</span></span>

<span data-ttu-id="381d0-104">將 **文字** 值寫入至指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="381d0-104">Writes a **WORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="381d0-105">語法</span><span class="sxs-lookup"><span data-stu-id="381d0-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteWORDTag(
  _In_ PDB  pdb,
  _In_ TAG  tTag,
  _In_ WORD wData
);
```



## <a name="parameters"></a><span data-ttu-id="381d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="381d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="381d0-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="381d0-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="381d0-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="381d0-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="381d0-109">*tTag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="381d0-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="381d0-110">專案的標記。</span><span class="sxs-lookup"><span data-stu-id="381d0-110">The TAG for the entry.</span></span> <span data-ttu-id="381d0-111">這個標記必須是類型 **標記 \_ 類型 \_ WORD**。</span><span class="sxs-lookup"><span data-stu-id="381d0-111">This TAG must be of type **TAG\_TYPE\_WORD**.</span></span>

</dd> <dt>

<span data-ttu-id="381d0-112">*wData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="381d0-112">*wData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="381d0-113">數值。</span><span class="sxs-lookup"><span data-stu-id="381d0-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="381d0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="381d0-114">Return value</span></span>

<span data-ttu-id="381d0-115">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="381d0-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="381d0-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="381d0-116">Requirements</span></span>



| <span data-ttu-id="381d0-117">需求</span><span class="sxs-lookup"><span data-stu-id="381d0-117">Requirement</span></span> | <span data-ttu-id="381d0-118">值</span><span class="sxs-lookup"><span data-stu-id="381d0-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="381d0-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="381d0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="381d0-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="381d0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="381d0-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="381d0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="381d0-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="381d0-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="381d0-123">DLL</span><span class="sxs-lookup"><span data-stu-id="381d0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="381d0-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="381d0-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="381d0-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="381d0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="381d0-126">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="381d0-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="381d0-127">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="381d0-127">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="381d0-128">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="381d0-128">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="381d0-129">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="381d0-129">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> </dl>

 

 




