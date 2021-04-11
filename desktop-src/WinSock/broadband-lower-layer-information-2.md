---
description: 此區段會列出寬頻較低層級資訊的類型定義。
ms.assetid: b987dd6b-a611-4297-abaa-fd080cc94f6f
title: 寬頻較低層資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af52d508bb80c8d2ad350fd56760eb094d06545
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690416"
---
# <a name="broadband-lower-layer-information"></a><span data-ttu-id="498aa-103">寬頻較低層資訊</span><span class="sxs-lookup"><span data-stu-id="498aa-103">Broadband Lower Layer Information</span></span>

<span data-ttu-id="498aa-104">此區段會列出寬頻較低層級資訊的類型定義。</span><span class="sxs-lookup"><span data-stu-id="498aa-104">This section lists the type definition for the broadband lower-layer information.</span></span>

``` syntax
#include <windows.h>

/* 
 *  values used for the Layer2Mode field in struct ATM_BLLI_IE
 */
#define BLLI_L2_MODE_NORMAL         0x40
#define BLLI_L2_MODE_EXT            0x80

/* 
 *  values used for the Layer3Mode field in struct ATM_BLLI_IE
 */
#define BLLI_L3_MODE_NORMAL         0x40
#define BLLI_L3_MODE_EXT            0x80

/* 
 *  values used for the Layer3DefaultPacketSize field in struct ATM_BLLI_IE
 */
#define BLLI_L3_PACKET_16           0x04
#define BLLI_L3_PACKET_32           0x05
#define BLLI_L3_PACKET_64           0x06
#define BLLI_L3_PACKET_128          0x07
#define BLLI_L3_PACKET_256          0x08
#define BLLI_L3_PACKET_512          0x09
#define BLLI_L3_PACKET_1024         0x0A
#define BLLI_L3_PACKET_2048         0x0B
#define BLLI_L3_PACKET_4096         0x0C



typedef struct {
    DWORD Layer2Protocol;                 /* User information layer 2 protocol           */
    UCHAR Layer2Mode;
    UCHAR Layer2WindowSize;
    DWORD Layer2UserSpecifiedProtocol;    /* User specified layer 2 protocol information */
    DWORD Layer3Protocol;                 /* User information layer 3 protocol           */
    UCHAR Layer3Mode;
    UCHAR Layer3DefaultPacketSize;
    UCHAR Layer3PacketWindowSize;
    DWORD Layer3UserSpecifiedProtocol;    /* User specified layer 3 protocol information */
    DWORD Layer3IPI;                      /* ISO/IEC TR 9577 Initial Protocol Identifier */
    UCHAR SnapID[5];                      /* SNAP ID consisting of OUI and PID           */
} ATM_BLLI_IE;
```

 

 



