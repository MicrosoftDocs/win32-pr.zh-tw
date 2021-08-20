---
title: 'ISoftKbd EnumSoftKeyboard 方法 (Softkbdc .h) '
description: ISoftKbd EnumSoftKeyboard 方法會列舉支援指定語言的可能軟鍵盤。
ms.assetid: c71f99e5-c4c2-4b09-a58f-d3f4348d0c5d
keywords:
- EnumSoftKeyboard 方法文字服務架構
- EnumSoftKeyboard 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，EnumSoftKeyboard 方法
topic_type:
- apiref
api_name:
- ISoftKbd.EnumSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8323d42719b28eb1f45921c70f77089f1a0e6f4e262b29a165e0cbb5d90c5866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952656"
---
# <a name="isoftkbdenumsoftkeyboard-method"></a>ISoftKbd：： EnumSoftKeyboard 方法

**ISoftKbd：： EnumSoftKeyboard** 方法會列舉支援指定語言的可能軟鍵盤。

## <a name="syntax"></a>語法


```C++
HRESULT EnumSoftKeyboard(
  [in]  LANGID langid,
  [out] DWORD  *lpdwKeyboard
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*langid* \[在\]
</dt> <dd>

語言識別項。

</dd> <dt>

*lpdwKeyboard* \[擴展\]
</dt> <dd>

緩衝區的指標，此方法會在其中取得可用軟鍵盤的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 描述                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法成功。<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *Langid* 參數無效。<br/> |



 

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

 

 





