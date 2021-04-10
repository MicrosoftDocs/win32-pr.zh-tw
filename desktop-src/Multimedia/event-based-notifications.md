---
title: Event-Based 通知
description: Event-Based 通知
ms.assetid: bd483865-f983-416a-9b72-475fe9679cd1
keywords:
- 操縱杆，通知
- 操縱杆，訊息
- 操縱杆，以事件為基礎的通知
- 操縱杆，移動閾值
- 以事件為基礎的搖桿通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1aa36809942593cdbe21b61af0d4f07f02b186a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681815"
---
# <a name="event-based-notifications"></a><span data-ttu-id="6b327-108">Event-Based 通知</span><span class="sxs-lookup"><span data-stu-id="6b327-108">Event-Based Notifications</span></span>

<span data-ttu-id="6b327-109">只要搖桿軸的位置值大於裝置的 *移動臨界* 值，您就可以要求系統將搖桿訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="6b327-109">You can ask the system to send joystick messages to an application whenever the position of a joystick axis changes by a value greater than the *movement threshold* of the device.</span></span> <span data-ttu-id="6b327-110">移動閾值是在搖桿位置變更訊息傳送至已捕獲裝置的視窗之前，搖桿必須移動的距離。</span><span class="sxs-lookup"><span data-stu-id="6b327-110">The movement threshold is the distance the joystick must be moved before a joystick position change message is sent to a window that has captured the device.</span></span> <span data-ttu-id="6b327-111">如需詳細資訊，請參閱 [**mm \_ JOY1MOVE**](mm-joy1move.md)、 [**mm \_ JOY1ZMOVE**](mm-joy1zmove.md)、 [**mm \_ JOY2MOVE**](mm-joy2move.md)或 [**mm \_ JOY2ZMOVE**](mm-joy2zmove.md)。</span><span class="sxs-lookup"><span data-stu-id="6b327-111">For more information, see [**MM\_JOY1MOVE**](mm-joy1move.md), [**MM\_JOY1ZMOVE**](mm-joy1zmove.md), [**MM\_JOY2MOVE**](mm-joy2move.md), or [**MM\_JOY2ZMOVE**](mm-joy2zmove.md).</span></span>

<span data-ttu-id="6b327-112">閾值一開始為零。</span><span class="sxs-lookup"><span data-stu-id="6b327-112">The threshold is initially zero.</span></span> <span data-ttu-id="6b327-113">您可以使用 [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) 函數來設定移動臨界值。</span><span class="sxs-lookup"><span data-stu-id="6b327-113">You can set the movement threshold by using the [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) function.</span></span> <span data-ttu-id="6b327-114">您可以使用 [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) 函式來取得搖桿的最小輪詢頻率。</span><span class="sxs-lookup"><span data-stu-id="6b327-114">You can retrieve the minimum polling frequency of the joystick by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function.</span></span>

 

 