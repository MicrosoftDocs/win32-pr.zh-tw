---
title: 'ISoftKbd GetSoftKeyboardTypeMode 方法 (Softkbdc .h) '
description: ISoftKbd GetSoftKeyboardTypeMode 方法會抓取軟鍵盤的類型模式。
ms.assetid: 77294652-b82e-4b69-bb55-5ebebc3c97c7
keywords:
- GetSoftKeyboardTypeMode 方法文字服務架構
- GetSoftKeyboardTypeMode 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，GetSoftKeyboardTypeMode 方法
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6aad6d60c50ee0050cf418018dd6db1c7a33efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383825"
---
# <a name="isoftkbdgetsoftkeyboardtypemode-method"></a>ISoftKbd：： GetSoftKeyboardTypeMode 方法

**ISoftKbd：： GetSoftKeyboardTypeMode** 方法會抓取軟鍵盤的類型模式。

## <a name="syntax"></a>語法


```C++
HRESULT GetSoftKeyboardTypeMode(
  [out] TYPEMODE *lpTypeMode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpTypeMode* \[擴展\]
</dt> <dd>

緩衝區的指標，此方法會在其中捕獲型別模式。 可能的值是針對 [**TYPEMODE**](typemode.md) 列舉而定義的。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 描述                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法成功。<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *LpTypeMode* 參數無效。<br/> |



 

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

[**ISoftKbd::SetSoftKeyboardTypeMode**](isoftkbd-setsoftkeyboardtypemode.md)
</dt> <dt>

[**TYPEMODE**](typemode.md)
</dt> </dl>

 

 





