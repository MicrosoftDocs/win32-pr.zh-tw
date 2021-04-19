---
description: 深入瞭解： JET_SNP
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
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
ms.openlocfilehash: 35ffb2d17c01c3d157fc7ed66a320529f844ff9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970364"
---
# <a name="jet_snp"></a><span data-ttu-id="8b0b8-103">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="8b0b8-103">JET_SNP</span></span>


<span data-ttu-id="8b0b8-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8b0b8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snp"></a><span data-ttu-id="8b0b8-105">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="8b0b8-105">JET_SNP</span></span>

<span data-ttu-id="8b0b8-106">**JET_SNP** 的常數群組描述要取得進度資訊的作業類型。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-106">The **JET_SNP** group of constants describe the type of the operation for which progress information is to be obtained.</span></span> <span data-ttu-id="8b0b8-107">這些常數會當做 [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)回呼函數的 *.snp* 參數使用。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-107">These constants are used as the *snp* parameter of the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8b0b8-108">常數/值</span><span class="sxs-lookup"><span data-stu-id="8b0b8-108">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="8b0b8-109">Description</span><span class="sxs-lookup"><span data-stu-id="8b0b8-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b0b8-110">JET_snpRepair</span><span class="sxs-lookup"><span data-stu-id="8b0b8-110">JET_snpRepair</span></span><br />
<span data-ttu-id="8b0b8-111">2</span><span class="sxs-lookup"><span data-stu-id="8b0b8-111">2</span></span></p></td>
<td><p><span data-ttu-id="8b0b8-112">回呼是用於修復作業。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-112">The callback is for a repair operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0b8-113">JET_snpCompact</span><span class="sxs-lookup"><span data-stu-id="8b0b8-113">JET_snpCompact</span></span><br />
<span data-ttu-id="8b0b8-114">4</span><span class="sxs-lookup"><span data-stu-id="8b0b8-114">4</span></span></p></td>
<td><p><span data-ttu-id="8b0b8-115">回呼適用于資料庫磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-115">The callback is for database defragmentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0b8-116">JET_snpRestore</span><span class="sxs-lookup"><span data-stu-id="8b0b8-116">JET_snpRestore</span></span><br />
<span data-ttu-id="8b0b8-117">8</span><span class="sxs-lookup"><span data-stu-id="8b0b8-117">8</span></span></p></td>
<td><p><span data-ttu-id="8b0b8-118">回呼是用於還原作業。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-118">The callback is for a restore operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0b8-119">JET_snpBackup</span><span class="sxs-lookup"><span data-stu-id="8b0b8-119">JET_snpBackup</span></span><br />
<span data-ttu-id="8b0b8-120">9</span><span class="sxs-lookup"><span data-stu-id="8b0b8-120">9</span></span></p></td>
<td><p><span data-ttu-id="8b0b8-121">回呼適用于備份作業。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-121">The callback is for a backup operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0b8-122">JET_snpUpgrade</span><span class="sxs-lookup"><span data-stu-id="8b0b8-122">JET_snpUpgrade</span></span><br />
<span data-ttu-id="8b0b8-123">10</span><span class="sxs-lookup"><span data-stu-id="8b0b8-123">10</span></span></p></td>
<td><p><span data-ttu-id="8b0b8-124">不支援。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-124">Not supported.</span></span></p>
<p><span data-ttu-id="8b0b8-125"><strong>Windows 2000：</strong>  回呼適用于資料庫格式升級作業。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-125"><strong>Windows 2000:</strong>  The callback is for the database format upgrade operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0b8-126">JET_snpScrub</span><span class="sxs-lookup"><span data-stu-id="8b0b8-126">JET_snpScrub</span></span><br />
<span data-ttu-id="8b0b8-127">11</span><span class="sxs-lookup"><span data-stu-id="8b0b8-127">11</span></span></p></td>
<td><p><span data-ttu-id="8b0b8-128">回呼適用于資料庫清空 (也就是清除) 作業。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-128">The callback is for a database zeroing (that is, scrubbing) operation.</span></span></p>
<p><span data-ttu-id="8b0b8-129"><strong>Windows Server 2003 和 windows 2000 伺服器：</strong>  不支援。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-129"><strong>Windows Server 2003 and Windows 2000 Server:</strong>  Not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0b8-130">JET_snpUpgradeRecordFormat</span><span class="sxs-lookup"><span data-stu-id="8b0b8-130">JET_snpUpgradeRecordFormat</span></span><br />
<span data-ttu-id="8b0b8-131">12</span><span class="sxs-lookup"><span data-stu-id="8b0b8-131">12</span></span></p></td>
<td><p><span data-ttu-id="8b0b8-132">回呼是用於升級所有資料庫頁面之記錄格式的程式。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-132">The callback is for the process of upgrading the record format of all database pages.</span></span></p>
<p><span data-ttu-id="8b0b8-133"><strong>Windows Server 2003 和 windows 2000 伺服器：</strong>  不支援。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-133"><strong>Windows Server 2003 and Windows 2000 Server:</strong>  Not supported.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="8b0b8-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b0b8-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b0b8-135"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="8b0b8-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8b0b8-136">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0b8-137"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="8b0b8-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8b0b8-138">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0b8-139"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="8b0b8-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8b0b8-140">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="8b0b8-140">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="8b0b8-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b0b8-141">See Also</span></span>

[<span data-ttu-id="8b0b8-142">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="8b0b8-142">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="8b0b8-143">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="8b0b8-143">JET_SNPROG</span></span>](./jet-snprog-structure.md)  
[<span data-ttu-id="8b0b8-144">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="8b0b8-144">JET_SNT</span></span>](./jet-snt.md)
