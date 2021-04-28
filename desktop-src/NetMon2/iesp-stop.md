---
description: IESP：： Stop 方法-Stop 方法會停止目前的捕捉。
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: 'IESP：： Stop 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ac262d8da5ab218db7300ea38da59d5c738421c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103766"
---
# <a name="iespstop-method"></a><span data-ttu-id="c9324-103">IESP：： Stop 方法</span><span class="sxs-lookup"><span data-stu-id="c9324-103">IESP::Stop method</span></span>

<span data-ttu-id="c9324-104">**Stop** 方法會停止目前的捕捉。</span><span class="sxs-lookup"><span data-stu-id="c9324-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9324-105">語法</span><span class="sxs-lookup"><span data-stu-id="c9324-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="c9324-106">參數</span><span class="sxs-lookup"><span data-stu-id="c9324-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9324-107">*lpStats* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c9324-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9324-108">[統計資料](statistics.md)結構的指標，其中包含網路統計資料，例如總畫面格總數和已捕獲的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="c9324-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9324-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9324-109">Return value</span></span>

<span data-ttu-id="c9324-110">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="c9324-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c9324-111">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="c9324-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c9324-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c9324-112">Return code</span></span>                                                                                          | <span data-ttu-id="c9324-113">Description</span><span class="sxs-lookup"><span data-stu-id="c9324-113">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9324-114"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="c9324-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c9324-115">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="c9324-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="c9324-116">呼叫 [IESP：： connect](iesp-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="c9324-116">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="c9324-117"><dt>**NMERR \_ 未 \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="c9324-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="c9324-118">NPP 不會捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="c9324-118">The NPP is not capturing data.</span></span> <span data-ttu-id="c9324-119">呼叫 [IESP：： start](iesp-start.md) 以開始捕獲。</span><span class="sxs-lookup"><span data-stu-id="c9324-119">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="c9324-120"><dt>**NMERR \_ 非 \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="c9324-120"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="c9324-121">NPP 已連接到網路，但不是使用 [IESP：： Connect](iesp-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c9324-121">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="c9324-122">備註</span><span class="sxs-lookup"><span data-stu-id="c9324-122">Remarks</span></span>

<span data-ttu-id="c9324-123">呼叫 **IESP：： Stop** 方法時，網路監視器會停止捕捉資料並關閉 capture 檔案 [*。*](c.md)</span><span class="sxs-lookup"><span data-stu-id="c9324-123">When the **IESP::Stop** method is called, Network Monitor stops capturing data and closes the [*capture file.*](c.md)</span></span> <span data-ttu-id="c9324-124"> (在呼叫 [IESP：： Start](iesp-start.md) 時傳回的 capture 檔名稱。 ) 您現在可以查看 capture 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="c9324-124">(The name of the capture file was returned when [IESP::Start](iesp-start.md) was called.) You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="c9324-125">當您停止並重新啟動捕捉時，請務必在每次呼叫[IESP：： Start](iesp-start.md)以重新開機捕獲時，呼叫[IESP：： Configure](iesp-configure.md)方法。</span><span class="sxs-lookup"><span data-stu-id="c9324-125">When you stop and restart the capture, make sure to call the [IESP::Configure](iesp-configure.md) method each time you call [IESP::Start](iesp-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9324-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9324-126">Requirements</span></span>



| <span data-ttu-id="c9324-127">需求</span><span class="sxs-lookup"><span data-stu-id="c9324-127">Requirement</span></span> | <span data-ttu-id="c9324-128">值</span><span class="sxs-lookup"><span data-stu-id="c9324-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9324-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9324-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c9324-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9324-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c9324-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9324-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c9324-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9324-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c9324-133">標頭</span><span class="sxs-lookup"><span data-stu-id="c9324-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9324-134"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="c9324-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c9324-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c9324-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9324-136"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9324-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9324-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9324-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9324-138">IESP</span><span class="sxs-lookup"><span data-stu-id="c9324-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="c9324-139">IESP：： Connect</span><span class="sxs-lookup"><span data-stu-id="c9324-139">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="c9324-140">IESP：： Start</span><span class="sxs-lookup"><span data-stu-id="c9324-140">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="c9324-141">統計</span><span class="sxs-lookup"><span data-stu-id="c9324-141">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




