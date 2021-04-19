---
description: 抓取目前 capture 的會話和工作站資訊。
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: 'IStats：： GetConversationStatistics 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 030fafb4ccf041c2804179f8adf0088ca3fba845
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975568"
---
# <a name="istatsgetconversationstatistics-method"></a><span data-ttu-id="1d4a4-103">IStats：： GetConversationStatistics 方法</span><span class="sxs-lookup"><span data-stu-id="1d4a4-103">IStats::GetConversationStatistics method</span></span>

<span data-ttu-id="1d4a4-104">**GetConversationStatistics** 方法會抓取目前 capture 的會話和站資訊。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-104">The **GetConversationStatistics** method retrieves session and station information about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d4a4-105">語法</span><span class="sxs-lookup"><span data-stu-id="1d4a4-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="1d4a4-106">參數</span><span class="sxs-lookup"><span data-stu-id="1d4a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d4a4-107">*nSessions* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1d4a4-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d4a4-108">DWORD 的指標，其中包含記錄給目前 capture 的 [*會話*](s.md) 數目。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-108">A pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="1d4a4-109">*lpSessionStats* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1d4a4-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d4a4-110">[**SESSIONSTATS**](sessionstats.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-110">A pointer to a [**SESSIONSTATS**](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1d4a4-111">*nStations* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1d4a4-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d4a4-112">DWORD 的指標，其中包含記錄給目前 capture 的 [*電臺*](s.md) 數目。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-112">A pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="1d4a4-113">*lpStationStats* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1d4a4-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d4a4-114">[**STATIONSTATS**](stationstats.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-114">A pointer to a [**STATIONSTATS**](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1d4a4-115">*fClearAfterReading* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1d4a4-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d4a4-116">用來指示網路監視器在抓取目前的資料之後，清除 [**SESSIONSTATS**](sessionstats.md) 和 [**STATIONSTATS**](stationstats.md) 結構內部儲存的旗標。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-116">Flag used to instruct Network Monitor to clear the internal storage of the [**SESSIONSTATS**](sessionstats.md) and [**STATIONSTATS**](stationstats.md) structures after the current data is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d4a4-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d4a4-117">Return value</span></span>

<span data-ttu-id="1d4a4-118">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1d4a4-119">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="1d4a4-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="1d4a4-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1d4a4-120">Return code</span></span>                                                                                                   | <span data-ttu-id="1d4a4-121">Description</span><span class="sxs-lookup"><span data-stu-id="1d4a4-121">Description</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d4a4-122"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="1d4a4-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="1d4a4-123">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="1d4a4-124">呼叫 [**IStats：： connect**](istats-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-124">Call [**IStats::Connect**](istats-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="1d4a4-125"><dt>**NMERR \_ 未 \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="1d4a4-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="1d4a4-126">NPP 不會捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-126">The NPP is not capturing data.</span></span> <span data-ttu-id="1d4a4-127">呼叫 [**IStats：： start**](istats-start.md) 以開始捕獲。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-127">Call [**IStats::Start**](istats-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="1d4a4-128"><dt>**NMERR \_ 不是 \_ 統計資料 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1d4a4-128"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>        | <span data-ttu-id="1d4a4-129">NPP 已連接到網路，但不是使用 [**IStats：： Connect**](istats-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-129">The NPP is connected to the network, but not with the [**IStats::Connect**](istats-connect.md) method.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="1d4a4-130"><dt>**NMERR \_ 沒有 \_ 交談 \_ 統計資料**</dt></span><span class="sxs-lookup"><span data-stu-id="1d4a4-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="1d4a4-131">此連接的設定會設定為 [不儲存對話統計資料]。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="1d4a4-132">若要儲存對話統計資料，請停止 capture，在設定 BLOB 中設定 **NoConversationStats = YES** ，然後重新開機 capture。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-132">To save conversation statistics, stop the capture, set **NoConversationStats = YES** in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1d4a4-133">備註</span><span class="sxs-lookup"><span data-stu-id="1d4a4-133">Remarks</span></span>

<span data-ttu-id="1d4a4-134">只有在資料捕獲進行中時，才可以呼叫此方法;當目前的捕獲暫停時，對此方法的呼叫將不會成功。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-134">This method can be called only while data capture is in progress; when the current capture is paused, a call to this method will not succeed.</span></span>

<span data-ttu-id="1d4a4-135">若要啟動 capture，請呼叫 [**IStats：： start**](istats-start.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-135">To start a capture, call the [**IStats::Start**](istats-start.md) method.</span></span> <span data-ttu-id="1d4a4-136">若要取得其他類型的統計資料，請呼叫 [**IStats：： GetTotalStatistics**](istats-gettotalstatistics.md)。</span><span class="sxs-lookup"><span data-stu-id="1d4a4-136">To retrieve other types of statistics, call [**IStats::GetTotalStatistics**](istats-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d4a4-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d4a4-137">Requirements</span></span>



| <span data-ttu-id="1d4a4-138">需求</span><span class="sxs-lookup"><span data-stu-id="1d4a4-138">Requirement</span></span> | <span data-ttu-id="1d4a4-139">值</span><span class="sxs-lookup"><span data-stu-id="1d4a4-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d4a4-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d4a4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1d4a4-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d4a4-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="1d4a4-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d4a4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1d4a4-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d4a4-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="1d4a4-144">標頭</span><span class="sxs-lookup"><span data-stu-id="1d4a4-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d4a4-145"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="1d4a4-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="1d4a4-146">DLL</span><span class="sxs-lookup"><span data-stu-id="1d4a4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d4a4-147"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d4a4-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d4a4-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d4a4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d4a4-149">**IStats**</span><span class="sxs-lookup"><span data-stu-id="1d4a4-149">**IStats**</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="1d4a4-150">**IStats::GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="1d4a4-150">**IStats::GetTotalStatistics**</span></span>](istats-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="1d4a4-151">**IStats：： Start**</span><span class="sxs-lookup"><span data-stu-id="1d4a4-151">**IStats::Start**</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="1d4a4-152">**IStats：： Connect**</span><span class="sxs-lookup"><span data-stu-id="1d4a4-152">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="1d4a4-153">**SESSIONSTATS**</span><span class="sxs-lookup"><span data-stu-id="1d4a4-153">**SESSIONSTATS**</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="1d4a4-154">**STATIONSTATS**</span><span class="sxs-lookup"><span data-stu-id="1d4a4-154">**STATIONSTATS**</span></span>](stationstats.md)
</dt> </dl>

 

 




