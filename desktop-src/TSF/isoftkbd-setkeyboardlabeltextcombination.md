---
title: 'ISoftKbd SetKeyboardLabelTextCombination 方法 (Softkbdc .h) '
description: ISoftKbd SetKeyboardLabelTextCombination 方法會設定用來描述軟鍵盤的標籤和文字的組合。
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- SetKeyboardLabelTextCombination 方法文字服務架構
- SetKeyboardLabelTextCombination 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，SetKeyboardLabelTextCombination 方法
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelTextCombination
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98dad124455625f0da3ada1a717c692437398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965925"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a>ISoftKbd：： SetKeyboardLabelTextCombination 方法

**ISoftKbd：： SetKeyboardLabelTextCombination** 方法會設定用來描述軟鍵盤的標籤和文字的組合。

## <a name="syntax"></a>語法


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nModifierCombination* \[在\]
</dt> <dd>

用來描述軟鍵盤的標籤和文字的組合。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 描述                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法成功。<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *NModifierCombination* 參數無效。<br/> |



 

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

[**ISoftKbd::SetKeyboardLabelText**](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 





