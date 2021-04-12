---
description: 深入瞭解： SnapshotPrepareGrbit 列舉
title: SnapshotPrepareGrbit 列舉
TOCTitle: SnapshotPrepareGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.snapshotpreparegrbit(v=EXCHG.10)
ms:contentKeyID: 39515688
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.CopySnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.IncrementalSnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.CopySnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.IncrementalSnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.None
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 32c11c609f78cc96862f9c2f15d93266f40ae941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318559"
---
# <a name="snapshotpreparegrbit-enumeration"></a><span data-ttu-id="6c8d4-103">SnapshotPrepareGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="6c8d4-103">SnapshotPrepareGrbit enumeration</span></span>

<span data-ttu-id="6c8d4-104">[JetOSSnapshotPrepare (JET_OSSNAPID、SnapshotPrepareGrbit) ](./api.jetossnapshotprepare-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-104">Options for [JetOSSnapshotPrepare(JET_OSSNAPID, SnapshotPrepareGrbit)](./api.jetossnapshotprepare-method.md).</span></span>

<span data-ttu-id="6c8d4-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="6c8d4-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6c8d4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6c8d4-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6c8d4-108">語法</span><span class="sxs-lookup"><span data-stu-id="6c8d4-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SnapshotPrepareGrbit
'Usage
Dim instance As SnapshotPrepareGrbit
```

``` csharp
[FlagsAttribute]
public enum SnapshotPrepareGrbit
```

## <a name="members"></a><span data-ttu-id="6c8d4-109">成員</span><span class="sxs-lookup"><span data-stu-id="6c8d4-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="6c8d4-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="6c8d4-110">Member name</span></span></th>
<th><span data-ttu-id="6c8d4-111">描述</span><span class="sxs-lookup"><span data-stu-id="6c8d4-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="6c8d4-112">無</span><span class="sxs-lookup"><span data-stu-id="6c8d4-112">None</span></span></td>
<td><span data-ttu-id="6c8d4-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="6c8d4-114">Incrementalsnapshot.xml 檔</span><span class="sxs-lookup"><span data-stu-id="6c8d4-114">IncrementalSnapshot</span></span></td>
<td><span data-ttu-id="6c8d4-115">只會取得記錄檔。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-115">Only logfiles will be taken.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="6c8d4-116">CopySnapshot</span><span class="sxs-lookup"><span data-stu-id="6c8d4-116">CopySnapshot</span></span></td>
<td><span data-ttu-id="6c8d4-117">複製快照集 (一般或累加) ，而不會截斷記錄。</span><span class="sxs-lookup"><span data-stu-id="6c8d4-117">A copy snapshot (normal or incremental) with no log truncation.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="6c8d4-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c8d4-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6c8d4-119">參考</span><span class="sxs-lookup"><span data-stu-id="6c8d4-119">Reference</span></span>

[<span data-ttu-id="6c8d4-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6c8d4-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
