---
description: '\_當已在資源回收中強制關閉開啟的電話裝置時，就會傳送 TAPI 電話關閉訊息。 傳送此訊息之後，裝置控制碼已不再有效。'
ms.assetid: 84650abf-235e-4792-a67d-2f0f08b85a32
title: 'PHONE_CLOSE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9a7641b437a10098806fc7ad52aa64200ca015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993383"
---
# <a name="phone_close-message"></a><span data-ttu-id="74957-104">電話 \_ 關閉訊息</span><span class="sxs-lookup"><span data-stu-id="74957-104">PHONE\_CLOSE message</span></span>

<span data-ttu-id="74957-105">當已在資源回收中強制關閉開啟的電話裝置時，就會傳送 TAPI **電話 \_ 關閉** 訊息。</span><span class="sxs-lookup"><span data-stu-id="74957-105">The TAPI **PHONE\_CLOSE** message is sent when an open phone device has been forcibly closed as part of resource reclamation.</span></span> <span data-ttu-id="74957-106">傳送此訊息之後，裝置控制碼已不再有效。</span><span class="sxs-lookup"><span data-stu-id="74957-106">The device handle is no longer valid once this message has been sent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="74957-107">參數</span><span class="sxs-lookup"><span data-stu-id="74957-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74957-108">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="74957-108">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="74957-109">已關閉之 open phone 裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="74957-109">A handle to the open phone device that was closed.</span></span> <span data-ttu-id="74957-110">傳送此訊息之後，控制碼已不再有效。</span><span class="sxs-lookup"><span data-stu-id="74957-110">The handle is no longer valid after this message has been sent.</span></span>

</dd> <dt>

<span data-ttu-id="74957-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="74957-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="74957-112">開啟手機裝置時提供的應用程式回呼實例。</span><span class="sxs-lookup"><span data-stu-id="74957-112">The application's callback instance that provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="74957-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="74957-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="74957-114">未使用的。</span><span class="sxs-lookup"><span data-stu-id="74957-114">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="74957-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="74957-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="74957-116">未使用的。</span><span class="sxs-lookup"><span data-stu-id="74957-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="74957-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="74957-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="74957-118">未使用的。</span><span class="sxs-lookup"><span data-stu-id="74957-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74957-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="74957-119">Return value</span></span>

<span data-ttu-id="74957-120">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="74957-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74957-121">備註</span><span class="sxs-lookup"><span data-stu-id="74957-121">Remarks</span></span>

<span data-ttu-id="74957-122">只有在已強制關閉開啟的電話之後，才會將 **電話 \_ 關閉** 訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="74957-122">The **PHONE\_CLOSE** message is only sent to an application after an open phone has been forcibly closed.</span></span> <span data-ttu-id="74957-123">這麼做是為了防止單一應用程式將手機裝置獨佔太長的時間。</span><span class="sxs-lookup"><span data-stu-id="74957-123">This can be done to prevent a single application from monopolizing a phone device for too long.</span></span> <span data-ttu-id="74957-124">是否可以在強制關閉之後立即重新開啟電話，即裝置特定。</span><span class="sxs-lookup"><span data-stu-id="74957-124">Whether the phone can be reopened immediately after a forced close is device specific.</span></span>

<span data-ttu-id="74957-125">在使用者修改該電話的設定或其驅動程式之後，也可以強制關閉開啟的電話裝置。</span><span class="sxs-lookup"><span data-stu-id="74957-125">An open phone device can also be forcibly closed after the user has modified the configuration of that phone or its driver.</span></span> <span data-ttu-id="74957-126">如果使用者想要讓設定變更立即生效 (而不是在下一次系統重新開機) 之後，而這些變更會影響應用程式目前的裝置視圖 (例如裝置功能) 的變更，則服務提供者可以強制關閉電話裝置。</span><span class="sxs-lookup"><span data-stu-id="74957-126">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and these changes affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the phone device.</span></span>

## <a name="requirements"></a><span data-ttu-id="74957-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="74957-127">Requirements</span></span>



| <span data-ttu-id="74957-128">需求</span><span class="sxs-lookup"><span data-stu-id="74957-128">Requirement</span></span> | <span data-ttu-id="74957-129">值</span><span class="sxs-lookup"><span data-stu-id="74957-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="74957-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="74957-130">TAPI version</span></span><br/> | <span data-ttu-id="74957-131">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="74957-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="74957-132">標頭</span><span class="sxs-lookup"><span data-stu-id="74957-132">Header</span></span><br/>       | <dl> <span data-ttu-id="74957-133"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="74957-133"><dt>Tapi.h</dt></span></span> </dl> |



 

 




