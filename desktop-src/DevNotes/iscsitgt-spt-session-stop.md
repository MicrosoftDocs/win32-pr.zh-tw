---
description: 搭配使用 IOCTL \_ SCSI \_ 微型埠 IOCTL 和 CTLCODE \_ ISCSITGT \_ SPT \_ SESSION \_ END (0x101) 控制程式代碼來停止會話。
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: ISCSITGT_SPT_SESSION_STOP 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCSITGT_SPT_SESSION_STOP
api_type:
- NA
api_location: ''
ms.openlocfilehash: e4501fbe2d1bbf884448d6b6a9476ee4782d3da7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "103853556"
---
# <a name="iscsitgt_spt_session_stop-structure"></a>ISCSITGT \_ SPT \_ 會話 \_ 停止結構

\[以下是可在 Windows Server 2012 R2 中使用的結構。 它在後續版本中可能會變更或無法使用。\]

搭配使用 [**IOCTL \_ SCSI \_ 微型埠**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) ioctl 和 CTLCODE \_ ISCSITGT \_ SPT \_ SESSION \_ END (0x101) 控制程式代碼來停止會話。

## <a name="syntax"></a>語法


```C++
typedef struct _ISCSITGT_SPT_SESSION_STOP {
  SRB_IO_CONTROL Header;
  SESSION_COOKIE ITNexusHandle;
} ISCSITGT_SPT_SESSION_STOP, *PISCSITGT_SPT_SESSION_STOP;
```



## <a name="members"></a>成員

<dl> <dt>

**標頭**
</dt> <dd>

必要標頭。

</dd> <dt>

**ITNexusHandle**
</dt> <dd>

代表會話的不透明控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | 都不支援<br/>                               |
| 伺服器支援結束<br/>    | Windows Server 2012 R2<br/>                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[iSCSI 目標傳遞](/powershell/module/iscsi)
</dt> <dt>

[**SRB \_ IO \_ 控制項**](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 
