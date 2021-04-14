---
description: 深入瞭解： JET_SNPROG 結構
title: JET_SNPROG 結構
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 961e9cf264652924cfb1d870fa1a04aabc7fb61a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468720"
---
# <a name="jet_snprog-structure"></a><span data-ttu-id="793a6-103">JET_SNPROG 結構</span><span class="sxs-lookup"><span data-stu-id="793a6-103">JET_SNPROG Structure</span></span>


<span data-ttu-id="793a6-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="793a6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snprog-structure"></a><span data-ttu-id="793a6-105">JET_SNPROG 結構</span><span class="sxs-lookup"><span data-stu-id="793a6-105">JET_SNPROG Structure</span></span>

<span data-ttu-id="793a6-106">**JET_SNPROG** 結構包含長時間執行之作業進度的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="793a6-106">The **JET_SNPROG** structure contains information about the progress of a long-running operation.</span></span> <span data-ttu-id="793a6-107">當呼叫回呼函式來通知作業的狀態，而且作業仍在進行時，回呼函式的最後一個參數就是 **JET_SNPROG** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="793a6-107">When the callback function is called to notify the status of the operation and the operation is still in progress, the last parameter of the callback function is a pointer to a **JET_SNPROG** structure.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a><span data-ttu-id="793a6-108">成員</span><span class="sxs-lookup"><span data-stu-id="793a6-108">Members</span></span>

<span data-ttu-id="793a6-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="793a6-109">**cbStruct**</span></span>

<span data-ttu-id="793a6-110">**JET_SNPROG** 結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="793a6-110">The size of the **JET_SNPROG** structure, in bytes.</span></span> <span data-ttu-id="793a6-111">此值會確認下欄欄位是否存在。</span><span class="sxs-lookup"><span data-stu-id="793a6-111">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="793a6-112">**cunitDone**</span><span class="sxs-lookup"><span data-stu-id="793a6-112">**cunitDone**</span></span>

<span data-ttu-id="793a6-113">長時間執行的函式期間已完成的工作單位數目。</span><span class="sxs-lookup"><span data-stu-id="793a6-113">The number of work units that are already completed during the long running function.</span></span>

<span data-ttu-id="793a6-114">**cunitTotal**</span><span class="sxs-lookup"><span data-stu-id="793a6-114">**cunitTotal**</span></span>

<span data-ttu-id="793a6-115">需要完成的工作單位數目。</span><span class="sxs-lookup"><span data-stu-id="793a6-115">The number of work units that need to be completed.</span></span> <span data-ttu-id="793a6-116">此值應該一律大於或等於 **cunitDone**。</span><span class="sxs-lookup"><span data-stu-id="793a6-116">This value should always be bigger than or equal to **cunitDone**.</span></span>

### <a name="requirements"></a><span data-ttu-id="793a6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="793a6-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="793a6-118"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="793a6-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="793a6-119">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="793a6-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="793a6-120"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="793a6-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="793a6-121">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="793a6-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="793a6-122"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="793a6-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="793a6-123">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="793a6-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

