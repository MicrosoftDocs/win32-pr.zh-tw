---
description: GetCaptureCommentFromFilename 函式會從 capture 檔案中解壓縮 capture 批註。
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: 'GetCaptureCommentFromFilename 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureCommentFromFilename
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1b92b81fa00834c3a4038a6a6bb9f295246a7c0b217c99779a5d2c569dbbf982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366809"
---
# <a name="getcapturecommentfromfilename-function"></a>GetCaptureCommentFromFilename 函式

**GetCaptureCommentFromFilename** 函式會從 [*capture*](c.md)檔案中解壓縮 capture 批註。

## <a name="syntax"></a>語法


```C++
DWORD  WINAPI GetCaptureCommentFromFilename(
  _In_ LPSTR lpFilename,
  _In_ LPSTR lpComment,
  _In_ DWORD BufferSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpFilename* \[在\]
</dt> <dd>

捕捉檔名稱的指標。

</dd> <dt>

*lpComment* \[在\]
</dt> <dd>

批註的預先配置字串指標。

</dd> <dt>

*BufferSize* \[在\]
</dt> <dd>

字串的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功 (也就是，如果找到並複製了批註，或在 capture 檔) 中沒有批註，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值為錯誤碼。



| 傳回碼                                                                                                 | Description                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 檔案 \_ 讀取 \_ 錯誤**</dt> </dl>     | 無法讀取 capture 批註。<br/>                               |
| <dl> <dt>**NMERR \_ 不正確 \_ 檔 \_ 格式**</dt> </dl> | 批註框架不是有效的檔案格式。<br/>                     |
| <dl> <dt>**\_ \_ \_ 找不到 NMERR 檔案**</dt> </dl>      | 找不到 *lpFilename* 參數所指定的檔案。<br/> |
| <dl> <dt>**NMERR \_ 不正確 \_ 參數**</dt> </dl>    | 其中一個參數指定不正確。<br/>                   |



 

## <a name="remarks"></a>備註

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetCaptureCommentFromFilename** 函數。

若要取得即時捕捉的批註，請呼叫 [GetCaptureComment](getcapturecomment.md) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[GetCaptureComment](getcapturecomment.md)
</dt> </dl>

 

 




