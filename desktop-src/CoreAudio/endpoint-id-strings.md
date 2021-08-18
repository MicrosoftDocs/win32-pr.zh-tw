---
description: 端點識別碼字串
ms.assetid: 3c955e2d-daaa-4b77-8ca5-890383bb2d39
title: 端點識別碼字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fdfbf12f3e037a23163bb3e8fef525db89c15904328c9e0fd8a71e5de004b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957307"
---
# <a name="endpoint-id-strings"></a>端點識別碼字串

在 Windows Vista 中，系統會產生端點識別碼字串來識別系統中的[音訊端點裝置](audio-endpoint-devices.md)。 端點識別碼字串是以 null 結尾的寬字元字串。 特定音訊端點裝置的端點識別碼字串可唯一識別系統中所有音訊端點裝置之間的裝置。

如果系統包含兩個或多個相同的音訊介面卡裝置，對應的音訊端點裝置將會有相同的易記名稱，但每個端點裝置都會有唯一的端點識別碼字串。 如需取得端點裝置之易記名稱的詳細資訊，請參閱 [裝置屬性](device-properties.md)。

取得音訊端點裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面實例之後，用戶端可以呼叫 [**IMMDevice：： GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) 方法來取得裝置的端點識別碼字串。 用戶端可以藉由呼叫 [**IMMDeviceEnumerator：： GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) 方法，使用端點識別碼字串來建立音訊端點裝置的實例，或在不同的進程中建立實例。

用戶端可以排列，以在任何音訊端點裝置的狀態變更時接收通知。 若要接收通知，用戶端會執行 [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) 介面，並使用 MMDevice API 來註冊該介面。 當端點裝置的狀態變更時，MMDevice API 會在用戶端的 [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) 介面中呼叫適當的方法。 方法的其中一個輸入參數是端點識別碼字串，可識別其狀態已變更的端點裝置。 如需 **EDataFlow** 的詳細資訊，請參閱 [裝置事件](device-events.md)。

舊版音訊 api （例如 DirectSound 和 Windows 多媒體功能）有自己的介面可用於列舉和識別音訊裝置。 在 Windows Vista 中，這些介面已經過擴充，可提供端點識別碼字串來識別以 api 呈現之裝置抽象化的端點裝置。

在 DirectSound 裝置列舉期間，DirectSound 會為其所列舉的每個裝置提供端點識別碼字串。 如需詳細資訊，請參閱 [舊版音訊應用程式的音訊事件](audio-events-for-legacy-audio-applications.md)。

若要取得舊版波形裝置的端點識別碼字串，請使用 [**waveOutMessage**](/previous-versions//dd743865(v=vs.85)) 或 [**waveInMessage**](/previous-versions//dd743846(v=vs.85)) 函式，將 winspool.drv \_ QUERYFUNCTIONINSTANCEID 訊息傳送到波形設備磁碟機。 如需示範如何使用此訊息的程式碼範例，請參閱[舊版 Windows 多媒體應用程式的裝置角色](device-roles-for-legacy-windows-multimedia-applications.md)。

如需使用核心音訊 Api 功能來增強使用舊版音訊 Api 之應用程式的詳細資訊，請參閱 [與舊版音訊 api 的互通性](interoperability-with-legacy-audio-apis.md)。

用戶端應將端點識別碼字串的內容視為不透明。 也就是說，用戶端不應該嘗試剖析字串的內容，以取得裝置的相關資訊。 原因是字串格式未定義，而且可能會從一個 MMDevice API 系統模組的執行變更為下一個。

端點識別碼字串的存留期會系結至裝置安裝。 如果使用者升級設備磁碟機，或使用者卸載裝置，並再次安裝裝置，則裝置的端點識別碼字串會變更。 不過，在系統重新開機時，端點識別碼字串會維持不變，且如果使用者拔除裝置並將其插回，則 USB 音訊裝置的端點識別碼字串會維持不變。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊端點裝置](audio-endpoint-devices.md)
</dt> </dl>

 

 
