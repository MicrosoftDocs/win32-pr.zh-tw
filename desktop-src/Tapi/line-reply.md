---
description: 傳送 TAPI 線路 \_ 回復訊息，以報告以非同步方式完成的函式呼叫結果。
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: 'LINE_REPLY 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed963a777a5073b0182e809eec83fb7f904768e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983214"
---
# <a name="line_reply-message"></a><span data-ttu-id="8596e-103">行 \_ 回復訊息</span><span class="sxs-lookup"><span data-stu-id="8596e-103">LINE\_REPLY message</span></span>

<span data-ttu-id="8596e-104">傳送 TAPI **線路 \_ 回復** 訊息，以報告以非同步方式完成的函式呼叫結果。</span><span class="sxs-lookup"><span data-stu-id="8596e-104">The TAPI **LINE\_REPLY** message is sent to report the results of function calls that completed asynchronously.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="8596e-105">參數</span><span class="sxs-lookup"><span data-stu-id="8596e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8596e-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="8596e-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="8596e-107">未使用。</span><span class="sxs-lookup"><span data-stu-id="8596e-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8596e-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="8596e-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="8596e-109">傳回應用程式的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="8596e-109">Returns the application's callback instance.</span></span>

</dd> <dt>

<span data-ttu-id="8596e-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="8596e-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="8596e-111">這是回復的要求識別碼。</span><span class="sxs-lookup"><span data-stu-id="8596e-111">The request identifier for which this is the reply.</span></span>

</dd> <dt>

<span data-ttu-id="8596e-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="8596e-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="8596e-113">成功或錯誤指示。</span><span class="sxs-lookup"><span data-stu-id="8596e-113">The success or error indication.</span></span> <span data-ttu-id="8596e-114">應用程式應該將此參數轉換為 LONG。</span><span class="sxs-lookup"><span data-stu-id="8596e-114">The application should cast this parameter into a LONG.</span></span> <span data-ttu-id="8596e-115">零表示成功;負數表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="8596e-115">Zero indicates success; a negative number indicates an error.</span></span>

</dd> <dt>

<span data-ttu-id="8596e-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="8596e-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="8596e-117">未使用的。</span><span class="sxs-lookup"><span data-stu-id="8596e-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8596e-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="8596e-118">Return value</span></span>

<span data-ttu-id="8596e-119">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="8596e-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8596e-120">備註</span><span class="sxs-lookup"><span data-stu-id="8596e-120">Remarks</span></span>

<span data-ttu-id="8596e-121">以非同步方式運作的函式會將正面要求識別碼值傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="8596e-121">Functions that operate asynchronously return a positive request identifier value to the application.</span></span> <span data-ttu-id="8596e-122">此要求識別碼會以回復訊息傳回，以識別已完成的要求。</span><span class="sxs-lookup"><span data-stu-id="8596e-122">This request identifier is returned with the reply message to identify the request that was completed.</span></span> <span data-ttu-id="8596e-123">**行 \_ 回復** 訊息的另一個參數會產生成功或失敗指示。</span><span class="sxs-lookup"><span data-stu-id="8596e-123">The other parameter for the **LINE\_REPLY** message carries the success or failure indication.</span></span> <span data-ttu-id="8596e-124">可能的錯誤與對應函式所定義的錯誤相同。</span><span class="sxs-lookup"><span data-stu-id="8596e-124">Possible errors are the same as those defined by the corresponding function.</span></span> <span data-ttu-id="8596e-125">無法停用此訊息。</span><span class="sxs-lookup"><span data-stu-id="8596e-125">This message cannot be disabled.</span></span>

<span data-ttu-id="8596e-126">在某些情況下，應用程式可能無法接收對應至非同步函式呼叫的 **行 \_ 回復** 訊息。</span><span class="sxs-lookup"><span data-stu-id="8596e-126">In some cases, an application may fail to receive the **LINE\_REPLY** message corresponding to a call to an asynchronous function.</span></span> <span data-ttu-id="8596e-127">如果在收到訊息之前將對應的呼叫控制碼解除配置，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="8596e-127">This occurs if the corresponding call handle is deallocated before the message has been received.</span></span>

> [!Note]  
> <span data-ttu-id="8596e-128">當應用程式叫用將資料寫入至應用程式記憶體的任何非同步作業時，應用程式必須保留該記憶體以供寫入，直到收到 **一行 \_ 回復** 或 [**行 \_ GATHERDIGITS**](line-gatherdigits.md) 訊息為止。</span><span class="sxs-lookup"><span data-stu-id="8596e-128">When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a **LINE\_REPLY** or [**LINE\_GATHERDIGITS**](line-gatherdigits.md) message is received.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8596e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="8596e-129">Requirements</span></span>



| <span data-ttu-id="8596e-130">需求</span><span class="sxs-lookup"><span data-stu-id="8596e-130">Requirement</span></span> | <span data-ttu-id="8596e-131">值</span><span class="sxs-lookup"><span data-stu-id="8596e-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8596e-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="8596e-132">TAPI version</span></span><br/> | <span data-ttu-id="8596e-133">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="8596e-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8596e-134">標頭</span><span class="sxs-lookup"><span data-stu-id="8596e-134">Header</span></span><br/>       | <dl> <span data-ttu-id="8596e-135"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="8596e-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8596e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8596e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8596e-137">**行 \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="8596e-137">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> </dl>

 

 




