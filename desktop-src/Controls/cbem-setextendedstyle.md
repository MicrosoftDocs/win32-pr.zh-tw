---
title: 'CBEM_SETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 設定 ComboBoxEx 控制項中的延伸樣式。
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- CBEM_SETEXTENDEDSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a60518d2f6130c2c89e379125308fc2e647c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965116"
---
# <a name="cbem_setextendedstyle-message"></a>CBEM \_ SETEXTENDEDSTYLE 訊息

設定 ComboBoxEx 控制項中的延伸樣式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**DWORD** 值，指出要對 *lParam* 中的哪些樣式造成影響。 只有 *wParam* 中的擴充樣式會變更。 如果此參數為零，則 *lParam* 中的所有樣式都會受到影響。

</dd> <dt>

*lParam* 
</dt> <dd>

**DWORD** 值，包含要為控制項設定的 [ComboBoxEx 控制項延伸樣式](comboboxex-control-extended-styles.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **DWORD** 值，包含先前用於控制項的延伸樣式。

## <a name="remarks"></a>備註

*wParam* 可讓您修改一或多個擴充樣式，而不需要先取出現有的樣式。 例如，如果您傳遞 [**CBES 的 \_ \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) for *wParam* 和0（ *lParam*），將會清除 **CBES \_ EX \_ NOEDITIMAGE** 樣式，但所有其他樣式都會保持不變。

如果您嘗試為以 [**CBS \_ 簡單**](combo-box-styles.md) 樣式建立的 ComboBoxEx 控制項設定擴充樣式，則可能無法正確地重新繪製。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





