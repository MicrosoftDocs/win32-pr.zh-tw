---
description: 深入瞭解： BackupGrbit 列舉
title: BackupGrbit 列舉
TOCTitle: BackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.backupgrbit(v=EXCHG.10)
ms:contentKeyID: 39512196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bda9754efcae8ebe353b8272ba57c5640ecdf946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980688"
---
# <a name="backupgrbit-enumeration"></a><span data-ttu-id="db514-103">BackupGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="db514-103">BackupGrbit enumeration</span></span>

<span data-ttu-id="db514-104">[JetBackupInstance (JET_INSTANCE、String、BackupGrbit JET_PFNSTATUS) ](./api.jetbackupinstance-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="db514-104">Options for [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span></span>

<span data-ttu-id="db514-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="db514-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="db514-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="db514-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="db514-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="db514-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="db514-108">語法</span><span class="sxs-lookup"><span data-stu-id="db514-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BackupGrbit
'Usage
Dim instance As BackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BackupGrbit
```

## <a name="members"></a><span data-ttu-id="db514-109">成員</span><span class="sxs-lookup"><span data-stu-id="db514-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="db514-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="db514-110">Member name</span></span></th>
<th><span data-ttu-id="db514-111">描述</span><span class="sxs-lookup"><span data-stu-id="db514-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="db514-112">無</span><span class="sxs-lookup"><span data-stu-id="db514-112">None</span></span></td>
<td><span data-ttu-id="db514-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="db514-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="db514-114">增量</span><span class="sxs-lookup"><span data-stu-id="db514-114">Incremental</span></span></td>
<td><span data-ttu-id="db514-115">建立增量備份，而不是完整備份。</span><span class="sxs-lookup"><span data-stu-id="db514-115">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="db514-116">這表示只會備份自上次完整或增量備份之後所建立的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="db514-116">This means that only the log files created since the last full or incremental backup will be backed up.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="db514-117">原子</span><span class="sxs-lookup"><span data-stu-id="db514-117">Atomic</span></span></td>
<td><span data-ttu-id="db514-118">建立資料庫的完整備份。</span><span class="sxs-lookup"><span data-stu-id="db514-118">Creates a full backup of the database.</span></span> <span data-ttu-id="db514-119">這可在新備份失敗時，將現有的備份保留在相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="db514-119">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="db514-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db514-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="db514-121">參考</span><span class="sxs-lookup"><span data-stu-id="db514-121">Reference</span></span>

[<span data-ttu-id="db514-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="db514-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
