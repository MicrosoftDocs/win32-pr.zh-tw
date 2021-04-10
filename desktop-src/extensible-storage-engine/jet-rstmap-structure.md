---
description: 深入瞭解： JET_RSTMAP 結構
title: JET_RSTMAP 結構
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
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
ms.openlocfilehash: 646a055230b6476abf70abcde582fc2015cb241c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689955"
---
# <a name="jet_rstmap-structure"></a><span data-ttu-id="52f15-103">JET_RSTMAP 結構</span><span class="sxs-lookup"><span data-stu-id="52f15-103">JET_RSTMAP Structure</span></span>


<span data-ttu-id="52f15-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="52f15-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_rstmap-structure"></a><span data-ttu-id="52f15-105">JET_RSTMAP 結構</span><span class="sxs-lookup"><span data-stu-id="52f15-105">JET_RSTMAP Structure</span></span>

<span data-ttu-id="52f15-106">當 [JetInit](./jetinit-function.md)和 [JetExternalRestore](./jetexternalrestore-function.md)函式使用時， **JET_RSTMAP** 結構可重新對應儲存在交易記錄檔中的資料庫檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="52f15-106">The **JET_RSTMAP** structure enables the remapping of database file paths that are stored in the transaction logs during recovery, when used by the [JetInit](./jetinit-function.md) and [JetExternalRestore](./jetexternalrestore-function.md) functions.</span></span> <span data-ttu-id="52f15-107">這可讓您在離線或從備份還原時，移動資料庫。</span><span class="sxs-lookup"><span data-stu-id="52f15-107">This enables the databases to be moved when offline or when restored from backup.</span></span>

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a><span data-ttu-id="52f15-108">成員</span><span class="sxs-lookup"><span data-stu-id="52f15-108">Members</span></span>

<span data-ttu-id="52f15-109">**szDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="52f15-109">**szDatabaseName**</span></span>

<span data-ttu-id="52f15-110">在復原期間，與交易記錄檔相關聯之資料庫的目前絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="52f15-110">The current absolute path of a database that is associated with the transaction logs that are replayed during recovery.</span></span>

<span data-ttu-id="52f15-111">**szNewDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="52f15-111">**szNewDatabaseName**</span></span>

<span data-ttu-id="52f15-112">資料庫的新絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="52f15-112">The new absolute path for the database.</span></span>

### <a name="requirements"></a><span data-ttu-id="52f15-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="52f15-113">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52f15-114"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="52f15-114"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="52f15-115">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="52f15-115">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52f15-116"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="52f15-116"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="52f15-117">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="52f15-117">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52f15-118"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="52f15-118"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="52f15-119">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="52f15-119">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52f15-120"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="52f15-120"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="52f15-121">實作為 <strong>JET_RSTMAP_W</strong> (Unicode) 和 <strong>JET_RSTMAP_A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="52f15-121">Implemented as <strong>JET_RSTMAP_W</strong> (Unicode) and <strong>JET_RSTMAP_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="52f15-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52f15-122">See Also</span></span>

[<span data-ttu-id="52f15-123">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="52f15-123">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="52f15-124">JetInit</span><span class="sxs-lookup"><span data-stu-id="52f15-124">JetInit</span></span>](./jetinit-function.md)
