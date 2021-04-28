---
description: IESP：： Resume 方法-Resume 方法會重新開機已暫停的捕獲。
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: 'IESP：： Resume 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 498beda4f2f6c61af918d542542c4ed7b789ba1a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084246"
---
# <a name="iespresume-method"></a><span data-ttu-id="3c0cb-103">IESP：： Resume 方法</span><span class="sxs-lookup"><span data-stu-id="3c0cb-103">IESP::Resume method</span></span>

<span data-ttu-id="3c0cb-104">**Resume** 方法會重新開機已暫停的捕獲。</span><span class="sxs-lookup"><span data-stu-id="3c0cb-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c0cb-105">語法</span><span class="sxs-lookup"><span data-stu-id="3c0cb-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="3c0cb-106">參數</span><span class="sxs-lookup"><span data-stu-id="3c0cb-106">Parameters</span></span>

<span data-ttu-id="3c0cb-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3c0cb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c0cb-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c0cb-108">Return value</span></span>

<span data-ttu-id="3c0cb-109">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="3c0cb-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3c0cb-110">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="3c0cb-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="3c0cb-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3c0cb-111">Return code</span></span>                                                                                                | <span data-ttu-id="3c0cb-112">Description</span><span class="sxs-lookup"><span data-stu-id="3c0cb-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c0cb-113"><dt>**NMERR \_ CAPTURE \_ 未 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="3c0cb-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="3c0cb-114">捕捉未暫停。</span><span class="sxs-lookup"><span data-stu-id="3c0cb-114">The capture is not paused.</span></span> <span data-ttu-id="3c0cb-115">呼叫 [**IESP：:P ause**](iesp-pause.md) 暫停捕捉。</span><span class="sxs-lookup"><span data-stu-id="3c0cb-115">Call [**IESP::Pause**](iesp-pause.md) to pause the capture.</span></span><br/>                        |
| <dl> <span data-ttu-id="3c0cb-116"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="3c0cb-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="3c0cb-117">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="3c0cb-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="3c0cb-118">呼叫 [**IESP：： connect**](iesp-connect.md) 以連接到網路。</span><span class="sxs-lookup"><span data-stu-id="3c0cb-118">Call [**IESP::Connect**](iesp-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="3c0cb-119"><dt>**NMERR \_ 非 \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="3c0cb-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>             | <span data-ttu-id="3c0cb-120">NPP 已連接到網路，但不是使用 [**IESP：： Connect**](iesp-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3c0cb-120">The NPP is connected to the network, but not with the [**IESP::Connect**](iesp-connect.md) method.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="3c0cb-121">備註</span><span class="sxs-lookup"><span data-stu-id="3c0cb-121">Remarks</span></span>

<span data-ttu-id="3c0cb-122">當捕捉處於暫停狀態時，在呼叫 **IESP：： Resume** 以重新開機 capture 之前，不會將新資料新增至目前的 [*capture*](c.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="3c0cb-122">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until **IESP::Resume** is called to restart the capture.</span></span> <span data-ttu-id="3c0cb-123">當 **暫停** 和 **繼續** 用來停止並重新啟動捕獲時，所有捕獲的資訊都會放在相同的捕獲檔案中。</span><span class="sxs-lookup"><span data-stu-id="3c0cb-123">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="3c0cb-124">當使用 [ **暫停** ] 和 [ **繼續** ] 來控制捕捉時，網路監視器會繼續將 [*對話統計資料*](c.md) 加入目前 capture 的現有統計資料。</span><span class="sxs-lookup"><span data-stu-id="3c0cb-124">When using **Pause** and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="3c0cb-125">若要停止捕捉，請呼叫 [**IESP：： stop**](iesp-stop.md)。</span><span class="sxs-lookup"><span data-stu-id="3c0cb-125">To stop the capture, call [**IESP::Stop**](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c0cb-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c0cb-126">Requirements</span></span>



| <span data-ttu-id="3c0cb-127">需求</span><span class="sxs-lookup"><span data-stu-id="3c0cb-127">Requirement</span></span> | <span data-ttu-id="3c0cb-128">值</span><span class="sxs-lookup"><span data-stu-id="3c0cb-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0cb-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c0cb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3c0cb-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c0cb-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="3c0cb-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c0cb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3c0cb-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c0cb-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="3c0cb-133">標頭</span><span class="sxs-lookup"><span data-stu-id="3c0cb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c0cb-134"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="3c0cb-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="3c0cb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3c0cb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c0cb-136"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c0cb-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c0cb-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c0cb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c0cb-138">IESP</span><span class="sxs-lookup"><span data-stu-id="3c0cb-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="3c0cb-139">**IESP：： Connect**</span><span class="sxs-lookup"><span data-stu-id="3c0cb-139">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="3c0cb-140">**IESP：:P ause**</span><span class="sxs-lookup"><span data-stu-id="3c0cb-140">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="3c0cb-141">**IESP：： Stop**</span><span class="sxs-lookup"><span data-stu-id="3c0cb-141">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> </dl>

 

 




