---
description: IDelaydC：： GetConversationStatistics 方法-GetConversationStatistics 方法會抓取目前 capture 的會話和站資訊。
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: 'IDelaydC：： GetConversationStatistics 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d4d4c1bb1ad7ecb45b640c16322e297f9f640ef1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103806"
---
# <a name="idelaydcgetconversationstatistics-method"></a><span data-ttu-id="c29cb-103">IDelaydC：： GetConversationStatistics 方法</span><span class="sxs-lookup"><span data-stu-id="c29cb-103">IDelaydC::GetConversationStatistics method</span></span>

<span data-ttu-id="c29cb-104">**GetConversationStatistics** 方法會抓取目前 capture 的 [*會話*](s.md)和 [*站資訊*](s.md)。</span><span class="sxs-lookup"><span data-stu-id="c29cb-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c29cb-105">語法</span><span class="sxs-lookup"><span data-stu-id="c29cb-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="c29cb-106">參數</span><span class="sxs-lookup"><span data-stu-id="c29cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c29cb-107">*nSessions* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c29cb-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c29cb-108">DWORD 的指標，其中包含記錄給目前 capture 的 [*會話*](s.md) 數目。</span><span class="sxs-lookup"><span data-stu-id="c29cb-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="c29cb-109">*lpSessionStats* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c29cb-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c29cb-110">[SESSIONSTATS](sessionstats.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c29cb-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c29cb-111">*nStations* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c29cb-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c29cb-112">DWORD 的指標，其中包含記錄給目前 capture 的 [*電臺*](s.md) 數目。</span><span class="sxs-lookup"><span data-stu-id="c29cb-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="c29cb-113">*lpStationStats* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c29cb-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c29cb-114">[STATIONSTATS](stationstats.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c29cb-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c29cb-115">*fClearAfterReading* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c29cb-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c29cb-116">用來告知網路監視器在抓取目前資訊之後，清除 [SESSIONSTATS](sessionstats.md) 和 [STATIONSTATS](stationstats.md) 結構內部儲存體的旗標。</span><span class="sxs-lookup"><span data-stu-id="c29cb-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c29cb-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="c29cb-117">Return value</span></span>

<span data-ttu-id="c29cb-118">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="c29cb-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c29cb-119">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="c29cb-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c29cb-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c29cb-120">Return code</span></span>                                                                                                   | <span data-ttu-id="c29cb-121">Description</span><span class="sxs-lookup"><span data-stu-id="c29cb-121">Description</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c29cb-122"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="c29cb-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="c29cb-123">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="c29cb-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="c29cb-124">呼叫 [IDelaydC：： connect](idelaydc-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="c29cb-124">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="c29cb-125"><dt>**NMERR \_ 未 \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="c29cb-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="c29cb-126">NPP 不會捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="c29cb-126">The NPP is not capturing data.</span></span> <span data-ttu-id="c29cb-127">呼叫 [IDelaydC：： start](idelaydc-start.md) 以開始捕獲。</span><span class="sxs-lookup"><span data-stu-id="c29cb-127">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="c29cb-128"><dt>**NMERR \_ 未 \_ 延遲**</dt></span><span class="sxs-lookup"><span data-stu-id="c29cb-128"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>            | <span data-ttu-id="c29cb-129">NPP 已連接到網路，但不是使用 [IDelaydC：： Connect](idelaydc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c29cb-129">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="c29cb-130"><dt>**NMERR \_ 沒有 \_ 交談 \_ 統計資料**</dt></span><span class="sxs-lookup"><span data-stu-id="c29cb-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="c29cb-131">此連接的設定會設定為 [不儲存對話統計資料]。</span><span class="sxs-lookup"><span data-stu-id="c29cb-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="c29cb-132">若要儲存對話統計資料，請停止 capture，在設定 BLOB 中設定 NoConversationStats = YES，然後重新開機 capture。</span><span class="sxs-lookup"><span data-stu-id="c29cb-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c29cb-133">備註</span><span class="sxs-lookup"><span data-stu-id="c29cb-133">Remarks</span></span>

<span data-ttu-id="c29cb-134">只有在資料捕捉正在進行中時，才能呼叫此方法;當目前的捕獲暫停時，對此方法的呼叫將不會成功。</span><span class="sxs-lookup"><span data-stu-id="c29cb-134">This method can only be called only while data capture is in progress; when the current capture is paused, calls to this method will not succeed.</span></span> <span data-ttu-id="c29cb-135">若要啟動 capture，請呼叫 [IDelaydC：： start](idelaydc-start.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c29cb-135">To start a capture, call the [IDelaydC::Start](idelaydc-start.md) method.</span></span>

<span data-ttu-id="c29cb-136">若要取得其他類型的統計資料，請呼叫 [IDelaydC：： GetTotalStatistics](idelaydc-gettotalstatistics.md)。</span><span class="sxs-lookup"><span data-stu-id="c29cb-136">To retrieve other types of statistics, call [IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c29cb-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="c29cb-137">Requirements</span></span>



| <span data-ttu-id="c29cb-138">需求</span><span class="sxs-lookup"><span data-stu-id="c29cb-138">Requirement</span></span> | <span data-ttu-id="c29cb-139">值</span><span class="sxs-lookup"><span data-stu-id="c29cb-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c29cb-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c29cb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c29cb-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c29cb-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c29cb-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c29cb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c29cb-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c29cb-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c29cb-144">標頭</span><span class="sxs-lookup"><span data-stu-id="c29cb-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c29cb-145"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="c29cb-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c29cb-146">DLL</span><span class="sxs-lookup"><span data-stu-id="c29cb-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c29cb-147"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c29cb-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c29cb-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c29cb-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c29cb-149">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="c29cb-149">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="c29cb-150">IDelaydC：： Connect</span><span class="sxs-lookup"><span data-stu-id="c29cb-150">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="c29cb-151">IDelaydC::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="c29cb-151">IDelaydC::GetTotalStatistics</span></span>](idelaydc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="c29cb-152">IDelaydC：： Start</span><span class="sxs-lookup"><span data-stu-id="c29cb-152">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="c29cb-153">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="c29cb-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="c29cb-154">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="c29cb-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




