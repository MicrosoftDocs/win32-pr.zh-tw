---
description: Resume 方法會重新開機已暫停的捕獲。
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: 'IRTC：： Resume 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 991f70944b44ce13641318219788d9d6122b15c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987480"
---
# <a name="irtcresume-method"></a><span data-ttu-id="c8200-103">IRTC：： Resume 方法</span><span class="sxs-lookup"><span data-stu-id="c8200-103">IRTC::Resume method</span></span>

<span data-ttu-id="c8200-104">**Resume** 方法會重新開機已暫停的捕獲。</span><span class="sxs-lookup"><span data-stu-id="c8200-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8200-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8200-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="c8200-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8200-106">Parameters</span></span>

<span data-ttu-id="c8200-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c8200-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8200-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8200-108">Return value</span></span>

<span data-ttu-id="c8200-109">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="c8200-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c8200-110">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="c8200-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c8200-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c8200-111">Return code</span></span>                                                                                                | <span data-ttu-id="c8200-112">Description</span><span class="sxs-lookup"><span data-stu-id="c8200-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8200-113"><dt>**NMERR \_ CAPTURE \_ 未 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="c8200-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="c8200-114">捕捉未暫停。</span><span class="sxs-lookup"><span data-stu-id="c8200-114">The capture is not paused.</span></span> <span data-ttu-id="c8200-115">呼叫 [IRTC：:P ause](irtc-pause.md) 暫停捕捉。</span><span class="sxs-lookup"><span data-stu-id="c8200-115">Call [IRTC::Pause](irtc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="c8200-116"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="c8200-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="c8200-117">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="c8200-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="c8200-118">呼叫 [IRTC：： connect](irtc-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="c8200-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="c8200-119"><dt>**NMERR \_ 無法 \_ 即時**</dt></span><span class="sxs-lookup"><span data-stu-id="c8200-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>        | <span data-ttu-id="c8200-120">NPP 已連接到網路，但不是使用 [IRTC：： Connect](irtc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c8200-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="c8200-121">備註</span><span class="sxs-lookup"><span data-stu-id="c8200-121">Remarks</span></span>

<span data-ttu-id="c8200-122">當捕捉處於暫停狀態時，在呼叫 [IRTC：： Resume](idelaydc-resume.md) 方法重新開機 capture 之前，不會建立新的資料。</span><span class="sxs-lookup"><span data-stu-id="c8200-122">While the capture is in a paused state, new data is not captured until a call to the [IRTC::Resume](idelaydc-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="c8200-123">使用 **Pause** 和 **Resume** 方法來控制捕捉時，網路監視器會繼續將 [*對話統計資料*](c.md) 新增至目前 capture 的現有統計資料。</span><span class="sxs-lookup"><span data-stu-id="c8200-123">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="c8200-124">若要停止捕捉，請呼叫 [IRTC：： stop](irtc-stop.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c8200-124">To stop the capture, call the [IRTC::Stop](irtc-stop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8200-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8200-125">Requirements</span></span>



| <span data-ttu-id="c8200-126">需求</span><span class="sxs-lookup"><span data-stu-id="c8200-126">Requirement</span></span> | <span data-ttu-id="c8200-127">值</span><span class="sxs-lookup"><span data-stu-id="c8200-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8200-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8200-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c8200-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8200-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c8200-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8200-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c8200-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8200-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c8200-132">標頭</span><span class="sxs-lookup"><span data-stu-id="c8200-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8200-133"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="c8200-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c8200-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c8200-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8200-135"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8200-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8200-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8200-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8200-137">IRTC</span><span class="sxs-lookup"><span data-stu-id="c8200-137">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="c8200-138">IRTC：： Connect</span><span class="sxs-lookup"><span data-stu-id="c8200-138">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="c8200-139">IRTC：:P ause</span><span class="sxs-lookup"><span data-stu-id="c8200-139">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="c8200-140">IRTC：： Stop</span><span class="sxs-lookup"><span data-stu-id="c8200-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




