---
title: 'CB_SETCUEBANNER 訊息 (Winuser .h) '
description: 設定為下拉式方塊編輯控制項顯示的提示橫幅文字。
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- CB_SETCUEBANNER 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb546b7113247f09d8929364984d5e73c3e28b6541d2ca04bd631405040bf6fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089038"
---
# <a name="cb_setcuebanner-message"></a>CB \_ SETCUEBANNER 訊息

設定為下拉式方塊編輯控制項顯示的提示橫幅文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

包含文字之以 null 結束之 Unicode 字串緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回1，否則會傳回錯誤值。

## <a name="remarks"></a>備註

提示橫幅是在沒有選取專案時，顯示在下拉式方塊編輯控制項中的文字。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>CommCtrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[下拉式列示方塊功能](combo-box-features.md)
</dt> </dl>

 

 





