---
title: 'EM_SETTABSTOPS 訊息 (Winuser .h) '
description: EM \_ SETTABSTOPS 訊息會設定多行編輯控制項中的定位停駐點。
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- EM_SETTABSTOPS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bf8285bbc8830f784b6cf2cf6671634bf4339a418c163bc3962150d6cb6674
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048078"
---
# <a name="em_settabstops-message"></a>EM \_ SETTABSTOPS 訊息

**EM \_ SETTABSTOPS** 訊息會設定多行編輯控制項中的定位停駐點。 當文字複製到控制項時，文字中的任何定位字元都會產生空間，直到下一個索引標籤停止為止。

此訊息只會由多行編輯控制項處理。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

陣列中包含的定位停駐點數目。 如果此參數為零，則會忽略 *lParam* 參數，並在每個32對話方塊範本單位上設定預設索引標籤停止。 如果這個參數是1，就會在每個 *n* 個對話方塊範本單位設定 tab 鍵停止，其中 *n* 是 *lParam* 參數所指向的距離。 如果此參數大於1， *lParam* 就會是定位點的陣列指標。

</dd> <dt>

*lParam* 
</dt> <dd>

在對話方塊範本單位中指定索引標籤的不帶正負號的整數陣列指標。 如果 *wParam* 參數為1，這個參數就是不帶正負號整數的指標，其中包含對話方塊範本單位中所有制表位之間的距離。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果設定了所有索引標籤，則傳回值為 **TRUE**。

如果未設定所有索引標籤，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

**EM \_ SETTABSTOPS** 訊息不會自動重新繪製編輯控制項視窗。 如果應用程式正在變更已在編輯控制項中之文字的定位停駐點，它應該呼叫 [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) 函式來重繪編輯控制項視窗。

陣列中指定的值位於對話方塊範本單位中，也就是對話方塊範本中使用的裝置獨立單位。 若要將度量從對話方塊範本單位轉換為螢幕單位 (圖元) ，請使用 [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) 函數。

**Rich Edit：** Microsoft Rich Edit 3.0 和更新版本支援。 Rich edit 控制項可具有最大索引標籤停止指定的最大 tab 鍵數目 \_ \_ 。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**其他資源**
</dt> <dt>

[**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

