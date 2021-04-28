---
description: IRTC：:P ause 方法-Pause 方法會暫停目前的捕獲。
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: 'IRTC： (Netmon 的:P ause 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d42af1912365a4237889e4e46d0fb3343377c772
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110676"
---
# <a name="irtcpause-method"></a><span data-ttu-id="07544-103">IRTC：:P ause 方法</span><span class="sxs-lookup"><span data-stu-id="07544-103">IRTC::Pause method</span></span>

<span data-ttu-id="07544-104">**Pause** 方法會暫停目前的捕獲。</span><span class="sxs-lookup"><span data-stu-id="07544-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="07544-105">語法</span><span class="sxs-lookup"><span data-stu-id="07544-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="07544-106">參數</span><span class="sxs-lookup"><span data-stu-id="07544-106">Parameters</span></span>

<span data-ttu-id="07544-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="07544-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07544-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="07544-108">Return value</span></span>

<span data-ttu-id="07544-109">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="07544-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="07544-110">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="07544-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="07544-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="07544-111">Return code</span></span>                                                                                           | <span data-ttu-id="07544-112">Description</span><span class="sxs-lookup"><span data-stu-id="07544-112">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="07544-113"><dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="07544-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="07544-114">此 capture 已經暫停。</span><span class="sxs-lookup"><span data-stu-id="07544-114">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="07544-115"><dt>**NMERR \_ 未 \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="07544-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="07544-116">NPP 不會捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="07544-116">The NPP is not capturing data.</span></span> <span data-ttu-id="07544-117">呼叫 [IRTC：： start](irtc-start.md) 以開始捕獲。</span><span class="sxs-lookup"><span data-stu-id="07544-117">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="07544-118"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="07544-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="07544-119">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="07544-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="07544-120">呼叫 [IRTC：： connect](irtc-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="07544-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="07544-121"><dt>**NMERR \_ 無法 \_ 即時**</dt></span><span class="sxs-lookup"><span data-stu-id="07544-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="07544-122">NPP 已連接到網路，但不是使用 [IRTC：： Connect](irtc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="07544-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="07544-123">備註</span><span class="sxs-lookup"><span data-stu-id="07544-123">Remarks</span></span>

<span data-ttu-id="07544-124">當捕捉處於暫停狀態時，在呼叫 [IRTC：： Resume](irtc-resume.md) 方法以重新開機 capture 之前，不會先建立新的框架。</span><span class="sxs-lookup"><span data-stu-id="07544-124">While the capture is in a paused state, new frames are not captured until the [IRTC::Resume](irtc-resume.md) method is called to restart the capture.</span></span>

<span data-ttu-id="07544-125">當您使用 **IRTC：:P ause** 和 **IRTC：： Resume** 方法來控制捕捉時，網路監視器會在每次執行時繼續新增 [*對話統計資料*](c.md) 。</span><span class="sxs-lookup"><span data-stu-id="07544-125">When you use the **IRTC::Pause** and **IRTC::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="07544-126">若要重新開機 capture 呼叫 [IRTC：： Resume](irtc-resume.md)。</span><span class="sxs-lookup"><span data-stu-id="07544-126">To restart the capture call [IRTC::Resume](irtc-resume.md).</span></span> <span data-ttu-id="07544-127">若要停止捕捉，請呼叫 [IRTC：： stop](irtc-stop.md)。</span><span class="sxs-lookup"><span data-stu-id="07544-127">To stop the capture, call [IRTC::Stop](irtc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07544-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="07544-128">Requirements</span></span>



| <span data-ttu-id="07544-129">需求</span><span class="sxs-lookup"><span data-stu-id="07544-129">Requirement</span></span> | <span data-ttu-id="07544-130">值</span><span class="sxs-lookup"><span data-stu-id="07544-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07544-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07544-131">Minimum supported client</span></span><br/> | <span data-ttu-id="07544-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07544-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="07544-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07544-133">Minimum supported server</span></span><br/> | <span data-ttu-id="07544-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07544-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="07544-135">標頭</span><span class="sxs-lookup"><span data-stu-id="07544-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="07544-136"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="07544-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="07544-137">DLL</span><span class="sxs-lookup"><span data-stu-id="07544-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07544-138"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07544-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07544-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07544-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07544-140">IRTC</span><span class="sxs-lookup"><span data-stu-id="07544-140">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="07544-141">IRTC：： Connect</span><span class="sxs-lookup"><span data-stu-id="07544-141">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="07544-142">IRTC：： Resume</span><span class="sxs-lookup"><span data-stu-id="07544-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="07544-143">IRTC：： Start</span><span class="sxs-lookup"><span data-stu-id="07544-143">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="07544-144">IRTC：： Stop</span><span class="sxs-lookup"><span data-stu-id="07544-144">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




