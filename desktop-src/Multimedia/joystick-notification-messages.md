---
title: 搖桿通知訊息
description: 搖桿通知訊息
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- 操縱杆，通知
- 操縱杆，訊息
- 操縱杆、位置
- 操縱杆，按鈕
- MM_JOY1 訊息
- MM_JOY2 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f999dab49ea6684e9184f6ed5c46286518b97
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967408"
---
# <a name="joystick-notification-messages"></a><span data-ttu-id="2cd88-109">搖桿通知訊息</span><span class="sxs-lookup"><span data-stu-id="2cd88-109">Joystick Notification Messages</span></span>

<span data-ttu-id="2cd88-110">操縱杆訊息會通知您的應用程式，搖桿已變更位置或其中一個按鈕的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="2cd88-110">Joystick messages notify your application that a joystick has changed position or that one of its buttons has changed states.</span></span> <span data-ttu-id="2cd88-111">\_如果您的應用程式使用識別碼 JOYSTICKID1 從搖桿要求輸入，則會將以 MM JOY1 開頭的訊息傳送至函式，而 \_ 如果您的應用程式使用識別碼 JOYSTICKID2 從搖桿要求輸入，則會傳送 mm JOY2 訊息。</span><span class="sxs-lookup"><span data-stu-id="2cd88-111">Messages beginning with MM\_JOY1 are sent to the function if your application requests input from the joystick using the identifier JOYSTICKID1, and MM\_JOY2 messages are sent if your application requests input from the joystick using the identifier JOYSTICKID2.</span></span>

<span data-ttu-id="2cd88-112">下表中的訊息會識別搖桿按鈕的狀態：</span><span class="sxs-lookup"><span data-stu-id="2cd88-112">The messages in the following table identify the status of the joystick buttons:</span></span>



| <span data-ttu-id="2cd88-113">訊息</span><span class="sxs-lookup"><span data-stu-id="2cd88-113">Message</span></span>                                         | <span data-ttu-id="2cd88-114">描述</span><span class="sxs-lookup"><span data-stu-id="2cd88-114">Description</span></span>                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="2cd88-115">**MM \_ JOY1BUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="2cd88-115">**MM\_JOY1BUTTONDOWN**</span></span>](mm-joy1buttondown.md) | <span data-ttu-id="2cd88-116">已按下游戲杆 JOYSTICKID1 上的按鈕。</span><span class="sxs-lookup"><span data-stu-id="2cd88-116">A button on joystick JOYSTICKID1 has been pressed.</span></span>              |
| [<span data-ttu-id="2cd88-117">**MM \_ JOY1BUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="2cd88-117">**MM\_JOY1BUTTONUP**</span></span>](mm-joy1buttonup.md)     | <span data-ttu-id="2cd88-118">已釋放搖桿 JOYSTICKID1 上的按鈕。</span><span class="sxs-lookup"><span data-stu-id="2cd88-118">A button on joystick JOYSTICKID1 has been released.</span></span>             |
| [<span data-ttu-id="2cd88-119">**MM \_ JOY1MOVE**</span><span class="sxs-lookup"><span data-stu-id="2cd88-119">**MM\_JOY1MOVE**</span></span>](mm-joy1move.md)             | <span data-ttu-id="2cd88-120">操縱杆 JOYSTICKID1 已變更 x 或 y 方向的位置。</span><span class="sxs-lookup"><span data-stu-id="2cd88-120">Joystick JOYSTICKID1 changed position in the x- or y-direction.</span></span> |
| [<span data-ttu-id="2cd88-121">**MM \_ JOY1ZMOVE**</span><span class="sxs-lookup"><span data-stu-id="2cd88-121">**MM\_JOY1ZMOVE**</span></span>](mm-joy1zmove.md)           | <span data-ttu-id="2cd88-122">操縱杆 JOYSTICKID1 以 z 方向變更位置。</span><span class="sxs-lookup"><span data-stu-id="2cd88-122">Joystick JOYSTICKID1 changed position in the z-direction.</span></span>       |
| [<span data-ttu-id="2cd88-123">**MM \_ JOY2BUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="2cd88-123">**MM\_JOY2BUTTONDOWN**</span></span>](mm-joy2buttondown.md) | <span data-ttu-id="2cd88-124">已按下游戲杆 JOYSTICKID2 上的按鈕。</span><span class="sxs-lookup"><span data-stu-id="2cd88-124">A button on joystick JOYSTICKID2 has been pressed.</span></span>              |
| [<span data-ttu-id="2cd88-125">**MM \_ JOY2BUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="2cd88-125">**MM\_JOY2BUTTONUP**</span></span>](mm-joy2buttonup.md)     | <span data-ttu-id="2cd88-126">已釋放搖桿 JOYSTICKID2 上的按鈕。</span><span class="sxs-lookup"><span data-stu-id="2cd88-126">A button on joystick JOYSTICKID2 has been released.</span></span>             |
| [<span data-ttu-id="2cd88-127">**MM \_ JOY2MOVE**</span><span class="sxs-lookup"><span data-stu-id="2cd88-127">**MM\_JOY2MOVE**</span></span>](mm-joy2move.md)             | <span data-ttu-id="2cd88-128">操縱杆 JOYSTICKID2 已變更 x 或 y 方向的位置</span><span class="sxs-lookup"><span data-stu-id="2cd88-128">Joystick JOYSTICKID2 changed position in the x- or y-direction</span></span>  |
| [<span data-ttu-id="2cd88-129">**MM \_ JOY2ZMOVE**</span><span class="sxs-lookup"><span data-stu-id="2cd88-129">**MM\_JOY2ZMOVE**</span></span>](mm-joy2zmove.md)           | <span data-ttu-id="2cd88-130">操縱杆 JOYSTICKID2 以 z 方向變更位置。</span><span class="sxs-lookup"><span data-stu-id="2cd88-130">Joystick JOYSTICKID2 changed position in the z-direction.</span></span>       |



 

<span data-ttu-id="2cd88-131">所有訊息都會將不存在的按鈕報告為已發行。</span><span class="sxs-lookup"><span data-stu-id="2cd88-131">All messages report nonexistent buttons as released.</span></span>

 

 




