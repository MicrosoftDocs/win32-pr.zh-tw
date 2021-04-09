---
title: 'EM_SETEDITSTYLEEX 訊息 (Richedit .h) '
description: 設定目前的擴充編輯樣式旗標。
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- EM_SETEDITSTYLEEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fe7a1ff420048f620d69196360678e9718a510
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934911"
---
# <a name="em_seteditstyleex-message"></a>EM \_ SETEDITSTYLEEX 訊息

設定目前的擴充編輯樣式旗標。


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定一或多個擴充編輯樣式旗標。 如需可能值的清單，請參閱 [**EM \_ GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex)。

</dd> <dt>

*lParam* 
</dt> <dd>

由一或多個 *wParam* 值所組成的遮罩。 只會設定或清除此遮罩中指定的值。 這可讓您設定或清除單一旗標，而不需要讀取目前的旗標狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

當 rich edit 嘗試執行編輯樣式變更之後，傳回值即為擴充編輯樣式旗標的狀態。 編輯樣式旗標是一組旗標，表示目前的編輯樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETEDITSTYLEEX**](em-geteditstyleex.md)
</dt> </dl>

 

