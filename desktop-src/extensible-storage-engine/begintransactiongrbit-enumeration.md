---
description: 深入瞭解： BeginTransactionGrbit 列舉
title: BeginTransactionGrbit 列舉
TOCTitle: BeginTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.begintransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39515115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5f407c54b7b6e76ab63dcfb97d1307458ba15277
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694620"
---
# <a name="begintransactiongrbit-enumeration"></a><span data-ttu-id="06a12-103">BeginTransactionGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="06a12-103">BeginTransactionGrbit enumeration</span></span>

<span data-ttu-id="06a12-104">[JetBeginTransaction2 (JET_SESID、BeginTransactionGrbit) ](./api.jetbegintransaction2-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="06a12-104">Options for [JetBeginTransaction2(JET_SESID, BeginTransactionGrbit)](./api.jetbegintransaction2-method.md).</span></span>

<span data-ttu-id="06a12-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="06a12-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="06a12-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="06a12-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="06a12-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="06a12-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="06a12-108">語法</span><span class="sxs-lookup"><span data-stu-id="06a12-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginTransactionGrbit
'Usage
Dim instance As BeginTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="06a12-109">成員</span><span class="sxs-lookup"><span data-stu-id="06a12-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="06a12-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="06a12-110">Member name</span></span></th>
<th><span data-ttu-id="06a12-111">描述</span><span class="sxs-lookup"><span data-stu-id="06a12-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="06a12-112">無</span><span class="sxs-lookup"><span data-stu-id="06a12-112">None</span></span></td>
<td><span data-ttu-id="06a12-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="06a12-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="06a12-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="06a12-114">ReadOnly</span></span></td>
<td><span data-ttu-id="06a12-115">交易不會修改資料庫。</span><span class="sxs-lookup"><span data-stu-id="06a12-115">The transaction will not modify the database.</span></span> <span data-ttu-id="06a12-116">如果嘗試更新，該作業將會因為 <a href="hh564840(v=exchg.10).md">TransReadOnly</a>而失敗。</span><span class="sxs-lookup"><span data-stu-id="06a12-116">If an update is attempted, that operation will fail with <a href="hh564840(v=exchg.10).md">TransReadOnly</a>.</span></span> <span data-ttu-id="06a12-117">除非指定的會話尚未存在於交易中，否則會忽略這個選項。</span><span class="sxs-lookup"><span data-stu-id="06a12-117">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="06a12-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06a12-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="06a12-119">參考</span><span class="sxs-lookup"><span data-stu-id="06a12-119">Reference</span></span>

[<span data-ttu-id="06a12-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="06a12-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
