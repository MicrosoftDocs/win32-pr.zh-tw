---
title: 取得驅動程式功能
description: 取得驅動程式功能
ms.assetid: 761886db-b2e5-449c-b526-6e992cc1b42f
keywords:
- 操縱杆，驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1b9f4d54e80dc589a4c730ef891d8f0bd132e52
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375028"
---
# <a name="getting-the-driver-capabilities"></a><span data-ttu-id="60229-104">取得驅動程式功能</span><span class="sxs-lookup"><span data-stu-id="60229-104">Getting the Driver Capabilities</span></span>

<span data-ttu-id="60229-105">下列範例會使用 [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) 和 [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) 來判斷搖桿服務是否可用，以及搖桿是否已連接到其中一個埠。</span><span class="sxs-lookup"><span data-stu-id="60229-105">The following example uses [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) and [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) to determine whether the joystick services are available and if a joystick is attached to one of the ports.</span></span>


```C++
JOYINFO joyinfo; 
UINT wNumDevs, wDeviceID; 
BOOL bDev1Attached, bDev2Attached; 
 
    if((wNumDevs = joyGetNumDevs()) == 0) 
        return ERR_NODRIVER; 
    bDev1Attached = joyGetPos(JOYSTICKID1,&joyinfo) != JOYERR_UNPLUGGED; 
    bDev2Attached = wNumDevs == 2 && joyGetPos(JOYSTICKID2,&joyinfo) != 
        JOYERR_UNPLUGGED; 
    if(bDev1Attached || bDev2Attached)   // decide which joystick to use 
        wDeviceID = bDev1Attached ? JOYSTICKID1 : JOYSTICKID2; 
    else 
        return ERR_NODEVICE; 

```



 

 