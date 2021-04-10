---
description: 將 Null 專案寫入至指定的資料庫。
ms.assetid: 2a29389b-d4f6-4527-a429-c9459b095f2f
title: SdbWriteNullTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteNULLTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 662d5c4db31f199df8b3b9f7368aba118ea6e8fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187664"
---
# <a name="sdbwritenulltag-function"></a><span data-ttu-id="05699-103">SdbWriteNullTag 函式</span><span class="sxs-lookup"><span data-stu-id="05699-103">SdbWriteNULLTag function</span></span>

<span data-ttu-id="05699-104">將 **Null** 專案寫入至指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="05699-104">Writes a **NULL** entry to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="05699-105">語法</span><span class="sxs-lookup"><span data-stu-id="05699-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteNULLTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a><span data-ttu-id="05699-106">參數</span><span class="sxs-lookup"><span data-stu-id="05699-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05699-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05699-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05699-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="05699-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="05699-109">*tTag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05699-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05699-110">專案的標記。</span><span class="sxs-lookup"><span data-stu-id="05699-110">The TAG for the entry.</span></span> <span data-ttu-id="05699-111">這個標記必須是類型 **標記 \_ 類型 \_ Null**。</span><span class="sxs-lookup"><span data-stu-id="05699-111">This TAG must be of type **TAG\_TYPE\_NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05699-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="05699-112">Return value</span></span>

<span data-ttu-id="05699-113">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="05699-113">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="05699-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="05699-114">Requirements</span></span>



| <span data-ttu-id="05699-115">需求</span><span class="sxs-lookup"><span data-stu-id="05699-115">Requirement</span></span> | <span data-ttu-id="05699-116">值</span><span class="sxs-lookup"><span data-stu-id="05699-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05699-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05699-117">Minimum supported client</span></span><br/> | <span data-ttu-id="05699-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05699-118">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="05699-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05699-119">Minimum supported server</span></span><br/> | <span data-ttu-id="05699-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05699-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="05699-121">DLL</span><span class="sxs-lookup"><span data-stu-id="05699-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05699-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05699-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05699-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05699-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05699-124">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="05699-124">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="05699-125">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="05699-125">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="05699-126">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="05699-126">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="05699-127">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="05699-127">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




