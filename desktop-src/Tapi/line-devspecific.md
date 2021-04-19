---
description: 傳送 TAPI 線路 \_ DEVSPECIFIC 訊息，以通知應用程式發生線上路、位址或電話上的裝置特定事件。 訊息的意義和參數的解讀是裝置特定的。
ms.assetid: 6a58e77b-6ee2-4d2d-aca2-71b239f6a1dc
title: 'LINE_DEVSPECIFIC 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91907b10c0176258648fa165bbeb922a61a402ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983125"
---
# <a name="line_devspecific-message"></a><span data-ttu-id="5988b-104">行 \_ DEVSPECIFIC 訊息</span><span class="sxs-lookup"><span data-stu-id="5988b-104">LINE\_DEVSPECIFIC message</span></span>

<span data-ttu-id="5988b-105">傳送 TAPI **線路 \_ DEVSPECIFIC** 訊息，以通知應用程式發生線上路、位址或電話上的裝置特定事件。</span><span class="sxs-lookup"><span data-stu-id="5988b-105">The TAPI **LINE\_DEVSPECIFIC** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="5988b-106">訊息的意義和參數的解讀是裝置特定的。</span><span class="sxs-lookup"><span data-stu-id="5988b-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="5988b-107">參數</span><span class="sxs-lookup"><span data-stu-id="5988b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5988b-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="5988b-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="5988b-109">線路裝置或呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5988b-109">A handle to either a line device or call.</span></span> <span data-ttu-id="5988b-110">這是裝置特定的。</span><span class="sxs-lookup"><span data-stu-id="5988b-110">This is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="5988b-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="5988b-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="5988b-112">開啟行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="5988b-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="5988b-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="5988b-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="5988b-114">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="5988b-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="5988b-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="5988b-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="5988b-116">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="5988b-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="5988b-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="5988b-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="5988b-118">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="5988b-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5988b-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="5988b-119">Return value</span></span>

<span data-ttu-id="5988b-120">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="5988b-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5988b-121">備註</span><span class="sxs-lookup"><span data-stu-id="5988b-121">Remarks</span></span>

<span data-ttu-id="5988b-122">服務提供者會使用 **LINE \_ DEVSPECIFIC** 訊息搭配 [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) 函數。</span><span class="sxs-lookup"><span data-stu-id="5988b-122">The **LINE\_DEVSPECIFIC** message is used by a service provider in conjunction with the [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) function.</span></span> <span data-ttu-id="5988b-123">其意義是裝置特定的。</span><span class="sxs-lookup"><span data-stu-id="5988b-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="5988b-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="5988b-124">Requirements</span></span>



| <span data-ttu-id="5988b-125">需求</span><span class="sxs-lookup"><span data-stu-id="5988b-125">Requirement</span></span> | <span data-ttu-id="5988b-126">值</span><span class="sxs-lookup"><span data-stu-id="5988b-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5988b-127">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="5988b-127">TAPI version</span></span><br/> | <span data-ttu-id="5988b-128">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5988b-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5988b-129">標頭</span><span class="sxs-lookup"><span data-stu-id="5988b-129">Header</span></span><br/>       | <dl> <span data-ttu-id="5988b-130"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="5988b-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




