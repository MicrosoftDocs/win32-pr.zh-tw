---
description: 深入瞭解： JET_ERR
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35120be9a26dcbdc8d012cd12c871ddcf8f71555
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106974901"
---
# <a name="jet_err"></a><span data-ttu-id="24467-103">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="24467-103">JET_ERR</span></span>


<span data-ttu-id="24467-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="24467-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_err"></a><span data-ttu-id="24467-105">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="24467-105">JET_ERR</span></span>

<span data-ttu-id="24467-106">**JET_ERR** 資料類型包含可延伸的 [儲存引擎錯誤碼](./extensible-storage-engine-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="24467-106">The **JET_ERR** data type contains an [Extensible Storage Engine error code](./extensible-storage-engine-error-codes.md).</span></span>

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a><span data-ttu-id="24467-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="24467-107">Data Types</span></span>

<span data-ttu-id="24467-108">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="24467-108">JET_ERR</span></span>

<span data-ttu-id="24467-109"> (對應至 JET_errSuccess 的零值) 表示呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="24467-109">A zero value (corresponding to JET_errSuccess) indicates that the call succeeded.</span></span> <span data-ttu-id="24467-110">正值會針對在其他成功呼叫期間發生的非嚴重狀況發出警告。</span><span class="sxs-lookup"><span data-stu-id="24467-110">A positive value warns of a non-fatal condition that occurred during an otherwise successful call.</span></span> <span data-ttu-id="24467-111">負數值表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="24467-111">A negative value indicates that the call failed.</span></span>

### <a name="remarks"></a><span data-ttu-id="24467-112">備註</span><span class="sxs-lookup"><span data-stu-id="24467-112">Remarks</span></span>

<span data-ttu-id="24467-113">如需以 Hresult 傳回錯誤的相關資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="24467-113">For information about returning errors as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span> <span data-ttu-id="24467-114">如需有關設定資料庫以處理錯誤之旗標的詳細資訊，請參閱 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="24467-114">For information about flags for configuring the database to handle errors, see [Error Handling Parameters](./error-handling-parameters.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="24467-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="24467-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24467-116"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="24467-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="24467-117">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="24467-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24467-118"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="24467-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="24467-119">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="24467-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24467-120"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="24467-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="24467-121">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="24467-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="24467-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24467-122">See Also</span></span>

[<span data-ttu-id="24467-123">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="24467-123">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="24467-124">可擴充儲存引擎錯誤碼</span><span class="sxs-lookup"><span data-stu-id="24467-124">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="24467-125">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="24467-125">Error Handling Parameters</span></span>](./error-handling-parameters.md)
