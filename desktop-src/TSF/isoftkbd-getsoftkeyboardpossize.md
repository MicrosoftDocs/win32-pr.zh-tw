---
title: 'ISoftKbd GetSoftKeyboardPosSize 方法 (Softkbdc .h) '
description: ISoftKbd GetSoftKeyboardPosSize 方法會抓取軟鍵盤的開始位置和大小。
ms.assetid: d4482e34-1723-4fe2-a488-e7c18eb3f68e
keywords:
- GetSoftKeyboardPosSize 方法文字服務架構
- GetSoftKeyboardPosSize 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，GetSoftKeyboardPosSize 方法
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af445efd3e1b510280d20667862f2d95404597f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317340"
---
# <a name="isoftkbdgetsoftkeyboardpossize-method"></a>ISoftKbd：： GetSoftKeyboardPosSize 方法

**ISoftKbd：： GetSoftKeyboardPosSize** 方法會抓取軟鍵盤的開始位置和大小。

## <a name="syntax"></a>語法


```C++
HRESULT GetSoftKeyboardPosSize(
  [out] POINT *lpStartPoint,
  [out] WORD  *lpwidth,
  [out] WORD  *lpheight
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpStartPoint* \[擴展\]
</dt> <dd>

緩衝區的指標，此方法會在此位置中抓取 [點](/previous-versions//dd162805(v=vs.85)) 結構，指出軟鍵盤左上角的座標。

</dd> <dt>

*lpwidth* \[擴展\]
</dt> <dd>

緩衝區的指標，此方法會在其中抓取軟鍵盤的寬度。

</dd> <dt>

*lpheight* \[擴展\]
</dt> <dd>

緩衝區的指標，此方法會在其中抓取軟鍵盤的高度。

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
| Idl<br/>                      | <dl> <dt>Softkbd .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::SetSoftKeyboardPosSize**](isoftkbd-setsoftkeyboardpossize.md)
</dt> </dl>

 

