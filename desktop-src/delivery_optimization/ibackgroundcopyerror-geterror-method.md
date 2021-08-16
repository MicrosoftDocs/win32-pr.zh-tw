---
title: 'IBackgroundCopyError GetError 方法 (>deliveryoptimization .h) '
description: 抓取錯誤碼，並找出發生錯誤的內容。
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- GetError 方法
- GetError 方法，IBackgroundCopyError 介面
- IBackgroundCopyError 介面，GetError 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d147bc877f9694617ec94651f53f4cf438c00de8d752710c3659f24ba4ffe21c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810323"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a>IBackgroundCopyError：： GetError 方法

抓取錯誤碼，並找出發生錯誤的內容。

## <a name="syntax"></a>語法


```C++
HRESULT GetError(
  [out] BG_ERROR_CONTEXT *pContext,
  [out] HRESULT          *pErrorCode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCoNtext* \[擴展\]
</dt> <dd>

發生錯誤的內容。 如需內容值的清單，請參閱 [**BG_ERROR_CONTEXT**](bg-error-context.md) 列舉。

</dd> <dt>

*pErrorCode* \[擴展\]
</dt> <dd>

發生的錯誤錯誤碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM HRESULT 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError 定義為19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError：： GetFile**](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





