---
description: 深入瞭解： CreateDatabaseGrbit 列舉
title: CreateDatabaseGrbit 列舉
TOCTitle: CreateDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39515634
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e23b7b875863b747fc5d2ba021c90d5f7f71048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026346"
---
# <a name="createdatabasegrbit-enumeration"></a><span data-ttu-id="41fb2-103">CreateDatabaseGrbit 列舉</span><span class="sxs-lookup"><span data-stu-id="41fb2-103">CreateDatabaseGrbit enumeration</span></span>

<span data-ttu-id="41fb2-104">[JetCreateDatabase (JET_SESID、string、string、JET_DBID、CreateDatabaseGrbit) ](./api.jetcreatedatabase-method.md)的選項。</span><span class="sxs-lookup"><span data-stu-id="41fb2-104">Options for [JetCreateDatabase(JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span></span>

<span data-ttu-id="41fb2-105">此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。</span><span class="sxs-lookup"><span data-stu-id="41fb2-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="41fb2-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="41fb2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="41fb2-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="41fb2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="41fb2-108">語法</span><span class="sxs-lookup"><span data-stu-id="41fb2-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateDatabaseGrbit
'Usage
Dim instance As CreateDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="41fb2-109">成員</span><span class="sxs-lookup"><span data-stu-id="41fb2-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="41fb2-110">成員名稱</span><span class="sxs-lookup"><span data-stu-id="41fb2-110">Member name</span></span></th>
<th><span data-ttu-id="41fb2-111">描述</span><span class="sxs-lookup"><span data-stu-id="41fb2-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="41fb2-112">無</span><span class="sxs-lookup"><span data-stu-id="41fb2-112">None</span></span></td>
<td><span data-ttu-id="41fb2-113">預設選項。</span><span class="sxs-lookup"><span data-stu-id="41fb2-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="41fb2-114">OverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="41fb2-114">OverwriteExisting</span></span></td>
<td><span data-ttu-id="41fb2-115">根據預設，如果呼叫 JetCreateDatabase，而且資料庫已存在，則 Api 呼叫將會失敗，而且不會覆寫原始資料庫。</span><span class="sxs-lookup"><span data-stu-id="41fb2-115">By default, if JetCreateDatabase is called and the database already exists, the Api call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="41fb2-116">OverwriteExisting 會變更這種行為，而舊的資料庫將會以新的資料庫覆寫。</span><span class="sxs-lookup"><span data-stu-id="41fb2-116">OverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="41fb2-117">RecoveryOff</span><span class="sxs-lookup"><span data-stu-id="41fb2-117">RecoveryOff</span></span></td>
<td><span data-ttu-id="41fb2-118">關閉記錄。</span><span class="sxs-lookup"><span data-stu-id="41fb2-118">Turns off logging.</span></span> <span data-ttu-id="41fb2-119">如此一來，就無法在損毀後重新執行記錄檔並將資料庫復原到一致的可用狀態。</span><span class="sxs-lookup"><span data-stu-id="41fb2-119">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a crash.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="41fb2-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41fb2-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="41fb2-121">參考</span><span class="sxs-lookup"><span data-stu-id="41fb2-121">Reference</span></span>

[<span data-ttu-id="41fb2-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="41fb2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
