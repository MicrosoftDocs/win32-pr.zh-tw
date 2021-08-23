---
title: 取得驅動程式功能
description: 取得驅動程式功能
ms.assetid: 761886db-b2e5-449c-b526-6e992cc1b42f
keywords:
- 操縱杆，驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd5bd178b1658ccecd9af26e6729fc00beab95b55fb4c8189feeada92c029d5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691308"
---
# <a name="getting-the-driver-capabilities"></a>取得驅動程式功能

下列範例會使用 [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) 和 [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) 來判斷搖桿服務是否可用，以及搖桿是否已連接到其中一個埠。


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



 

 