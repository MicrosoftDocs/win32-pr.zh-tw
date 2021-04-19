---
description: '\_當指定的線路裝置已強制關閉時，就會傳送 TAPI 線路關閉訊息。 一旦傳送此訊息之後，行裝置控制碼或該行的任何呼叫控制碼將不再有效。'
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: 'LINE_CLOSE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4fde53d1017b2dcd9fe4ea833803055d9f2dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987095"
---
# <a name="line_close-message"></a><span data-ttu-id="9c5ed-104">行 \_ 關閉訊息</span><span class="sxs-lookup"><span data-stu-id="9c5ed-104">LINE\_CLOSE message</span></span>

<span data-ttu-id="9c5ed-105">當指定的線路裝置已強制關閉時，就會傳送 TAPI **線路 \_ 關閉** 訊息。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-105">The TAPI **LINE\_CLOSE** message is sent when the specified line device has been forcibly closed.</span></span> <span data-ttu-id="9c5ed-106">一旦傳送此訊息之後，行裝置控制碼或該行的任何呼叫控制碼將不再有效。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-106">The line device handle or any call handles for calls on the line are no longer valid once this message has been sent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="9c5ed-107">參數</span><span class="sxs-lookup"><span data-stu-id="9c5ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c5ed-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="9c5ed-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="9c5ed-109">已關閉之線路裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-109">A handle to the line device that was closed.</span></span> <span data-ttu-id="9c5ed-110">這個控制碼已不再有效。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-110">This handle is no longer valid.</span></span>

</dd> <dt>

<span data-ttu-id="9c5ed-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="9c5ed-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="9c5ed-112">開啟行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="9c5ed-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="9c5ed-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="9c5ed-114">未使用的。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-114">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="9c5ed-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="9c5ed-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="9c5ed-116">未使用的。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="9c5ed-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="9c5ed-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="9c5ed-118">未使用的。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c5ed-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c5ed-119">Return value</span></span>

<span data-ttu-id="9c5ed-120">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c5ed-121">備註</span><span class="sxs-lookup"><span data-stu-id="9c5ed-121">Remarks</span></span>

<span data-ttu-id="9c5ed-122">只有在 TAPI 服務提供者 (TSP) 強制關閉開啟行後，才會將 **行 \_ 關閉** 訊息傳送至任何應用程式。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-122">The **LINE\_CLOSE** message is sent to any application only after the TAPI service provider (TSP) has forcibly closed an open line.</span></span> <span data-ttu-id="9c5ed-123">是否可以在強制關閉之後立即重新開啟行，就是裝置特定的。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-123">Whether or not the line can be reopened immediately after a forced close is device-specific.</span></span>

<span data-ttu-id="9c5ed-124">造成的狀況可能是狀態的重大變更、硬體錯誤、伺服器的連線中斷，或甚至可能防止單一應用程式獨佔線路裝置的時間太長。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-124">The causing condition can be a significant change of state, a hardware error, a loss of connection to a server, or even potentially to prevent a single application from monopolizing a line device for too long.</span></span> <span data-ttu-id="9c5ed-125">在使用者修改該行或其驅動程式的設定之後，也可以強制關閉線路裝置。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-125">A line device can also be forcibly closed after the user has modified the configuration of that line or its driver.</span></span> <span data-ttu-id="9c5ed-126">如果使用者想要讓設定變更立即生效 (而不是在下一次系統重新開機) 後，它們會影響應用程式目前的裝置視圖 (例如裝置功能) 的變更，則服務提供者可以強制關閉線路裝置。</span><span class="sxs-lookup"><span data-stu-id="9c5ed-126">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and they affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the line device.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c5ed-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c5ed-127">Requirements</span></span>



| <span data-ttu-id="9c5ed-128">需求</span><span class="sxs-lookup"><span data-stu-id="9c5ed-128">Requirement</span></span> | <span data-ttu-id="9c5ed-129">值</span><span class="sxs-lookup"><span data-stu-id="9c5ed-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9c5ed-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="9c5ed-130">TAPI version</span></span><br/> | <span data-ttu-id="9c5ed-131">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9c5ed-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="9c5ed-132">標頭</span><span class="sxs-lookup"><span data-stu-id="9c5ed-132">Header</span></span><br/>       | <dl> <span data-ttu-id="9c5ed-133"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="9c5ed-133"><dt>Tapi.h</dt></span></span> </dl> |



 

 




