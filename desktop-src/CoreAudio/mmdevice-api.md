---
description: 關於 MMDevice API
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: 關於 MMDevice API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e2f33c6969e00006c12b0bc6dc1ba37b70c5ff38ea2846633d5eb61da03b19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077542"
---
# <a name="about-mmdevice-api"></a>關於 MMDevice API

Windows 多媒體裝置 (MMDevice) API 可讓音訊用戶端探索[音訊端點裝置](audio-endpoint-devices.md)、判斷其功能，以及為這些裝置建立驅動程式實例。

標頭檔 Mmdeviceapi 會定義 MMDevice API 中的介面。

MMDevice API 包含數個介面。 其中第一個是 [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面。 若要存取 MMDevice API 中的介面，用戶端會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)函式來取得裝置列舉值物件的 **IMMDeviceEnumerator** 介面參考，如下列程式碼片段所示：


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



在上述的程式碼片段中，CLSID \_ MMDeviceEnumerator 和 IID \_ IMMDeviceEnumerator 是以屬性形式附加至 **MMDeviceEnumerator** 類別物件和 [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面的 GUID 值。 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)呼叫會以傳址方式傳遞這些值。 變數 `hr` 的類型為 **HRESULT**，而變數 `pEnumerator` 則是裝置列舉值物件之 **IMMDeviceEnumerator** 介面的指標。 **IMMDeviceEnumerator** 提供列舉音訊端點裝置的方法。 如需 **\_ \_ uuidof** 運算子、 **CoCreateInstance** 函數和 CLSCTX Xxx 常數的詳細資訊 \_  ，請參閱 Windows SDK 檔。

透過 [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面，用戶端可以取得 MMDevice API 中其他介面的參考。 MMDevice API 會執行下列介面。



| 介面                                          | 描述                                     |
|----------------------------------------------------|-------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | 代表音訊裝置。                     |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | 代表音訊裝置的集合。       |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | 提供列舉音訊裝置的方法。 |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | 代表音訊端點裝置。            |



 

此外，MMDevice API 的用戶端必須在音訊端點裝置中執行狀態變更的通知，才能執行下列介面。



| 介面                                              | 描述                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | 當新增或移除音訊端點裝置、裝置的狀態或屬性變更時，或指派給裝置的預設角色變更時，會提供通知。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊端點裝置](audio-endpoint-devices.md)
</dt> <dt>

[**程式設計參考**](programming-reference.md)
</dt> </dl>

 

 
