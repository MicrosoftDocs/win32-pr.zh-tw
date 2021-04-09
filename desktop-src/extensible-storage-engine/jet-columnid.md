---
description: 深入瞭解： JET_COLUMNID
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be5b8bb64dc9e0fc42055cf5e4d4f67caa7654bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847713"
---
# <a name="jet_columnid"></a><span data-ttu-id="9a904-103">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9a904-103">JET_COLUMNID</span></span>


<span data-ttu-id="9a904-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9a904-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnid"></a><span data-ttu-id="9a904-105">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9a904-105">JET_COLUMNID</span></span>

<span data-ttu-id="9a904-106">**JET_COLUMNID** 資料類型會識別資料表中的資料行。</span><span class="sxs-lookup"><span data-stu-id="9a904-106">The **JET_COLUMNID** data type identifies a column within a table.</span></span>

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a><span data-ttu-id="9a904-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="9a904-107">Data Types</span></span>

<span data-ttu-id="9a904-108">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9a904-108">JET_COLUMNID</span></span>

<span data-ttu-id="9a904-109">識別資料表內的資料行。</span><span class="sxs-lookup"><span data-stu-id="9a904-109">Identifies a column within a table.</span></span>

### <a name="remarks"></a><span data-ttu-id="9a904-110">備註</span><span class="sxs-lookup"><span data-stu-id="9a904-110">Remarks</span></span>

<span data-ttu-id="9a904-111">資料行識別碼在單一資料表中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="9a904-111">Column IDs are unique within a single table.</span></span> <span data-ttu-id="9a904-112">一旦已知資料行有特定的資料行識別碼，它一定會有該資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a904-112">Once a column is known to have a certain column ID, it will always have that column ID.</span></span> <span data-ttu-id="9a904-113">從備份還原將不會變更資料行識別碼的值。</span><span class="sxs-lookup"><span data-stu-id="9a904-113">Restore from backup will not change the value of a column ID.</span></span> <span data-ttu-id="9a904-114">但是，如果在特定資料表資料行之前刪除一或多個資料表資料行，則 compact 資料庫會接著變更資料行識別碼的值。</span><span class="sxs-lookup"><span data-stu-id="9a904-114">However, if one or more table columns, prior to a specific table column, are deleted, a compact database can then change the value of a column ID.</span></span>

<span data-ttu-id="9a904-115">在某些情況下，資料行識別碼是識別資料行的唯一方法。</span><span class="sxs-lookup"><span data-stu-id="9a904-115">In some cases, column IDs are the only means of identifying columns.</span></span> <span data-ttu-id="9a904-116">建立臨時表時，其資料行沒有名稱，但 create 函數會傳回資料行識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="9a904-116">When a temporary table is created, its columns do not have names, but an array of column IDs is returned by the create function.</span></span>

<span data-ttu-id="9a904-117">不同資料表中的資料行可以有相同的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a904-117">Columns in different tables can have the same column ID.</span></span>

### <a name="requirements"></a><span data-ttu-id="9a904-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a904-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a904-119"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="9a904-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9a904-120">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="9a904-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a904-121"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="9a904-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9a904-122">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="9a904-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a904-123"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="9a904-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9a904-124">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="9a904-124">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

