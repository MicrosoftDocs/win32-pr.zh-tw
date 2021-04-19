---
description: Stop 方法會停止目前的捕捉。
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: 'IRTC：： Stop 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: f25bf9d56a6f41acefad9a552dd2f591158bc74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997117"
---
# <a name="irtcstop-method"></a><span data-ttu-id="e225b-103">IRTC：： Stop 方法</span><span class="sxs-lookup"><span data-stu-id="e225b-103">IRTC::Stop method</span></span>

<span data-ttu-id="e225b-104">**Stop** 方法會停止目前的捕捉。</span><span class="sxs-lookup"><span data-stu-id="e225b-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e225b-105">語法</span><span class="sxs-lookup"><span data-stu-id="e225b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="e225b-106">參數</span><span class="sxs-lookup"><span data-stu-id="e225b-106">Parameters</span></span>

<span data-ttu-id="e225b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e225b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e225b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e225b-108">Return value</span></span>

<span data-ttu-id="e225b-109">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="e225b-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e225b-110">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="e225b-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="e225b-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e225b-111">Return code</span></span>                                                                                          | <span data-ttu-id="e225b-112">Description</span><span class="sxs-lookup"><span data-stu-id="e225b-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e225b-113"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="e225b-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="e225b-114">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="e225b-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="e225b-115">呼叫 [IRTC：： connect](irtc-connect.md) 以將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="e225b-115">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="e225b-116"><dt>**NMERR \_ 未 \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="e225b-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="e225b-117">NPP 不會捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="e225b-117">The NPP is not capturing data.</span></span> <span data-ttu-id="e225b-118">呼叫 [IRTC：： start](irtc-start.md) 以開始捕獲。</span><span class="sxs-lookup"><span data-stu-id="e225b-118">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="e225b-119"><dt>**NMERR \_ 無法 \_ 即時**</dt></span><span class="sxs-lookup"><span data-stu-id="e225b-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="e225b-120">NPP 已連接到網路，但不是使用 [IRTC：： Connect](irtc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="e225b-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="e225b-121">備註</span><span class="sxs-lookup"><span data-stu-id="e225b-121">Remarks</span></span>

<span data-ttu-id="e225b-122">當您在呼叫 **IRTC：： Stop** 方法之後重新開機 capture 時，請務必在每次呼叫 [IRTC：： Start](irtc-start.md)以重新開機捕獲時，呼叫 [IRTC：： Configure](irtc-configure.md) 。</span><span class="sxs-lookup"><span data-stu-id="e225b-122">When you restart the capture after calling the **IRTC::Stop** method, make sure to call [IRTC::Configure](irtc-configure.md) each time you call [IRTC::Start](irtc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="e225b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e225b-123">Requirements</span></span>



| <span data-ttu-id="e225b-124">需求</span><span class="sxs-lookup"><span data-stu-id="e225b-124">Requirement</span></span> | <span data-ttu-id="e225b-125">值</span><span class="sxs-lookup"><span data-stu-id="e225b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e225b-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e225b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e225b-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e225b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="e225b-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e225b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e225b-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e225b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="e225b-130">標頭</span><span class="sxs-lookup"><span data-stu-id="e225b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e225b-131"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="e225b-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="e225b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e225b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e225b-133"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e225b-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e225b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e225b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e225b-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="e225b-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="e225b-136">IRTC：： Connect</span><span class="sxs-lookup"><span data-stu-id="e225b-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="e225b-137">IRTC：： Configure</span><span class="sxs-lookup"><span data-stu-id="e225b-137">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="e225b-138">IRTC：： Start</span><span class="sxs-lookup"><span data-stu-id="e225b-138">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




