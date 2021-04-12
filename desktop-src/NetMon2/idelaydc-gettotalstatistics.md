---
description: GetTotalStatistics 方法會抓取目前 capture 的統計資料總計。
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: 'IDelaydC：： GetTotalStatistics 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0d194426933532fcf7a1965ed59b099489eefcb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386100"
---
# <a name="idelaydcgettotalstatistics-method"></a><span data-ttu-id="4fad2-103">IDelaydC：： GetTotalStatistics 方法</span><span class="sxs-lookup"><span data-stu-id="4fad2-103">IDelaydC::GetTotalStatistics method</span></span>

<span data-ttu-id="4fad2-104">**GetTotalStatistics** 方法會 [*抓取目前 capture*](c.md)的 [*統計資料總計*](t.md)。</span><span class="sxs-lookup"><span data-stu-id="4fad2-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4fad2-105">語法</span><span class="sxs-lookup"><span data-stu-id="4fad2-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="4fad2-106">參數</span><span class="sxs-lookup"><span data-stu-id="4fad2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fad2-107">*lpStats* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4fad2-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fad2-108">[統計資料](statistics.md)結構的指標，此結構會提供捕獲的統計資料總計。</span><span class="sxs-lookup"><span data-stu-id="4fad2-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="4fad2-109">呼叫端負責配置和釋放 **統計資料** 結構所使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4fad2-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="4fad2-110">*fClearAfterReading* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4fad2-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fad2-111">用來告訴網路監視器如何處理統計資料總計的內部儲存體的旗標。</span><span class="sxs-lookup"><span data-stu-id="4fad2-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="4fad2-112">設定為 [ **TRUE** ] 會告知網路監視器在抓取目前的資訊之後，清除總統計資料的內部儲存體。</span><span class="sxs-lookup"><span data-stu-id="4fad2-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fad2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4fad2-113">Return value</span></span>

<span data-ttu-id="4fad2-114">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="4fad2-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4fad2-115">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="4fad2-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="4fad2-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4fad2-116">Return code</span></span>                                                                                          | <span data-ttu-id="4fad2-117">Description</span><span class="sxs-lookup"><span data-stu-id="4fad2-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4fad2-118"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="4fad2-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="4fad2-119">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="4fad2-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="4fad2-120">呼叫 [IDelaydC：： connect](idelaydc-connect.md) 以連接到網路。</span><span class="sxs-lookup"><span data-stu-id="4fad2-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="4fad2-121"><dt>**NMERR \_ 未 \_ 延遲**</dt></span><span class="sxs-lookup"><span data-stu-id="4fad2-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="4fad2-122">NPP 已連接到網路，但不是使用 [IDelaydC：： Connect](idelaydc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4fad2-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="4fad2-123"><dt>**NMERR \_ 未 \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="4fad2-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="4fad2-124">NPP 不會捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="4fad2-124">The NPP is not capturing data.</span></span> <span data-ttu-id="4fad2-125">呼叫 [IDelaydC：： start](idelaydc-start.md) 以開始捕獲資料。</span><span class="sxs-lookup"><span data-stu-id="4fad2-125">Call [IDelaydC::Start](idelaydc-start.md) to start capturing data.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="4fad2-126">備註</span><span class="sxs-lookup"><span data-stu-id="4fad2-126">Remarks</span></span>

<span data-ttu-id="4fad2-127">只有在正在進行捕捉時，此方法才會傳回資料;當捕捉暫停時，對此方法的呼叫將不會成功。</span><span class="sxs-lookup"><span data-stu-id="4fad2-127">This method returns data only while a capture is in progress; when the capture is paused, calls to this method will not succeed.</span></span>

<span data-ttu-id="4fad2-128">網路監視器也會儲存 [*對話統計資料*](c.md)，您可以藉由呼叫 [IDelaydC：： GetConversationStatistics](idelaydc-getconversationstatistics.md) 方法來加以取出。</span><span class="sxs-lookup"><span data-stu-id="4fad2-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fad2-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fad2-129">Requirements</span></span>



| <span data-ttu-id="4fad2-130">需求</span><span class="sxs-lookup"><span data-stu-id="4fad2-130">Requirement</span></span> | <span data-ttu-id="4fad2-131">值</span><span class="sxs-lookup"><span data-stu-id="4fad2-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fad2-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4fad2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4fad2-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fad2-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="4fad2-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4fad2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4fad2-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fad2-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="4fad2-136">標頭</span><span class="sxs-lookup"><span data-stu-id="4fad2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fad2-137"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="4fad2-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="4fad2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4fad2-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fad2-139"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fad2-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fad2-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fad2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fad2-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="4fad2-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="4fad2-142">IDelaydC：： Connect</span><span class="sxs-lookup"><span data-stu-id="4fad2-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="4fad2-143">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="4fad2-143">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="4fad2-144">IDelaydC：： Start</span><span class="sxs-lookup"><span data-stu-id="4fad2-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="4fad2-145">統計</span><span class="sxs-lookup"><span data-stu-id="4fad2-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




