---
description: PhoneDevSpecific 函式和其相關聯的電話 \_ DEVSPECIFIC 訊息可讓應用程式存取裝置特定的電話功能，這些功能無法透過手機的一般電話語音服務來使用。
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: 函數和訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cabdc271548e42b20de695296321f5f5ab0fdbe45a246be2b7ccb1993ee5d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660730"
---
# <a name="functions-and-messages"></a>函數和訊息

[**PhoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)函式和其相關聯的 [**電話 \_ DEVSPECIFIC**](phone-devspecific.md)訊息可讓應用程式存取裝置特定的電話功能，這些功能無法透過手機的一般電話語音服務來使用。 換句話說， **phoneDevSpecific** 是裝置專屬的 escape 函式，允許廠商相依的擴充功能，而 PHONE \_ DEVSPECIFIC 則是傳送至應用程式的裝置特定訊息。

[**PhoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)函式的參數設定檔是泛型，因為參數的小部分解釋是由 TAPI 進行。 相反地，參數的解讀是由服務提供者所定義，而且必須由使用這些參數的應用程式加以瞭解。 這些參數只會由 TAPI 從應用程式傳遞至服務提供者。 依賴裝置專屬延伸模組的應用程式通常不會與其他服務提供者合作，但寫入至一般電話語音電話語音的應用程式則可與擴充的服務提供者搭配使用。

 

 



