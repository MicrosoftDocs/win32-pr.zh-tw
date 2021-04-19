---
description: TAPI 會將電話 \_ DEVSPECIFIC 訊息傳送至應用程式，以通知應用程式發生在電話上的裝置特定事件。 訊息的意義和參數的解讀是實作為定義。
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: 'PHONE_DEVSPECIFIC 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c817f273a49fdcda36995cec335811fb06c8a917
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988641"
---
# <a name="phone_devspecific-message"></a><span data-ttu-id="c1c9f-104">電話 \_ DEVSPECIFIC 訊息</span><span class="sxs-lookup"><span data-stu-id="c1c9f-104">PHONE\_DEVSPECIFIC message</span></span>

<span data-ttu-id="c1c9f-105">TAPI 會將 **電話 \_ DEVSPECIFIC** 訊息傳送至應用程式，以通知應用程式發生在電話上的裝置特定事件。</span><span class="sxs-lookup"><span data-stu-id="c1c9f-105">TAPI sends the **PHONE\_DEVSPECIFIC** message to an application to notify the application about device-specific events occurring at the phone.</span></span> <span data-ttu-id="c1c9f-106">訊息的意義和參數的解讀是實作為定義。</span><span class="sxs-lookup"><span data-stu-id="c1c9f-106">The meaning of the message and the interpretation of the parameters is implementation-defined.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="c1c9f-107">參數</span><span class="sxs-lookup"><span data-stu-id="c1c9f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1c9f-108">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="c1c9f-108">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="c1c9f-109">手機裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c1c9f-109">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="c1c9f-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="c1c9f-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="c1c9f-111">開啟手機裝置時提供的應用程式回呼實例。</span><span class="sxs-lookup"><span data-stu-id="c1c9f-111">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="c1c9f-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="c1c9f-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="c1c9f-113">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="c1c9f-113">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="c1c9f-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="c1c9f-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="c1c9f-115">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="c1c9f-115">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="c1c9f-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="c1c9f-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="c1c9f-117">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="c1c9f-117">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1c9f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1c9f-118">Return value</span></span>

<span data-ttu-id="c1c9f-119">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="c1c9f-119">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1c9f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1c9f-120">Requirements</span></span>



| <span data-ttu-id="c1c9f-121">需求</span><span class="sxs-lookup"><span data-stu-id="c1c9f-121">Requirement</span></span> | <span data-ttu-id="c1c9f-122">值</span><span class="sxs-lookup"><span data-stu-id="c1c9f-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c1c9f-123">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="c1c9f-123">TAPI version</span></span><br/> | <span data-ttu-id="c1c9f-124">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c1c9f-124">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c1c9f-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c1c9f-125">Header</span></span><br/>       | <dl> <span data-ttu-id="c1c9f-126"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="c1c9f-126"><dt>Tapi.h</dt></span></span> </dl> |



 

 




