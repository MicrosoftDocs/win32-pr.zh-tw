---
description: Pause 方法會暫停目前的捕獲。
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: 'IESP： (Netmon 的:P ause 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0558c5dfe36f26e3aad9f31101364d2e8e5c4967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510968"
---
# <a name="iesppause-method"></a><span data-ttu-id="8fed2-103">IESP：:P ause 方法</span><span class="sxs-lookup"><span data-stu-id="8fed2-103">IESP::Pause method</span></span>

<span data-ttu-id="8fed2-104">**Pause** 方法會暫停目前的捕獲。</span><span class="sxs-lookup"><span data-stu-id="8fed2-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fed2-105">語法</span><span class="sxs-lookup"><span data-stu-id="8fed2-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="8fed2-106">參數</span><span class="sxs-lookup"><span data-stu-id="8fed2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fed2-107">*lpStats*</span><span class="sxs-lookup"><span data-stu-id="8fed2-107">*lpStats*</span></span> 
</dt> <dd>

<span data-ttu-id="8fed2-108">已過時。</span><span class="sxs-lookup"><span data-stu-id="8fed2-108">Obsolete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fed2-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fed2-109">Return value</span></span>

<span data-ttu-id="8fed2-110">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="8fed2-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8fed2-111">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="8fed2-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="8fed2-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8fed2-112">Return code</span></span>                                                                                           | <span data-ttu-id="8fed2-113">Description</span><span class="sxs-lookup"><span data-stu-id="8fed2-113">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8fed2-114"><dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="8fed2-114"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="8fed2-115">此 capture 已經暫停。</span><span class="sxs-lookup"><span data-stu-id="8fed2-115">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="8fed2-116"><dt>**NMERR \_ 未 \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="8fed2-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="8fed2-117">NPP 不會捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="8fed2-117">The NPP is not capturing data.</span></span> <span data-ttu-id="8fed2-118">呼叫 [IESP：： start](iesp-start.md) 以開始捕獲。</span><span class="sxs-lookup"><span data-stu-id="8fed2-118">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="8fed2-119"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="8fed2-119"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="8fed2-120">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="8fed2-120">The NPP is not connected to the network.</span></span> <span data-ttu-id="8fed2-121">呼叫 [IESP：： connect](iesp-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="8fed2-121">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="8fed2-122"><dt>**NMERR \_ 非 \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="8fed2-122"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="8fed2-123">NPP 已連接到網路，但不是使用 [IESP：： Connect](iesp-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="8fed2-123">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="8fed2-124">備註</span><span class="sxs-lookup"><span data-stu-id="8fed2-124">Remarks</span></span>

<span data-ttu-id="8fed2-125">當捕捉處於暫停狀態時，除非您呼叫 [IESP：： Resume](iesp-resume.md)方法來重新開機 capture，否則新的資料不會加入至目前的 [*capture*](c.md)檔。</span><span class="sxs-lookup"><span data-stu-id="8fed2-125">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until you call the [IESP::Resume](iesp-resume.md) method to restart the capture.</span></span> <span data-ttu-id="8fed2-126">當 **暫停** 和 **繼續** 用來停止並重新啟動捕獲時，所有捕獲的資訊都會放在相同的捕獲檔案中。</span><span class="sxs-lookup"><span data-stu-id="8fed2-126">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="8fed2-127">當您使用 **IESP：:P ause** 和 **IESP：： Resume** 方法來控制捕捉時，網路監視器會在每次執行時繼續新增 [*對話統計資料*](c.md) 。</span><span class="sxs-lookup"><span data-stu-id="8fed2-127">When you use the **IESP::Pause** and **IESP::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="8fed2-128">若要重新開機捕獲，請呼叫 [IESP：： Resume](iesp-resume.md)。</span><span class="sxs-lookup"><span data-stu-id="8fed2-128">To restart the capture, call [IESP::Resume](iesp-resume.md).</span></span> <span data-ttu-id="8fed2-129">若要停止捕捉，請呼叫 [IESP：： stop](iesp-stop.md)。</span><span class="sxs-lookup"><span data-stu-id="8fed2-129">To stop the capture, call [IESP::Stop](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fed2-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fed2-130">Requirements</span></span>



| <span data-ttu-id="8fed2-131">需求</span><span class="sxs-lookup"><span data-stu-id="8fed2-131">Requirement</span></span> | <span data-ttu-id="8fed2-132">值</span><span class="sxs-lookup"><span data-stu-id="8fed2-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fed2-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fed2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8fed2-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fed2-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="8fed2-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fed2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8fed2-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fed2-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="8fed2-137">標頭</span><span class="sxs-lookup"><span data-stu-id="8fed2-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fed2-138"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="8fed2-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="8fed2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8fed2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fed2-140"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fed2-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fed2-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fed2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fed2-142">IESP</span><span class="sxs-lookup"><span data-stu-id="8fed2-142">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="8fed2-143">IESP：： Connect</span><span class="sxs-lookup"><span data-stu-id="8fed2-143">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="8fed2-144">IESP：： Resume</span><span class="sxs-lookup"><span data-stu-id="8fed2-144">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="8fed2-145">IESP：： Start</span><span class="sxs-lookup"><span data-stu-id="8fed2-145">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="8fed2-146">IESP：： Stop</span><span class="sxs-lookup"><span data-stu-id="8fed2-146">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




