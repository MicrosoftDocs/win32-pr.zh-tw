---
description: 深入瞭解： GotoSecondaryIndexBookmarkGrbit 列舉
title: GotoSecondaryIndexBookmarkGrbit 列舉
TOCTitle: GotoSecondaryIndexBookmarkGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.gotosecondaryindexbookmarkgrbit(v=EXCHG.10)
ms:contentKeyID: 39515224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.BookmarkPermitVirtualCurrency
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.BookmarkPermitVirtualCurrency
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f38b5f26abc4dfafb95d5560b3ff1def4267527c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974573"
---
# <a name="gotosecondaryindexbookmarkgrbit-enumeration"></a><span data-ttu-id="bdd1e-103">GotoSecondaryIndexBookmarkGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="bdd1e-103">GotoSecondaryIndexBookmarkGrbit enumeration</span></span>

<span data-ttu-id="bdd1e-104">[JetGotoSecondaryIndexBookmark (JET_SESID、JET_TABLEID、 \[ \] 、int32、 \[ \] 、int32、GotoSecondaryIndexBookmarkGrbit) ](./api.jetgotosecondaryindexbookmark-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="bdd1e-104">Options for [JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, \[\], Int32, \[\], Int32, GotoSecondaryIndexBookmarkGrbit)](./api.jetgotosecondaryindexbookmark-method.md).</span></span>

<span data-ttu-id="bdd1e-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="bdd1e-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="bdd1e-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bdd1e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bdd1e-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="bdd1e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd1e-108">語法</span><span class="sxs-lookup"><span data-stu-id="bdd1e-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GotoSecondaryIndexBookmarkGrbit
'Usage
Dim instance As GotoSecondaryIndexBookmarkGrbit
```

``` csharp
[FlagsAttribute]
public enum GotoSecondaryIndexBookmarkGrbit
```

## <a name="members"></a><span data-ttu-id="bdd1e-109">成員</span><span class="sxs-lookup"><span data-stu-id="bdd1e-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="bdd1e-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="bdd1e-110">Member name</span></span></th>
<th><span data-ttu-id="bdd1e-111">描述</span><span class="sxs-lookup"><span data-stu-id="bdd1e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="bdd1e-112">無</span><span class="sxs-lookup"><span data-stu-id="bdd1e-112">None</span></span></td>
<td><span data-ttu-id="bdd1e-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="bdd1e-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="bdd1e-114">BookmarkPermitVirtualCurrency</span><span class="sxs-lookup"><span data-stu-id="bdd1e-114">BookmarkPermitVirtualCurrency</span></span></td>
<td><span data-ttu-id="bdd1e-115">如果找不到索引項目，就會將游標放在先前找到索引項目的位置。</span><span class="sxs-lookup"><span data-stu-id="bdd1e-115">In the event that the index entry can no longer be found, the cursor will be left positioned where that index entry was previously found.</span></span> <span data-ttu-id="bdd1e-116">作業仍會因為 JET_errRecordDeleted 而失敗;不過，您可以移至下一個或上一個索引項目（相對於現在遺漏的索引項目）。</span><span class="sxs-lookup"><span data-stu-id="bdd1e-116">The operation will still fail with JET_errRecordDeleted; however, it will be possible to move to the next or previous index entry relative to the index entry that is now missing.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="bdd1e-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bdd1e-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bdd1e-118">參考</span><span class="sxs-lookup"><span data-stu-id="bdd1e-118">Reference</span></span>

[<span data-ttu-id="bdd1e-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="bdd1e-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
