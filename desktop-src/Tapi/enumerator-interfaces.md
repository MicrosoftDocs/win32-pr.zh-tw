---
description: 下列介面會根據 COM 標準來列舉 TAPI 3 元素。 這些介面會構成獨立的物件，而且也會以其相關物件摘要。
ms.assetid: 5281aaf8-9774-4332-8861-1f97cf378f42
title: 列舉值介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5204e6e2c10f7dccb561188460cc3b55bc993360a1df78ce2ac7094315e17b3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117945537"
---
# <a name="enumerator-interfaces"></a>列舉值介面

下列介面會根據 COM 標準來列舉 TAPI 3 元素。 這些介面會構成獨立的物件，而且也會以其相關物件摘要。



| 介面                                                                  | 列舉的專案                                                                                                                                    |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress)                                       | [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)                                                                                                                     |
| [**IEnumBstr**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)                                             | **BSTR** 字串，例如 [**ITAddressCapabilities：： EnumerateDeviceClasses**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-enumeratedeviceclasses)所傳回的字串。 |
| [**IEnumCall**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall)                                             | [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)                                                                                                                   |
| [**IEnumCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub)                                       | [**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)                                                                                                                     |
| [**IEnumCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard)                               | [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)                                                                                                             |
| [**IEnumLocation**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumlocation)                                     | [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)                                                                                                           |
| [**IEnumParticipant**](ienumparticipant.md)                               | [**ITParticipant**](itparticipant.md)                                                                                                             |
| [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                                           | [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                                                                                                         |
| [**IEnumPluggableSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo)       | [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo)                                                                     |
| [**IEnumPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo) | [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo)                                                                               |
| [**IEnumQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumqueue)                                           | [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue)                                                                                                                         |
| [**IEnumTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal)                                     | [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                                                                                                   |
| [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass)                           | [**Terminal 類別**](terminal-class.md)                                                                                                           |



 

 

 
