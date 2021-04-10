---
description: 深入瞭解： ObjectInfoFlags 列舉
title: ObjectInfoFlags 列舉
TOCTitle: ObjectInfoFlags enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfoflags(v=EXCHG.10)
ms:contentKeyID: 39515824
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3f301f1e786d126dbd57c071fe89356e0acc891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849543"
---
# <a name="objectinfoflags-enumeration"></a><span data-ttu-id="04340-103">ObjectInfoFlags 列舉</span><span class="sxs-lookup"><span data-stu-id="04340-103">ObjectInfoFlags enumeration</span></span>

<span data-ttu-id="04340-104"> (資料表) 之 ESENT 物件的旗標。</span><span class="sxs-lookup"><span data-stu-id="04340-104">Flags for ESENT objects (tables).</span></span> <span data-ttu-id="04340-105">用於 [JET_OBJECTINFO](./jet-objectinfo-class.md)。</span><span class="sxs-lookup"><span data-stu-id="04340-105">Used in [JET_OBJECTINFO](./jet-objectinfo-class.md).</span></span>

<span data-ttu-id="04340-106">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="04340-106">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="04340-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="04340-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="04340-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="04340-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="04340-109">語法</span><span class="sxs-lookup"><span data-stu-id="04340-109">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoFlags
'Usage
Dim instance As ObjectInfoFlags
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoFlags
```

## <a name="members"></a><span data-ttu-id="04340-110">成員</span><span class="sxs-lookup"><span data-stu-id="04340-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="04340-111">成員名稱</span><span class="sxs-lookup"><span data-stu-id="04340-111">Member name</span></span></th>
<th><span data-ttu-id="04340-112">描述</span><span class="sxs-lookup"><span data-stu-id="04340-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="04340-113">無</span><span class="sxs-lookup"><span data-stu-id="04340-113">None</span></span></td>
<td><span data-ttu-id="04340-114">預設選項。</span><span class="sxs-lookup"><span data-stu-id="04340-114">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="04340-115">系統</span><span class="sxs-lookup"><span data-stu-id="04340-115">System</span></span></td>
<td><span data-ttu-id="04340-116">物件僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="04340-116">Object is for internal use only.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="04340-117">TableFixedDDL</span><span class="sxs-lookup"><span data-stu-id="04340-117">TableFixedDDL</span></span></td>
<td><span data-ttu-id="04340-118">資料表的 DDL 是固定的。</span><span class="sxs-lookup"><span data-stu-id="04340-118">Table's DDL is fixed.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="04340-119">TableTemplate</span><span class="sxs-lookup"><span data-stu-id="04340-119">TableTemplate</span></span></td>
<td><span data-ttu-id="04340-120">資料表的 DDL 是可繼承的。</span><span class="sxs-lookup"><span data-stu-id="04340-120">Table's DDL is inheritable.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="04340-121">TableDerived</span><span class="sxs-lookup"><span data-stu-id="04340-121">TableDerived</span></span></td>
<td><span data-ttu-id="04340-122">資料表的 DDL 繼承自範本資料表。</span><span class="sxs-lookup"><span data-stu-id="04340-122">Table's DDL is inherited from a template table.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="04340-123">TableNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="04340-123">TableNoFixedVarColumnsInDerivedTables</span></span></td>
<td><span data-ttu-id="04340-124">固定或 (衍生資料表中的資料行，讓固定或變數資料行可以在未來的) 中加入至範本。</span><span class="sxs-lookup"><span data-stu-id="04340-124">Fixed or variable columns in derived tables (so that fixed or variable columns can be added to the template in the future).</span></span> <span data-ttu-id="04340-125">與 TableTemplate 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="04340-125">Used in conjunction with TableTemplate.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="04340-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04340-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="04340-127">參考</span><span class="sxs-lookup"><span data-stu-id="04340-127">Reference</span></span>

[<span data-ttu-id="04340-128">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="04340-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
