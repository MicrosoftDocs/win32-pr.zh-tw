---
description: 這些方法必須由衍生類別覆寫。
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: CMSPAddress 純虛擬方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93c9b2a995554dd2f7412c8fa5bf153ea8871e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985458"
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

 

 



