---
description: IDelaydC：： Resume 方法-Resume 方法會重新開機已暫停的捕獲。
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: 'IDelaydC：： Resume 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9c8c3b505e0e9fb306a444111cce22c8c580d015
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109186"
---
# <a name="idelaydcresume-method"></a><span data-ttu-id="0fcbf-103">IDelaydC：： Resume 方法</span><span class="sxs-lookup"><span data-stu-id="0fcbf-103">IDelaydC::Resume method</span></span>

<span data-ttu-id="0fcbf-104">**Resume** 方法會重新開機已暫停的捕獲。</span><span class="sxs-lookup"><span data-stu-id="0fcbf-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fcbf-105">語法</span><span class="sxs-lookup"><span data-stu-id="0fcbf-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="0fcbf-106">參數</span><span class="sxs-lookup"><span data-stu-id="0fcbf-106">Parameters</span></span>

<span data-ttu-id="0fcbf-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0fcbf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0fcbf-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="0fcbf-108">Return value</span></span>

<span data-ttu-id="0fcbf-109">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="0fcbf-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0fcbf-110">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="0fcbf-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0fcbf-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0fcbf-111">Return code</span></span>                                                                                                | <span data-ttu-id="0fcbf-112">Description</span><span class="sxs-lookup"><span data-stu-id="0fcbf-112">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0fcbf-113"><dt>**NMERR \_ CAPTURE \_ 未 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="0fcbf-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="0fcbf-114">捕捉未暫停。</span><span class="sxs-lookup"><span data-stu-id="0fcbf-114">The capture is not paused.</span></span> <span data-ttu-id="0fcbf-115">呼叫 [**IDelaydC：:P ause**](idelaydc-pause.md) 暫停捕捉。</span><span class="sxs-lookup"><span data-stu-id="0fcbf-115">Call [**IDelaydC::Pause**](idelaydc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="0fcbf-116"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="0fcbf-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="0fcbf-117">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="0fcbf-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="0fcbf-118">呼叫 [**IDelaydC：： connect**](idelaydc-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="0fcbf-118">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="0fcbf-119"><dt>**NMERR \_ 未 \_ 延遲**</dt></span><span class="sxs-lookup"><span data-stu-id="0fcbf-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>         | <span data-ttu-id="0fcbf-120">NPP 已連接到網路，但不是使用 [**IDelaydC：： Connect**](idelaydc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="0fcbf-120">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="0fcbf-121">備註</span><span class="sxs-lookup"><span data-stu-id="0fcbf-121">Remarks</span></span>

<span data-ttu-id="0fcbf-122">當捕捉暫停時，不會將新資料新增至目前的 [*capture*](c.md) 檔案，直到呼叫 **IDelaydC：： Resume** 方法來重新開機捕獲為止。</span><span class="sxs-lookup"><span data-stu-id="0fcbf-122">While the capture is paused, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="0fcbf-123">當 [**暫停**](idelaydc-pause.md) 和 **繼續** 用來停止並重新啟動捕獲時，所有捕獲的資訊都會放在相同的捕獲檔案中。</span><span class="sxs-lookup"><span data-stu-id="0fcbf-123">When [**Pause**](idelaydc-pause.md) and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="0fcbf-124">當使用 [ [**暫停**](idelaydc-pause.md) ] 和 [ **繼續** ] 來控制捕捉時，網路監視器會繼續將 [*對話統計資料*](c.md) 加入目前 capture 的現有統計資料。</span><span class="sxs-lookup"><span data-stu-id="0fcbf-124">When using [**Pause**](idelaydc-pause.md) and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="0fcbf-125">若要停止捕捉，請呼叫 [**IDelaydC：： stop**](idelaydc-stop.md)。</span><span class="sxs-lookup"><span data-stu-id="0fcbf-125">To stop the capture, call [**IDelaydC::Stop**](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fcbf-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fcbf-126">Requirements</span></span>



| <span data-ttu-id="0fcbf-127">需求</span><span class="sxs-lookup"><span data-stu-id="0fcbf-127">Requirement</span></span> | <span data-ttu-id="0fcbf-128">值</span><span class="sxs-lookup"><span data-stu-id="0fcbf-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fcbf-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fcbf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0fcbf-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fcbf-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0fcbf-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0fcbf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0fcbf-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fcbf-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0fcbf-133">標頭</span><span class="sxs-lookup"><span data-stu-id="0fcbf-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fcbf-134"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="0fcbf-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0fcbf-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0fcbf-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fcbf-136"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fcbf-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fcbf-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0fcbf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fcbf-138">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="0fcbf-138">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="0fcbf-139">**IDelaydC：： Connect**</span><span class="sxs-lookup"><span data-stu-id="0fcbf-139">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="0fcbf-140">**IDelaydC：:P ause**</span><span class="sxs-lookup"><span data-stu-id="0fcbf-140">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="0fcbf-141">**IDelaydC：： Stop**</span><span class="sxs-lookup"><span data-stu-id="0fcbf-141">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




