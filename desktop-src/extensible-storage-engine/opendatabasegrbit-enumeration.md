---
description: 深入瞭解： OpenDatabaseGrbit 列舉
title: OpenDatabaseGrbit 列舉
TOCTitle: OpenDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opendatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514563
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d14fb779ec02137f6a4fce1cfdd92f46dedcb832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193036"
---
# <a name="opendatabasegrbit-enumeration"></a><span data-ttu-id="1881a-103">OpenDatabaseGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="1881a-103">OpenDatabaseGrbit enumeration</span></span>

<span data-ttu-id="1881a-104">[JetOpenDatabase (JET_SESID、string、string、JET_DBID、OpenDatabaseGrbit) ](./api.jetopendatabase-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="1881a-104">Options for [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="1881a-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="1881a-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="1881a-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1881a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1881a-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1881a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1881a-108">語法</span><span class="sxs-lookup"><span data-stu-id="1881a-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenDatabaseGrbit
'Usage
Dim instance As OpenDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="1881a-109">成員</span><span class="sxs-lookup"><span data-stu-id="1881a-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="1881a-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="1881a-110">Member name</span></span></th>
<th><span data-ttu-id="1881a-111">描述</span><span class="sxs-lookup"><span data-stu-id="1881a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1881a-112">無</span><span class="sxs-lookup"><span data-stu-id="1881a-112">None</span></span></td>
<td><span data-ttu-id="1881a-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="1881a-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1881a-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1881a-114">ReadOnly</span></span></td>
<td><span data-ttu-id="1881a-115">防止修改資料庫。</span><span class="sxs-lookup"><span data-stu-id="1881a-115">Prevents modifications to the database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1881a-116">獨佔</span><span class="sxs-lookup"><span data-stu-id="1881a-116">Exclusive</span></span></td>
<td><span data-ttu-id="1881a-117">只允許單一會話附加資料庫。</span><span class="sxs-lookup"><span data-stu-id="1881a-117">Allows only a single session to attach a database.</span></span> <span data-ttu-id="1881a-118">一般來說，數個會話可以開啟資料庫。</span><span class="sxs-lookup"><span data-stu-id="1881a-118">Normally, several sessions can open a database.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="1881a-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1881a-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1881a-120">參考</span><span class="sxs-lookup"><span data-stu-id="1881a-120">Reference</span></span>

[<span data-ttu-id="1881a-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1881a-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
