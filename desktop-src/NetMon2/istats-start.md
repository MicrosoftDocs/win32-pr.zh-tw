---
description: IStats：： Start 方法-Start 方法會啟動 capture。
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: 'IStats：： Start 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 64f02529ba10d98092eb30a1bcc350d5c72049fc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094546"
---
# <a name="istatsstart-method"></a><span data-ttu-id="f4ff0-103">IStats：： Start 方法</span><span class="sxs-lookup"><span data-stu-id="f4ff0-103">IStats::Start method</span></span>

<span data-ttu-id="f4ff0-104">**Start** 方法會啟動 capture。</span><span class="sxs-lookup"><span data-stu-id="f4ff0-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ff0-105">語法</span><span class="sxs-lookup"><span data-stu-id="f4ff0-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="f4ff0-106">參數</span><span class="sxs-lookup"><span data-stu-id="f4ff0-106">Parameters</span></span>

<span data-ttu-id="f4ff0-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f4ff0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4ff0-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4ff0-108">Return value</span></span>

<span data-ttu-id="f4ff0-109">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="f4ff0-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f4ff0-110">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="f4ff0-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="f4ff0-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f4ff0-111">Return code</span></span>                                                                                            | <span data-ttu-id="f4ff0-112">Description</span><span class="sxs-lookup"><span data-stu-id="f4ff0-112">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f4ff0-113"><dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ff0-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="f4ff0-114">Capture 已暫停，必須先停止，才能重新開機。</span><span class="sxs-lookup"><span data-stu-id="f4ff0-114">The capture has paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="f4ff0-115">呼叫 [IStats：： stop](istats-stop.md) 方法以停止捕捉。</span><span class="sxs-lookup"><span data-stu-id="f4ff0-115">Call the [IStats::Stop](istats-stop.md) method to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="f4ff0-116"><dt>**NMERR \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ff0-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="f4ff0-117">已啟動 capture。</span><span class="sxs-lookup"><span data-stu-id="f4ff0-117">The capture has already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="f4ff0-118"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ff0-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="f4ff0-119">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="f4ff0-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="f4ff0-120">呼叫 [IStats：： connect](istats-connect.md) 方法，將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="f4ff0-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/>           |
| <dl> <span data-ttu-id="f4ff0-121"><dt>**NMERR \_ 不是 \_ 統計資料 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ff0-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="f4ff0-122">NPP 已連接到網路，但不是使用 [IStats：： Connect](istats-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f4ff0-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="f4ff0-123">備註</span><span class="sxs-lookup"><span data-stu-id="f4ff0-123">Remarks</span></span>

<span data-ttu-id="f4ff0-124">使用 IStats：： Start 和 [IStats：： Stop](istats-stop.md) 方法重新開機捕捉時，您必須呼叫 [IStats：： Configure](istats-configure.md) 方法，以在每次呼叫 IStats：： start 重新開機資料捕獲時重新設定連接。</span><span class="sxs-lookup"><span data-stu-id="f4ff0-124">When restarting the capture by using the IStats::Start and [IStats::Stop](istats-stop.md) methods, you must call the [IStats::Configure](istats-configure.md) method to reconfigure the connection each time you call IStats::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="f4ff0-125">您也可以使用 [IStats：:P ause](istats-pause.md) 和 [IStats：： Resume](istats-resume.md) 方法來啟動和停止捕捉。</span><span class="sxs-lookup"><span data-stu-id="f4ff0-125">You can also start and stop the capture by using the [IStats::Pause](istats-pause.md) and [IStats::Resume](istats-resume.md) methods.</span></span> <span data-ttu-id="f4ff0-126">當您使用這些方法時，所捕獲的資料會儲存在相同的捕獲檔案中。</span><span class="sxs-lookup"><span data-stu-id="f4ff0-126">When you use these methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f4ff0-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4ff0-127">Requirements</span></span>



| <span data-ttu-id="f4ff0-128">需求</span><span class="sxs-lookup"><span data-stu-id="f4ff0-128">Requirement</span></span> | <span data-ttu-id="f4ff0-129">值</span><span class="sxs-lookup"><span data-stu-id="f4ff0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ff0-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4ff0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f4ff0-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4ff0-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="f4ff0-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4ff0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f4ff0-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4ff0-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="f4ff0-134">標頭</span><span class="sxs-lookup"><span data-stu-id="f4ff0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4ff0-135"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="f4ff0-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="f4ff0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f4ff0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4ff0-137"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4ff0-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4ff0-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4ff0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ff0-139">IStats</span><span class="sxs-lookup"><span data-stu-id="f4ff0-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="f4ff0-140">IStats：： Configure</span><span class="sxs-lookup"><span data-stu-id="f4ff0-140">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="f4ff0-141">IStats：： Connect</span><span class="sxs-lookup"><span data-stu-id="f4ff0-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="f4ff0-142">IStats：:P ause</span><span class="sxs-lookup"><span data-stu-id="f4ff0-142">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="f4ff0-143">IStats：： Resume</span><span class="sxs-lookup"><span data-stu-id="f4ff0-143">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="f4ff0-144">IStats：： Stop</span><span class="sxs-lookup"><span data-stu-id="f4ff0-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




