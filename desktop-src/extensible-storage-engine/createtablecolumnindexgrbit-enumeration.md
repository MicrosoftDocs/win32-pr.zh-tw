---
description: 深入瞭解： CreateTableColumnIndexGrbit 列舉
title: CreateTableColumnIndexGrbit 列舉
TOCTitle: CreateTableColumnIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createtablecolumnindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39516657
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72f91c5d41b8262e3b2804159914b0a9ccaaaa7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945281"
---
# <a name="createtablecolumnindexgrbit-enumeration"></a><span data-ttu-id="f8c46-103">CreateTableColumnIndexGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="f8c46-103">CreateTableColumnIndexGrbit enumeration</span></span>

<span data-ttu-id="f8c46-104">JetCreateTableColumnIndex 的選項。</span><span class="sxs-lookup"><span data-stu-id="f8c46-104">Options for JetCreateTableColumnIndex.</span></span>

<span data-ttu-id="f8c46-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="f8c46-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="f8c46-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8c46-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f8c46-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f8c46-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8c46-108">語法</span><span class="sxs-lookup"><span data-stu-id="f8c46-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateTableColumnIndexGrbit
'Usage
Dim instance As CreateTableColumnIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateTableColumnIndexGrbit
```

## <a name="members"></a><span data-ttu-id="f8c46-109">成員</span><span class="sxs-lookup"><span data-stu-id="f8c46-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f8c46-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="f8c46-110">Member name</span></span></th>
<th><span data-ttu-id="f8c46-111">描述</span><span class="sxs-lookup"><span data-stu-id="f8c46-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f8c46-112">無</span><span class="sxs-lookup"><span data-stu-id="f8c46-112">None</span></span></td>
<td><span data-ttu-id="f8c46-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="f8c46-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f8c46-114">FixedDDL</span><span class="sxs-lookup"><span data-stu-id="f8c46-114">FixedDDL</span></span></td>
<td><span data-ttu-id="f8c46-115">DDL 已修正。</span><span class="sxs-lookup"><span data-stu-id="f8c46-115">The DDL is fixed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f8c46-116">TemplateTable</span><span class="sxs-lookup"><span data-stu-id="f8c46-116">TemplateTable</span></span></td>
<td><span data-ttu-id="f8c46-117">DDL 是可繼承的。</span><span class="sxs-lookup"><span data-stu-id="f8c46-117">The DDL is inheritable.</span></span> <span data-ttu-id="f8c46-118">意指 FixedDDL。</span><span class="sxs-lookup"><span data-stu-id="f8c46-118">Implies FixedDDL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f8c46-119">NoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="f8c46-119">NoFixedVarColumnsInDerivedTables</span></span></td>
<td><span data-ttu-id="f8c46-120">與 TemplateTable 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="f8c46-120">Used in conjunction with TemplateTable.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f8c46-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8c46-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8c46-122">參考</span><span class="sxs-lookup"><span data-stu-id="f8c46-122">Reference</span></span>

[<span data-ttu-id="f8c46-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f8c46-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
