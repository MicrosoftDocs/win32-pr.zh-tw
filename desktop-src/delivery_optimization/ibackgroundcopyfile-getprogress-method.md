---
title: 'IBackgroundCopyFile GetProgress 方法 (>deliveryoptimization .h) '
description: 捕獲檔案傳輸進度的資訊。
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- GetProgress 方法
- GetProgress 方法，IBackgroundCopyFile 介面
- IBackgroundCopyFile 介面，GetProgress 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0828105822700f9d34cd180c8877634bc3a6013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465080"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a>IBackgroundCopyFile：： GetProgress 方法

捕獲檔案傳輸進度的資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pProgress* \[擴展\]
</dt> <dd>

結構，其成員表示檔案傳輸的進度。 如需可用進度資訊類型的詳細資訊，請參閱 [**BG_FILE_PROGRESS**](bg-file-progress.md) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile 定義為01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyJob：： GetProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





