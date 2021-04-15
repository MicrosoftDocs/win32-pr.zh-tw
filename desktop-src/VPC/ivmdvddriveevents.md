---
title: 'IVMDVDDriveEvents 介面 (VPCCOMInterfaces .h) '
description: 定義 IVMDVDDrive 介面的外寄事件介面。
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- IVMDVDDriveEvents 介面 Virtual PC
- IVMDVDDriveEvents 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b301a423f5272288c12a900d0fbd19c0a5d5170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466837"
---
# <a name="ivmdvddriveevents-interface"></a>IVMDVDDriveEvents 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義 [**IVMDVDDrive**](ivmdvddrive.md) 介面的外寄事件介面。

## <a name="members"></a>成員

**IVMDVDDriveEvents** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMDVDDriveEvents** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IVMDVDDriveEvents** 介面具有這些方法。



| 方法                                                   | 描述                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmdvddriveevents-onmediaeject.md)   | 接收媒體已從磁片磁碟機中取出的通知。<br/>  |
| [**OnMediaInsert**](ivmdvddriveevents-onmediainsert.md) | 接收媒體已插入磁片磁碟機的通知。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents 定義為 c2a7d8e9-e76c-4eb8-94f7-71a5122d249b<br/>         |



 

