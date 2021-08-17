---
title: 'EM_SETPASSWORDCHAR 訊息 (Winuser .h) '
description: 設定或移除編輯控制項的密碼字元。 設定密碼字元時，會顯示該字元來取代使用者輸入的字元。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- EM_SETPASSWORDCHAR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56cdfbc108ad5bc1b3e2e11b72937a92da473bcbfa01e974056743ed2e6fde1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412313"
---
# <a name="em_setpasswordchar-message"></a>EM \_ SETPASSWORDCHAR 訊息

設定或移除編輯控制項的密碼字元。 設定密碼字元時，會顯示該字元來取代使用者輸入的字元。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要顯示的字元，用來取代使用者輸入的字元。 如果此參數為零，控制項會移除目前的密碼字元，並顯示使用者輸入的字元。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

當編輯控制項收到 **EM \_ SETPASSWORDCHAR** 訊息時，控制項會使用 *wParam* 參數指定的字元來重繪所有可見字元。 如果 *wParam* 為零，控制項會使用使用者輸入的字元來重繪所有可見字元。

如果以 [**ES \_ 密碼**](edit-control-styles.md) 樣式建立編輯控制項，則預設密碼字元會設定為星號 (\*) 。 如果建立不含 **ES \_ 密碼** 樣式的編輯控制項，則不會有密碼字元。 如果 **EM \_ SETPASSWORDCHAR** 訊息是以 *wParam* 參數設定為零，則會移除 **ES \_ 密碼** 樣式。

**編輯控制項：** 多行編輯控制項不支援密碼樣式或訊息。

**Rich Edit：** Microsoft Rich Edit 2.0 和更新版本支援。 單行和多行編輯控制項都支援密碼樣式和訊息。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETPASSWORDCHAR**](em-getpasswordchar.md)
</dt> </dl>

 

 





