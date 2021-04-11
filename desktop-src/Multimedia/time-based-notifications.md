---
title: Time-Based 通知
description: Time-Based 通知
ms.assetid: cf7bc0d4-f3bd-4416-b85f-0ff51a0efbbc
keywords:
- 操縱杆，通知
- 操縱杆，訊息
- 操縱杆，以時間為基礎的通知
- 以時間為基礎的搖桿通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15dff2a6140bd993157f20e92488afce1b646e20
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933096"
---
# <a name="time-based-notifications"></a><span data-ttu-id="470d0-107">Time-Based 通知</span><span class="sxs-lookup"><span data-stu-id="470d0-107">Time-Based Notifications</span></span>

<span data-ttu-id="470d0-108">您可以藉由將 [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture)的 *fChanged* 參數設定為 **FALSE** ，並指定連續訊息之間的間隔長度，來通知作業系統將搖桿訊息定期傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="470d0-108">You can notify the operating system to send joystick messages to an application at regular time intervals by setting the *fChanged* parameter of [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) to **FALSE** and by specifying the interval length between successive messages.</span></span> <span data-ttu-id="470d0-109">若要這樣做，請在搖桿的最小和最大輪詢頻率之間指派一個值給 *uPeriod* 參數。</span><span class="sxs-lookup"><span data-stu-id="470d0-109">To do this, assign the *uPeriod* parameter a value between the minimum and maximum polling frequencies for the joystick.</span></span> <span data-ttu-id="470d0-110">您可以使用 [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps)函式來判斷此範圍，該函數會填入 [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps)結構中的 **wPeriodMin** 和 **wPeriodMax** 成員。</span><span class="sxs-lookup"><span data-stu-id="470d0-110">You can determine this range by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function, which fills the **wPeriodMin** and **wPeriodMax** members in the [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) structure.</span></span> <span data-ttu-id="470d0-111">如果 *uPeriod* 值超出搖桿的有效輪詢頻率範圍，則搖桿驅動程式會使用最小或最大的輪詢頻率，以較接近 *uPeriod* 的值為准。</span><span class="sxs-lookup"><span data-stu-id="470d0-111">If the *uPeriod* value is outside the range of valid polling frequencies for the joystick, the joystick driver uses the minimum or maximum polling frequency, whichever is closer to the *uPeriod* value.</span></span>

> [!Note]  
> <span data-ttu-id="470d0-112">Windows 會在每次呼叫 **joySetCapture** 時設定計時器事件。</span><span class="sxs-lookup"><span data-stu-id="470d0-112">Windows sets up a timer event with each call to **joySetCapture**.</span></span>

 

 

 