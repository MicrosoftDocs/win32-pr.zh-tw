---
description: Stop 方法會停止目前的捕捉。
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: 'IStats：： Stop 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7b7b58527e7bde0c3bbdec4fc162b705dd178c10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991765"
---
# <a name="istatsstop-method"></a><span data-ttu-id="1ee8f-103">IStats：： Stop 方法</span><span class="sxs-lookup"><span data-stu-id="1ee8f-103">IStats::Stop method</span></span>

<span data-ttu-id="1ee8f-104">**Stop** 方法會停止目前的捕捉。</span><span class="sxs-lookup"><span data-stu-id="1ee8f-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ee8f-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ee8f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="1ee8f-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ee8f-106">Parameters</span></span>

<span data-ttu-id="1ee8f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1ee8f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1ee8f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ee8f-108">Return value</span></span>

<span data-ttu-id="1ee8f-109">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="1ee8f-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1ee8f-110">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="1ee8f-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="1ee8f-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1ee8f-111">Return code</span></span>                                                                                            | <span data-ttu-id="1ee8f-112">Description</span><span class="sxs-lookup"><span data-stu-id="1ee8f-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ee8f-113"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee8f-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="1ee8f-114">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="1ee8f-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="1ee8f-115">呼叫 [IStats：： connect](istats-connect.md) 方法，將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="1ee8f-115">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="1ee8f-116"><dt>**NMERR \_ 未 \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee8f-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="1ee8f-117">NPP 不會捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="1ee8f-117">The NPP is not capturing data.</span></span> <span data-ttu-id="1ee8f-118">呼叫 [IStats：： start](istats-start.md) 方法來啟動 capture。</span><span class="sxs-lookup"><span data-stu-id="1ee8f-118">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="1ee8f-119"><dt>**NMERR \_ 不是 \_ 統計資料 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee8f-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="1ee8f-120">NPP 已連接到網路，但不是使用 [IStats：： Connect](istats-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="1ee8f-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="1ee8f-121">備註</span><span class="sxs-lookup"><span data-stu-id="1ee8f-121">Remarks</span></span>

<span data-ttu-id="1ee8f-122">在呼叫 **IStats：： Stop** 之後重新開機 capture 時，請務必在每次呼叫 [IStats：： Start](istats-start.md)以重新開機捕獲時，呼叫 [IStats：： Configure](istats-configure.md)方法。</span><span class="sxs-lookup"><span data-stu-id="1ee8f-122">When restarting the capture after **IStats::Stop** has been called, make sure you call the [IStats::Configure](istats-configure.md) method each time you call [IStats::Start](istats-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ee8f-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ee8f-123">Requirements</span></span>



| <span data-ttu-id="1ee8f-124">需求</span><span class="sxs-lookup"><span data-stu-id="1ee8f-124">Requirement</span></span> | <span data-ttu-id="1ee8f-125">值</span><span class="sxs-lookup"><span data-stu-id="1ee8f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee8f-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ee8f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee8f-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ee8f-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="1ee8f-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ee8f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee8f-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ee8f-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="1ee8f-130">標頭</span><span class="sxs-lookup"><span data-stu-id="1ee8f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ee8f-131"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="1ee8f-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="1ee8f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1ee8f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ee8f-133"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ee8f-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ee8f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ee8f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee8f-135">IStats</span><span class="sxs-lookup"><span data-stu-id="1ee8f-135">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="1ee8f-136">IStats：： Connect</span><span class="sxs-lookup"><span data-stu-id="1ee8f-136">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="1ee8f-137">IStats：： Configure</span><span class="sxs-lookup"><span data-stu-id="1ee8f-137">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="1ee8f-138">IStats：： Start</span><span class="sxs-lookup"><span data-stu-id="1ee8f-138">IStats::Start</span></span>](istats-start.md)
</dt> </dl>

 

 




