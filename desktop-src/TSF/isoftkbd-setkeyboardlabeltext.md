---
title: 'ISoftKbd SetKeyboardLabelText 方法 (Softkbdc .h) '
description: ISoftKbd SetKeyboardLabelText 方法會從軟鍵盤的版面配置設定標籤文字。
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- SetKeyboardLabelText 方法文字服務架構
- SetKeyboardLabelText 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，SetKeyboardLabelText 方法
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelText
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15e81e2ff29affaa6bf6e87f87410d9c9d3ef7e913998a1bffa1ab6b0dff3fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877413"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a>ISoftKbd：： SetKeyboardLabelText 方法

**ISoftKbd：： SetKeyboardLabelText** 方法會從軟鍵盤的配置設定標籤文字。

## <a name="syntax"></a>語法


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hKl* \[在\]
</dt> <dd>

用來取得已安裝之軟鍵盤配置的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 描述                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法成功。<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *HKl* 參數無效。<br/> |



 

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
</dt> <dt>

[**ISoftKbd::SetKeyboardLabelTextCombination**](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





