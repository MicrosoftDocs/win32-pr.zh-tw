---
title: 搖桿參考
description: 搖桿參考
ms.assetid: c2ad092f-a0c5-4e28-ada7-227dc52c3c83
keywords:
- Windows 多媒體、搖桿參考
- 多媒體、搖桿參考
- 多媒體輸入、搖桿參考
- 操縱杆，參考
- 操縱杆的參考，關於
- 搖桿參考，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242f3fb21f9da9b1853ae8e9e7f694b9ad3bf711
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842143"
---
# <a name="joystick-reference"></a><span data-ttu-id="447bf-109">搖桿參考</span><span class="sxs-lookup"><span data-stu-id="447bf-109">Joystick Reference</span></span>

<span data-ttu-id="447bf-110">本節說明與操縱杆相關聯的函式、結構和訊息。</span><span class="sxs-lookup"><span data-stu-id="447bf-110">This section describes the functions, structures, and messages associated with joysticks.</span></span> <span data-ttu-id="447bf-111">元素的分組方式如下：</span><span class="sxs-lookup"><span data-stu-id="447bf-111">The elements are grouped as follows:</span></span>

## <a name="device-capabilities"></a><span data-ttu-id="447bf-112">裝置功能</span><span class="sxs-lookup"><span data-stu-id="447bf-112">Device Capabilities</span></span>

-   [<span data-ttu-id="447bf-113">**joyGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="447bf-113">**joyGetDevCaps**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps)
-   [<span data-ttu-id="447bf-114">**joyGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="447bf-114">**joyGetNumDevs**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs)
-   [<span data-ttu-id="447bf-115">**JOYCAPS**</span><span class="sxs-lookup"><span data-stu-id="447bf-115">**JOYCAPS**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joycaps)

## <a name="querying-a-joystick"></a><span data-ttu-id="447bf-116">查詢搖桿</span><span class="sxs-lookup"><span data-stu-id="447bf-116">Querying a Joystick</span></span>

-   [<span data-ttu-id="447bf-117">**joyConfigChanged**</span><span class="sxs-lookup"><span data-stu-id="447bf-117">**joyConfigChanged**</span></span>](/windows/desktop/api/joystickapi/nf-joystickapi-joyconfigchanged)
-   [<span data-ttu-id="447bf-118">**joyGetPos**</span><span class="sxs-lookup"><span data-stu-id="447bf-118">**joyGetPos**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos)
-   [<span data-ttu-id="447bf-119">**joyGetPosEx**</span><span class="sxs-lookup"><span data-stu-id="447bf-119">**joyGetPosEx**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex)
-   [<span data-ttu-id="447bf-120">**JOYINFO**</span><span class="sxs-lookup"><span data-stu-id="447bf-120">**JOYINFO**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joyinfo)
-   [<span data-ttu-id="447bf-121">**JOYINFOEX**</span><span class="sxs-lookup"><span data-stu-id="447bf-121">**JOYINFOEX**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joyinfoex)

## <a name="capturing-a-joystick"></a><span data-ttu-id="447bf-122">捕捉搖桿</span><span class="sxs-lookup"><span data-stu-id="447bf-122">Capturing a Joystick</span></span>

-   [<span data-ttu-id="447bf-123">**joyGetThreshold**</span><span class="sxs-lookup"><span data-stu-id="447bf-123">**joyGetThreshold**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetthreshold)
-   [<span data-ttu-id="447bf-124">**joyReleaseCapture**</span><span class="sxs-lookup"><span data-stu-id="447bf-124">**joyReleaseCapture**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture)
-   [<span data-ttu-id="447bf-125">**joySetCapture**</span><span class="sxs-lookup"><span data-stu-id="447bf-125">**joySetCapture**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture)
-   [<span data-ttu-id="447bf-126">**joySetThreshold**</span><span class="sxs-lookup"><span data-stu-id="447bf-126">**joySetThreshold**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold)
-   [<span data-ttu-id="447bf-127">**MM \_ JOY1BUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="447bf-127">**MM\_JOY1BUTTONDOWN**</span></span>](mm-joy1buttondown.md)
-   [<span data-ttu-id="447bf-128">**MM \_ JOY1BUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="447bf-128">**MM\_JOY1BUTTONUP**</span></span>](mm-joy1buttonup.md)
-   [<span data-ttu-id="447bf-129">**MM \_ JOY1MOVE**</span><span class="sxs-lookup"><span data-stu-id="447bf-129">**MM\_JOY1MOVE**</span></span>](mm-joy1move.md)
-   [<span data-ttu-id="447bf-130">**MM \_ JOY1ZMOVE**</span><span class="sxs-lookup"><span data-stu-id="447bf-130">**MM\_JOY1ZMOVE**</span></span>](mm-joy1zmove.md)
-   [<span data-ttu-id="447bf-131">**MM \_ JOY2BUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="447bf-131">**MM\_JOY2BUTTONDOWN**</span></span>](mm-joy2buttondown.md)
-   [<span data-ttu-id="447bf-132">**MM \_ JOY2BUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="447bf-132">**MM\_JOY2BUTTONUP**</span></span>](mm-joy2buttonup.md)
-   [<span data-ttu-id="447bf-133">**MM \_ JOY2MOVE**</span><span class="sxs-lookup"><span data-stu-id="447bf-133">**MM\_JOY2MOVE**</span></span>](mm-joy2move.md)
-   [<span data-ttu-id="447bf-134">**MM \_ JOY2ZMOVE**</span><span class="sxs-lookup"><span data-stu-id="447bf-134">**MM\_JOY2ZMOVE**</span></span>](mm-joy2zmove.md)

## <a name="related-topics"></a><span data-ttu-id="447bf-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="447bf-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="447bf-136">操縱 杆</span><span class="sxs-lookup"><span data-stu-id="447bf-136">Joysticks</span></span>](joysticks.md)
</dt> </dl>

 

 