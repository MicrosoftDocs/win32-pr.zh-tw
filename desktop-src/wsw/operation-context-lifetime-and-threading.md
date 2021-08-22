---
title: 作業內容存留期和執行緒
description: 作業內容的存留期（以 WS 作業 \_ \_ 內容控制碼表示）會決定它所包含之屬性的存留期。
ms.assetid: 37caf382-2b33-464d-b6c1-e4bd3271a5aa
keywords:
- Windows 的操作內容存留期和執行緒 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd2748f797e43bab750f4e02409e62e6293b39cb44d4cfd3626f86099502fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344828"
---
# <a name="operation-context-lifetime-and-threading"></a>作業內容存留期和執行緒

作業內容的存留期（以 [WS 作業 \_ \_ 內容](ws-operation-context.md) 控制碼表示）會決定它所包含之屬性的存留期。 因此，應該只在 [服務](service-operation.md) 作業的存留期內或其提供的回呼中使用內容。 同步呼叫的存留期是函數本身的執行。 若為非同步呼叫，存留期會在非同步呼叫完成後結束。 一旦呼叫完成後，服務模型不會保證內容。 依賴作業內容或其任何屬性超過其存留期的行為未定義。


另請參閱以會話為基礎的計算機範例， [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md)。

## <a name="threading-model"></a>執行緒模型

作業內容支援無限制執行緒，不過，這對作業內容本身而言是正確的，而且不會套用至它所包含的任何屬性。

當您透過 [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) 函式註冊服務作業的取消回呼時，請注意，第一次註冊將會成功;不過，將取消回呼設定多次會失敗。

 

 




