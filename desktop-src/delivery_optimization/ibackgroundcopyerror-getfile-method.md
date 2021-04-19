---
title: 'IBackgroundCopyError GetFile 方法 (>deliveryoptimization .h) '
description: 捕獲與錯誤相關聯之檔案物件的介面指標。
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- GetFile 方法
- GetFile 方法，IBackgroundCopyError 介面
- IBackgroundCopyError 介面，GetFile 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b84396797378c77a6f774b4c63a3966b0d601b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969158"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a>IBackgroundCopyError：： GetFile 方法

捕獲與錯誤相關聯之檔案物件的介面指標。

## <a name="syntax"></a>語法


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppFile* \[擴展\]
</dt> <dd>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)介面指標，其方法可用來判斷與錯誤相關聯的本機和遠端檔案名。 如果錯誤未與本機或遠端檔案相關聯， *ppFile* 參數會設為 **Null** 。 完成時，發行 *ppFile*。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值。



| 傳回碼                                                                                                | Description                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>                   | 已成功取出檔案物件的介面指標。<br/>                                     |
| <dl> <dt>**DO_E_FILE_NOT_AVAILABLE**</dt> </dl> | 錯誤未與本機或遠端檔案相關聯。 *PpFile* 參數設定為 **Null**。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError 定義為19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError::GetError**](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





