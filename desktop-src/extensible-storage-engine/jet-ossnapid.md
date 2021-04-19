---
description: 深入瞭解： JET_OSSNAPID
title: JET_OSSNAPID
TOCTitle: JET_OSSNAPID
ms:assetid: 89b15492-674a-46e4-8aea-991df4f22a6f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269325(v=EXCHG.10)
ms:contentKeyID: 32765615
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
ms.openlocfilehash: b0ca1bb5e2e5a80c9166574708efc7875ed95446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990386"
---
# <a name="jet_ossnapid"></a><span data-ttu-id="39466-103">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="39466-103">JET_OSSNAPID</span></span>


<span data-ttu-id="39466-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="39466-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_ossnapid"></a><span data-ttu-id="39466-105">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="39466-105">JET_OSSNAPID</span></span>

<span data-ttu-id="39466-106">**JET_OSSNAPID** 資料類型包含資料庫快照集的控制碼。</span><span class="sxs-lookup"><span data-stu-id="39466-106">The **JET_OSSNAPID** data type contains a handle to a snapshot of the database.</span></span>

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a><span data-ttu-id="39466-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="39466-107">Data Types</span></span>

<span data-ttu-id="39466-108">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="39466-108">JET_OSSNAPID</span></span>

<span data-ttu-id="39466-109">資料庫快照集的控制碼。</span><span class="sxs-lookup"><span data-stu-id="39466-109">A handle to a snapshot of the database.</span></span> <span data-ttu-id="39466-110">此控制碼用於與快照集備份相關的 JET API 元素中。</span><span class="sxs-lookup"><span data-stu-id="39466-110">This handle is used in JET API elements that are involved with snapshot backup.</span></span>

<span data-ttu-id="39466-111">**Null** 可以用來表示不正確控制碼。</span><span class="sxs-lookup"><span data-stu-id="39466-111">**NULL** can be used to indicate an invalid handle.</span></span>

### <a name="requirements"></a><span data-ttu-id="39466-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="39466-112">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39466-113"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="39466-113"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="39466-114">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="39466-114">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39466-115"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="39466-115"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="39466-116">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="39466-116">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39466-117"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="39466-117"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="39466-118">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="39466-118">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

