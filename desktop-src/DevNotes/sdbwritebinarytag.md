---
description: 將二進位資料寫入至指定的資料庫。
ms.assetid: 935321b8-904e-46be-ad11-77d89670a072
title: SdbWriteBinaryTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e79de8549eb4c0a0f1b8a914c59d21ccfb3bcf7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510492"
---
# <a name="sdbwritebinarytag-function"></a><span data-ttu-id="4a772-103">SdbWriteBinaryTag 函式</span><span class="sxs-lookup"><span data-stu-id="4a772-103">SdbWriteBinaryTag function</span></span>

<span data-ttu-id="4a772-104">將二進位資料寫入至指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4a772-104">Writes binary data to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a772-105">語法</span><span class="sxs-lookup"><span data-stu-id="4a772-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteBinaryTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ PBYTE pBuffer,
  _In_ DWORD dwSize
);
```



## <a name="parameters"></a><span data-ttu-id="4a772-106">參數</span><span class="sxs-lookup"><span data-stu-id="4a772-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a772-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4a772-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a772-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4a772-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="4a772-109">*tTag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4a772-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a772-110">專案的標記。</span><span class="sxs-lookup"><span data-stu-id="4a772-110">The TAG for the entry.</span></span> <span data-ttu-id="4a772-111">這個標記必須是 **標記 \_ 類型 \_ BINARY** 類型。</span><span class="sxs-lookup"><span data-stu-id="4a772-111">This TAG must be of type **TAG\_TYPE\_BINARY**.</span></span>

</dd> <dt>

<span data-ttu-id="4a772-112">*pBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4a772-112">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a772-113">包含資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4a772-113">The buffer that contains the data.</span></span> <span data-ttu-id="4a772-114">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4a772-114">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4a772-115">*dwSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4a772-115">*dwSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a772-116">*PBuffer* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4a772-116">The size of the *pBuffer* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a772-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a772-117">Return value</span></span>

<span data-ttu-id="4a772-118">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="4a772-118">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a772-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a772-119">Requirements</span></span>



| <span data-ttu-id="4a772-120">需求</span><span class="sxs-lookup"><span data-stu-id="4a772-120">Requirement</span></span> | <span data-ttu-id="4a772-121">值</span><span class="sxs-lookup"><span data-stu-id="4a772-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a772-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a772-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4a772-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a772-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4a772-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a772-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4a772-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a772-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4a772-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4a772-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a772-127"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a772-127"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a772-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a772-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a772-129">**SdbWriteBinaryTagFromFile**</span><span class="sxs-lookup"><span data-stu-id="4a772-129">**SdbWriteBinaryTagFromFile**</span></span>](sdbwritebinarytagfromfile.md)
</dt> <dt>

[<span data-ttu-id="4a772-130">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="4a772-130">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="4a772-131">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="4a772-131">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="4a772-132">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="4a772-132">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="4a772-133">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="4a772-133">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




