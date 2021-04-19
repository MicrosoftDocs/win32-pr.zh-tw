---
title: 'IWMDRMLicenseBackupRestoreStatus GetStatus 方法 (Wmdrmsdk .h) '
description: GetStatus 方法會抓取有關授權備份或還原作業的詳細狀態資訊。
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- GetStatus 方法 windows Media 格式
- GetStatus 方法 windows Media Format，IWMDRMLicenseBackupRestoreStatus 介面
- IWMDRMLicenseBackupRestoreStatus 介面 windows Media Format，GetStatus 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus.GetStatus
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3373e71bcae9dc1054e97e8b758ac72389b9a712
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996267"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a>IWMDRMLicenseBackupRestoreStatus：： GetStatus 方法

**GetStatus** 方法會抓取有關授權備份或還原作業的詳細狀態資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStatus* \[擴展\]
</dt> <dd>

可接收狀態資訊之 [**WM \_ 備份 \_ 還原 \_ 狀態**](wm-backup-restore-status.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicenseBackupRestoreStatus 介面**](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





