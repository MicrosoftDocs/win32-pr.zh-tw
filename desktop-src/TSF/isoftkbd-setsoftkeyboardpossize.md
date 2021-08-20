---
title: 'ISoftKbd SetSoftKeyboardPosSize 方法 (Softkbdc .h) '
description: ISoftKbd SetSoftKeyboardPosSize 方法會設定軟鍵盤的開始位置和大小。
ms.assetid: bf827b07-0e8b-4d5a-8178-45d75af83551
keywords:
- SetSoftKeyboardPosSize 方法文字服務架構
- SetSoftKeyboardPosSize 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，SetSoftKeyboardPosSize 方法
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b624bea0496b7d7ea8ede3fce2f74c7704b17cd9a66e7f1d9b7ce5bdbf9d98e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952565"
---
# <a name="isoftkbdsetsoftkeyboardpossize-method"></a>ISoftKbd：： SetSoftKeyboardPosSize 方法

**ISoftKbd：： SetSoftKeyboardPosSize** 方法會設定軟鍵盤的開始位置和大小。

## <a name="syntax"></a>語法


```C++
HRESULT SetSoftKeyboardPosSize(
  [in] POINT StartPoint,
  [in] WORD  width,
  [in] WORD  height
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartPoint* \[在\]
</dt> <dd>

[點](/previous-versions//dd162805(v=vs.85))結構，指出軟鍵盤左上位置的座標。

</dd> <dt>

*寬度* \[在\]
</dt> <dd>

軟鍵盤的寬度。

</dd> <dt>

*高度* \[在\]
</dt> <dd>

軟鍵盤的高度。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 描述                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法成功。<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 其中一個參數無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Softkbdc。h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> </dl>

 

