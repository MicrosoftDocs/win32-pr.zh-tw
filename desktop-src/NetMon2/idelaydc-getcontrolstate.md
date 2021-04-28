---
description: IDelaydC：： GetControlState 方法-GetControlState 方法會抓取 capture 的狀態，以指出正在執行或暫停捕捉。
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: 'IDelaydC：： GetControlState 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 825112ec9a33ef176d5a69765837214249e33102
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110766"
---
# <a name="idelaydcgetcontrolstate-method"></a><span data-ttu-id="b6115-103">IDelaydC：： GetControlState 方法</span><span class="sxs-lookup"><span data-stu-id="b6115-103">IDelaydC::GetControlState method</span></span>

<span data-ttu-id="b6115-104">**GetControlState** 方法會 [*抓取 capture*](c.md)的狀態，以指出 capture 是否正在執行或已暫停。</span><span class="sxs-lookup"><span data-stu-id="b6115-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6115-105">語法</span><span class="sxs-lookup"><span data-stu-id="b6115-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="b6115-106">參數</span><span class="sxs-lookup"><span data-stu-id="b6115-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6115-107">*IsRunnning* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b6115-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6115-108">目前正在執行之捕捉的指標，包括是否暫停捕捉。</span><span class="sxs-lookup"><span data-stu-id="b6115-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="b6115-109">*IsPaused* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b6115-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6115-110">指標，表示目前的捕獲已暫停。</span><span class="sxs-lookup"><span data-stu-id="b6115-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6115-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6115-111">Return value</span></span>

<span data-ttu-id="b6115-112">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="b6115-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b6115-113">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="b6115-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="b6115-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b6115-114">Return code</span></span>                                                                                          | <span data-ttu-id="b6115-115">Description</span><span class="sxs-lookup"><span data-stu-id="b6115-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6115-116"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="b6115-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b6115-117">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="b6115-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="b6115-118">呼叫 [IDelaydC：： connect](idelaydc-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="b6115-118">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="b6115-119"><dt>**NMERR \_ 未 \_ 延遲**</dt></span><span class="sxs-lookup"><span data-stu-id="b6115-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="b6115-120">NPP 已連接到網路，但不是使用 [IDelaydC：： Connect](idelaydc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b6115-120">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="b6115-121">備註</span><span class="sxs-lookup"><span data-stu-id="b6115-121">Remarks</span></span>

<span data-ttu-id="b6115-122">只要使用 [IDelaydC](idelaydc.md) 介面將 NPP 連接到網路，就可以呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="b6115-122">This method can be called any time the NPP is connected to the network by using the [IDelaydC](idelaydc.md) interface.</span></span> <span data-ttu-id="b6115-123">您可以使用這個方法來找出正在執行的捕捉、捕捉是否已暫停，或是已停止 capture 但 NPP 未中斷連線。</span><span class="sxs-lookup"><span data-stu-id="b6115-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

<span data-ttu-id="b6115-124">用來啟動、暫停和停止捕捉的方法會列在下列 [另請參閱] 清單中。</span><span class="sxs-lookup"><span data-stu-id="b6115-124">The methods used to start, pause, and, stop the capture are listed in the See Also list below.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6115-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6115-125">Requirements</span></span>



| <span data-ttu-id="b6115-126">需求</span><span class="sxs-lookup"><span data-stu-id="b6115-126">Requirement</span></span> | <span data-ttu-id="b6115-127">值</span><span class="sxs-lookup"><span data-stu-id="b6115-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6115-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6115-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b6115-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6115-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="b6115-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6115-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b6115-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6115-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="b6115-132">標頭</span><span class="sxs-lookup"><span data-stu-id="b6115-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6115-133"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="b6115-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="b6115-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b6115-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6115-135"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6115-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6115-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6115-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6115-137">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="b6115-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="b6115-138">IDelaydC：： Connect</span><span class="sxs-lookup"><span data-stu-id="b6115-138">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="b6115-139">IDelaydC：:P ause</span><span class="sxs-lookup"><span data-stu-id="b6115-139">IDelaydC::Pause</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="b6115-140">IDelaydC：： Start</span><span class="sxs-lookup"><span data-stu-id="b6115-140">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="b6115-141">IDelaydC：： Stop</span><span class="sxs-lookup"><span data-stu-id="b6115-141">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




