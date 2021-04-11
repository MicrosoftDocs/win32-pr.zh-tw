---
description: 深入瞭解： DetachDatabaseGrbit 列舉
title: DetachDatabaseGrbit 列舉
TOCTitle: DetachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.detachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 55100985
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceClose
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceCloseAndDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceClose
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceCloseAndDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceDetach
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e67962420ee0179571da8262f17ea5279f59016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195014"
---
# <a name="detachdatabasegrbit-enumeration"></a><span data-ttu-id="a3a22-103">DetachDatabaseGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="a3a22-103">DetachDatabaseGrbit enumeration</span></span>

<span data-ttu-id="a3a22-104">[JetDetachDatabase2 (JET_SESID、String、DetachDatabaseGrbit) ](./api.jetdetachdatabase2-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="a3a22-104">Options for [JetDetachDatabase2(JET_SESID, String, DetachDatabaseGrbit)](./api.jetdetachdatabase2-method.md).</span></span>

<span data-ttu-id="a3a22-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="a3a22-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="a3a22-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a3a22-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a3a22-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a3a22-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a3a22-108">語法</span><span class="sxs-lookup"><span data-stu-id="a3a22-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DetachDatabaseGrbit
'Usage
Dim instance As DetachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum DetachDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="a3a22-109">成員</span><span class="sxs-lookup"><span data-stu-id="a3a22-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="a3a22-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="a3a22-110">Member name</span></span></th>
<th><span data-ttu-id="a3a22-111">描述</span><span class="sxs-lookup"><span data-stu-id="a3a22-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a3a22-112">無</span><span class="sxs-lookup"><span data-stu-id="a3a22-112">None</span></span></td>
<td><span data-ttu-id="a3a22-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="a3a22-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a3a22-114">ForceDetach</span><span class="sxs-lookup"><span data-stu-id="a3a22-114">ForceDetach</span></span></td>
<td><span data-ttu-id="a3a22-115"><strong>已淘汰。</strong></span><span class="sxs-lookup"><span data-stu-id="a3a22-115"><strong>Obsolete.</strong></span></span> <span data-ttu-id="a3a22-116">如果使用 ForceDetach，則會傳回 <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> 。</span><span class="sxs-lookup"><span data-stu-id="a3a22-116">If ForceDetach is used, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> will be returned.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a3a22-117">ForceClose</span><span class="sxs-lookup"><span data-stu-id="a3a22-117">ForceClose</span></span></td>
<td><span data-ttu-id="a3a22-118"><strong>已淘汰。</strong></span><span class="sxs-lookup"><span data-stu-id="a3a22-118"><strong>Obsolete.</strong></span></span> <span data-ttu-id="a3a22-119">不再使用 ForceClose。</span><span class="sxs-lookup"><span data-stu-id="a3a22-119">ForceClose is no longer used.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a3a22-120">ForceCloseAndDetach</span><span class="sxs-lookup"><span data-stu-id="a3a22-120">ForceCloseAndDetach</span></span></td>
<td><span data-ttu-id="a3a22-121"><strong>已淘汰。</strong></span><span class="sxs-lookup"><span data-stu-id="a3a22-121"><strong>Obsolete.</strong></span></span> <span data-ttu-id="a3a22-122">如果使用 ForceCloseAndDetach，則會傳回 <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> 。</span><span class="sxs-lookup"><span data-stu-id="a3a22-122">If ForceCloseAndDetach is used, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> will be returned.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="a3a22-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3a22-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a3a22-124">參考</span><span class="sxs-lookup"><span data-stu-id="a3a22-124">Reference</span></span>

[<span data-ttu-id="a3a22-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a3a22-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
