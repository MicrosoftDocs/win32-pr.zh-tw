---
description: 深入瞭解： JET_HANDLE
title: JET_HANDLE
TOCTitle: JET_HANDLE
ms:assetid: 30748d98-f119-47df-92dd-a8ae8c2761c7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269217(v=EXCHG.10)
ms:contentKeyID: 32765520
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
ms.openlocfilehash: ecb483da26105a0d1f8fbdf0c27561e6d7e8fe26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852268"
---
# <a name="jet_handle"></a><span data-ttu-id="afa01-103">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="afa01-103">JET_HANDLE</span></span>


<span data-ttu-id="afa01-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="afa01-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_handle"></a><span data-ttu-id="afa01-105">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="afa01-105">JET_HANDLE</span></span>

<span data-ttu-id="afa01-106">**JET_HANDLE** 資料類型包含泛型控制碼。</span><span class="sxs-lookup"><span data-stu-id="afa01-106">The **JET_HANDLE** data type contains a generic handle.</span></span>

```cpp
    typedef JET_API_PTR JET_HANDLE;
```

### <a name="data-types"></a><span data-ttu-id="afa01-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="afa01-107">Data Types</span></span>

<span data-ttu-id="afa01-108">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="afa01-108">JET_HANDLE</span></span>

<span data-ttu-id="afa01-109">**Null** 值表示不正確控制碼。</span><span class="sxs-lookup"><span data-stu-id="afa01-109">A value of **NULL** indicates an invalid handle.</span></span>

### <a name="requirements"></a><span data-ttu-id="afa01-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="afa01-110">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="afa01-111"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="afa01-111"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="afa01-112">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="afa01-112">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afa01-113"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="afa01-113"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="afa01-114">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="afa01-114">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afa01-115"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="afa01-115"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="afa01-116">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="afa01-116">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

