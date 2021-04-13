---
title: 'SisFreeRestoreStructure 函式 (Sisbkup) '
description: 釋出配置給指定之 SIS 還原結構的記憶體，並執行工作來準備 SIS 篩選器，以正確地設定在還原作業期間建立的連結。
ms.assetid: dbdccb53-b38e-465d-a6d0-ee86923a5879
keywords:
- SisFreeRestoreStructure 函式備份
topic_type:
- apiref
api_name:
- SisFreeRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7293514d798fe65c82863a83549039b05ec8eb3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466649"
---
# <a name="sisfreerestorestructure-function"></a>SisFreeRestoreStructure 函式

**SisFreeRestoreStructure** 函式會釋出配置給指定之 SIS 還原結構的記憶體，並執行工作來準備 SIS 篩選器，以正確地設定在還原作業期間所建立的連結。

## <a name="syntax"></a>語法


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sisRestoreStructure* \[在\]
</dt> <dd>

從 [**SisCreateRestoreStructure**](siscreaterestorestructure.md)傳回的 SIS 還原結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功完成，則此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。 呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得呼叫失敗原因的詳細資訊。

## <a name="remarks"></a>備註

在呼叫此函式完成之前存取 SIS 連結，可能會導致磁片區檢查或部分的連結內容讀取。

請注意，這並不安全地假設它只會解除配置記憶體。 例如，此函式也可以針對 SIS 架構執行額外的系統管理作業。 因此，即使您的還原作業之後會立即結束，也請呼叫此函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Sisbkup。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Sisbkup .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> </dl>

 

