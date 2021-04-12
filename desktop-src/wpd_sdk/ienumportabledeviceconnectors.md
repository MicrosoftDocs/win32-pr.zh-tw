---
description: 支援 IPortableDeviceConnector 介面的列舉，代表與電腦配對的 MTP/藍牙裝置。
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: 'IEnumPortableDeviceConnectors 介面 (Devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 7c5340502c7653283e2ea1f2d02e35e7d1222f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192815"
---
# <a name="ienumportabledeviceconnectors-interface"></a>IEnumPortableDeviceConnectors 介面

**IEnumPortableDeviceConnectors** 介面支援 [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)介面的列舉，代表與電腦配對的 MTP/藍牙裝置。 請注意，這將會取出所有先前配對的裝置，包括已配對但已中斷連線的裝置。 若要判斷裝置是否仍在連線，請查詢該裝置的 **DEVPKEY \_ MTPBTH \_ IsConnected** 屬性。

## <a name="members"></a>成員

**IEnumPortableDeviceConnectors** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IEnumPortableDeviceConnectors** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IEnumPortableDeviceConnectors** 介面具有這些方法。



| 方法                                               | 描述                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**克隆**](ienumportabledeviceconnectors-clone.md) | 建立目前 **IEnumPortableDeviceConnectors** 介面的複本。<br/>                                                       |
| [**下一步**](ienumportabledeviceconnectors-next.md)   | 抓取列舉順序中的下一個或多個 [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) 物件。<br/> |
| [**重設**](ienumportabledeviceconnectors-reset.md) | 將列舉序列重設為開頭。<br/>                                                                                |
| [**跳過**](ienumportabledeviceconnectors-skip.md)   | 略過列舉序列中指定的裝置數目。<br/>                                                               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                                                                             |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                                                              |
| 標頭<br/>                   | <dl> <dt>Devpkey .h;</dt><dt>Portabledeviceconnectapi .h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi .idl</dt> </dl>                                                                |
| 程式庫<br/>                  | <dl> <dt>PortableDeviceGuids .lib</dt> </dl>                                                                     |



 

