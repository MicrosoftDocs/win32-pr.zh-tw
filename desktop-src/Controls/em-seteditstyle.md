---
title: 'EM_SETEDITSTYLE 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的目前編輯樣式旗標。
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- EM_SETEDITSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14c7b7e1d3990a00fb6931ed39bbd28aa6f8c2ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509171"
---
# <a name="em_seteditstyle-message"></a>EM \_ SETEDITSTYLE 訊息

設定 rich edit 控制項的目前編輯樣式旗標。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定一或多個編輯樣式旗標。 如需可能值的清單，請參閱 [**EM \_ GETEDITSTYLE**](em-geteditstyle.md)。

</dd> <dt>

*lParam* 
</dt> <dd>

由一或多個 *wParam* 值所組成的遮罩。 只會設定或清除此遮罩中指定的值。 這可讓您設定或清除單一旗標，而不需要讀取目前的旗標狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

當 rich edit 控制項嘗試執行編輯樣式變更之後，傳回值即為編輯樣式旗標的狀態。 編輯樣式旗標是一組旗標，表示目前的編輯樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Rich Edit 3。0<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETEDITSTYLE**](em-geteditstyle.md)
</dt> </dl>

 

 





