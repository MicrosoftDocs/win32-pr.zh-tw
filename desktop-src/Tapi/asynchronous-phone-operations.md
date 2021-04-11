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
# <a name="asynchronous-phone-operations"></a><span data-ttu-id="90d25-103">非同步電話作業</span><span class="sxs-lookup"><span data-stu-id="90d25-103">Asynchronous Phone Operations</span></span>

<span data-ttu-id="90d25-104">電話有九個相關的非同步作業。</span><span class="sxs-lookup"><span data-stu-id="90d25-104">There are nine asynchronous operations related to phones.</span></span> <span data-ttu-id="90d25-105">這些是由 [**TSPI \_ phoneDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_phonedevspecific)、 [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo)、 [**TSPI \_ phoneSetData**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdata)、 [**TSPI \_ phoneSetDisplay**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdisplay)、 [**TSPI \_ phoneSetGain**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetgain)、 [**TSPI \_ phoneSetHookSwitch**](/windows/win32/api/tspi/nf-tspi-tspi_phonesethookswitch)、 [**TSPI \_ phoneSetLamp**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetlamp)、 [**TSPI \_ phoneSetRing**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetring)和 [**TSPI \_ phoneSetVolume**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetvolume) 函數所起始。</span><span class="sxs-lookup"><span data-stu-id="90d25-105">These are initiated by the [**TSPI\_phoneDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_phonedevspecific), [**TSPI\_phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo), [**TSPI\_phoneSetData**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdata), [**TSPI\_phoneSetDisplay**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdisplay), [**TSPI\_phoneSetGain**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetgain), [**TSPI\_phoneSetHookSwitch**](/windows/win32/api/tspi/nf-tspi-tspi_phonesethookswitch), [**TSPI\_phoneSetLamp**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetlamp), [**TSPI\_phoneSetRing**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetring), and [**TSPI\_phoneSetVolume**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetvolume) functions.</span></span> <span data-ttu-id="90d25-106">如果應用程式呼叫 TAPI [**phoneClose**](/windows/win32/api/tapi/nf-tapi-phoneclose) 函式，且具有手機唯一的控制碼，則 TAPI 會呼叫 [**TSPI \_ phoneClose**](/windows/win32/api/tspi/nf-tspi-tspi_phoneclose) 函式，以指示服務提供者終止非同步作業，並適當地呼叫 [*完成 \_ 程式回檔*](/windows/win32/api/tspi/nc-tspi-async_completion) 函式。</span><span class="sxs-lookup"><span data-stu-id="90d25-106">If an application calls the TAPI [**phoneClose**](/windows/win32/api/tapi/nf-tapi-phoneclose) function and has the only handle to the phone, TAPI calls the [**TSPI\_phoneClose**](/windows/win32/api/tspi/nf-tspi-tspi_phoneclose) function to direct the service provider to terminate the asynchronous operations and call the [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) callback function as appropriate.</span></span> <span data-ttu-id="90d25-107">如果應用程式沒有手機的唯一控制碼，服務提供者不會收到要求的通知，且任何未完成的非同步作業都會保持作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="90d25-107">If the application does not have the only handle to the phone, the service provider receives no notification of the request and any outstanding asynchronous operations remain active.</span></span>

 

 
