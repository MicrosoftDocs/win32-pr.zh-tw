---
title: 'VMDriveType 列舉 (VPCCOMInterfaces) '
description: 指定連接至匯流排位置的磁片磁碟機類型。
ms.assetid: 7d3acff2-e1e3-4622-a448-0996ee7436ae
keywords:
- VMDriveType 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMDriveType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5288988ff481bb785c4478bbd0ab8d5bf96e14d06ed016bdc9f9e593a677fc12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394318"
---
# <a name="vmdrivetype-enumeration"></a>VMDriveType 列舉

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

指定連接至匯流排位置的磁片磁碟機類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmDriveType_Null      = 0,
  vmDriveType_HardDisk  = 1,
  vmDriveType_DVD       = 2
} VMDriveType;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmDriveType \_ Null**
</dt> <dd>

沒有連接的磁片磁碟機。

</dd> <dt>

<span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**vmDriveType \_ 硬碟**
</dt> <dd>

磁片磁碟機已連接。

</dd> <dt>

<span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**vmDriveType \_ DVD**
</dt> <dd>

已附加 CD 或 DVD 光碟機。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine::AttachedDriveTypes**](ivmvirtualmachine-attacheddrivetypes.md)
</dt> </dl>

 

