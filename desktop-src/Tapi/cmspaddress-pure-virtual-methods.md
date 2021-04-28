---
description: CMSPAddress 純虛擬方法-這些方法必須由衍生類別覆寫。
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: CMSPAddress 純虛擬方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d9b9494e4ee42972d97433927fd587034af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084206"
---
# <a name="cmspaddress-pure-virtual-methods"></a>CMSPAddress 純虛擬方法

這些方法必須由衍生類別覆寫。



| CMSPAddress 純虛擬方法                           | Description                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | 位址的私用 AddRef 方法。                                                                                                                                                 |
| [**MSPAddressRelease**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | 位址的私用版本方法。                                                                                                                                                |
| [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | 由 TAPI 呼叫以建立呼叫物件。 衍生類別中的實應只呼叫 [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) 函數。        |
| [**ShutdownMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | 由 TAPI 呼叫以關閉呼叫物件。 衍生類別中的實應只呼叫 [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) 函數。 |
| [**GetCallMediaTypes**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | 取得 MSP 所支援的媒體類型。                                                                                                                                                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



