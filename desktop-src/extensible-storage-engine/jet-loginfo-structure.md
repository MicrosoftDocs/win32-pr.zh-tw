---
description: 深入瞭解： JET_LOGINFO 結構
title: JET_LOGINFO 結構
TOCTitle: JET_LOGINFO Structure
ms:assetid: b34b3f24-5d19-4e11-a657-a0e59204d628
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294063(v=EXCHG.10)
ms:contentKeyID: 32765678
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
ms.openlocfilehash: b7e643d775d1fb8e0c19286bfb7a50d887644e99
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106982052"
---
# <a name="jet_loginfo-structure"></a><span data-ttu-id="ba676-103">JET_LOGINFO 結構</span><span class="sxs-lookup"><span data-stu-id="ba676-103">JET_LOGINFO Structure</span></span>


<span data-ttu-id="ba676-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ba676-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_loginfo-structure"></a><span data-ttu-id="ba676-105">JET_LOGINFO 結構</span><span class="sxs-lookup"><span data-stu-id="ba676-105">JET_LOGINFO Structure</span></span>

<span data-ttu-id="ba676-106">**JET_LOGINFO** 結構會傳回一組交易記錄檔的結構化資訊，這些記錄檔應該是備份檔案集的一部分。</span><span class="sxs-lookup"><span data-stu-id="ba676-106">The **JET_LOGINFO** structure returns structured information about the set of transaction log files that should be a part of a backup file set.</span></span> <span data-ttu-id="ba676-107">**JET_LOGINFO** 結構是一組最基本的資訊，需要用來表示以 [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md)抓取的一系列記錄，或針對使用 [JetExternalRestore2](./jetexternalrestore2-function.md)進行硬復原的指定。</span><span class="sxs-lookup"><span data-stu-id="ba676-107">The **JET_LOGINFO** structure is the minimal set of information needed to represent a range of logs that is retrieved with [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) or specified for a hard recovery with [JetExternalRestore2](./jetexternalrestore2-function.md).</span></span>

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a><span data-ttu-id="ba676-108">成員</span><span class="sxs-lookup"><span data-stu-id="ba676-108">Members</span></span>

<span data-ttu-id="ba676-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="ba676-109">**cbSize**</span></span>

<span data-ttu-id="ba676-110">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ba676-110">The size of the structure, in bytes.</span></span>

<span data-ttu-id="ba676-111">這個成員可以在未來擴充此結構，同時啟用回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="ba676-111">This member enables future expansion of this structure while enabling backwards compatibility.</span></span> <span data-ttu-id="ba676-112">它應該一律設定為 sizeof ( JET_LOGINFO ) 。</span><span class="sxs-lookup"><span data-stu-id="ba676-112">It should always be set to sizeof( JET_LOGINFO ).</span></span>

<span data-ttu-id="ba676-113">**ulGenLow**</span><span class="sxs-lookup"><span data-stu-id="ba676-113">**ulGenLow**</span></span>

<span data-ttu-id="ba676-114">還原的最低 (或最舊的) 記錄檔編號。</span><span class="sxs-lookup"><span data-stu-id="ba676-114">The lowest (or oldest) log file number that is restored.</span></span> <span data-ttu-id="ba676-115">不帶正負號長度的完整精確度應該保留下來，但在目前的引擎版本中，這個數位是從0x00000 到0xFFFFF 的範圍內的十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="ba676-115">The full fidelity of an unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="ba676-116">這可能會在未來的版本中變更。</span><span class="sxs-lookup"><span data-stu-id="ba676-116">This might change in future versions.</span></span>

<span data-ttu-id="ba676-117">**ulGenHigh**</span><span class="sxs-lookup"><span data-stu-id="ba676-117">**ulGenHigh**</span></span>

<span data-ttu-id="ba676-118">還原的最高 (或最新的) 記錄檔編號。</span><span class="sxs-lookup"><span data-stu-id="ba676-118">The highest (or most recent) log file number that is restored.</span></span> <span data-ttu-id="ba676-119">不帶正負號長度的完整精確度應該保留，但在目前的引擎版本中，這個數位是從0x00000 到0xFFFFF 的十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="ba676-119">The full fidelity of a unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="ba676-120">這可能會在未來的版本中變更。</span><span class="sxs-lookup"><span data-stu-id="ba676-120">This might change in future versions.</span></span>

<span data-ttu-id="ba676-121">**szBaseName**</span><span class="sxs-lookup"><span data-stu-id="ba676-121">**szBaseName**</span></span>

<span data-ttu-id="ba676-122">用來命名交易記錄檔的前置詞。</span><span class="sxs-lookup"><span data-stu-id="ba676-122">The prefix used to name the transaction log files.</span></span>

<span data-ttu-id="ba676-123">這個成員傳回的值一律等於產生此資訊之實例 [JET_paramBaseName](./transaction-log-parameters.md) 的設定。</span><span class="sxs-lookup"><span data-stu-id="ba676-123">The value that is returned in this member is always equal to the setting for [JET_paramBaseName](./transaction-log-parameters.md) for the instance that generated this information.</span></span>

### <a name="remarks"></a><span data-ttu-id="ba676-124">備註</span><span class="sxs-lookup"><span data-stu-id="ba676-124">Remarks</span></span>

<span data-ttu-id="ba676-125">交易記錄檔會根據實例的基底名稱和記錄檔的產生編號來命名。</span><span class="sxs-lookup"><span data-stu-id="ba676-125">Transaction log files are named according to the instance base name and the generation number of the log file.</span></span> <span data-ttu-id="ba676-126">名稱的格式為 BBBXXXXX。日誌。</span><span class="sxs-lookup"><span data-stu-id="ba676-126">The name is of the format BBBXXXXX.LOG.</span></span> <span data-ttu-id="ba676-127">BBB 會對應至記錄檔的基底名稱，且長度一律為三個字元。</span><span class="sxs-lookup"><span data-stu-id="ba676-127">BBB corresponds to the base name for the log file and is always three characters in length.</span></span> <span data-ttu-id="ba676-128">XXXXX 對應到記錄檔的產生編號（以零填補的十六進位形式），且長度一律為五個字元。</span><span class="sxs-lookup"><span data-stu-id="ba676-128">XXXXX corresponds to the generation number of the log file in zero padded hexadecimal and is always five characters in length.</span></span> <span data-ttu-id="ba676-129">記錄檔是由引擎永遠提供給交易記錄檔的副檔名。</span><span class="sxs-lookup"><span data-stu-id="ba676-129">LOG is the file extension that is always given to transaction log files by the engine.</span></span>

<span data-ttu-id="ba676-130">建議您不要使用此結構化資訊，因為它會讓應用程式對交易記錄檔的這個命名配置具有透徹的瞭解。</span><span class="sxs-lookup"><span data-stu-id="ba676-130">Use of this structured information is discouraged because it causes the application to have intimate knowledge of this naming scheme for transaction log files.</span></span> <span data-ttu-id="ba676-131">如果未來的命名配置變更，則這種應用程式將無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="ba676-131">If the naming scheme ever changes in the future then such an application will no longer function properly.</span></span> <span data-ttu-id="ba676-132">您可以想像，記錄格式將會變更為在未來加入8個十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="ba676-132">It is conceivable that the log format will change to incorporate 8 hex digits in the future.</span></span> <span data-ttu-id="ba676-133">應用程式應該改為使用 [JetGetLogInfo](./jetgetloginfo-function.md) 所傳回之檔案名的明確清單。</span><span class="sxs-lookup"><span data-stu-id="ba676-133">Applications should use the explicit list of file names returned by [JetGetLogInfo](./jetgetloginfo-function.md) instead.</span></span>

### <a name="requirements"></a><span data-ttu-id="ba676-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba676-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba676-135"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="ba676-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ba676-136">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="ba676-136">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba676-137"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="ba676-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ba676-138">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="ba676-138">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba676-139"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="ba676-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ba676-140">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="ba676-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba676-141"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ba676-141"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ba676-142">實作為 <strong>JET_LOGINFO_W</strong> (Unicode) 和 <strong>JET_LOGINFO_A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="ba676-142">Implemented as <strong>JET_LOGINFO_W</strong> (Unicode) and <strong>JET_LOGINFO_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ba676-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba676-143">See Also</span></span>

[<span data-ttu-id="ba676-144">JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="ba676-144">JetExternalRestore2</span></span>](./jetexternalrestore2-function.md)  
[<span data-ttu-id="ba676-145">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="ba676-145">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="ba676-146">JetGetLogInfoInstance2</span><span class="sxs-lookup"><span data-stu-id="ba676-146">JetGetLogInfoInstance2</span></span>](./jetgetloginfoinstance2-function.md)  
[<span data-ttu-id="ba676-147">系統參數</span><span class="sxs-lookup"><span data-stu-id="ba676-147">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
