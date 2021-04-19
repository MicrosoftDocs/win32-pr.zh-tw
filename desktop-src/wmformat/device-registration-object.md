---
title: 裝置註冊物件
description: 裝置註冊物件
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- Windows Media Format SDK，裝置註冊物件
- Advanced Systems Format (ASF) 、裝置註冊物件
- ASF (Advanced 系統格式) 、裝置註冊物件
- 物件、裝置註冊物件
- 裝置註冊物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6b72637cf7ba439d0bb38109645742cda4ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106966231"
---
# <a name="device-registration-object"></a>裝置註冊物件

裝置註冊物件會管理裝置註冊資料庫。 此資料庫會儲存連線至用戶端電腦的網路裝置相關資訊，例如機頂尖的影片播放程式。 裝置註冊資料庫的主要目的是要管理使用「網路裝置的 Windows Media DRM 10」通訊協定來接收安全資料流程的裝置。

如果您的應用程式支援網路裝置的 Windows Media DRM 10，您必須使用此物件的介面來註冊網路裝置，以及驗證這些裝置。 您也可以使用裝置註冊資料庫來儲存有關網路裝置的資訊，這些資訊不會將 Windows Media DRM 10 用於網路裝置，但資料庫中的所有資訊都不會套用到這類裝置。

裝置註冊物件是由 [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) 函式所建立，該函式會將指標設定為 **IWMDeviceRegistration** 介面。 您可以藉由呼叫 **QueryInterface** 方法來取得裝置註冊物件的其他方法。

裝置註冊物件支援下列介面。



| 介面                                              | 描述                               |
|--------------------------------------------------------|-------------------------------------------|
| [**IWMDeviceRegistration**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | 管理裝置註冊資料庫。 |
| [**IWMDRMMessageParser**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | 剖析裝置所傳送的訊息。          |
| [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | 管理裝置驗證。                |



 

下列回呼介面必須由應用程式執行，才能使用 **IWMProximityDetection** 介面的方法。



| 介面                                      | 描述                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | 接收在個別執行緒中執行之進程的狀態訊息。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件**](objects.md)
</dt> </dl>

 

 




