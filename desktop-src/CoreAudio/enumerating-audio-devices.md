---
description: 列舉音訊裝置
ms.assetid: 20110ffc-5eff-4279-abea-53115803b6ee
title: 列舉音訊裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707b9a88181c83344757c711af1c0199c19ebc16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025943"
---
# <a name="enumerating-audio-devices"></a>列舉音訊裝置

用戶端音訊應用程式的第一個工作是尋找要使用的適當音訊裝置。 [MMDEVICE API](mmdevice-api.md)可讓用戶端探索系統中的[音訊端點裝置](audio-endpoint-devices.md)，並判斷哪些裝置適合應用程式使用。 此 API 可讓用戶端取出可用端點裝置的集合，並取得每個裝置的功能。 標頭檔 Mmdeviceapi 會定義 MMDevice API 中的介面。

音訊介面卡可能包含數個裝置，例如 wave 轉譯裝置和 wave 捕獲裝置。 這些是介面卡裝置，而不是端點裝置。 如先前所述，隨插即用 manager 會註冊介面卡裝置，相較于端點管理員所註冊的端點裝置。 每個介面卡裝置一般都支援一或多個端點裝置。 轉譯端點裝置 (例如，耳機) 可以接收來自用戶端應用程式的音訊資料串流，而捕捉端點裝置 (例如，麥克風) 可將音訊串流傳送至用戶端應用程式。

在列舉系統中的端點裝置之前，用戶端必須先呼叫 Windows [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函式來建立裝置枚舉器。 裝置列舉值是具有 [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面的物件。 如需 **CoCreateInstance** 的詳細資訊，請參閱 Windows SDK 檔。

用戶端會呼叫 [**IMMDeviceEnumerator：： EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) 方法，以建立端點物件的集合。 每個端點物件都代表系統中的音訊端點裝置。 在此呼叫中，用戶端會指定集合是否應包含系統中的所有轉譯裝置、所有的捕獲裝置，或兩者。

裝置集合是具有 [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) 介面的物件。 裝置集合中的每個專案都是一個端點物件，至少有下列兩個介面：

-   [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)介面。 用戶端藉由呼叫 [**IMMDeviceCollection：： Item**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item)方法，取得裝置集合中端點物件之 **IMMDevice** 介面的參考。
-   [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)介面。 用戶端藉由呼叫 [**IMMDevice：： QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法，取得端點物件之 **IMMEndpoint** 介面的參考。

在取得端點裝置的集合之後，用戶端可以查詢集合中個別裝置的屬性，以判斷其是否適合使用。 如需示範如何列舉端點裝置並查詢其屬性的程式碼範例，請參閱 [裝置屬性](device-properties.md)。

選取適當的裝置之後，用戶端可以呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 方法，以啟用 [WASAPI](wasapi.md)、 [DeviceTopology API](devicetopology-api.md)和 [EndpointVolume API](endpointvolume-api.md)中的裝置特定介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊端點裝置](audio-endpoint-devices.md)
</dt> </dl>

 

 
