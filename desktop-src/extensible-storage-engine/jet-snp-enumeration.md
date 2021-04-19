---
description: 深入瞭解： JET_SNP 列舉
title: JET_SNP 列舉
TOCTitle: JET_SNP enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNP
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snp(v=EXCHG.10)
ms:contentKeyID: 39511218
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10061d0c00d90aa5ca4e0778cba046d2e6f62f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971165"
---
# <a name="jet_snp-enumeration"></a><span data-ttu-id="10579-103">JET_SNP 列舉</span><span class="sxs-lookup"><span data-stu-id="10579-103">JET_SNP enumeration</span></span>

<span data-ttu-id="10579-104">報告進度的作業類型。</span><span class="sxs-lookup"><span data-stu-id="10579-104">The type of operation that progress is being reported for.</span></span>

<span data-ttu-id="10579-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="10579-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="10579-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="10579-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="10579-107">語法</span><span class="sxs-lookup"><span data-stu-id="10579-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_SNP
'Usage
Dim instance As JET_SNP
```

``` csharp
public enum JET_SNP
```

## <a name="members"></a><span data-ttu-id="10579-108">成員</span><span class="sxs-lookup"><span data-stu-id="10579-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="10579-109">成員名稱</span><span class="sxs-lookup"><span data-stu-id="10579-109">Member name</span></span></th>
<th><span data-ttu-id="10579-110">說明</span><span class="sxs-lookup"><span data-stu-id="10579-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="10579-111">修復</span><span class="sxs-lookup"><span data-stu-id="10579-111">Repair</span></span></td>
<td><span data-ttu-id="10579-112">回呼適用于 repair 選項。</span><span class="sxs-lookup"><span data-stu-id="10579-112">Callback is for a repair option.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="10579-113">精簡</span><span class="sxs-lookup"><span data-stu-id="10579-113">Compact</span></span></td>
<td><span data-ttu-id="10579-114">回呼適用于資料庫磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="10579-114">Callback is for database defragmentation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="10579-115">還原</span><span class="sxs-lookup"><span data-stu-id="10579-115">Restore</span></span></td>
<td><span data-ttu-id="10579-116">回呼適用于還原選項。</span><span class="sxs-lookup"><span data-stu-id="10579-116">Callback is for a restore options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="10579-117">備份</span><span class="sxs-lookup"><span data-stu-id="10579-117">Backup</span></span></td>
<td><span data-ttu-id="10579-118">回呼適用于備份選項。</span><span class="sxs-lookup"><span data-stu-id="10579-118">Callback is for a backup options.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="10579-119">擦洗</span><span class="sxs-lookup"><span data-stu-id="10579-119">Scrub</span></span></td>
<td><span data-ttu-id="10579-120">回呼適用于資料庫清空。</span><span class="sxs-lookup"><span data-stu-id="10579-120">Callback is for database zeroing.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="10579-121">UpgradeRecordFormat</span><span class="sxs-lookup"><span data-stu-id="10579-121">UpgradeRecordFormat</span></span></td>
<td><span data-ttu-id="10579-122">回呼是用於升級所有資料庫頁面之記錄格式的程式。</span><span class="sxs-lookup"><span data-stu-id="10579-122">Callback is for the process of upgrading the record format of all database pages.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="10579-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10579-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="10579-124">參考</span><span class="sxs-lookup"><span data-stu-id="10579-124">Reference</span></span>

[<span data-ttu-id="10579-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="10579-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
