---
description: 深入瞭解： GetLockGrbit 列舉
title: GetLockGrbit 列舉
TOCTitle: GetLockGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetLockGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getlockgrbit(v=EXCHG.10)
ms:contentKeyID: 39512424
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cfcad088fa93d73910a0333d3aca9a700e97996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943743"
---
# <a name="getlockgrbit-enumeration"></a><span data-ttu-id="3477d-103">GetLockGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="3477d-103">GetLockGrbit enumeration</span></span>

<span data-ttu-id="3477d-104">JetGetLock 的選項。</span><span class="sxs-lookup"><span data-stu-id="3477d-104">Options for JetGetLock.</span></span>

<span data-ttu-id="3477d-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="3477d-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="3477d-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3477d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3477d-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3477d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3477d-108">語法</span><span class="sxs-lookup"><span data-stu-id="3477d-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetLockGrbit
'Usage
Dim instance As GetLockGrbit
```

``` csharp
[FlagsAttribute]
public enum GetLockGrbit
```

## <a name="members"></a><span data-ttu-id="3477d-109">成員</span><span class="sxs-lookup"><span data-stu-id="3477d-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="3477d-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="3477d-110">Member name</span></span></th>
<th><span data-ttu-id="3477d-111">說明</span><span class="sxs-lookup"><span data-stu-id="3477d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3477d-112">讀取</span><span class="sxs-lookup"><span data-stu-id="3477d-112">Read</span></span></td>
<td><span data-ttu-id="3477d-113">取得目前記錄的讀取鎖定。</span><span class="sxs-lookup"><span data-stu-id="3477d-113">Acquire a read lock on the current record.</span></span> <span data-ttu-id="3477d-114">讀取鎖定與其他會話已保留的寫入鎖定不相容，但與其他會話所持有的讀取鎖定相容。</span><span class="sxs-lookup"><span data-stu-id="3477d-114">Read locks are incompatible with write locks already held by other sessions but are compatible with read locks held by other sessions.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3477d-115">寫入</span><span class="sxs-lookup"><span data-stu-id="3477d-115">Write</span></span></td>
<td><span data-ttu-id="3477d-116">取得目前記錄的寫入鎖定。</span><span class="sxs-lookup"><span data-stu-id="3477d-116">Acquire a write lock on the current record.</span></span> <span data-ttu-id="3477d-117">寫入鎖定與其他會話所持有的寫入或讀取鎖定不相容，但與相同會話所持有的讀取鎖定相容。</span><span class="sxs-lookup"><span data-stu-id="3477d-117">Write locks are not compatible with write or read locks held by other sessions but are compatible with read locks held by the same session.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="3477d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3477d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3477d-119">參考</span><span class="sxs-lookup"><span data-stu-id="3477d-119">Reference</span></span>

[<span data-ttu-id="3477d-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3477d-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
