---
description: 中斷 NPP 與網路的連線。
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: 'IStats： (Netmon 的:D isconnect 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a5fa56c05036380b5dba42089979b43d776a4b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997850"
---
# <a name="istatsdisconnect-method"></a><span data-ttu-id="72249-103">IStats：:D isconnect 方法</span><span class="sxs-lookup"><span data-stu-id="72249-103">IStats::Disconnect method</span></span>

<span data-ttu-id="72249-104">**中斷** 連線方法會中斷 NPP 與網路的連線。</span><span class="sxs-lookup"><span data-stu-id="72249-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="72249-105">語法</span><span class="sxs-lookup"><span data-stu-id="72249-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="72249-106">參數</span><span class="sxs-lookup"><span data-stu-id="72249-106">Parameters</span></span>

<span data-ttu-id="72249-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="72249-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72249-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="72249-108">Return value</span></span>

<span data-ttu-id="72249-109">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="72249-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="72249-110">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="72249-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="72249-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="72249-111">Return code</span></span>                                                                                            | <span data-ttu-id="72249-112">Description</span><span class="sxs-lookup"><span data-stu-id="72249-112">Description</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="72249-113"><dt>**NMERR \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="72249-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="72249-114">NPP 目前正在捕獲資料。</span><span class="sxs-lookup"><span data-stu-id="72249-114">The NPP is currently capturing data.</span></span> <span data-ttu-id="72249-115">當資料捕捉正在進行中時，您無法中斷與網路的連線。</span><span class="sxs-lookup"><span data-stu-id="72249-115">You cannot disconnect from the network while a data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="72249-116"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="72249-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="72249-117">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="72249-117">The NPP is not connected to the network.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="72249-118"><dt>**NMERR \_ 不是 \_ 統計資料 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="72249-118"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="72249-119">NPP 已連接到網路，但不是使用 [**IStats：： Connect**](istats-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="72249-119">The NPP is connected to the network, but not with the [**IStats::Connect**](istats-connect.md) method.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="72249-120">備註</span><span class="sxs-lookup"><span data-stu-id="72249-120">Remarks</span></span>

<span data-ttu-id="72249-121">當 NPP 正在捕捉資料時，無法呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="72249-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="72249-122">先呼叫 **IStats：:D isconnect** 方法，然後呼叫 [**IStats：： Stop**](istats-stop.md)。</span><span class="sxs-lookup"><span data-stu-id="72249-122">Call the **IStats::Disconnect** method first and then call [**IStats::Stop**](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72249-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="72249-123">Requirements</span></span>



| <span data-ttu-id="72249-124">需求</span><span class="sxs-lookup"><span data-stu-id="72249-124">Requirement</span></span> | <span data-ttu-id="72249-125">值</span><span class="sxs-lookup"><span data-stu-id="72249-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72249-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72249-126">Minimum supported client</span></span><br/> | <span data-ttu-id="72249-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72249-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="72249-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72249-128">Minimum supported server</span></span><br/> | <span data-ttu-id="72249-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72249-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="72249-130">標頭</span><span class="sxs-lookup"><span data-stu-id="72249-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="72249-131"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="72249-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="72249-132">DLL</span><span class="sxs-lookup"><span data-stu-id="72249-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72249-133"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72249-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72249-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72249-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72249-135">**IStats**</span><span class="sxs-lookup"><span data-stu-id="72249-135">**IStats**</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="72249-136">**IStats：： Connect**</span><span class="sxs-lookup"><span data-stu-id="72249-136">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="72249-137">**IStats：： Stop**</span><span class="sxs-lookup"><span data-stu-id="72249-137">**IStats::Stop**</span></span>](istats-stop.md)
</dt> </dl>

 

 




