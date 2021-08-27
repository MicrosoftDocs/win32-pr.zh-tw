---
description: 當新的通訊會話抵達時，在位址和媒體類型中註冊感興趣的 TAPI 應用程式將會收到事件通知。
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: 回應在別處起始的會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c74554b48919f7532561bfdf0bab7a163a58fbeb3734dc15e4a8d7e0869dad2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072848"
---
# <a name="respond-to-session-initiated-elsewhere"></a>回應在別處起始的會話

當新的通訊會話抵達時，在 [位址](address-ovr.md) 和 [媒體類型](media-type-ovr.md) 中註冊感興趣的 TAPI 應用程式將會收到 [事件通知](event-notification.md)。 只有一個應用程式會透過會話提供擁有權 [許可權](privilege-ovr.md) 。 此應用程式無法拒絕會話。

傳入會話的初始撥號狀態為 [提供]。 當通話處於供應狀態時，如果服務提供者提供了此資訊且可供使用，則應用程式可以取得持有人模式和呼叫原因等資訊。 某些呼叫資訊可能無法立即使用，例如呼叫者識別碼。

提供的會話有六個基本的回應： [回答](answer-ovr.md)、 [接受](accept-ovr.md)、 [遞交](handoffs-ovr.md)、 [捨棄](drop-ovr.md)、 [轉寄](forward-ovr.md)和重新 [導向](redirect-ovr.md)。 根據服務提供者，這些作業的完整集合可能無法使用。

 

 



