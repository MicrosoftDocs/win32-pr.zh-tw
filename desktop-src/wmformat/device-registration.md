---
title: 裝置註冊
description: 裝置註冊
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- Windows Media Format SDK、裝置註冊
- Windows Media Format SDK，裝置的註冊
- Advanced Systems Format (ASF) 、裝置註冊
- ASF (Advanced 系統格式) 、裝置註冊
- Advanced Systems Format (ASF) 、裝置註冊
- ASF (Advanced 系統格式) 、裝置註冊
- 數位版權管理 (DRM) 、裝置註冊
- DRM (數位版權管理) 、裝置註冊
- 數位版權管理 (DRM) 、裝置註冊
- DRM (數位版權管理) 、裝置註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf4954d9b59abfb62f3a86127a387299d45cb4a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023040"
---
# <a name="device-registration"></a>裝置註冊

Windows Media Format SDK 可讓您存取裝置註冊資料庫。 此資料庫會在用戶端電腦上受到保護，並可用於為網路裝置註冊支援 Windows Media DRM 10 的裝置。

將裝置新增至用戶端電腦所連線的網路時，裝置會嘗試連線到網路裝置發送器應用程式的 Windows Media DRM 10。 建立通訊之後，裝置會傳送註冊要求訊息。

當您的應用程式收到註冊要求訊息時，應該執行下列步驟：

1.  藉由呼叫 [**IWMDRMMessageParser：:P arseregistrationreqmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) 方法來剖析訊息。 這個方法會抓取裝置憑證和裝置序號，這兩者都需要識別裝置。
2.  呼叫 [**IWMDeviceRegistration：： GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) 方法，並傳入在步驟1中取出的憑證和裝置序號。 如果找到裝置，則該裝置已註冊，您可以略過下一個步驟。
3.  呼叫 [**IWMDeviceRegistration：： >registerdevice.js**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) 方法，將裝置新增至裝置註冊資料庫。

您可以藉由取出與其相關聯的已註冊裝置物件，來存取註冊資料庫中任何裝置的相關資訊。 有兩種方式可取得已註冊的裝置物件。 如果您有裝置的憑證和序號，您可以呼叫 [**IWMDeviceRegistration：： GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) 方法。 如果您沒有裝置的憑證和序號，您可以藉由呼叫 IWMDeviceRegistration：： GetFirstRegisteredDevice 來列舉資料庫中的所有裝置，然後呼叫 [**：：**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) ，然後再呼叫 [**IWMDeviceRegistration：： GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) ，直到呼叫傳回 S \_ FALSE。

在您的應用程式可以將資料傳送至裝置之前，您必須確定裝置已通過核准、驗證並開啟。

裝置核准應牽涉到與使用者的互動。 當裝置傳送註冊訊息時，您的應用程式可以提示使用者決定裝置是否為應該接收該使用者資料的裝置。 然後，藉由呼叫 [**IWMRegisteredDevice：：核准**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) 方法來更新裝置註冊資料庫，並適當地傳遞 **TRUE** 或 **FALSE** 。

驗證也稱為鄰近偵測。 這是 Windows Media 格式 SDK 的內部 DRM 物件在執行應用程式以安全傳輸媒體時，所用的程式，可判斷裝置是否「接近」。 Nearness 是由取得訊息回應所需的時間來決定。 這項功能的目的是要防止未經授權的使用者存取您的網路，並取得安全的媒體。 如需詳細資訊，請參閱 [執行鄰近性偵測](performing-proximity-detection.md)。

若要開啟裝置，請呼叫 [**IWMRegisteredDevice：： open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open)。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[**使用 Windows Media DRM 10 進行網路裝置通訊協定**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




