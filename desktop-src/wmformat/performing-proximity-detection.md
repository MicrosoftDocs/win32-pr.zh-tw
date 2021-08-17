---
title: 執行鄰近性偵測
description: 執行鄰近性偵測
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- Windows媒體格式 SDK，執行鄰近性偵測
- Windows媒體格式 SDK，鄰近性偵測
- Advanced Systems Format (ASF) ，執行鄰近性偵測
- ASF (Advanced 系統格式) ，執行鄰近性偵測
- Advanced Systems Format (ASF) 、鄰近性偵測
- ASF (Advanced 系統格式) 、鄰近偵測
- 數位版權管理 (DRM) ，執行鄰近性偵測
- DRM (數位版權管理) ，執行鄰近性偵測
- 數位版權管理 (DRM) ，鄰近性偵測
- DRM (數位版權管理) ，鄰近性偵測
- 鄰近性偵測
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181b13d56e4c2b1fea0da1ff761f6d915680ff89c42747b9faf4260184ae4205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963977"
---
# <a name="performing-proximity-detection"></a>執行鄰近性偵測

在您可以將加密資料串流至 Windows 媒體 DRM 10 for Network Devices protocol 中的已註冊裝置之前，您必須執行稱為鄰近偵測的進程 (也稱為驗證) 。 此程式牽涉到將訊息傳送至裝置，並接收回應。 接收回應所需的時間是用來判斷裝置是否接近網路上的電腦，以接收安全的資料。 確認裝置實際接近網路上的用戶端電腦有助於防止詐騙和其他未經授權的存取。

當近接偵測順利完成時，裝置就會被視為有效。 您可以藉由呼叫 [**IWMRegisteredDevice：： IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) 方法來檢查裝置是否有效。 裝置必須每隔48小時進行驗證。 在您的程式執行之前經過驗證超過48小時的裝置，必須重新驗證，方法是再次執行鄰近性偵測處理常式。

若要執行鄰近性偵測，您必須建立與裝置的通訊，然後呼叫 [**IWMProximityDetection：： StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) 方法。 偵測程式是由 Windows 媒體格式 SDK 的內部 DRM 元件以非同步方式完成。 您的應用程式必須包含 [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) 介面的執行，以處理鄰近性偵測訊息。

近接偵測程式會傳送兩則訊息：結果訊息和完成訊息。

\_ \_ 當偵測程式完成時，會傳送結果訊息 WMT 鄰近結果。 [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)回呼方法的 *hr* 參數會指出裝置是否夠接近用戶端電腦。 如果結果訊息的 *hr* 參數表示成功，則 *pValue* 參數會包含 **DWORD** ，以指定裝置的測量延遲（以毫秒為單位）。

完成偵測時，會傳送完成訊息（WMT \_ 鄰近性 \_ 已完成）。 只有在收到此訊息之後，您才應該釋放 [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) 介面。

裝置的鄰近性偵測成功時，會自動更新裝置註冊資料庫。 [**IWMRegisteredDevice：： IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid)的後續呼叫會傳回 **TRUE** ，直到超過48小時，而且必須重新驗證裝置。

**注意** 此 SDK 的 x64 版本不支援 DRM。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用 Windows 媒體 DRM 10 進行網路裝置通訊協定**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




