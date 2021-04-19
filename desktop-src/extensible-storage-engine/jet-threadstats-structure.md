---
description: 深入瞭解： JET_THREADSTATS 結構
title: JET_THREADSTATS 結構
TOCTitle: JET_THREADSTATS Structure
ms:assetid: 37e86e14-7719-4991-aae8-bcff1baa80df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269227(v=EXCHG.10)
ms:contentKeyID: 32765529
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
ms.openlocfilehash: 2b84de9a4f64db5dda261b8ee177787f62fd01ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979975"
---
# <a name="jet_threadstats-structure"></a><span data-ttu-id="e7ca8-103">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="e7ca8-103">JET_THREADSTATS Structure</span></span>


<span data-ttu-id="e7ca8-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e7ca8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_threadstats-structure"></a><span data-ttu-id="e7ca8-105">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="e7ca8-105">JET_THREADSTATS Structure</span></span>

<span data-ttu-id="e7ca8-106">**JET_THREADSTATS** 結構包含目前線程上資料庫引擎所執行之工作的累計統計資料。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-106">The **JET_THREADSTATS** structure contains cumulative statistics on the work performed by the database engine on the current thread.</span></span> <span data-ttu-id="e7ca8-107">這項資訊會透過 [JetGetThreadStats](./jetgetthreadstats-function.md)傳回。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-107">This information is returned via [JetGetThreadStats](./jetgetthreadstats-function.md).</span></span>

<span data-ttu-id="e7ca8-108">**Windows Vista：**  在 Windows Vista 中引進 **JET_THREADSTATS** 結構。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-108">**Windows Vista:**  The **JET_THREADSTATS** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cPageReferenced;
      unsigned long cPageRead;
      unsigned long cPagePreread;
      unsigned long cPageDirtied;
      unsigned long cPageRedirtied;
      unsigned long cLogRecord;
      unsigned long cbLogRecord;
    } JET_THREADSTATS;
```

### <a name="members"></a><span data-ttu-id="e7ca8-109">成員</span><span class="sxs-lookup"><span data-stu-id="e7ca8-109">Members</span></span>

<span data-ttu-id="e7ca8-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="e7ca8-110">**cbStruct**</span></span>

<span data-ttu-id="e7ca8-111">傳回 **JET_THREADSTATS** 結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-111">The size of the returned **JET_THREADSTATS** structure, in bytes.</span></span>

<span data-ttu-id="e7ca8-112">**注意** **JET_THREADSTATS** 結構會在未來擴充，以包含更多統計資料。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-112">**Note**  The **JET_THREADSTATS** structure will expand in the future to contain more statistics.</span></span> <span data-ttu-id="e7ca8-113">新的統計資料會加入至結構的結尾，而且可以使用增加的輸出緩衝區大小來抓取。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-113">New statistics will be added to the end of the structure and can be retrieved with an increased output buffer size.</span></span> <span data-ttu-id="e7ca8-114">有更多的 **cbStruct** 值可以推斷出額外的統計資料。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-114">The presence of additional statistics can be inferred by a larger **cbStruct** value.</span></span>

<span data-ttu-id="e7ca8-115">**cPageReferenced**</span><span class="sxs-lookup"><span data-stu-id="e7ca8-115">**cPageReferenced**</span></span>

<span data-ttu-id="e7ca8-116">資料庫引擎在目前線程上造訪的資料庫頁面總數。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-116">The total number of database pages visited by the database engine on the current thread.</span></span>

<span data-ttu-id="e7ca8-117">**cPageRead**</span><span class="sxs-lookup"><span data-stu-id="e7ca8-117">**cPageRead**</span></span>

<span data-ttu-id="e7ca8-118">目前線程上資料庫引擎從磁片提取的資料庫頁面總數。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-118">The total number of database pages fetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="e7ca8-119">**cPagePreread**</span><span class="sxs-lookup"><span data-stu-id="e7ca8-119">**cPagePreread**</span></span>

<span data-ttu-id="e7ca8-120">目前線程上的資料庫引擎從磁片預先提取的資料庫頁面總數。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-120">The total number of database pages prefetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="e7ca8-121">**cPageDirtied**</span><span class="sxs-lookup"><span data-stu-id="e7ca8-121">**cPageDirtied**</span></span>

<span data-ttu-id="e7ca8-122">資料庫引擎在目前的執行緒上修改的資料庫頁面總數（沒有不成文變更）。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-122">The total number of database pages, with no unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="e7ca8-123">**cPageRedirtied**</span><span class="sxs-lookup"><span data-stu-id="e7ca8-123">**cPageRedirtied**</span></span>

<span data-ttu-id="e7ca8-124">在目前的執行緒上，資料庫引擎已修改資料庫頁面（具有不成文變更）的總數。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-124">The total number of database pages, with unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="e7ca8-125">**cLogRecord**</span><span class="sxs-lookup"><span data-stu-id="e7ca8-125">**cLogRecord**</span></span>

<span data-ttu-id="e7ca8-126">目前線程上的資料庫引擎所產生的交易記錄檔記錄總數。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-126">The total number of transaction log records that have been generated by the database engine on the current thread.</span></span>

<span data-ttu-id="e7ca8-127">**cbLogRecord**</span><span class="sxs-lookup"><span data-stu-id="e7ca8-127">**cbLogRecord**</span></span>

<span data-ttu-id="e7ca8-128">目前線程上資料庫引擎所產生的交易記錄檔記錄大小總計（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-128">The total size in bytes of transaction log records that have been generated by the database engine on the current thread.</span></span>

### <a name="requirements"></a><span data-ttu-id="e7ca8-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7ca8-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7ca8-130"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="e7ca8-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e7ca8-131">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-131">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7ca8-132"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="e7ca8-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e7ca8-133">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-133">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7ca8-134"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="e7ca8-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e7ca8-135">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="e7ca8-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e7ca8-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7ca8-136">See Also</span></span>

[<span data-ttu-id="e7ca8-137">JetGetThreadStats</span><span class="sxs-lookup"><span data-stu-id="e7ca8-137">JetGetThreadStats</span></span>](./jetgetthreadstats-function.md)
