---
description: 這些方法必須由衍生類別覆寫。
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: CMSPCallBase 純虛擬方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d8dea4c1a240e362a4dc3a19b3c09a37a318947
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849421"
---
# <a name="cmspcallbase-pure-virtual-methods"></a>CMSPCallBase 純虛擬方法

這些方法必須由衍生類別覆寫。



| CMSPCallBase 純虛擬方法                                 | Description                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPCallAddRef**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | Call 物件的私用 AddRef 方法。                                                                                              |
| [**MSPCallRelease**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | 呼叫物件的私用版本方法。                                                                                             |
| [**Init**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | 由 MSP 位址物件呼叫 (在方法 [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall) 中) 初始化 MSP 呼叫物件。 |
| [**關閉**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | 由 MSP 位址物件呼叫，以關閉呼叫。                                                                                |
| [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | 由 [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) 呼叫以建立資料流程物件。                                               |
| [**CreateStreamObject**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | 由 [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) 呼叫以建立資料流程物件。                                  |
| [**RemoveStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | 由應用程式呼叫以從呼叫中移除資料流程                                                                              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
