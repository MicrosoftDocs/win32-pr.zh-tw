---
title: 建立和系結至要求佇列
description: 要求佇列是保留特定應用程式暫止要求的服務佇列。
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c3a36fbbb9a8bcaa1c4e708240e99c276b09448ca56615df7da3d2cdf26836
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914278"
---
# <a name="creating-and-binding-to-a-request-queue"></a>建立和系結至要求佇列

要求佇列是保留特定應用程式暫止要求的服務佇列。 應用程式會藉由呼叫 [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) 函式來建立獨立于 URL 群組或伺服器會話的要求佇列，並藉由呼叫 [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) 函數來設定要求佇列屬性。 這些屬性是503回應的詳細資訊、佇列的最大長度，以及活動狀態。

為了將要求路由傳送至其要求佇列，應用程式會藉 [**由呼叫**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) *Property* 參數中指定的 **HttpServerBindingProperty** ，將其建立為 [執行時間](run-time-configuration.md)設定一部分的 URL 群組系結至佇列。 從群組中的 Url 傳入的要求會路由傳送至指定的要求佇列。

 

 




