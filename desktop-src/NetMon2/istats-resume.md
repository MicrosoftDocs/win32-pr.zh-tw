---
description: Resume 方法會重新開機已暫停的捕獲。
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: 'IStats：： Resume 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: db84f51d2a2a2c2d15e3b4164fe1fac09e72bf20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850904"
---
# <a name="istatsresume-method"></a><span data-ttu-id="5f2fc-103">IStats：： Resume 方法</span><span class="sxs-lookup"><span data-stu-id="5f2fc-103">IStats::Resume method</span></span>

<span data-ttu-id="5f2fc-104">**Resume** 方法會重新開機已暫停的捕獲。</span><span class="sxs-lookup"><span data-stu-id="5f2fc-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f2fc-105">語法</span><span class="sxs-lookup"><span data-stu-id="5f2fc-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="5f2fc-106">參數</span><span class="sxs-lookup"><span data-stu-id="5f2fc-106">Parameters</span></span>

<span data-ttu-id="5f2fc-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5f2fc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f2fc-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f2fc-108">Return value</span></span>

<span data-ttu-id="5f2fc-109">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="5f2fc-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5f2fc-110">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="5f2fc-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="5f2fc-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5f2fc-111">Return code</span></span>                                                                                                | <span data-ttu-id="5f2fc-112">Description</span><span class="sxs-lookup"><span data-stu-id="5f2fc-112">Description</span></span>                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5f2fc-113"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="5f2fc-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="5f2fc-114">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="5f2fc-114">The NPP is not connected to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="5f2fc-115"><dt>**NMERR \_ CAPTURE \_ 未 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="5f2fc-115"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="5f2fc-116">捕捉未暫停。</span><span class="sxs-lookup"><span data-stu-id="5f2fc-116">The capture is not paused.</span></span> <span data-ttu-id="5f2fc-117">呼叫 [IStats：:P ause](istats-pause.md) 方法以暫時停止捕捉。</span><span class="sxs-lookup"><span data-stu-id="5f2fc-117">Call the [IStats::Pause](istats-pause.md) method to temporarily stop the capture.</span></span><br/>                     |
| <dl> <span data-ttu-id="5f2fc-118"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="5f2fc-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="5f2fc-119">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="5f2fc-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="5f2fc-120">呼叫 [IStats：： connect](istats-connect.md) 方法，將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="5f2fc-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="5f2fc-121"><dt>**NMERR \_ 不是 \_ 統計資料 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f2fc-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>     | <span data-ttu-id="5f2fc-122">NPP 已連接到網路，但不是使用 [IStats：： Connect](istats-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5f2fc-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="5f2fc-123">備註</span><span class="sxs-lookup"><span data-stu-id="5f2fc-123">Remarks</span></span>

<span data-ttu-id="5f2fc-124">當捕捉處於暫停狀態時，在呼叫 IStats：： Resume 方法來重新開機 capture 之前，不會捕獲新的資料。</span><span class="sxs-lookup"><span data-stu-id="5f2fc-124">While the capture is in a paused state, new data is not captured until the IStats::Resume method is called to restart the capture.</span></span>

<span data-ttu-id="5f2fc-125">使用 **Pause** 和 **Resume** 方法來控制捕捉時，網路監視器會繼續將 [*對話統計資料*](c.md) 新增至目前 capture 的現有統計資料。</span><span class="sxs-lookup"><span data-stu-id="5f2fc-125">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="5f2fc-126">若要停止捕捉，請呼叫 [IStats：： stop](istats-stop.md)。</span><span class="sxs-lookup"><span data-stu-id="5f2fc-126">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f2fc-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f2fc-127">Requirements</span></span>



| <span data-ttu-id="5f2fc-128">需求</span><span class="sxs-lookup"><span data-stu-id="5f2fc-128">Requirement</span></span> | <span data-ttu-id="5f2fc-129">值</span><span class="sxs-lookup"><span data-stu-id="5f2fc-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f2fc-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f2fc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5f2fc-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f2fc-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="5f2fc-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f2fc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5f2fc-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f2fc-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="5f2fc-134">標頭</span><span class="sxs-lookup"><span data-stu-id="5f2fc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f2fc-135"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="5f2fc-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="5f2fc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5f2fc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f2fc-137"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f2fc-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f2fc-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f2fc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f2fc-139">IStats</span><span class="sxs-lookup"><span data-stu-id="5f2fc-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="5f2fc-140">IStats：： Connect</span><span class="sxs-lookup"><span data-stu-id="5f2fc-140">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="5f2fc-141">IStats：:P ause</span><span class="sxs-lookup"><span data-stu-id="5f2fc-141">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="5f2fc-142">IStats：： Stop</span><span class="sxs-lookup"><span data-stu-id="5f2fc-142">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




