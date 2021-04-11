---
description: 深入瞭解： JetGetVersion 函數
title: JetGetVersion 函式
TOCTitle: JetGetVersion Function
ms:assetid: f25c3639-ae2b-4357-9947-563ef3df72c6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294133(v=EXCHG.10)
ms:contentKeyID: 32765747
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetVersion
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38128358d814ea85cf087c270a65a3fada976e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194877"
---
# <a name="jetgetversion-function"></a><span data-ttu-id="4b4cf-103">JetGetVersion 函式</span><span class="sxs-lookup"><span data-stu-id="4b4cf-103">JetGetVersion Function</span></span>


<span data-ttu-id="4b4cf-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4b4cf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetversion-function"></a><span data-ttu-id="4b4cf-105">JetGetVersion 函式</span><span class="sxs-lookup"><span data-stu-id="4b4cf-105">JetGetVersion Function</span></span>

<span data-ttu-id="4b4cf-106">**JetGetVersion** 函數會抓取資料庫引擎的版本。</span><span class="sxs-lookup"><span data-stu-id="4b4cf-106">The **JetGetVersion** function retrieves the version of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetGetVersion(
      __in          JET_SESID sesid,
      __out         unsigned long* pwVersion
    );
```

### <a name="parameters"></a><span data-ttu-id="4b4cf-107">參數</span><span class="sxs-lookup"><span data-stu-id="4b4cf-107">Parameters</span></span>

<span data-ttu-id="4b4cf-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="4b4cf-108">*sesid*</span></span>

<span data-ttu-id="4b4cf-109">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="4b4cf-109">The session to use for this call.</span></span>

<span data-ttu-id="4b4cf-110">*pwVersion*</span><span class="sxs-lookup"><span data-stu-id="4b4cf-110">*pwVersion*</span></span>

<span data-ttu-id="4b4cf-111">資料庫引擎版本號碼的指標。</span><span class="sxs-lookup"><span data-stu-id="4b4cf-111">A pointer to the version number of the database engine.</span></span>

### <a name="return-value"></a><span data-ttu-id="4b4cf-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b4cf-112">Return Value</span></span>

<span data-ttu-id="4b4cf-113">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="4b4cf-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4b4cf-114">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="4b4cf-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b4cf-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4b4cf-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="4b4cf-116">Description</span><span class="sxs-lookup"><span data-stu-id="4b4cf-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b4cf-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4b4cf-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4b4cf-118">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="4b4cf-118">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4b4cf-119">如果此函式成功，則會取出資料庫引擎的版本。</span><span class="sxs-lookup"><span data-stu-id="4b4cf-119">If this function succeeds, the version of the database engine is retrieved.</span></span>

<span data-ttu-id="4b4cf-120">沒有已知的失敗模式。</span><span class="sxs-lookup"><span data-stu-id="4b4cf-120">There are no known failure modes.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4b4cf-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b4cf-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b4cf-122"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="4b4cf-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4b4cf-123">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="4b4cf-123">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b4cf-124"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="4b4cf-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4b4cf-125">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="4b4cf-125">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b4cf-126"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="4b4cf-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4b4cf-127">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="4b4cf-127">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b4cf-128"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="4b4cf-128"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4b4cf-129">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="4b4cf-129">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b4cf-130"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4b4cf-130"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4b4cf-131">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="4b4cf-131">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4b4cf-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b4cf-132">See Also</span></span>

[<span data-ttu-id="4b4cf-133">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="4b4cf-133">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="4b4cf-134">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="4b4cf-134">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="4b4cf-135">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4b4cf-135">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4b4cf-136">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4b4cf-136">JET_SESID</span></span>](./jet-sesid.md)
