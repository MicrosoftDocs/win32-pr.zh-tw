---
description: 深入瞭解： IdleGrbit 列舉
title: IdleGrbit 列舉
TOCTitle: IdleGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.IdleGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.idlegrbit(v=EXCHG.10)
ms:contentKeyID: 39514282
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IdleGrbit
- Microsoft.Isam.Esent.Interop.IdleGrbit.Compact
- Microsoft.Isam.Esent.Interop.IdleGrbit.FlushBuffers
- Microsoft.Isam.Esent.Interop.IdleGrbit.GetStatus
- Microsoft.Isam.Esent.Interop.IdleGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IdleGrbit.Compact
- Microsoft.Isam.Esent.Interop.IdleGrbit.FlushBuffers
- Microsoft.Isam.Esent.Interop.IdleGrbit
- Microsoft.Isam.Esent.Interop.IdleGrbit.None
- Microsoft.Isam.Esent.Interop.IdleGrbit.GetStatus
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f02937241066762b6d711d89e62e67cfed9f41f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191800"
---
# <a name="idlegrbit-enumeration"></a><span data-ttu-id="e6c6f-103">IdleGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="e6c6f-103">IdleGrbit enumeration</span></span>

<span data-ttu-id="e6c6f-104">[JetIdle (JET_SESID、IdleGrbit) ](./api.jetidle-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="e6c6f-104">Options for [JetIdle(JET_SESID, IdleGrbit)](./api.jetidle-method.md).</span></span>

<span data-ttu-id="e6c6f-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="e6c6f-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="e6c6f-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e6c6f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e6c6f-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e6c6f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c6f-108">語法</span><span class="sxs-lookup"><span data-stu-id="e6c6f-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration IdleGrbit
'Usage
Dim instance As IdleGrbit
```

``` csharp
[FlagsAttribute]
public enum IdleGrbit
```

## <a name="members"></a><span data-ttu-id="e6c6f-109">成員</span><span class="sxs-lookup"><span data-stu-id="e6c6f-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e6c6f-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="e6c6f-110">Member name</span></span></th>
<th><span data-ttu-id="e6c6f-111">描述</span><span class="sxs-lookup"><span data-stu-id="e6c6f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e6c6f-112">無</span><span class="sxs-lookup"><span data-stu-id="e6c6f-112">None</span></span></td>
<td><span data-ttu-id="e6c6f-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="e6c6f-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e6c6f-114">FlushBuffers</span><span class="sxs-lookup"><span data-stu-id="e6c6f-114">FlushBuffers</span></span></td>
<td><span data-ttu-id="e6c6f-115">觸發版本存放區的清除。</span><span class="sxs-lookup"><span data-stu-id="e6c6f-115">Triggers cleanup of the version store.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e6c6f-116">精簡</span><span class="sxs-lookup"><span data-stu-id="e6c6f-116">Compact</span></span></td>
<td><span data-ttu-id="e6c6f-117">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="e6c6f-117">Reserved for future use.</span></span> <span data-ttu-id="e6c6f-118">如果指定此旗標，API 將會傳回 <a href="hh564840(v=exchg.10).md">InvalidGrbit</a>。</span><span class="sxs-lookup"><span data-stu-id="e6c6f-118">If this flag is specified, the API will return <a href="hh564840(v=exchg.10).md">InvalidGrbit</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e6c6f-119">GetStatus</span><span class="sxs-lookup"><span data-stu-id="e6c6f-119">GetStatus</span></span></td>
<td><span data-ttu-id="e6c6f-120">如果版本存放區已滿一半，則傳回 <a href="hh557250(v=exchg.10).md">IdleFull</a> 。</span><span class="sxs-lookup"><span data-stu-id="e6c6f-120">Returns <a href="hh557250(v=exchg.10).md">IdleFull</a> if version store is more than half full.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="e6c6f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6c6f-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6c6f-122">參考</span><span class="sxs-lookup"><span data-stu-id="e6c6f-122">Reference</span></span>

[<span data-ttu-id="e6c6f-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e6c6f-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
