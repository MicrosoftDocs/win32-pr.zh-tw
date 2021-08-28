---
title: IMsRdpDeviceV2 介面
description: 包含裝置物件的相關資訊。 這是 IMsRdpDevice 介面的增強功能。
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- IMsRdpDeviceV2 介面遠端桌面服務
- IMsRdpDeviceV2 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca125024592851b260fb8e4c1f43c7621d4897fec0fc19dfc80d18278e09cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000748"
---
# <a name="imsrdpdevicev2-interface"></a>IMsRdpDeviceV2 介面

包含裝置物件的相關資訊。 這是 [**IMsRdpDevice**](imsrdpdevice.md) 介面的增強功能。

## <a name="members"></a>成員

**IMsRdpDeviceV2** 介面繼承自 [**IMsRdpDevice**](imsrdpdevice.md)。 **IMsRdpDeviceV2** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpDeviceV2** 介面具有這些屬性。



| 屬性                                                                 | 存取類型          | 描述                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**CmClassGuid**](imsrdpdevicev2-cmclassguid.md)<br/>             | 唯讀<br/> | 包含裝置的 configuration manager 安裝類別 GUID。<br/>                     |
| [**CmDeviceInstance**](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | 唯讀<br/> | 包含裝置的 configuration manager 裝置實例。<br/>                       |
| [**DeviceText**](imsrdpdevicev2-devicetext.md)<br/>               | 唯讀<br/> | 包含裝置文字。<br/>                                                               |
| [**DriveLetterBitmap**](imsrdpdevicev2-driveletterbitmap.md)<br/> | 唯讀<br/> | 包含代表裝置內所含之磁碟機號對應的位位。<br/> |
| [**IsCompositeDevice**](imsrdpdevicev2-iscompositedevice.md)<br/> | 唯讀<br/> | 指定裝置是否為複合裝置。<br/>                                          |
| [**IsOptionalDevice**](imsrdpdevicev2-isoptionaldevice.md)<br/>   | 唯讀<br/> | 指定裝置是否為 USB 重新導向的選用裝置。<br/>                                |
| [**IsUSBDevice**](imsrdpdevicev2-isusbdevice.md)<br/>             | 唯讀<br/> | 指定裝置是否用於 USB 重新導向。<br/>                                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 SP1<br/>                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 包含 SP1<br/>                                             |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 定義為5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



 

 





