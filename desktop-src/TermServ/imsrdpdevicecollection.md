---
title: IMsRdpDeviceCollection 介面
description: 代表裝置物件的集合。
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- IMsRdpDeviceCollection 介面遠端桌面服務
- IMsRdpDeviceCollection 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cace1bc684be4e3e8cf20db84ec8923c9b35a8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383882"
---
# <a name="imsrdpdevicecollection-interface"></a>IMsRdpDeviceCollection 介面

代表裝置物件的集合。

## <a name="members"></a>成員

**IMsRdpDeviceCollection** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IMsRdpDeviceCollection** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IMsRdpDeviceCollection** 介面具有這些方法。



| 方法                                                        | 描述                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [**RescanDevices**](imsrdpdevicecollection-rescandevices.md) | 重新整理集合中的物件清單。<br/> |



 

### <a name="properties"></a>屬性

**IMsRdpDeviceCollection** 介面具有這些屬性。



| 屬性                                                                 | 存取類型          | Description                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [**DeviceById**](imsrdpdevicecollection-devicebyid.md)<br/>       | 唯讀<br/> | 使用指定的識別碼抓取裝置。<br/> |
| [**DeviceByIndex**](imsrdpdevicecollection-devicebyindex.md)<br/> | 唯讀<br/> | 在指定的索引處抓取裝置。<br/>        |
| [**DeviceCount**](imsrdpdevicecollection-devicecount.md)<br/>     | 唯讀<br/> | 抓取集合中的物件計數。<br/>   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                            |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsRdpDeviceCollection 定義為 56540617-d281-488c-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

