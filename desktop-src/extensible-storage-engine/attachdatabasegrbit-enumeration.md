---
description: 深入瞭解： AttachDatabaseGrbit 列舉
title: AttachDatabaseGrbit 列舉
TOCTitle: AttachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.attachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514410
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81525e97f1b6266ba15baab50168404566bd7bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990483"
---
# <a name="attachdatabasegrbit-enumeration"></a><span data-ttu-id="3b8fc-103">AttachDatabaseGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="3b8fc-103">AttachDatabaseGrbit enumeration</span></span>

<span data-ttu-id="3b8fc-104">JetAttachDatabase 的選項。</span><span class="sxs-lookup"><span data-stu-id="3b8fc-104">Options for JetAttachDatabase.</span></span>

<span data-ttu-id="3b8fc-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="3b8fc-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="3b8fc-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3b8fc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3b8fc-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3b8fc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3b8fc-108">語法</span><span class="sxs-lookup"><span data-stu-id="3b8fc-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration AttachDatabaseGrbit
'Usage
Dim instance As AttachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum AttachDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="3b8fc-109">成員</span><span class="sxs-lookup"><span data-stu-id="3b8fc-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="3b8fc-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="3b8fc-110">Member name</span></span></th>
<th><span data-ttu-id="3b8fc-111">描述</span><span class="sxs-lookup"><span data-stu-id="3b8fc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3b8fc-112">無</span><span class="sxs-lookup"><span data-stu-id="3b8fc-112">None</span></span></td>
<td><span data-ttu-id="3b8fc-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="3b8fc-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3b8fc-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3b8fc-114">ReadOnly</span></span></td>
<td><span data-ttu-id="3b8fc-115">防止修改資料庫。</span><span class="sxs-lookup"><span data-stu-id="3b8fc-115">Prevents modifications to the database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3b8fc-116">DeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="3b8fc-116">DeleteCorruptIndexes</span></span></td>
<td><span data-ttu-id="3b8fc-117">如果已設定 JET_paramEnableIndexChecking，將會刪除 Unicode 資料上的所有索引。</span><span class="sxs-lookup"><span data-stu-id="3b8fc-117">If JET_paramEnableIndexChecking has been set, all indexes over Unicode data will be deleted.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="3b8fc-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b8fc-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3b8fc-119">參考</span><span class="sxs-lookup"><span data-stu-id="3b8fc-119">Reference</span></span>

[<span data-ttu-id="3b8fc-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3b8fc-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
