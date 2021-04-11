---
description: 深入瞭解： ConditionalColumnGrbit 列舉
title: ConditionalColumnGrbit 列舉
TOCTitle: ConditionalColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conditionalcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39513009
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNonNull
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNull
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNonNull
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82828df5d5a25dac08a2a8ab560225456f075a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943649"
---
# <a name="conditionalcolumngrbit-enumeration"></a><span data-ttu-id="7b4ae-103">ConditionalColumnGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="7b4ae-103">ConditionalColumnGrbit enumeration</span></span>

<span data-ttu-id="7b4ae-104">JET_CONDITIONALCOLUMN 結構的選項。</span><span class="sxs-lookup"><span data-stu-id="7b4ae-104">Options for the JET_CONDITIONALCOLUMN structure.</span></span>

<span data-ttu-id="7b4ae-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="7b4ae-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="7b4ae-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7b4ae-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7b4ae-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7b4ae-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7b4ae-108">語法</span><span class="sxs-lookup"><span data-stu-id="7b4ae-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ConditionalColumnGrbit
'Usage
Dim instance As ConditionalColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum ConditionalColumnGrbit
```

## <a name="members"></a><span data-ttu-id="7b4ae-109">成員</span><span class="sxs-lookup"><span data-stu-id="7b4ae-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="7b4ae-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="7b4ae-110">Member name</span></span></th>
<th><span data-ttu-id="7b4ae-111">說明</span><span class="sxs-lookup"><span data-stu-id="7b4ae-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7b4ae-112">ColumnMustBeNull</span><span class="sxs-lookup"><span data-stu-id="7b4ae-112">ColumnMustBeNull</span></span></td>
<td><span data-ttu-id="7b4ae-113">此資料行必須是 null，索引項目目才會出現在索引中。</span><span class="sxs-lookup"><span data-stu-id="7b4ae-113">The column must be null for an index entry to appear in the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7b4ae-114">ColumnMustBeNonNull</span><span class="sxs-lookup"><span data-stu-id="7b4ae-114">ColumnMustBeNonNull</span></span></td>
<td><span data-ttu-id="7b4ae-115">此資料行必須為非 null，索引項目目才會出現在索引中。</span><span class="sxs-lookup"><span data-stu-id="7b4ae-115">The column must be non-null for an index entry to appear in the index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="7b4ae-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b4ae-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7b4ae-117">參考</span><span class="sxs-lookup"><span data-stu-id="7b4ae-117">Reference</span></span>

[<span data-ttu-id="7b4ae-118">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7b4ae-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
