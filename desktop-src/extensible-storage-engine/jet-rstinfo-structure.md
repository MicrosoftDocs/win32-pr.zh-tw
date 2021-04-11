---
description: 深入瞭解： JET_RSTINFO 結構
title: JET_RSTINFO 結構
TOCTitle: JET_RSTINFO Structure
ms:assetid: 2f144d68-dcd9-4d0d-9d9e-a7d2a5c350fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269216(v=EXCHG.10)
ms:contentKeyID: 32765519
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
ms.openlocfilehash: 3a776c84d89dfc97272c65bb0c0684faba814fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112549"
---
# <a name="jet_rstinfo-structure"></a><span data-ttu-id="4fda0-103">JET_RSTINFO 結構</span><span class="sxs-lookup"><span data-stu-id="4fda0-103">JET_RSTINFO Structure</span></span>


<span data-ttu-id="4fda0-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4fda0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_rstinfo-structure"></a><span data-ttu-id="4fda0-105">JET_RSTINFO 結構</span><span class="sxs-lookup"><span data-stu-id="4fda0-105">JET_RSTINFO Structure</span></span>

<span data-ttu-id="4fda0-106">**JET_RSTINFO** 結構包含復原程式的控制資訊，例如資料庫重新配置資訊，以及控制停止復原的能力。</span><span class="sxs-lookup"><span data-stu-id="4fda0-106">The **JET_RSTINFO** structure contains control information for the recovery process like database relocation information and ability to control stopping recovery.</span></span>

<span data-ttu-id="4fda0-107">**Windows Vista：** 在 Windows Vista 中引進 **JET_RSTINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="4fda0-107">**Windows Vista:** The **JET_RSTINFO** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_RSTMAP* rgrstmap;
      long crstmap;
      JET_LGPOS lgposStop;
      JET_LOGTIME logtimeStop;
      JET_PFNSTATUS pfnStatus;
    } JET_RSTINFO;
```

### <a name="members"></a><span data-ttu-id="4fda0-108">成員</span><span class="sxs-lookup"><span data-stu-id="4fda0-108">Members</span></span>

<span data-ttu-id="4fda0-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="4fda0-109">**cbStruct**</span></span>

<span data-ttu-id="4fda0-110">結構的大小。</span><span class="sxs-lookup"><span data-stu-id="4fda0-110">The size of the structure.</span></span>

<span data-ttu-id="4fda0-111">**rgrstmap**</span><span class="sxs-lookup"><span data-stu-id="4fda0-111">**rgrstmap**</span></span>

<span data-ttu-id="4fda0-112">結構，描述已還原資料庫的舊路徑和新路徑。</span><span class="sxs-lookup"><span data-stu-id="4fda0-112">The structure that describes the old and new path of a restored database.</span></span>

<span data-ttu-id="4fda0-113">**crstmap**</span><span class="sxs-lookup"><span data-stu-id="4fda0-113">**crstmap**</span></span>

<span data-ttu-id="4fda0-114">Rgrstmap 中的陣列專案計數。</span><span class="sxs-lookup"><span data-stu-id="4fda0-114">Count of array entries in the rgrstmap.</span></span>

<span data-ttu-id="4fda0-115">**lgposStop**</span><span class="sxs-lookup"><span data-stu-id="4fda0-115">**lgposStop**</span></span>

<span data-ttu-id="4fda0-116">停止復原的記錄位置。</span><span class="sxs-lookup"><span data-stu-id="4fda0-116">The log position to stop recovery at.</span></span> <span data-ttu-id="4fda0-117">不會執行任何復原。</span><span class="sxs-lookup"><span data-stu-id="4fda0-117">No undo will be done.</span></span>

<span data-ttu-id="4fda0-118">**logtimeStop**</span><span class="sxs-lookup"><span data-stu-id="4fda0-118">**logtimeStop**</span></span>

<span data-ttu-id="4fda0-119">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="4fda0-119">Reserved for future use.</span></span>

<span data-ttu-id="4fda0-120">**pfnStatus**</span><span class="sxs-lookup"><span data-stu-id="4fda0-120">**pfnStatus**</span></span>

<span data-ttu-id="4fda0-121">用於報告復原狀態的狀態函數。</span><span class="sxs-lookup"><span data-stu-id="4fda0-121">A status function for reporting status of recovery.</span></span>

### <a name="requirements"></a><span data-ttu-id="4fda0-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fda0-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4fda0-123"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="4fda0-123"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4fda0-124">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="4fda0-124">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fda0-125"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="4fda0-125"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4fda0-126">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="4fda0-126">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fda0-127"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="4fda0-127"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4fda0-128">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="4fda0-128">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fda0-129"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="4fda0-129"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4fda0-130">實作為 <strong>JET_RSTINFO_W</strong> (Unicode) 和 <strong>JET_RSTINFO_A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="4fda0-130">Implemented as <strong>JET_RSTINFO_W</strong> (Unicode) and <strong>JET_RSTINFO_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4fda0-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fda0-131">See Also</span></span>

[<span data-ttu-id="4fda0-132">JetInit3</span><span class="sxs-lookup"><span data-stu-id="4fda0-132">JetInit3</span></span>](./jetinit3-function.md)
