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
ms.openlocfilehash: a7c5fe4a9fcfac86403fd7f4c330d437156e57179b3bf692f53bf3777399b9bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610498"
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
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
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

 

 





