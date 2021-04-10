---
description: 深入瞭解：不正確控制碼常數
title: 不正確控制碼常數
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: f5614b36acfca8b5be4c13849d459d25f984336a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027376"
---
# <a name="invalid-handle-constants"></a><span data-ttu-id="a3402-103">不正確控制碼常數</span><span class="sxs-lookup"><span data-stu-id="a3402-103">Invalid Handle Constants</span></span>


<span data-ttu-id="a3402-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a3402-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="invalid-handle-constants"></a><span data-ttu-id="a3402-105">不正確控制碼常數</span><span class="sxs-lookup"><span data-stu-id="a3402-105">Invalid Handle Constants</span></span>

<span data-ttu-id="a3402-106">下列常數表示 ESE 不同方面的無效控制碼。</span><span class="sxs-lookup"><span data-stu-id="a3402-106">The following constants indicate invalid handles for different aspects of ESE.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3402-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="a3402-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="a3402-108">Description</span><span class="sxs-lookup"><span data-stu-id="a3402-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3402-109">JET_instanceNil</span><span class="sxs-lookup"><span data-stu-id="a3402-109">JET_instanceNil</span></span><br />
<span data-ttu-id="a3402-110"> (~ (JET_INSTANCE) 0) </span><span class="sxs-lookup"><span data-stu-id="a3402-110">(~(JET_INSTANCE)0)</span></span></p></td>
<td><p><span data-ttu-id="a3402-111">資料庫實例的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="a3402-111">An invalid handle for a database instance.</span></span><br /><span data-ttu-id="a3402-112">
<strong>WINDOWS XP：</strong> 在 Windows XP 中引進。</span><span class="sxs-lookup"><span data-stu-id="a3402-112">
<strong>Windows XP:</strong> Introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3402-113">JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="a3402-113">JET_sesidNil</span></span><br />
<span data-ttu-id="a3402-114"> (~ (JET_SESID) 0) </span><span class="sxs-lookup"><span data-stu-id="a3402-114">(~(JET_SESID)0)</span></span></p></td>
<td><p><span data-ttu-id="a3402-115">會話識別碼的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="a3402-115">An invalid handle for a session ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3402-116">JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="a3402-116">JET_tableidNil</span></span><br />
<span data-ttu-id="a3402-117"> (~ (JET_TABLEID) 0) </span><span class="sxs-lookup"><span data-stu-id="a3402-117">(~(JET_TABLEID)0)</span></span></p></td>
<td><p><span data-ttu-id="a3402-118">資料表識別碼的無效控制碼。</span><span class="sxs-lookup"><span data-stu-id="a3402-118">An invalid handle for a table ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3402-119">JET_bitNil</span><span class="sxs-lookup"><span data-stu-id="a3402-119">JET_bitNil</span></span><br />
<span data-ttu-id="a3402-120"> ( (JET_GRBIT) 0) </span><span class="sxs-lookup"><span data-stu-id="a3402-120">((JET_GRBIT)0)</span></span></p></td>
<td><p><span data-ttu-id="a3402-121">位群組的無效控制碼。</span><span class="sxs-lookup"><span data-stu-id="a3402-121">An invalid handle for a group of bits.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3402-122">JET_LSNil</span><span class="sxs-lookup"><span data-stu-id="a3402-122">JET_LSNil</span></span><br />
<span data-ttu-id="a3402-123"> (~ (JET_LS) 0) </span><span class="sxs-lookup"><span data-stu-id="a3402-123">(~(JET_LS)0)</span></span></p></td>
<td><p><span data-ttu-id="a3402-124">本機儲存區的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="a3402-124">An invalid handle for the Local Storage.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3402-125">JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="a3402-125">JET_dbidNil</span></span><br />
<span data-ttu-id="a3402-126"> ( (JET_DBID) 0xFFFFFFFF) </span><span class="sxs-lookup"><span data-stu-id="a3402-126">((JET_DBID) 0xFFFFFFFF)</span></span></p></td>
<td><p><span data-ttu-id="a3402-127">資料庫識別碼的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="a3402-127">An invalid handle for the database ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="a3402-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3402-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3402-129"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="a3402-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a3402-130">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="a3402-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3402-131"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="a3402-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a3402-132">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="a3402-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3402-133"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="a3402-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a3402-134">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="a3402-134">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

