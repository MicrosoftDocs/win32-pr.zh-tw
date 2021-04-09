---
description: Pause 方法會暫停目前的捕獲。
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: 'IDelaydC： (Netmon 的:P ause 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d44ae7792388d9ca637232b45e63d618a37acb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847729"
---
# <a name="idelaydcpause-method"></a><span data-ttu-id="32a8f-103">IDelaydC：:P ause 方法</span><span class="sxs-lookup"><span data-stu-id="32a8f-103">IDelaydC::Pause method</span></span>

<span data-ttu-id="32a8f-104">**Pause** 方法會暫停目前的捕獲。</span><span class="sxs-lookup"><span data-stu-id="32a8f-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="32a8f-105">語法</span><span class="sxs-lookup"><span data-stu-id="32a8f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="32a8f-106">參數</span><span class="sxs-lookup"><span data-stu-id="32a8f-106">Parameters</span></span>

<span data-ttu-id="32a8f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="32a8f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32a8f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="32a8f-108">Return value</span></span>

<span data-ttu-id="32a8f-109">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="32a8f-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="32a8f-110">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="32a8f-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="32a8f-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="32a8f-111">Return code</span></span>                                                                                           | <span data-ttu-id="32a8f-112">Description</span><span class="sxs-lookup"><span data-stu-id="32a8f-112">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="32a8f-113"><dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="32a8f-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="32a8f-114">此捕獲已處於暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="32a8f-114">The capture is already in a paused state.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="32a8f-115"><dt>**NMERR \_ 未 \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="32a8f-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="32a8f-116">NPP 不會捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="32a8f-116">The NPP is not capturing data.</span></span> <span data-ttu-id="32a8f-117">呼叫 [IDelaydC：： start](idelaydc-start.md) 以開始捕獲。</span><span class="sxs-lookup"><span data-stu-id="32a8f-117">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="32a8f-118"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="32a8f-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="32a8f-119">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="32a8f-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="32a8f-120">呼叫 [IDelaydC：： connect](idelaydc-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="32a8f-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="32a8f-121"><dt>**NMERR \_ 未 \_ 延遲**</dt></span><span class="sxs-lookup"><span data-stu-id="32a8f-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="32a8f-122">NPP 已連接到網路，但不是使用 [IDelaydC：： Connect](idelaydc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="32a8f-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="32a8f-123">備註</span><span class="sxs-lookup"><span data-stu-id="32a8f-123">Remarks</span></span>

<span data-ttu-id="32a8f-124">當捕捉處於暫停狀態時，在呼叫 **IDelaydC：： Resume** 方法來重新開機 capture 之前，不會將新的資料加入至目前的 [*capture*](c.md)檔。</span><span class="sxs-lookup"><span data-stu-id="32a8f-124">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="32a8f-125">當 **暫停** 和 **繼續** 用來停止並重新啟動捕獲時，所有捕獲的資訊都會放在相同的捕獲檔案中。</span><span class="sxs-lookup"><span data-stu-id="32a8f-125">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="32a8f-126">使用 **IDelaydC：:P ause** 和 **IDelaydC：： Resume** 來控制捕捉時，網路監視器會在每次執行時繼續新增 [*對話統計資料*](c.md) 。</span><span class="sxs-lookup"><span data-stu-id="32a8f-126">When using **IDelaydC::Pause** and **IDelaydC::Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="32a8f-127">若要重新開機捕獲，請呼叫 [IDelaydC：： Resume](idelaydc-resume.md)。</span><span class="sxs-lookup"><span data-stu-id="32a8f-127">To restart the capture, call [IDelaydC::Resume](idelaydc-resume.md).</span></span>

<span data-ttu-id="32a8f-128">若要停止捕捉，請呼叫 [IDelaydC：： stop](idelaydc-stop.md)。</span><span class="sxs-lookup"><span data-stu-id="32a8f-128">To stop the capture, call [IDelaydC::Stop](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32a8f-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="32a8f-129">Requirements</span></span>



| <span data-ttu-id="32a8f-130">需求</span><span class="sxs-lookup"><span data-stu-id="32a8f-130">Requirement</span></span> | <span data-ttu-id="32a8f-131">值</span><span class="sxs-lookup"><span data-stu-id="32a8f-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32a8f-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32a8f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="32a8f-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32a8f-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="32a8f-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32a8f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="32a8f-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32a8f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="32a8f-136">標頭</span><span class="sxs-lookup"><span data-stu-id="32a8f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="32a8f-137"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="32a8f-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="32a8f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="32a8f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32a8f-139"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32a8f-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32a8f-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32a8f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32a8f-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="32a8f-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="32a8f-142">IDelaydC：： Connect</span><span class="sxs-lookup"><span data-stu-id="32a8f-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="32a8f-143">IDelaydC：： Resume</span><span class="sxs-lookup"><span data-stu-id="32a8f-143">IDelaydC::Resume</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="32a8f-144">IDelaydC：： Start</span><span class="sxs-lookup"><span data-stu-id="32a8f-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="32a8f-145">IDelaydC：： Stop</span><span class="sxs-lookup"><span data-stu-id="32a8f-145">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




