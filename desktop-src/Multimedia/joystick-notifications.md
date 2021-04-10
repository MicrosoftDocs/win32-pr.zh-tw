---
title: 搖桿通知
description: 搖桿通知
ms.assetid: 523dfae3-bbd5-4955-96f3-1710e29d003f
keywords:
- 操縱杆，通知
- 操縱杆，訊息
- 捕捉的搖桿
- 未插的操縱杆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2791f8da14107d50afe90d8efbdbfe79acba3093
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023436"
---
# <a name="joystick-notifications"></a><span data-ttu-id="8e9c9-107">搖桿通知</span><span class="sxs-lookup"><span data-stu-id="8e9c9-107">Joystick Notifications</span></span>

<span data-ttu-id="8e9c9-108">您可以使用 [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) 函式來捕捉要傳送至函式的直接搖桿訊息。</span><span class="sxs-lookup"><span data-stu-id="8e9c9-108">You can capture direct joystick messages to be sent to a function by using the [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) function.</span></span> <span data-ttu-id="8e9c9-109">一次只有一個應用程式可以從搖桿捕捉訊息，但您可以使用 [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) 或 [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) 函式，從另一個應用程式查詢搖桿。</span><span class="sxs-lookup"><span data-stu-id="8e9c9-109">Only one application at a time can capture messages from a joystick, but you can query the joystick from another application by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) or [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) function.</span></span>

> [!Note]  
> <span data-ttu-id="8e9c9-110">如果第二個應用程式使用 **joyGetPos** 或 **joyGetPosEx** 來查詢搖桿（大約是傳送訊息的相同時間），則搖桿訊息可能無法連線到捕捉搖桿的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8e9c9-110">A joystick message can fail to reach the application that captured the joystick if a second application uses **joyGetPos** or **joyGetPosEx** to query the joystick at approximately the same time that the message is sent.</span></span> <span data-ttu-id="8e9c9-111">在此情況下，第二個應用程式可能會攔截訊息。</span><span class="sxs-lookup"><span data-stu-id="8e9c9-111">In this case, the second application could intercept the message.</span></span>

 

<span data-ttu-id="8e9c9-112">如果您想要從連接到系統的兩個操縱杆中捕捉訊息，請針對每個搖桿使用 [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) 兩次。</span><span class="sxs-lookup"><span data-stu-id="8e9c9-112">If you want to capture messages from two joysticks attached to the system, use [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) twice, once for each joystick.</span></span> <span data-ttu-id="8e9c9-113">您的視窗會針對每個裝置接收不同的不同訊息。</span><span class="sxs-lookup"><span data-stu-id="8e9c9-113">Your window receives separate and distinct messages for each device.</span></span>

<span data-ttu-id="8e9c9-114">您可以使用 [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) 函式來釋放已捕捉的搖桿。</span><span class="sxs-lookup"><span data-stu-id="8e9c9-114">You can release a captured joystick by using the [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) function.</span></span> <span data-ttu-id="8e9c9-115">如果應用程式未在結束之前釋出遊戲杆，則會在「捕獲視窗」終結後立即自動釋出遊戲杆。</span><span class="sxs-lookup"><span data-stu-id="8e9c9-115">If an application does not release the joystick before ending, the joystick is automatically released shortly after the capture window is destroyed.</span></span>

<span data-ttu-id="8e9c9-116">您無法抓取未插的搖桿。</span><span class="sxs-lookup"><span data-stu-id="8e9c9-116">You cannot capture an unplugged joystick.</span></span> <span data-ttu-id="8e9c9-117">如果未插上指定的裝置， **joySetCapture** 函式會傳回 JOYERR \_ 插即用。</span><span class="sxs-lookup"><span data-stu-id="8e9c9-117">The **joySetCapture** function returns JOYERR\_UNPLUGGED if the specified device is unplugged.</span></span>

 

 