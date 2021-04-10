---
title: 'VMFloppyDriveAttachmentType 列舉 (VPCCOMInterfaces) '
description: 指定連接到軟碟磁碟機的內容。
ms.assetid: aba1be92-bd07-4edb-ad62-f8d76dbd19b9
keywords:
- VMFloppyDriveAttachmentType 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMFloppyDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4a291778b2fea8039bf41fc04799a03421342f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934566"
---
# <a name="vmfloppydriveattachmenttype-enumeration"></a>VMFloppyDriveAttachmentType 列舉

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

指定連接到軟碟磁碟機的內容。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmFloppyDrive_None       = 0,
  vmFloppyDrive_Image      = 1,
  vmFloppyDrive_HostDrive  = 2
} VMFloppyDriveAttachmentType;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmFloppyDrive \_ 無**
</dt> <dd>

沒有附加任何專案。

</dd> <dt>

<span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**vmFloppyDrive \_ 影像**
</dt> <dd>

已附加磁片磁碟機。

</dd> <dt>

<span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**vmFloppyDrive \_ HostDrive**
</dt> <dd>

有連接的主機軟碟磁碟機。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMFloppyDrive：：附件**](ivmfloppydrive-attachment.md)
</dt> </dl>

 

