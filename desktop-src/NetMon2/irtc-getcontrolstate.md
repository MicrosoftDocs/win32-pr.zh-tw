---
description: GetControlState 方法會抓取 capture 的狀態，以指出 capture 是否正在執行或已暫停。
ms.assetid: ae0cf869-bf5b-4c23-a924-014554053c92
title: 'IRTC：： GetControlState 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d437d9463ed3225cd3a474e78220acf1f07af4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848768"
---
# <a name="irtcgetcontrolstate-method"></a><span data-ttu-id="3bcaa-103">IRTC：： GetControlState 方法</span><span class="sxs-lookup"><span data-stu-id="3bcaa-103">IRTC::GetControlState method</span></span>

<span data-ttu-id="3bcaa-104">**GetControlState** 方法會 [*抓取 capture*](c.md)的狀態，以指出 capture 是否正在執行或已暫停。</span><span class="sxs-lookup"><span data-stu-id="3bcaa-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bcaa-105">語法</span><span class="sxs-lookup"><span data-stu-id="3bcaa-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="3bcaa-106">參數</span><span class="sxs-lookup"><span data-stu-id="3bcaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bcaa-107">*IsRunnning* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3bcaa-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bcaa-108">目前正在執行之捕捉的指標，包括是否暫停捕捉。</span><span class="sxs-lookup"><span data-stu-id="3bcaa-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="3bcaa-109">*IsPaused* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3bcaa-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bcaa-110">指標，表示目前的捕獲已暫停。</span><span class="sxs-lookup"><span data-stu-id="3bcaa-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bcaa-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3bcaa-111">Return value</span></span>

<span data-ttu-id="3bcaa-112">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="3bcaa-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3bcaa-113">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="3bcaa-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="3bcaa-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3bcaa-114">Return code</span></span>                                                                                          | <span data-ttu-id="3bcaa-115">Description</span><span class="sxs-lookup"><span data-stu-id="3bcaa-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3bcaa-116"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="3bcaa-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="3bcaa-117">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="3bcaa-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="3bcaa-118">呼叫 [IRTC：： connect](irtc-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="3bcaa-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="3bcaa-119"><dt>**NMERR \_ 無法 \_ 即時**</dt></span><span class="sxs-lookup"><span data-stu-id="3bcaa-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="3bcaa-120">NPP 已連接到網路，但不是使用 [IRTC：： Connect](irtc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3bcaa-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="3bcaa-121">備註</span><span class="sxs-lookup"><span data-stu-id="3bcaa-121">Remarks</span></span>

<span data-ttu-id="3bcaa-122">每當 NPP 連接到網路時，都可以呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3bcaa-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="3bcaa-123">您可以使用這個方法來找出 capture 是否正在執行、是否已暫停捕捉，或是已停止 capture 但 NPP 仍在連線。</span><span class="sxs-lookup"><span data-stu-id="3bcaa-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bcaa-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bcaa-124">Requirements</span></span>



| <span data-ttu-id="3bcaa-125">需求</span><span class="sxs-lookup"><span data-stu-id="3bcaa-125">Requirement</span></span> | <span data-ttu-id="3bcaa-126">值</span><span class="sxs-lookup"><span data-stu-id="3bcaa-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bcaa-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3bcaa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3bcaa-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bcaa-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="3bcaa-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3bcaa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3bcaa-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bcaa-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="3bcaa-131">標頭</span><span class="sxs-lookup"><span data-stu-id="3bcaa-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bcaa-132"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="3bcaa-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="3bcaa-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3bcaa-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bcaa-134"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bcaa-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bcaa-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bcaa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bcaa-136">IRTC</span><span class="sxs-lookup"><span data-stu-id="3bcaa-136">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="3bcaa-137">IRTC：： Connect</span><span class="sxs-lookup"><span data-stu-id="3bcaa-137">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="3bcaa-138">IRTC：:P ause</span><span class="sxs-lookup"><span data-stu-id="3bcaa-138">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="3bcaa-139">IRTC：： Start</span><span class="sxs-lookup"><span data-stu-id="3bcaa-139">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="3bcaa-140">IRTC：： Stop</span><span class="sxs-lookup"><span data-stu-id="3bcaa-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




