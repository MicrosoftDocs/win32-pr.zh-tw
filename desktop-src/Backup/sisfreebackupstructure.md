---
title: 'SisFreeBackupStructure 函式 (Sisbkup) '
description: 釋出指定的 SIS 備份結構。
ms.assetid: 34d5e919-e4bf-4105-ac15-a2ff5adfbdee
keywords:
- SisFreeBackupStructure 函式備份
topic_type:
- apiref
api_name:
- SisFreeBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e506881110ad9fbb60ea12479c64f8ef8024f8e0f9ddee753813795d31f3dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021356"
---
# <a name="sisfreebackupstructure-function"></a>SisFreeBackupStructure 函式

**SisFreeBackupStructure** 函式會釋出指定的 SIS 備份結構。

## <a name="syntax"></a>語法


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sisBackupStructure* \[在\]
</dt> <dd>

從 [**SisCreateBackupStructure**](siscreatebackupstructure.md)傳回之 SIS 備份結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功完成，則此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。 呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得呼叫失敗原因的詳細資訊。

## <a name="remarks"></a>備註

當完成 *sisBackupStructure* 參數值所識別之磁片區的備份作業之後，應該呼叫此函式。

請注意，這並不安全地假設它只會解除配置記憶體。 例如，此函式也可以針對 SIS 架構執行額外的系統管理作業。 因此，即使您的備份作業在之後立即結束，也請呼叫此函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Sisbkup。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Sisbkup .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

