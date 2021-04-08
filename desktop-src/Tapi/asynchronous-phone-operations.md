---
description: 電話有九個相關的非同步作業。
ms.assetid: b255bdde-1677-401f-b02d-4850e0e98dc4
title: 非同步電話作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4a70a1d980c4f0d42d5160ee020531b538f488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850483"
---
# <a name="asynchronous-phone-operations"></a>非同步電話作業

電話有九個相關的非同步作業。 這些是由 [**TSPI \_ phoneDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_phonedevspecific)、 [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo)、 [**TSPI \_ phoneSetData**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdata)、 [**TSPI \_ phoneSetDisplay**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdisplay)、 [**TSPI \_ phoneSetGain**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetgain)、 [**TSPI \_ phoneSetHookSwitch**](/windows/win32/api/tspi/nf-tspi-tspi_phonesethookswitch)、 [**TSPI \_ phoneSetLamp**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetlamp)、 [**TSPI \_ phoneSetRing**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetring)和 [**TSPI \_ phoneSetVolume**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetvolume) 函數所起始。 如果應用程式呼叫 TAPI [**phoneClose**](/windows/win32/api/tapi/nf-tapi-phoneclose) 函式，且具有手機唯一的控制碼，則 TAPI 會呼叫 [**TSPI \_ phoneClose**](/windows/win32/api/tspi/nf-tspi-tspi_phoneclose) 函式，以指示服務提供者終止非同步作業，並適當地呼叫 [*完成 \_ 程式回檔*](/windows/win32/api/tspi/nc-tspi-async_completion) 函式。 如果應用程式沒有手機的唯一控制碼，服務提供者不會收到要求的通知，且任何未完成的非同步作業都會保持作用中狀態。

 

 
