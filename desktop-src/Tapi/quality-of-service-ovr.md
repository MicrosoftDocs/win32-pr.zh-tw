---
description: 非同步傳輸模式 (ATM) 網路功能逐漸進入運算的主要部分，而對 ATM 的支援已新增至作業系統的許多部分。
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: '服務品質 (電話語音 API) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 131f54d69cd44799f9ea694fe83d50f28fded0ac7c8c15dabfd7a2db499b2293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761229"
---
# <a name="quality-of-service-telephony-api"></a>服務品質 (電話語音 API) 

非同步傳輸模式 (ATM) 網路功能逐漸進入運算的主要部分，而對 ATM 的支援已新增至作業系統的許多部分。 TAPI 也支援在 ATM 設施上建立呼叫的重要屬性。 從應用程式的觀點來看，最重要的就是能夠要求、協調、重新協商和接收服務品質的徵兆， (QOS) 參數的傳入和撥出電話。

TAPI 中的 QOS 資訊會在 [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec)結構中所定義的應用程式與服務提供者之間進行交換，Windows 通訊端2.0 中定義。

應用程式會在啟動通訊會話之前，藉由設定會話資訊值來要求撥出電話的 QOS。 服務提供者將嘗試提供指定的 QOS，如果無法，則會使呼叫失敗。 然後，應用程式可以調整其參數，然後再次嘗試呼叫。 建立呼叫之後，應用程式可以要求 QOS 中的變更。

如果 QOS 層級有任何變更，TAPI 會提供事件通知給擁有者或監視應用程式。

對 QOS 的支援不限於 ATM 傳輸;任何服務提供者都可以執行 QOS 功能。

並非所有服務提供者都支援使用這項資訊。

* * TAPI 2.x： * *[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice)、 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)、 **dwSendingFlowspecSize**、 **dwSendingFlowspecOffset**、 **dwReceivingFlowspecSize** 和 **dwReceivingFlowspecOffset** 成員 [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)

* * TAPI 3.x： * *[**ITBasicCallControl：： SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos)， [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)

 

 
