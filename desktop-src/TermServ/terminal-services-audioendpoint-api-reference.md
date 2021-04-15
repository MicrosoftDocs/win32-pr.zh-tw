---
title: 遠端桌面服務 AudioEndpoint API 參考
description: 支援用於音訊端點註冊和資料傳輸的介面。
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- 遠端桌面服務遠端桌面服務 AudioEndpoint API 參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1958b21643083a14110ddad77f68024cc464dd36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372440"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a>遠端桌面服務 AudioEndpoint API 參考

*音訊端點* 代表音訊裝置、音訊 API 或任何其他音訊來源或接收器，可用來將資料傳送到音訊引擎或從中取用資料。 音訊端點必須透過 *連線連接到音訊引擎，而且* 每個連接只能有一個連接到的端點。 註冊端點之後，音訊引擎會將端點附加至連接。

每個端點物件都必須執行下列介面：

-   [**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) 可讓音訊引擎取得端點的相關資訊。
-   [**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) 可在執行處理行程之前取得資料緩衝區的相關資訊，並在傳遞完成時通知端點。
-   [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)或 [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)介面，取決於端點物件是否正在捕捉或轉譯音訊。
-   [**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

音訊引擎會使用這些介面來取得附加至引擎之端點的相關資訊。 端點執行必須提供機制，以便將資料傳遞至或取用來自引擎的資料（如這些介面所指定）。

遠端桌面服務 AudioEndpoint API 支援列舉類型、介面和結構。

## <a name="in-this-section"></a>本節內容

-   [遠端桌面服務 AudioEndpoint 列舉類型](terminal-services-audioendpoint-enumeration-types.md)
-   [遠端桌面服務 AudioEndpoint 函式](remote-desktop-services-audioendpoint-functions.md)
-   [遠端桌面服務 AudioEndpoint 介面](terminal-services-audioendpoint-interfaces.md)
-   [遠端桌面服務 AudioEndpoint 結構](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a>備註

遠端桌面服務 AudioEndpoint API 適用于遠端桌面案例;它不適用於用戶端應用程式。

 

 




