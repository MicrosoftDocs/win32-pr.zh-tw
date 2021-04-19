---
description: 擴充的電話語音功能會依類別列在下表中。
ms.assetid: f16aabf1-c034-4f91-87b2-c98cdf6d67ea
title: 擴充電話語音服務參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86980d7e23b031729c493660d7a31cdb06dc45de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972042"
---
# <a name="extended-telephony-services-reference"></a>擴充電話語音服務參考

擴充的電話語音功能會依類別列在下表中。

## <a name="extended-telephony-functions-for-line-devices"></a>線路裝置的擴充電話語音功能



| 函式                                                   | 描述                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) | 允許應用程式與指定的線路裝置協調使用延伸模組版本。 非同步： |
| [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)                 | 提供服務提供者存取其他 TAPI 功能未提供之裝置特定功能的存取權。 Synchronous： |
| [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)   | 將裝置特定的交換器功能傳送至交換器。 非同步：                                           |



 

## <a name="extended-telephony-functions-for-phone-devices"></a>電話裝置的擴充電話語音功能



| 函式                                                     | 描述                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)                 | 裝置特定的 escape 函式，允許廠商相依的擴充功能。 非同步：                          |
| [**PhoneNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | 允許應用程式與指定的電話裝置協調使用延伸模組版本。 Synchronous： |



 

 

 



