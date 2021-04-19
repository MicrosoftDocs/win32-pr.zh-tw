---
description: 傳送 TAPI 線路 \_ DEVSPECIFICEX 訊息，以通知應用程式發生線上路、位址或電話上的裝置特定事件。 訊息的意義和參數的解讀是裝置特定的。
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: 'LINE_DEVSPECIFICEX 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba25047858c641ea4c6cec7d15ba06df24e8ee39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994783"
---
# <a name="line_devspecificex-message"></a><span data-ttu-id="4baf3-104">行 \_ DEVSPECIFICEX 訊息</span><span class="sxs-lookup"><span data-stu-id="4baf3-104">LINE\_DEVSPECIFICEX message</span></span>

<span data-ttu-id="4baf3-105">傳送 TAPI **線路 \_ DEVSPECIFICEX** 訊息，以通知應用程式發生線上路、位址或電話上的裝置特定事件。</span><span class="sxs-lookup"><span data-stu-id="4baf3-105">The TAPI **LINE\_DEVSPECIFICEX** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="4baf3-106">訊息的意義和參數的解讀是裝置特定的。</span><span class="sxs-lookup"><span data-stu-id="4baf3-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="4baf3-107">參數</span><span class="sxs-lookup"><span data-stu-id="4baf3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4baf3-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="4baf3-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="4baf3-109">線路裝置或呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4baf3-109">A handle to either a line device or call.</span></span> <span data-ttu-id="4baf3-110">此參數是裝置特定的。</span><span class="sxs-lookup"><span data-stu-id="4baf3-110">This parameter is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="4baf3-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="4baf3-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="4baf3-112">開啟行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="4baf3-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="4baf3-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="4baf3-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="4baf3-114">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="4baf3-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="4baf3-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="4baf3-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="4baf3-116">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="4baf3-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="4baf3-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="4baf3-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="4baf3-118">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="4baf3-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4baf3-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="4baf3-119">Return value</span></span>

<span data-ttu-id="4baf3-120">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="4baf3-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4baf3-121">備註</span><span class="sxs-lookup"><span data-stu-id="4baf3-121">Remarks</span></span>

<span data-ttu-id="4baf3-122">服務提供者會使用 **LINE \_ DEVSPECIFICEX** 訊息搭配 [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) 函數。</span><span class="sxs-lookup"><span data-stu-id="4baf3-122">The **LINE\_DEVSPECIFICEX** message is used by a service provider in conjunction with the [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) function.</span></span> <span data-ttu-id="4baf3-123">其意義是裝置特定的。</span><span class="sxs-lookup"><span data-stu-id="4baf3-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="4baf3-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="4baf3-124">Requirements</span></span>



| <span data-ttu-id="4baf3-125">需求</span><span class="sxs-lookup"><span data-stu-id="4baf3-125">Requirement</span></span> | <span data-ttu-id="4baf3-126">值</span><span class="sxs-lookup"><span data-stu-id="4baf3-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4baf3-127">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="4baf3-127">TAPI version</span></span><br/> | <span data-ttu-id="4baf3-128">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="4baf3-128">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="4baf3-129">標頭</span><span class="sxs-lookup"><span data-stu-id="4baf3-129">Header</span></span><br/>       | <dl> <span data-ttu-id="4baf3-130"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="4baf3-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




