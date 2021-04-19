---
description: TAPI 電話 \_ 回復訊息會傳送至應用程式，以報告以非同步方式完成的函式呼叫結果。
ms.assetid: 434f37d6-f385-4cc9-9658-2b683cab532c
title: 'PHONE_REPLY 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091920c631bf56d58959d60288a1af039495d2d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976764"
---
# <a name="phone_reply-message"></a><span data-ttu-id="17a99-103">電話 \_ 回復訊息</span><span class="sxs-lookup"><span data-stu-id="17a99-103">PHONE\_REPLY message</span></span>

<span data-ttu-id="17a99-104">TAPI **電話 \_ 回復** 訊息會傳送至應用程式，以報告以非同步方式完成的函式呼叫結果。</span><span class="sxs-lookup"><span data-stu-id="17a99-104">The TAPI **PHONE\_REPLY** message is sent to an application to report the results of function call that completed asynchronously.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="17a99-105">參數</span><span class="sxs-lookup"><span data-stu-id="17a99-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17a99-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="17a99-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="17a99-107">未使用的。</span><span class="sxs-lookup"><span data-stu-id="17a99-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="17a99-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="17a99-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="17a99-109">傳回應用程式的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="17a99-109">Returns the application's callback instance.</span></span>

</dd> <dt>

<span data-ttu-id="17a99-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="17a99-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="17a99-111">這是回復的要求識別碼。</span><span class="sxs-lookup"><span data-stu-id="17a99-111">The request identifier for which this is the reply.</span></span>

</dd> <dt>

<span data-ttu-id="17a99-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="17a99-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="17a99-113">成功或錯誤指示。</span><span class="sxs-lookup"><span data-stu-id="17a99-113">The success or error indication.</span></span> <span data-ttu-id="17a99-114">應用程式應該將此參數轉換為 LONG。</span><span class="sxs-lookup"><span data-stu-id="17a99-114">The application should cast this parameter into a LONG.</span></span> <span data-ttu-id="17a99-115">零表示成功;負數表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="17a99-115">Zero indicates success; a negative number indicates an error.</span></span>

</dd> <dt>

<span data-ttu-id="17a99-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="17a99-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="17a99-117">未使用的。</span><span class="sxs-lookup"><span data-stu-id="17a99-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17a99-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="17a99-118">Return value</span></span>

<span data-ttu-id="17a99-119">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="17a99-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17a99-120">備註</span><span class="sxs-lookup"><span data-stu-id="17a99-120">Remarks</span></span>

<span data-ttu-id="17a99-121">以非同步方式運作的函式會將正面要求識別碼值傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="17a99-121">Functions that operate asynchronously return a positive request identifier value to the application.</span></span> <span data-ttu-id="17a99-122">此要求識別碼會以回復訊息傳回，以識別已完成的要求。</span><span class="sxs-lookup"><span data-stu-id="17a99-122">This request identifier is returned with the reply message to identify the request that was completed.</span></span> <span data-ttu-id="17a99-123">**電話 \_ 回復** 訊息的另一個參數會產生成功或失敗的指示。</span><span class="sxs-lookup"><span data-stu-id="17a99-123">The other parameter for the **PHONE\_REPLY** message carries the success or failure indication.</span></span> <span data-ttu-id="17a99-124">可能的錯誤與對應函式所定義的錯誤相同。</span><span class="sxs-lookup"><span data-stu-id="17a99-124">Possible errors are the same as those defined by the corresponding function.</span></span> <span data-ttu-id="17a99-125">無法停用此訊息。</span><span class="sxs-lookup"><span data-stu-id="17a99-125">This message cannot be disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="17a99-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="17a99-126">Requirements</span></span>



| <span data-ttu-id="17a99-127">需求</span><span class="sxs-lookup"><span data-stu-id="17a99-127">Requirement</span></span> | <span data-ttu-id="17a99-128">值</span><span class="sxs-lookup"><span data-stu-id="17a99-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="17a99-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="17a99-129">TAPI version</span></span><br/> | <span data-ttu-id="17a99-130">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="17a99-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="17a99-131">標頭</span><span class="sxs-lookup"><span data-stu-id="17a99-131">Header</span></span><br/>       | <dl> <span data-ttu-id="17a99-132"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="17a99-132"><dt>Tapi.h</dt></span></span> </dl> |



 

 




