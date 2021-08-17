---
title: 設定要求佇列
description: 設定要求佇列
ms.assetid: ab03089c-2ef1-457d-a5f5-a4d400f3a7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08a8f931d8875fda43b485bada93d2bf5291d0d2b90e85c8b31bd631e8c7fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014926"
---
# <a name="configuring-the-request-queue"></a>設定要求佇列

當要求佇列開啟或建立時，呼叫的應用程式會收到它的控制碼，可用於傳送要求或設定要求佇列。 使用 **HttpServerBindingProperty** 呼叫 [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) ，並在 HTTP 系結 [**\_ \_ 資訊**](/windows/desktop/api/Http/ns-http-http_binding_info)結構中提供要求佇列控制碼（在 *PPROPERTYINFORMATION* 參數中指定），就會將 URL 群組與要求佇列產生關聯。 要求佇列屬性只能由建立要求佇列的應用程式設定。 例如，若要設定 server queue length 屬性，建立者應用程式會呼叫 [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty)指定 *property* 參數中的 **HttpServerQueueLengthProperty** 。

 

 




