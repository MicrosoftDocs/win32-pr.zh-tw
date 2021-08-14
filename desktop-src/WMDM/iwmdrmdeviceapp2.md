---
title: IWMDRMDeviceApp2 介面
description: IWMDRMDeviceApp2 介面會藉由提供新版本的 QueryDeviceStatus 方法來擴充 IWMDRMDeviceApp。
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- IWMDRMDeviceApp2 介面 windows Media 裝置管理員
- IWMDRMDeviceApp2 interface windows Media 裝置管理員，說明
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17bd0d7aa729103a81fca6732ed178ac5ced583566dd353a28716d4933e602ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584492"
---
# <a name="iwmdrmdeviceapp2-interface"></a>IWMDRMDeviceApp2 介面

**IWMDRMDeviceApp2** 介面會藉由提供新版本的 [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)方法來擴充 [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) 。 **QueryDeviceStatus2** 可讓呼叫端查詢特定的 DRM 需求。

若要取得此介面，請呼叫 **CoCreateInstance** 並傳入 CLSID \_ WMDRMDeviceApp。

> [!Note]  
> 此介面定義于從 WMDRMDeviceApp 建立的標頭檔中。 此標頭 **\# 包含**"wmdm .h"。 您可能需要變更這個檔案名，以符合 WMDM 所建立的標頭。

 

## <a name="members"></a>成員

**IWMDRMDeviceApp2** 介面繼承自 [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)。 **IWMDRMDeviceApp2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMDRMDeviceApp2** 介面具有這些方法。



| 方法                                                            | 描述                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) | 查詢裝置的特定 DRM 狀態或功能。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**處理應用程式中受保護的內容**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**應用程式的介面**](interfaces-for-applications.md)
</dt> <dt>

[**計量內容使用方式**](metering-content-usage.md)
</dt> </dl>

 

 





