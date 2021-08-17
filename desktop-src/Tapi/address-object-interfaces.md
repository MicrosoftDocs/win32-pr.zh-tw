---
description: 位址物件是可以進行或接收呼叫的實體。 相關的介面和方法可讓應用程式取得和設定位址的相關資訊，例如位址是否有呼叫端識別碼支援。
ms.assetid: 6e347e4c-aec3-4bbd-95f3-a68e6e136e11
title: 位址物件介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2254ba47e81ebd40f5ce95a1c870c363d09243c69cec0c4ec358cf3ee5604de7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949174"
---
# <a name="address-object-interfaces"></a>位址物件介面

[位址物件](address-object.md) 是可以進行或接收呼叫的實體。 相關的介面和方法可讓應用程式取得和設定位址的相關資訊，例如位址是否有呼叫端識別碼支援。

[**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent)、 [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo)、 [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)、 [**ITForwardInformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation)、 [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)和 [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress)介面不會直接在位址物件上公開，但與其緊密相關，並在此處列出以供參考便利性。



| 介面                                                            | 描述                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)                                       | 作為 Address 物件的基底介面。                                                                                                  |
| [**ITAddress2**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2)                                     | 衍生自 [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress);提供支援電話裝置的其他方法。                                            |
| [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)               | 取得位址功能的相關資訊。                                                                                          |
| [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent)                             | 提供有關位址事件的資訊。                                                                                                 |
| [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation)                 | 執行位址轉譯。                                                                                                                   |
| [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo)         | 取得位址轉譯資訊。                                                                                                           |
| [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)                               | 提供方法來取出電話卡資訊。                                                                                          |
| [**ITForwardInformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation)                 | 提供設定和執行呼叫轉送的方法。                                                                               |
| [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol)   | 支援需要直接存取裝置及其設定的繼承應用程式。                                                      |
| [**ITLegacyAddressMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2) | 藉由允許設定與線路裝置相關的參數來擴充 [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol) 。 |
| [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)                             | 取得呼叫方的位置相關資訊。                                                                                  |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                             | 取得位址媒體支援功能的相關資訊。                                                                            |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                       | 取得可用終端機的相關資訊，並提供建立額外終端機的方法。                                                   |
| [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress)                                 | 列舉 [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)。                                                                                                      |
| [**IEnumCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard)                         | 列舉 [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)。                                                                                              |



 

如果位址是 [WAVE MSP](wave-msp.md) 位址， [**ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport) 介面也會公開在 address 物件上。

 

 
