---
title: 'ISoftKbd SelectSoftKeyboard 方法 (Softkbdc .h) '
description: ISoftKbd SelectSoftKeyboard 方法會選取指定的軟鍵盤。
ms.assetid: 7e85d346-3741-457d-aadd-11d3a6710e85
keywords:
- SelectSoftKeyboard 方法文字服務架構
- SelectSoftKeyboard 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，SelectSoftKeyboard 方法
topic_type:
- apiref
api_name:
- ISoftKbd.SelectSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda9399297e9776e7fbd7cecb364fd7f6cd4604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509067"
---
# <a name="isoftkbdselectsoftkeyboard-method"></a>ISoftKbd：： SelectSoftKeyboard 方法

**ISoftKbd：： SelectSoftKeyboard** 方法會選取指定的軟鍵盤。

## <a name="syntax"></a>語法


```C++
HRESULT SelectSoftKeyboard(
  [in] DWORD dwKeyboardId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwKeyboardId* \[在\]
</dt> <dd>

要選取之軟鍵盤的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 描述                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法成功。<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *DwKeyboardId* 參數無效。<br/> |



 

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
</dt> </dl>

 

 





