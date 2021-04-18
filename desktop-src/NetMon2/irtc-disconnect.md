---
description: 中斷連線方法會中斷 NPP 與網路的連線。
ms.assetid: 47a0cce0-a50d-4bad-9787-672cc3d13d07
title: 'IRTC： (Netmon 的:D isconnect 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: df58d6ac0e61ecc370510474c3bc067726d9824b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192216"
---
# <a name="irtcdisconnect-method"></a><span data-ttu-id="f0ffc-103">IRTC：:D isconnect 方法</span><span class="sxs-lookup"><span data-stu-id="f0ffc-103">IRTC::Disconnect method</span></span>

<span data-ttu-id="f0ffc-104">**中斷** 連線方法會中斷 NPP 與網路的連線。</span><span class="sxs-lookup"><span data-stu-id="f0ffc-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ffc-105">語法</span><span class="sxs-lookup"><span data-stu-id="f0ffc-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="f0ffc-106">參數</span><span class="sxs-lookup"><span data-stu-id="f0ffc-106">Parameters</span></span>

<span data-ttu-id="f0ffc-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f0ffc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0ffc-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0ffc-108">Return value</span></span>

<span data-ttu-id="f0ffc-109">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="f0ffc-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f0ffc-110">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="f0ffc-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="f0ffc-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f0ffc-111">Return code</span></span>                                                                                          | <span data-ttu-id="f0ffc-112">Description</span><span class="sxs-lookup"><span data-stu-id="f0ffc-112">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0ffc-113"><dt>**NMERR \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ffc-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="f0ffc-114">NPP 正在捕獲資料。</span><span class="sxs-lookup"><span data-stu-id="f0ffc-114">The NPP is capturing data.</span></span> <span data-ttu-id="f0ffc-115">當資料捕捉正在進行中時，您無法中斷與網路的連線。</span><span class="sxs-lookup"><span data-stu-id="f0ffc-115">You cannot disconnect from the network while the data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="f0ffc-116"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ffc-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="f0ffc-117">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="f0ffc-117">The NPP is not connected to the network.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="f0ffc-118"><dt>**NMERR \_ 無法 \_ 即時**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ffc-118"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="f0ffc-119">NPP 已連接到網路，但不是使用 [IRTC：： Connect](irtc-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f0ffc-119">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="f0ffc-120">備註</span><span class="sxs-lookup"><span data-stu-id="f0ffc-120">Remarks</span></span>

<span data-ttu-id="f0ffc-121">當 NPP 正在捕捉資料時，無法呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="f0ffc-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="f0ffc-122">呼叫 IRTC：:D isconnect 之前，您必須先呼叫 [IRTC：： Stop](irtc-stop.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f0ffc-122">You must call the [IRTC::Stop](irtc-stop.md) method before calling IRTC::Disconnect.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0ffc-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0ffc-123">Requirements</span></span>



| <span data-ttu-id="f0ffc-124">需求</span><span class="sxs-lookup"><span data-stu-id="f0ffc-124">Requirement</span></span> | <span data-ttu-id="f0ffc-125">值</span><span class="sxs-lookup"><span data-stu-id="f0ffc-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ffc-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0ffc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f0ffc-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0ffc-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="f0ffc-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0ffc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f0ffc-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0ffc-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="f0ffc-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f0ffc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0ffc-131"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="f0ffc-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="f0ffc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f0ffc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0ffc-133"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0ffc-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0ffc-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0ffc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ffc-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="f0ffc-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="f0ffc-136">IRTC：： Connect</span><span class="sxs-lookup"><span data-stu-id="f0ffc-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="f0ffc-137">IRTC：： Stop</span><span class="sxs-lookup"><span data-stu-id="f0ffc-137">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




