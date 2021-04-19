---
description: 深入瞭解： SnapshotTruncateLogGrbit 列舉
title: 'SnapshotTruncateLogGrbit 列舉 (的列舉) '
TOCTitle: SnapshotTruncateLogGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.snapshottruncateloggrbit(v=EXCHG.10)
ms:contentKeyID: 39516474
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.AllDatabasesSnapshot
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.AllDatabasesSnapshot
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.None
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8baf9f9ec15e91183d2b01a07da9aeda0c7fec18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973874"
---
# <a name="snapshottruncateloggrbit-enumeration"></a><span data-ttu-id="958ff-103">SnapshotTruncateLogGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="958ff-103">SnapshotTruncateLogGrbit enumeration</span></span>

<span data-ttu-id="958ff-104">[JetOSSnapshotTruncateLog (JET_OSSNAPID、SnapshotTruncateLogGrbit) ](./vistaapi.jetossnapshottruncatelog-method.md)和[JetOSSnapshotTruncateLogInstance (JET_OSSNAPID、JET_INSTANCE、SnapshotTruncateLogGrbit) ](./vistaapi.jetossnapshottruncateloginstance-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="958ff-104">Options for [JetOSSnapshotTruncateLog(JET_OSSNAPID, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncatelog-method.md) and [JetOSSnapshotTruncateLogInstance(JET_OSSNAPID, JET_INSTANCE, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncateloginstance-method.md).</span></span>

<span data-ttu-id="958ff-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="958ff-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="958ff-106">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="958ff-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="958ff-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="958ff-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="958ff-108">語法</span><span class="sxs-lookup"><span data-stu-id="958ff-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SnapshotTruncateLogGrbit
'Usage
Dim instance As SnapshotTruncateLogGrbit
```

``` csharp
[FlagsAttribute]
public enum SnapshotTruncateLogGrbit
```

## <a name="members"></a><span data-ttu-id="958ff-109">成員</span><span class="sxs-lookup"><span data-stu-id="958ff-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="958ff-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="958ff-110">Member name</span></span></th>
<th><span data-ttu-id="958ff-111">描述</span><span class="sxs-lookup"><span data-stu-id="958ff-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="958ff-112">無</span><span class="sxs-lookup"><span data-stu-id="958ff-112">None</span></span></td>
<td><span data-ttu-id="958ff-113">不會發生截斷。</span><span class="sxs-lookup"><span data-stu-id="958ff-113">No truncation will occur.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="958ff-114">AllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="958ff-114">AllDatabasesSnapshot</span></span></td>
<td><span data-ttu-id="958ff-115">附加所有資料庫，讓儲存引擎可以計算並進行記錄截斷。</span><span class="sxs-lookup"><span data-stu-id="958ff-115">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="958ff-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="958ff-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="958ff-117">參考</span><span class="sxs-lookup"><span data-stu-id="958ff-117">Reference</span></span>

[<span data-ttu-id="958ff-118">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="958ff-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
