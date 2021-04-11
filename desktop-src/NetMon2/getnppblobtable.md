---
description: GetNPPBlobTable 函式會抓取代表本機電腦上註冊 Nic 的 NPP BLOB 資料表。
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: 'GetNPPBlobTable 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 883493215aaac0fa2568baec69232b379b8aa808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850151"
---
# <a name="getnppblobtable-function"></a><span data-ttu-id="05c43-103">GetNPPBlobTable 函式</span><span class="sxs-lookup"><span data-stu-id="05c43-103">GetNPPBlobTable function</span></span>

<span data-ttu-id="05c43-104">**GetNPPBlobTable** 函式會抓取代表本機電腦上註冊 NIC 的 NPP BLOB 資料表。</span><span class="sxs-lookup"><span data-stu-id="05c43-104">The **GetNPPBlobTable** function retrieves an NPP BLOB table that represents the register NICs on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="05c43-105">語法</span><span class="sxs-lookup"><span data-stu-id="05c43-105">Syntax</span></span>


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a><span data-ttu-id="05c43-106">參數</span><span class="sxs-lookup"><span data-stu-id="05c43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05c43-107">*hFilterBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05c43-107">*hFilterBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05c43-108">篩選 BLOB 的控制碼，限制在資料表中傳回的 NPP Blob。</span><span class="sxs-lookup"><span data-stu-id="05c43-108">Handle to a filter BLOB that limits the NPP BLOBs returned in the table.</span></span>

</dd> <dt>

<span data-ttu-id="05c43-109">*ppBlobTable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="05c43-109">*ppBlobTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05c43-110">[Blob \_ 資料表](blob-table.md)結構的指標，其中包含至少一個 blob 指標。</span><span class="sxs-lookup"><span data-stu-id="05c43-110">Pointer to a [BLOB\_TABLE](blob-table.md) structure that contains at least one BLOB pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05c43-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="05c43-111">Return value</span></span>

<span data-ttu-id="05c43-112">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="05c43-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="05c43-113">如果函式不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="05c43-113">If the function is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="05c43-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="05c43-114">Return code</span></span>                                                                                                | <span data-ttu-id="05c43-115">Description</span><span class="sxs-lookup"><span data-stu-id="05c43-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05c43-116"><dt>**NMERR \_ NO \_ NPP \_ DLL**</dt></span><span class="sxs-lookup"><span data-stu-id="05c43-116"><dt>**NMERR\_NO\_NPP\_DLL**</dt></span></span> </dl>         | <span data-ttu-id="05c43-117">在 NPP 目錄中找不到任何 Dll。</span><span class="sxs-lookup"><span data-stu-id="05c43-117">No DLLs were found in the NPP directory.</span></span><br/>                    |
| <dl> <span data-ttu-id="05c43-118"><dt>**NMERR \_ 沒有 \_ 有效的 \_ NPP \_ DLL**</dt></span><span class="sxs-lookup"><span data-stu-id="05c43-118"><dt>**NMERR\_NO\_VALID\_NPP\_DLLS**</dt></span></span> </dl> | <span data-ttu-id="05c43-119">NPP 目錄中的 Dll 都不是有效的 NPP Dll。</span><span class="sxs-lookup"><span data-stu-id="05c43-119">None of the DLLs in the NPP directory were valid NPP DLLs.</span></span><br/>  |
| <dl> <span data-ttu-id="05c43-120"><dt>**NMERR \_ 沒有 \_ 相符的 \_ NPPS**</dt></span><span class="sxs-lookup"><span data-stu-id="05c43-120"><dt>**NMERR\_NO\_MATCHING\_NPPS**</dt></span></span> </dl>   | <span data-ttu-id="05c43-121">探索到 NPP Blob，但未通過篩選測試。</span><span class="sxs-lookup"><span data-stu-id="05c43-121">NPP BLOBs were discovered, but none passed the filter test.</span></span><br/> |
| <dl> <span data-ttu-id="05c43-122"><dt>**NMERR \_ OUT \_ OF \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="05c43-122"><dt>**NMERR\_OUT\_OF\_MEMOR**</dt></span></span> </dl>       | <span data-ttu-id="05c43-123">網路監視器無法配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="05c43-123">Network Monitor was not able to allocate memory.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="05c43-124">備註</span><span class="sxs-lookup"><span data-stu-id="05c43-124">Remarks</span></span>

<span data-ttu-id="05c43-125">*HFilterBlob* 命名的 blob 也可以是特殊的 blob。</span><span class="sxs-lookup"><span data-stu-id="05c43-125">The BLOB named by *hFilterBlob* can also be a special BLOB.</span></span>

<span data-ttu-id="05c43-126">如果您將篩選 BLOB 中的旗標設定為 **TRUE**，則傳回的 blob 資料表也可以包含特殊 blob。</span><span class="sxs-lookup"><span data-stu-id="05c43-126">If you set the flag in the filter BLOB to **TRUE**, the returned BLOB table can also include special BLOBs .</span></span>

<span data-ttu-id="05c43-127">如果以 *hFilterBlob* 命名的 blob 是特殊 blob，網路監視器 UI 將會嘗試處理它。</span><span class="sxs-lookup"><span data-stu-id="05c43-127">If the BLOB named by *hFilterBlob* is a special BLOB, the Network Monitor UI will attempt to process it.</span></span> <span data-ttu-id="05c43-128">例如，假設先前的呼叫會從遠端 NPP 傳回特殊的 BLOB。</span><span class="sxs-lookup"><span data-stu-id="05c43-128">For example, suppose that a previous call returns a special BLOB from the remote NPP.</span></span> <span data-ttu-id="05c43-129">應用程式會插入必要的標記、電腦 \_ 名稱。</span><span class="sxs-lookup"><span data-stu-id="05c43-129">The application inserts the required tag, MACHINE\_NAME.</span></span> <span data-ttu-id="05c43-130">然後，搜尋工具會將此 BLOB 傳遞到遠端 NPP，然後傳回與電腦名稱稱相關聯的 NPP Blob 資料表。</span><span class="sxs-lookup"><span data-stu-id="05c43-130">The finder then passes this BLOB to the remote NPP, which then returns a table of the NPP BLOBs associated with the machine name.</span></span>

<span data-ttu-id="05c43-131">為了終結所有傳回的 Blob 和 BLOB 資料表，呼叫端會負責呼叫 **DestroyBlob** 函數。</span><span class="sxs-lookup"><span data-stu-id="05c43-131">To destroy all returned BLOBs and the BLOB table, the caller is responsible for calling the **DestroyBlob** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="05c43-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="05c43-132">Requirements</span></span>



| <span data-ttu-id="05c43-133">需求</span><span class="sxs-lookup"><span data-stu-id="05c43-133">Requirement</span></span> | <span data-ttu-id="05c43-134">值</span><span class="sxs-lookup"><span data-stu-id="05c43-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05c43-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05c43-135">Minimum supported client</span></span><br/> | <span data-ttu-id="05c43-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05c43-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="05c43-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05c43-137">Minimum supported server</span></span><br/> | <span data-ttu-id="05c43-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05c43-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="05c43-139">標頭</span><span class="sxs-lookup"><span data-stu-id="05c43-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="05c43-140"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="05c43-140"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="05c43-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="05c43-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="05c43-142"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="05c43-142"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="05c43-143">DLL</span><span class="sxs-lookup"><span data-stu-id="05c43-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05c43-144"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05c43-144"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




