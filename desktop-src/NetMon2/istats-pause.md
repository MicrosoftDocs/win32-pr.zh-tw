---
description: Pause 方法會暫時停止目前的捕獲。
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: 'IStats： (Netmon 的:P ause 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d9e9f04ce3d25399866c711dad7a853f2c43c2ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985164"
---
# <a name="istatspause-method"></a><span data-ttu-id="af0ee-103">IStats：:P ause 方法</span><span class="sxs-lookup"><span data-stu-id="af0ee-103">IStats::Pause method</span></span>

<span data-ttu-id="af0ee-104">**Pause** 方法會暫時停止目前的捕獲。</span><span class="sxs-lookup"><span data-stu-id="af0ee-104">The **Pause** method temporarily stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="af0ee-105">語法</span><span class="sxs-lookup"><span data-stu-id="af0ee-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="af0ee-106">參數</span><span class="sxs-lookup"><span data-stu-id="af0ee-106">Parameters</span></span>

<span data-ttu-id="af0ee-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="af0ee-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="af0ee-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="af0ee-108">Return value</span></span>

<span data-ttu-id="af0ee-109">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="af0ee-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="af0ee-110">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="af0ee-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="af0ee-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="af0ee-111">Return code</span></span>                                                                                            | <span data-ttu-id="af0ee-112">Description</span><span class="sxs-lookup"><span data-stu-id="af0ee-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="af0ee-113"><dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="af0ee-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="af0ee-114">此 capture 已經暫停。</span><span class="sxs-lookup"><span data-stu-id="af0ee-114">The capture is already paused.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="af0ee-115"><dt>**NMERR \_ 未 \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="af0ee-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="af0ee-116">NPP 不會捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="af0ee-116">The NPP is not capturing data.</span></span> <span data-ttu-id="af0ee-117">呼叫 [IStats：： start](istats-start.md) 方法來啟動 capture。</span><span class="sxs-lookup"><span data-stu-id="af0ee-117">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="af0ee-118"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="af0ee-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="af0ee-119">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="af0ee-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="af0ee-120">呼叫 [IStats：： connect](istats-connect.md) 方法，將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="af0ee-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="af0ee-121"><dt>**NMERR \_ 不是 \_ 統計資料 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="af0ee-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="af0ee-122">NPP 已連接到網路，但不是使用 [IStats：： Connect](istats-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="af0ee-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="af0ee-123">備註</span><span class="sxs-lookup"><span data-stu-id="af0ee-123">Remarks</span></span>

<span data-ttu-id="af0ee-124">當捕捉暫停時，除非呼叫 [IStats：： Resume](istats-resume.md) 方法重新開機 capture，否則不會捕獲新的框架。</span><span class="sxs-lookup"><span data-stu-id="af0ee-124">While the capture is paused, new frames are not captured until a call to the [IStats::Resume](istats-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="af0ee-125">當您使用 **IStats：:P ause** 和 **IStats：： Resume** 方法來控制捕捉時，網路監視器會在每次執行時繼續新增 [*對話統計資料*](c.md) 。</span><span class="sxs-lookup"><span data-stu-id="af0ee-125">When you use the **IStats::Pause** and **IStats::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="af0ee-126">若要重新開機 capture 呼叫 [IStats：： Resume](istats-resume.md)。</span><span class="sxs-lookup"><span data-stu-id="af0ee-126">To restart the capture call [IStats::Resume](istats-resume.md).</span></span> <span data-ttu-id="af0ee-127">若要停止捕捉，請呼叫 [IStats：： stop](istats-stop.md)。</span><span class="sxs-lookup"><span data-stu-id="af0ee-127">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af0ee-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="af0ee-128">Requirements</span></span>



| <span data-ttu-id="af0ee-129">需求</span><span class="sxs-lookup"><span data-stu-id="af0ee-129">Requirement</span></span> | <span data-ttu-id="af0ee-130">值</span><span class="sxs-lookup"><span data-stu-id="af0ee-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af0ee-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af0ee-131">Minimum supported client</span></span><br/> | <span data-ttu-id="af0ee-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af0ee-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="af0ee-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af0ee-133">Minimum supported server</span></span><br/> | <span data-ttu-id="af0ee-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af0ee-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="af0ee-135">標頭</span><span class="sxs-lookup"><span data-stu-id="af0ee-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="af0ee-136"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="af0ee-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="af0ee-137">DLL</span><span class="sxs-lookup"><span data-stu-id="af0ee-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af0ee-138"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af0ee-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af0ee-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af0ee-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af0ee-140">IStats</span><span class="sxs-lookup"><span data-stu-id="af0ee-140">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="af0ee-141">IStats：： Connect</span><span class="sxs-lookup"><span data-stu-id="af0ee-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="af0ee-142">IStats：： Resume</span><span class="sxs-lookup"><span data-stu-id="af0ee-142">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="af0ee-143">IStats：： Start</span><span class="sxs-lookup"><span data-stu-id="af0ee-143">IStats::Start</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="af0ee-144">IStats：： Stop</span><span class="sxs-lookup"><span data-stu-id="af0ee-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




