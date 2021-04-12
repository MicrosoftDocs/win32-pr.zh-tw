---
description: 深入瞭解： JET_SNT
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d1d4fa75c8a41528e9868bc94fa638042d01cff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191133"
---
# <a name="jet_snt"></a><span data-ttu-id="2b144-103">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="2b144-103">JET_SNT</span></span>


<span data-ttu-id="2b144-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2b144-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snt"></a><span data-ttu-id="2b144-105">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="2b144-105">JET_SNT</span></span>

<span data-ttu-id="2b144-106">[JET_SNT]()的常數群組描述作業的進度點，這是在呼叫[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)回呼函數時所要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="2b144-106">The [JET_SNT]() group of constants describe the points of the progress of an operation about which information is requested in a call to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b144-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="2b144-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="2b144-108">Description</span><span class="sxs-lookup"><span data-stu-id="2b144-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b144-109">JET_sntBegin</span><span class="sxs-lookup"><span data-stu-id="2b144-109">JET_sntBegin</span></span><br />
<span data-ttu-id="2b144-110">5</span><span class="sxs-lookup"><span data-stu-id="2b144-110">5</span></span></p></td>
<td><p><span data-ttu-id="2b144-111">作業的開頭</span><span class="sxs-lookup"><span data-stu-id="2b144-111">The beginning of an operation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b144-112">JET_sntRequirements</span><span class="sxs-lookup"><span data-stu-id="2b144-112">JET_sntRequirements</span></span><br />
<span data-ttu-id="2b144-113">7</span><span class="sxs-lookup"><span data-stu-id="2b144-113">7</span></span></p></td>
<td><p><span data-ttu-id="2b144-114">不支援。</span><span class="sxs-lookup"><span data-stu-id="2b144-114">Not supported.</span></span></p>
<p><span data-ttu-id="2b144-115"><strong>Windows 2000 伺服器：</strong>  作業已啟動。</span><span class="sxs-lookup"><span data-stu-id="2b144-115"><strong>Windows 2000 Server:</strong>  The operation is started.</span></span> <span data-ttu-id="2b144-116">在此情況下，回呼函式的最後一個參數應該是指向 <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> 結構的有效指標，指出要執行的單位總數。</span><span class="sxs-lookup"><span data-stu-id="2b144-116">In this case, the last parameter of the callback function should be a valid pointer to a <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> structure indicating the total number of units to be executed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b144-117">JET_sntProgress</span><span class="sxs-lookup"><span data-stu-id="2b144-117">JET_sntProgress</span></span><br />
<span data-ttu-id="2b144-118">0</span><span class="sxs-lookup"><span data-stu-id="2b144-118">0</span></span></p></td>
<td><p><span data-ttu-id="2b144-119">完成的單位數和尚未完成的單位數。</span><span class="sxs-lookup"><span data-stu-id="2b144-119">The number of units completed and number of units yet to be done.</span></span> <span data-ttu-id="2b144-120">這項資訊會在 <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> 結構的成員中傳回。</span><span class="sxs-lookup"><span data-stu-id="2b144-120">This information is returned in the members of a <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b144-121">JET_sntComplete</span><span class="sxs-lookup"><span data-stu-id="2b144-121">JET_sntComplete</span></span><br />
<span data-ttu-id="2b144-122">6</span><span class="sxs-lookup"><span data-stu-id="2b144-122">6</span></span></p></td>
<td><p><span data-ttu-id="2b144-123">作業完成。</span><span class="sxs-lookup"><span data-stu-id="2b144-123">The completion of an operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b144-124">JET_sntFail</span><span class="sxs-lookup"><span data-stu-id="2b144-124">JET_sntFail</span></span><br />
<span data-ttu-id="2b144-125">3</span><span class="sxs-lookup"><span data-stu-id="2b144-125">3</span></span></p></td>
<td><p><span data-ttu-id="2b144-126">作業失敗。</span><span class="sxs-lookup"><span data-stu-id="2b144-126">The failure of an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b144-127">JET_sntRecoveryStep</span><span class="sxs-lookup"><span data-stu-id="2b144-127">JET_sntRecoveryStep</span></span><br />
<span data-ttu-id="2b144-128">8</span><span class="sxs-lookup"><span data-stu-id="2b144-128">8</span></span></p></td>
<td><p><span data-ttu-id="2b144-129">操作的復原控制。</span><span class="sxs-lookup"><span data-stu-id="2b144-129">The recovery control of an operation.</span></span></p>
<div class="alert">

> [!NOTE]
> <P><span data-ttu-id="2b144-130">此值不適用於從 Windows 8 開始的 Windows 作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="2b144-130">This value is not applicable to versions of the Windows operating system starting with Windows 8.</span></span></P>


</div></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="2b144-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b144-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b144-132"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="2b144-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2b144-133">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="2b144-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b144-134"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="2b144-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2b144-135">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="2b144-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b144-136"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="2b144-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2b144-137">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="2b144-137">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="2b144-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b144-138">See Also</span></span>

[<span data-ttu-id="2b144-139">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="2b144-139">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="2b144-140">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="2b144-140">JET_SNP</span></span>](./jet-snp.md)  
[<span data-ttu-id="2b144-141">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="2b144-141">JET_SNPROG</span></span>](./jet-snprog-structure.md)
