---
title: 'WM_BACKUP_RESTORE_STATUS 結構 (Wmdrmsdk .h) '
description: WM \_ 備份 \_ 還原 \_ 狀態結構會保存有關暫止授權備份或還原作業的資訊。
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- WM_BACKUP_RESTORE_STATUS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WM_BACKUP_RESTORE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476cd4ddab42ec9f8f44ff51b492bd3913824cf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995416"
---
# <a name="wm_backup_restore_status-structure"></a>WM \_ 備份 \_ 還原 \_ 狀態結構

**WM \_ 備份 \_ 還原 \_ 狀態** 結構會保存有關暫止授權備份或還原作業的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct WM_BACKUP_RESTORE_STATUS {
  MSDRM_STATUS eStatus;
  BSTR         bstrError;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**eStatus**
</dt> <dd>

[**MSDRM \_ 狀態**](msdrm-status.md)列舉的成員，指定狀態。

</dd> <dt>

**bstrError**
</dt> <dd>

包含錯誤的字串。

</dd> </dl>

## <a name="remarks"></a>備註

當您呼叫 [**IWMDRMLicenseBackupRestoreStatus：： GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) 方法時，就會收到此結構。 它包含在呼叫時暫止的備份或還原作業的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





