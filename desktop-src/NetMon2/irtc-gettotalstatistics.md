---
description: GetTotalStatistics 方法會抓取目前 capture 的統計資料總計。
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: 'IRTC：： GetTotalStatistics 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 27128048b4326aae14ae6a2e2e6c0540b1105538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989339"
---
# <a name="irtcgettotalstatistics-method"></a><span data-ttu-id="29402-103">IRTC：： GetTotalStatistics 方法</span><span class="sxs-lookup"><span data-stu-id="29402-103">IRTC::GetTotalStatistics method</span></span>

<span data-ttu-id="29402-104">**GetTotalStatistics** 方法會 [*抓取目前 capture*](c.md)的 [*統計資料總計*](t.md)。</span><span class="sxs-lookup"><span data-stu-id="29402-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="29402-105">語法</span><span class="sxs-lookup"><span data-stu-id="29402-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="29402-106">參數</span><span class="sxs-lookup"><span data-stu-id="29402-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29402-107">*lpStats* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="29402-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29402-108">[統計資料](statistics.md)結構的指標，此結構會提供捕獲的統計資料總計。</span><span class="sxs-lookup"><span data-stu-id="29402-108">Pointer to a [STATISTICS](statistics.md) structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="29402-109">呼叫端負責配置和釋放 **統計資料** 結構所使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="29402-109">It is the callers responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="29402-110">*fClearAfterReading* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29402-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29402-111">用來告訴網路監視器如何處理統計資料總計的內部儲存體的旗標。</span><span class="sxs-lookup"><span data-stu-id="29402-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="29402-112">設定為 [ **TRUE** ] 會告知網路監視器在抓取目前的資訊之後，清除總統計資料的內部儲存體。</span><span class="sxs-lookup"><span data-stu-id="29402-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29402-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="29402-113">Return value</span></span>

<span data-ttu-id="29402-114">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="29402-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="29402-115">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="29402-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="29402-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="29402-116">Return code</span></span>                                                                                          | <span data-ttu-id="29402-117">Description</span><span class="sxs-lookup"><span data-stu-id="29402-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="29402-118"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="29402-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="29402-119">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="29402-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="29402-120">呼叫 [IRTC：： connect](irtc-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="29402-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="29402-121"><dt>**NMERR \_ 無法 \_ 即時**</dt></span><span class="sxs-lookup"><span data-stu-id="29402-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="29402-122">NPP 已連接到網路，但不是使用 [IRTC：： Connect](irtc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="29402-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |
| <dl> <span data-ttu-id="29402-123"><dt>**NMERR \_ 未 \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="29402-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="29402-124">NPP 不會捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="29402-124">The NPP is not capturing data.</span></span> <span data-ttu-id="29402-125">呼叫 [IRTC：： start](irtc-start.md) 以開始捕獲資料。</span><span class="sxs-lookup"><span data-stu-id="29402-125">Call [IRTC::Start](irtc-start.md) to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="29402-126">備註</span><span class="sxs-lookup"><span data-stu-id="29402-126">Remarks</span></span>

<span data-ttu-id="29402-127">只有在正在進行捕捉時，此方法才會傳回資料，包括在暫停時暫停。</span><span class="sxs-lookup"><span data-stu-id="29402-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="29402-128">網路監視器也會儲存 [*對話統計資料*](c.md)。</span><span class="sxs-lookup"><span data-stu-id="29402-128">Network Monitor also stores [*conversation statistics*](c.md).</span></span> <span data-ttu-id="29402-129">若要取得對話統計資料，請呼叫 [IRTC：： GetConversationStatistics](irtc-getconversationstatistics.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="29402-129">To retrieve conversation statistics, call the [IRTC::GetConversationStatistics](irtc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="29402-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="29402-130">Requirements</span></span>



| <span data-ttu-id="29402-131">需求</span><span class="sxs-lookup"><span data-stu-id="29402-131">Requirement</span></span> | <span data-ttu-id="29402-132">值</span><span class="sxs-lookup"><span data-stu-id="29402-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29402-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29402-133">Minimum supported client</span></span><br/> | <span data-ttu-id="29402-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29402-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="29402-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29402-135">Minimum supported server</span></span><br/> | <span data-ttu-id="29402-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29402-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="29402-137">標頭</span><span class="sxs-lookup"><span data-stu-id="29402-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="29402-138"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="29402-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="29402-139">DLL</span><span class="sxs-lookup"><span data-stu-id="29402-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29402-140"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29402-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29402-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29402-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29402-142">IRTC</span><span class="sxs-lookup"><span data-stu-id="29402-142">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="29402-143">IRTC：： Connect</span><span class="sxs-lookup"><span data-stu-id="29402-143">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="29402-144">IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="29402-144">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="29402-145">IRTC：： Start</span><span class="sxs-lookup"><span data-stu-id="29402-145">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="29402-146">統計</span><span class="sxs-lookup"><span data-stu-id="29402-146">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




