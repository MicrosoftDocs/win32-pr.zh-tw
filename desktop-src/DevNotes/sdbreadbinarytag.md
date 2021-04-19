---
Description: 抓取指定之 TAGID 的二進位資料。
ms.assetid: b349f2af-2505-4efc-bd59-203f7666ce61
title: SdbReadBinaryTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 024b432c3210b98721a0cf3058bad0f765287fde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967334"
---
# <a name="sdbreadbinarytag-function"></a><span data-ttu-id="af435-103">SdbReadBinaryTag 函式</span><span class="sxs-lookup"><span data-stu-id="af435-103">SdbReadBinaryTag function</span></span>

<span data-ttu-id="af435-104">抓取指定之 **TAGID** 的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="af435-104">Retrieves the binary data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="af435-105">語法</span><span class="sxs-lookup"><span data-stu-id="af435-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadBinaryTag(
  _In_  PDB   pdb,
  _In_  TAGID tiWhich,
  _Out_ PBYTE pBuffer,
  _In_  DWORD dwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="af435-106">參數</span><span class="sxs-lookup"><span data-stu-id="af435-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af435-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af435-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af435-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="af435-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="af435-109">*tiWhich* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af435-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af435-110">對應至要抓取之資料的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="af435-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="af435-111">*pBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="af435-111">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af435-112">接收二進位資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="af435-112">The buffer that receives the binary data.</span></span> <span data-ttu-id="af435-113">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="af435-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="af435-114">*dwBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af435-114">*dwBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af435-115">*PBuffer* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="af435-115">The size of the *pBuffer* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af435-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="af435-116">Return value</span></span>

<span data-ttu-id="af435-117">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="af435-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="af435-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="af435-118">Requirements</span></span>



| <span data-ttu-id="af435-119">需求</span><span class="sxs-lookup"><span data-stu-id="af435-119">Requirement</span></span> | <span data-ttu-id="af435-120">值</span><span class="sxs-lookup"><span data-stu-id="af435-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af435-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af435-121">Minimum supported client</span></span><br/> | <span data-ttu-id="af435-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af435-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="af435-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af435-123">Minimum supported server</span></span><br/> | <span data-ttu-id="af435-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af435-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="af435-125">DLL</span><span class="sxs-lookup"><span data-stu-id="af435-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af435-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af435-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af435-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af435-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af435-128">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="af435-128">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="af435-129">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="af435-129">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="af435-130">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="af435-130">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="af435-131">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="af435-131">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




