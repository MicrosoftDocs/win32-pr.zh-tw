---
description: 深入瞭解： JET_DBID
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
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
ms.openlocfilehash: fe3a8ccd813ececcb42388c7d577f78e9055d5b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690364"
---
# <a name="jet_dbid"></a><span data-ttu-id="30292-103">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="30292-103">JET_DBID</span></span>


<span data-ttu-id="30292-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="30292-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbid"></a><span data-ttu-id="30292-105">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="30292-105">JET_DBID</span></span>

<span data-ttu-id="30292-106">**JET_DBID** 資料類型包含資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="30292-106">The **JET_DBID** data type contains the handle to the database.</span></span> <span data-ttu-id="30292-107">資料庫控制碼是用來管理資料庫的架構。</span><span class="sxs-lookup"><span data-stu-id="30292-107">A database handle is used to manage the schema of a database.</span></span> <span data-ttu-id="30292-108">它也可以用來管理該資料庫內的資料表。</span><span class="sxs-lookup"><span data-stu-id="30292-108">It can also be used to manage the tables inside of that database.</span></span>

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a><span data-ttu-id="30292-109">資料類型</span><span class="sxs-lookup"><span data-stu-id="30292-109">Data Types</span></span>

<span data-ttu-id="30292-110">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="30292-110">JET_DBID</span></span>

<span data-ttu-id="30292-111">資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="30292-111">Handle to the database.</span></span>

<span data-ttu-id="30292-112">JET_dbidNil 的值表示控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="30292-112">A value of JET_dbidNil indicates that the handle is invalid.</span></span>

### <a name="remarks"></a><span data-ttu-id="30292-113">備註</span><span class="sxs-lookup"><span data-stu-id="30292-113">Remarks</span></span>

<span data-ttu-id="30292-114">資料庫控制碼是透過呼叫 [JetCreateDatabase](./jetcreatedatabase-function.md) 或 [JetOpenDatabase](./jetopendatabase-function.md)來建立。</span><span class="sxs-lookup"><span data-stu-id="30292-114">A database handle is created by means of a call to [JetCreateDatabase](./jetcreatedatabase-function.md) or [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

<span data-ttu-id="30292-115">[JetCloseDatabase](./jetclosedatabase-function.md)可以明確關閉資料庫控制碼，或由[JetEndSession](./jetendsession-function.md)或[JetTerm](./jetterm-function.md)隱含關閉。</span><span class="sxs-lookup"><span data-stu-id="30292-115">A database handle can be explicitly closed by [JetCloseDatabase](./jetclosedatabase-function.md) or implicitly closed by [JetEndSession](./jetendsession-function.md) or [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="30292-116">資料庫控制碼只能在建立它的會話內使用。</span><span class="sxs-lookup"><span data-stu-id="30292-116">A database handle can be used only within the session in which it was created.</span></span> <span data-ttu-id="30292-117">資料庫控制碼是否存在，會對應至資料庫的邏輯開啟。</span><span class="sxs-lookup"><span data-stu-id="30292-117">The existence of a database handle corresponds to the logical open of a database.</span></span> <span data-ttu-id="30292-118">邏輯開啟與資料庫的實體開放式不同，這會在資料庫附加至系統時發生。</span><span class="sxs-lookup"><span data-stu-id="30292-118">A logical open is different from the physical open of a database, which happens when a database is attached to the system.</span></span>

### <a name="requirements"></a><span data-ttu-id="30292-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="30292-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30292-120"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="30292-120"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="30292-121">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="30292-121">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30292-122"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="30292-122"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="30292-123">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="30292-123">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30292-124"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="30292-124"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="30292-125">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="30292-125">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="30292-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30292-126">See Also</span></span>

[<span data-ttu-id="30292-127">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="30292-127">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="30292-128">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="30292-128">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="30292-129">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="30292-129">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="30292-130">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="30292-130">JetEndSession</span></span>](./jetendsession-function.md)
