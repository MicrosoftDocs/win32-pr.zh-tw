---
title: DeviceDeparture 事件
description: 從 CachedDevices 方法傳回的裝置清單中移除新的裝置時發生。
ms.assetid: 10451878-e685-4042-9f92-ba3a408c4da0
keywords:
- DeviceDeparture 事件媒體串流 API
topic_type:
- apiref
api_name:
- DeviceDeparture
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e225afcbe8b373b22584eaa3d9fcb09e1eff29c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966852"
---
# <a name="devicedeparture-event"></a><span data-ttu-id="8cd36-104">DeviceDeparture 事件</span><span class="sxs-lookup"><span data-stu-id="8cd36-104">DeviceDeparture event</span></span>

<span data-ttu-id="8cd36-105">從 [**CachedDevices**](idevicecontroller-cacheddevices.md) 方法傳回的裝置清單中移除新的裝置時發生。</span><span class="sxs-lookup"><span data-stu-id="8cd36-105">Occurs when a new device is removed from the list of devices returned by the [**CachedDevices**](idevicecontroller-cacheddevices.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cd36-106">語法</span><span class="sxs-lookup"><span data-stu-id="8cd36-106">Syntax</span></span>


```C++
void DeviceDeparture();
```



## <a name="parameters"></a><span data-ttu-id="8cd36-107">參數</span><span class="sxs-lookup"><span data-stu-id="8cd36-107">Parameters</span></span>

<span data-ttu-id="8cd36-108">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8cd36-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8cd36-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8cd36-109">Return value</span></span>

<span data-ttu-id="8cd36-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8cd36-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cd36-111">備註</span><span class="sxs-lookup"><span data-stu-id="8cd36-111">Remarks</span></span>

<span data-ttu-id="8cd36-112">若要處理此事件的通知，請使用 [**add \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture)方法來註冊 [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))事件處理常式函式。</span><span class="sxs-lookup"><span data-stu-id="8cd36-112">To handle notifications from this event, register a [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) event handler function using the [**add\_DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) method.</span></span> <span data-ttu-id="8cd36-113">若要取消註冊事件處理常式，請使用 [**remove \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) 方法。</span><span class="sxs-lookup"><span data-stu-id="8cd36-113">To unregister the event handler, use the [**remove\_DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) method.</span></span>

 

 