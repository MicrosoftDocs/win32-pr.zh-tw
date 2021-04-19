---
description: 深入瞭解： BeginExternalBackupGrbit 列舉
title: BeginExternalBackupGrbit 列舉
TOCTitle: BeginExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.beginexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39509773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b68cbfc75d0a71eacedb4bbd462fcd8a93d43690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983898"
---
# <a name="beginexternalbackupgrbit-enumeration"></a><span data-ttu-id="03c29-103">BeginExternalBackupGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="03c29-103">BeginExternalBackupGrbit enumeration</span></span>

<span data-ttu-id="03c29-104">[JetBeginExternalBackupInstance (JET_INSTANCE、BeginExternalBackupGrbit) ](./api.jetbeginexternalbackupinstance-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="03c29-104">Options for [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md).</span></span>

<span data-ttu-id="03c29-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="03c29-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="03c29-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="03c29-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="03c29-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="03c29-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="03c29-108">語法</span><span class="sxs-lookup"><span data-stu-id="03c29-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginExternalBackupGrbit
'Usage
Dim instance As BeginExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginExternalBackupGrbit
```

## <a name="members"></a><span data-ttu-id="03c29-109">成員</span><span class="sxs-lookup"><span data-stu-id="03c29-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="03c29-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="03c29-110">Member name</span></span></th>
<th><span data-ttu-id="03c29-111">描述</span><span class="sxs-lookup"><span data-stu-id="03c29-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="03c29-112">無</span><span class="sxs-lookup"><span data-stu-id="03c29-112">None</span></span></td>
<td><span data-ttu-id="03c29-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="03c29-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="03c29-114">增量</span><span class="sxs-lookup"><span data-stu-id="03c29-114">Incremental</span></span></td>
<td><span data-ttu-id="03c29-115">建立增量備份，而不是完整備份。</span><span class="sxs-lookup"><span data-stu-id="03c29-115">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="03c29-116">這表示只會備份自上次完整或增量備份之後的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="03c29-116">This means that only the log files since the last full or incremental backup will be backed up.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="03c29-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03c29-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="03c29-118">參考</span><span class="sxs-lookup"><span data-stu-id="03c29-118">Reference</span></span>

[<span data-ttu-id="03c29-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="03c29-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
