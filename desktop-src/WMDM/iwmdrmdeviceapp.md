---
title: IWMDRMDeviceApp 介面
description: IWMDRMDeviceApp 介面可讓應用程式計量、同步處理授權，以及更新裝置的 DRM 元件。
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- IWMDRMDeviceApp 介面 windows Media 裝置管理員
- IWMDRMDeviceApp interface windows Media 裝置管理員，說明
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9cf44295c9972d7549eb4a82fda7c415ba81c31d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965253"
---
# <a name="iwmdrmdeviceapp-interface"></a>IWMDRMDeviceApp 介面

\[Windows Media DRM 功能已被取代，不應該使用。 請改用 [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) 。\]

**IWMDRMDeviceApp** 介面可讓應用程式計量、同步處理授權，以及更新裝置的 DRM 元件。 此介面只適用于支援可攜式裝置之 Windows Media DRM 10 的裝置。

若要取得此介面，請呼叫 **CoCreateInstance**，並傳入 CLSID \_ WMDRMDeviceApp。

> [!Note]  
> 此介面定義于從 WMDRMDeviceApp 建立的標頭檔中。 此標頭 **\# 包含** s "wmdm .h"。 您可能需要變更這個檔案名，以符合 WMDM 所建立的標頭。

 

## <a name="members"></a>成員

**IWMDRMDeviceApp** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IWMDRMDeviceApp** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMDRMDeviceApp** 介面具有這些方法。



| 方法                                                                   | 描述                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)           | 初始化或重設裝置安全時鐘<br/>                                                                                     |
| [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md) | 從裝置取得計量資料。<br/>                                                                                           |
| [**ProcessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md)     | 重設裝置上的部分或所有計量計數（從裝置的資料傳送到伺服器並處理）之後。<br/> |
| [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)           | 查詢裝置的目前 DRM 狀態和功能。<br/>                                                                   |
| [**SynchronizeLicenses**](iwmdrmdeviceapp-synchronizelicenses.md)       | 當裝置上的授權接近到期時，更新該裝置上的授權。<br/>                                                                   |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**處理應用程式中受保護的內容**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**應用程式的介面**](interfaces-for-applications.md)
</dt> <dt>

[**計量內容使用方式**](metering-content-usage.md)
</dt> </dl>

 

