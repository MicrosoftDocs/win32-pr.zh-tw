---
title: 'IVMFloppyDriveEvents 介面 (VPCCOMInterfaces .h) '
description: 定義 IVMFloppyDrive 介面的外寄事件介面。 用戶端會執行這些方法來接收從 IVMFloppyDrive 傳送的事件。
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- IVMFloppyDriveEvents 介面 Virtual PC
- IVMFloppyDriveEvents 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53cd275c45e23de1bb437b4c233ff64118952afae76e7c6b9bc9366facf4fe8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653508"
---
# <a name="ivmfloppydriveevents-interface"></a>IVMFloppyDriveEvents 介面

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義 [**IVMFloppyDrive**](ivmfloppydrive.md) 介面的外寄事件介面。 用戶端會執行這些方法來接收從 **IVMFloppyDrive** 傳送的事件。

## <a name="members"></a>成員

**IVMFloppyDriveEvents** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMFloppyDriveEvents** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IVMFloppyDriveEvents** 介面具有這些方法。



| 方法                                                      | 描述                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmfloppydriveevents-onmediaeject.md)   | 接收媒體已從磁片磁碟機中取出的通知。<br/>  |
| [**OnMediaInsert**](ivmfloppydriveevents-onmediainsert.md) | 接收媒體已插入磁片磁碟機的通知。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents 定義為 a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



 

