---
description: 傳送 TAPI 線路 \_ 建立訊息，以通知應用程式建立新的線路裝置。
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: 'LINE_CREATE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9973849c3942b5427dfb6b3fe7c47bc4d2a716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995744"
---
# <a name="line_create-message"></a><span data-ttu-id="83331-103">行 \_ 建立訊息</span><span class="sxs-lookup"><span data-stu-id="83331-103">LINE\_CREATE message</span></span>

<span data-ttu-id="83331-104">傳送 TAPI **線路 \_ 建立** 訊息，以通知應用程式建立新的線路裝置。</span><span class="sxs-lookup"><span data-stu-id="83331-104">The TAPI **LINE\_CREATE** message is sent to inform the application of the creation of a new line device.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="83331-105">參數</span><span class="sxs-lookup"><span data-stu-id="83331-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83331-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="83331-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="83331-107">未使用的。</span><span class="sxs-lookup"><span data-stu-id="83331-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="83331-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="83331-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="83331-109">未使用的。</span><span class="sxs-lookup"><span data-stu-id="83331-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="83331-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="83331-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="83331-111">新建立裝置的 *hDeviceID* 。</span><span class="sxs-lookup"><span data-stu-id="83331-111">The *hDeviceID* of the newly created device.</span></span>

</dd> <dt>

<span data-ttu-id="83331-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="83331-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="83331-113">未使用的。</span><span class="sxs-lookup"><span data-stu-id="83331-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="83331-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="83331-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="83331-115">未使用的。</span><span class="sxs-lookup"><span data-stu-id="83331-115">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83331-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="83331-116">Return value</span></span>

<span data-ttu-id="83331-117">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="83331-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83331-118">備註</span><span class="sxs-lookup"><span data-stu-id="83331-118">Remarks</span></span>

<span data-ttu-id="83331-119">較舊的應用程式 (協商 TAPI 1.3 版) 會傳送指定 LINEDEVSTATE 重新初始化的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息 \_ ，要求他們關閉 API 的使用，並再次呼叫 [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) 來取得新的裝置數目。</span><span class="sxs-lookup"><span data-stu-id="83331-119">Older applications (that negotiated TAPI version 1.3) are sent a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message specifying LINEDEVSTATE\_REINIT, which requires them to shut down their use of the API and call [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) again to obtain the new number of devices.</span></span> <span data-ttu-id="83331-120">但與舊版 TAPI 不同的是，此版本不需要在允許重新初始化應用程式之前關閉所有應用程式;在建立新裝置時，將會立即進行重新初始化 (當服務提供者從系統) 移除時，仍需要完成關閉。</span><span class="sxs-lookup"><span data-stu-id="83331-120">Unlike previous versions of TAPI, however, this version does not require all applications to shut down before allowing applications to reinitialize; reinitialization can take place immediately when a new device is created (complete shutdown is still required when a service provider is removed from the system).</span></span>

<span data-ttu-id="83331-121">支援 TAPI 1.4 版或更新版本的應用程式會傳送 **LINE \_ CREATE** message。</span><span class="sxs-lookup"><span data-stu-id="83331-121">Applications supporting TAPI version 1.4 or later are sent a **LINE\_CREATE** message.</span></span> <span data-ttu-id="83331-122">這會通知他們有新裝置和其新的裝置識別碼存在。</span><span class="sxs-lookup"><span data-stu-id="83331-122">This informs them of the existence of the new device and its new device identifier.</span></span> <span data-ttu-id="83331-123">然後，應用程式可以選擇是否嘗試在新裝置的休閒中使用。</span><span class="sxs-lookup"><span data-stu-id="83331-123">The application can then choose whether or not to attempt working with the new device at its leisure.</span></span> <span data-ttu-id="83331-124">這則訊息會傳送至所有支援此 API 或後續版本 API 的應用程式，此 API 稱為 [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) 或 [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)，包括當時沒有任何線路裝置開啟的應用程式。</span><span class="sxs-lookup"><span data-stu-id="83331-124">This message is sent to all applications supporting this or subsequent versions of the API that have called [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), including those that do not have any line devices open at the time.</span></span>

## <a name="requirements"></a><span data-ttu-id="83331-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="83331-125">Requirements</span></span>



| <span data-ttu-id="83331-126">需求</span><span class="sxs-lookup"><span data-stu-id="83331-126">Requirement</span></span> | <span data-ttu-id="83331-127">值</span><span class="sxs-lookup"><span data-stu-id="83331-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="83331-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="83331-128">TAPI version</span></span><br/> | <span data-ttu-id="83331-129">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="83331-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="83331-130">標頭</span><span class="sxs-lookup"><span data-stu-id="83331-130">Header</span></span><br/>       | <dl> <span data-ttu-id="83331-131"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="83331-131"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83331-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83331-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83331-133">**行 \_ LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="83331-133">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="83331-134">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="83331-134">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="83331-135">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="83331-135">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




