---
description: 在指定的資料庫中宣告新的索引。
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: SdbDeclareIndex 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbDeclareIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 68004a29d01288a2e1d177b8a33df32b919e73ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971325"
---
# <a name="sdbdeclareindex-function"></a><span data-ttu-id="887eb-103">SdbDeclareIndex 函式</span><span class="sxs-lookup"><span data-stu-id="887eb-103">SdbDeclareIndex function</span></span>

<span data-ttu-id="887eb-104">在指定的資料庫中宣告新的索引。</span><span class="sxs-lookup"><span data-stu-id="887eb-104">Declares a new index in the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="887eb-105">語法</span><span class="sxs-lookup"><span data-stu-id="887eb-105">Syntax</span></span>


```C++
BOOL WINAPI SdbDeclareIndex(
  _In_  PDB     pdb,
  _In_  TAG     tWhich,
  _In_  TAG     tKey,
  _In_  DWORD   dwEntries,
  _In_  BOOL    bUniqueKey,
  _Out_ INDEXID *piiIndex
);
```



## <a name="parameters"></a><span data-ttu-id="887eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="887eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="887eb-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="887eb-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887eb-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="887eb-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="887eb-109">*tWhich* \[在\]</span><span class="sxs-lookup"><span data-stu-id="887eb-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887eb-110">此參數必須是 **標記 \_ 類型 \_ 清單**。</span><span class="sxs-lookup"><span data-stu-id="887eb-110">This parameter must be **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="887eb-111">*tKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="887eb-111">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887eb-112">指定要做為索引鍵之類型的標記。</span><span class="sxs-lookup"><span data-stu-id="887eb-112">The TAG that specifies the type to be used as the key.</span></span> <span data-ttu-id="887eb-113">此參數不可以是 **標記 \_ 類型 \_ 清單**。</span><span class="sxs-lookup"><span data-stu-id="887eb-113">This parameter cannot be **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="887eb-114">*dwEntries* \[在\]</span><span class="sxs-lookup"><span data-stu-id="887eb-114">*dwEntries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887eb-115">要在索引中配置的專案數目。</span><span class="sxs-lookup"><span data-stu-id="887eb-115">The number of entries to allocate in the index.</span></span>

</dd> <dt>

<span data-ttu-id="887eb-116">*bUniqueKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="887eb-116">*bUniqueKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887eb-117">如果此參數為 **TRUE**，則索引是唯一索引鍵索引。</span><span class="sxs-lookup"><span data-stu-id="887eb-117">If this parameter is **TRUE**, the index is a unique-key index.</span></span>

</dd> <dt>

<span data-ttu-id="887eb-118">*piiIndex* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="887eb-118">*piiIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="887eb-119">新宣告索引的結果 **INDEXID** 。</span><span class="sxs-lookup"><span data-stu-id="887eb-119">The resulting **INDEXID** of the newly declared index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="887eb-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="887eb-120">Return value</span></span>

<span data-ttu-id="887eb-121">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="887eb-121">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="887eb-122">備註</span><span class="sxs-lookup"><span data-stu-id="887eb-122">Remarks</span></span>

<span data-ttu-id="887eb-123">將標記寫入新的索引之前，請先呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="887eb-123">Call this function before writing tags to the new index.</span></span>

## <a name="requirements"></a><span data-ttu-id="887eb-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="887eb-124">Requirements</span></span>



| <span data-ttu-id="887eb-125">需求</span><span class="sxs-lookup"><span data-stu-id="887eb-125">Requirement</span></span> | <span data-ttu-id="887eb-126">值</span><span class="sxs-lookup"><span data-stu-id="887eb-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="887eb-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="887eb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="887eb-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="887eb-128">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="887eb-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="887eb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="887eb-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="887eb-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="887eb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="887eb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="887eb-132"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="887eb-132"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="887eb-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="887eb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="887eb-134">**INDEXID**</span><span class="sxs-lookup"><span data-stu-id="887eb-134">**INDEXID**</span></span>](indexid.md)
</dt> <dt>

[<span data-ttu-id="887eb-135">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="887eb-135">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="887eb-136">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="887eb-136">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="887eb-137">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="887eb-137">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




