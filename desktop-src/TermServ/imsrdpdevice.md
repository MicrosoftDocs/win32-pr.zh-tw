---
title: IMsRdpDevice 介面
description: 包含裝置物件的相關資訊。
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- IMsRdpDevice 介面遠端桌面服務
- IMsRdpDevice 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d545bebde1ed2df8a4c67cdf8d32d0a91499ed42076b2c1b31539d96069d3688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033088"
---
# <a name="imsrdpdevice-interface"></a>IMsRdpDevice 介面

包含裝置物件的相關資訊。

## <a name="members"></a>成員

**IMsRdpDevice** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IMsRdpDevice** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpDevice** 介面具有這些屬性。



| 屬性                                                               | 存取類型           | 描述                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [**DeviceDescription**](imsrdpdevice-devicedescription.md)<br/> | 唯讀<br/>  | 抓取顯示名稱無法使用時，要向使用者顯示的裝置描述。<br/> |
| [**DeviceInstanceId**](imsrdpdevice-deviceinstanceid.md)<br/>   | 唯讀<br/>  | 抓取裝置的裝置實例識別碼。<br/>                                            |
| [**FriendlyName**](imsrdpdevice-friendlyname.md)<br/>           | 唯讀<br/>  | 抓取裝置的顯示名稱。<br/>                                                         |
| [**RedirectionState**](imsrdpdevice-redirectionstate.md)<br/>   | 讀取/寫入<br/> | 指出裝置的重新導向狀態。<br/>                                                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDevice 定義為60c3b9c8-9e92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

