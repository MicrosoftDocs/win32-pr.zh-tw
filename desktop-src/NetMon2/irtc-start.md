---
description: Start 方法會啟動 capture。
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: 'IRTC：： Start 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3ee30112baf7813c983230fb90cd15ea7f52e2bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848764"
---
# <a name="irtcstart-method"></a><span data-ttu-id="20841-103">IRTC：： Start 方法</span><span class="sxs-lookup"><span data-stu-id="20841-103">IRTC::Start method</span></span>

<span data-ttu-id="20841-104">**Start** 方法會啟動 capture。</span><span class="sxs-lookup"><span data-stu-id="20841-104">The **Start** method starts the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="20841-105">語法</span><span class="sxs-lookup"><span data-stu-id="20841-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="20841-106">參數</span><span class="sxs-lookup"><span data-stu-id="20841-106">Parameters</span></span>

<span data-ttu-id="20841-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="20841-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20841-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="20841-108">Return value</span></span>

<span data-ttu-id="20841-109">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="20841-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="20841-110">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="20841-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="20841-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="20841-111">Return code</span></span>                                                                                           | <span data-ttu-id="20841-112">Description</span><span class="sxs-lookup"><span data-stu-id="20841-112">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20841-113"><dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="20841-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="20841-114">捕捉處於暫停狀態，必須先停止，才能重新開機。</span><span class="sxs-lookup"><span data-stu-id="20841-114">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="20841-115">呼叫 [IRTC：： stop](idelaydc-stop.md) 以停止捕捉。</span><span class="sxs-lookup"><span data-stu-id="20841-115">Call [IRTC::Stop](idelaydc-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="20841-116"><dt>**NMERR \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="20841-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="20841-117">已啟動 capture。</span><span class="sxs-lookup"><span data-stu-id="20841-117">The capture is already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="20841-118"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="20841-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="20841-119">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="20841-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="20841-120">呼叫 [IRTC：： connect](irtc-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="20841-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                         |
| <dl> <span data-ttu-id="20841-121"><dt>**NMERR \_ 無法 \_ 即時**</dt></span><span class="sxs-lookup"><span data-stu-id="20841-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="20841-122">NPP 已連接到網路，但不是使用 [IRTC：： Connect](irtc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="20841-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="20841-123">備註</span><span class="sxs-lookup"><span data-stu-id="20841-123">Remarks</span></span>

<span data-ttu-id="20841-124">當您使用 IRTC：： Start 和 [IRTC：： Stop](irtc-stop.md) 方法重新開機捕捉時，您必須呼叫 [IRTC：： Configure](irtc-configure.md) 方法，以在每次呼叫 IRTC：： start 重新開機資料捕獲時重新設定連接。</span><span class="sxs-lookup"><span data-stu-id="20841-124">When you restart the capture by using the IRTC::Start and [IRTC::Stop](irtc-stop.md) methods, you must call the [IRTC::Configure](irtc-configure.md) method to reconfigure the connection each time you call IRTC::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="20841-125">您也可以使用 [IRTC：:P ause](irtc-pause.md) 和 [IRTC：： Resume](irtc-resume.md) 方法來啟動和停止捕捉。</span><span class="sxs-lookup"><span data-stu-id="20841-125">You can also start and stop the capture by using the [IRTC::Pause](irtc-pause.md) and [IRTC::Resume](irtc-resume.md) methods.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="20841-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="20841-126">Requirements</span></span>



| <span data-ttu-id="20841-127">需求</span><span class="sxs-lookup"><span data-stu-id="20841-127">Requirement</span></span> | <span data-ttu-id="20841-128">值</span><span class="sxs-lookup"><span data-stu-id="20841-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20841-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20841-129">Minimum supported client</span></span><br/> | <span data-ttu-id="20841-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20841-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="20841-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20841-131">Minimum supported server</span></span><br/> | <span data-ttu-id="20841-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20841-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="20841-133">標頭</span><span class="sxs-lookup"><span data-stu-id="20841-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="20841-134"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="20841-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="20841-135">DLL</span><span class="sxs-lookup"><span data-stu-id="20841-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20841-136"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20841-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20841-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20841-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20841-138">IRTC</span><span class="sxs-lookup"><span data-stu-id="20841-138">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="20841-139">IRTC：： Configure</span><span class="sxs-lookup"><span data-stu-id="20841-139">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="20841-140">IRTC：： Connect</span><span class="sxs-lookup"><span data-stu-id="20841-140">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="20841-141">IRTC：:P ause</span><span class="sxs-lookup"><span data-stu-id="20841-141">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="20841-142">IRTC：： Resume</span><span class="sxs-lookup"><span data-stu-id="20841-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="20841-143">IRTC：： Stop</span><span class="sxs-lookup"><span data-stu-id="20841-143">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




