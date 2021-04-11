---
description: PhoneDevSpecific 函式和其相關聯的電話 \_ DEVSPECIFIC 訊息可讓應用程式存取裝置特定的電話功能，這些功能無法透過手機的一般電話語音服務來使用。
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: 函數和訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f85e2ea57ac11da8150d4d0a183c7c4fd2c88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944211"
---
# <a name="functions-and-messages"></a><span data-ttu-id="d203d-103">函數和訊息</span><span class="sxs-lookup"><span data-stu-id="d203d-103">Functions and Messages</span></span>

<span data-ttu-id="d203d-104">[**PhoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)函式和其相關聯的 [**電話 \_ DEVSPECIFIC**](phone-devspecific.md)訊息可讓應用程式存取裝置特定的電話功能，這些功能無法透過手機的一般電話語音服務來使用。</span><span class="sxs-lookup"><span data-stu-id="d203d-104">The [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) function and its associated [**PHONE\_DEVSPECIFIC**](phone-devspecific.md) message enable an application to access device-specific phone features that are unavailable through the common telephony services for phones.</span></span> <span data-ttu-id="d203d-105">換句話說， **phoneDevSpecific** 是裝置專屬的 escape 函式，允許廠商相依的擴充功能，而 PHONE \_ DEVSPECIFIC 則是傳送至應用程式的裝置特定訊息。</span><span class="sxs-lookup"><span data-stu-id="d203d-105">In other words, **phoneDevSpecific** is the device-specific escape function that allows vendor-dependent extensions, and PHONE\_DEVSPECIFIC is the device-specific message that is sent to the application.</span></span>

<span data-ttu-id="d203d-106">[**PhoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)函式的參數設定檔是泛型，因為參數的小部分解釋是由 TAPI 進行。</span><span class="sxs-lookup"><span data-stu-id="d203d-106">The parameter profile of the [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) function is generic in that little interpretation of the parameters is made by TAPI.</span></span> <span data-ttu-id="d203d-107">相反地，參數的解讀是由服務提供者所定義，而且必須由使用這些參數的應用程式加以瞭解。</span><span class="sxs-lookup"><span data-stu-id="d203d-107">Rather, the interpretation of the parameters is defined by the service provider and must be understood by an application that uses them.</span></span> <span data-ttu-id="d203d-108">這些參數只會由 TAPI 從應用程式傳遞至服務提供者。</span><span class="sxs-lookup"><span data-stu-id="d203d-108">The parameters are simply passed through by TAPI from the application to the service provider.</span></span> <span data-ttu-id="d203d-109">依賴裝置專屬延伸模組的應用程式通常不會與其他服務提供者合作，但寫入至一般電話語音電話語音的應用程式則可與擴充的服務提供者搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d203d-109">An application that relies on device-specific extensions will usually not work with other service providers, but applications written to the common telephony phone services will work with the extended service provider.</span></span>

 

 



