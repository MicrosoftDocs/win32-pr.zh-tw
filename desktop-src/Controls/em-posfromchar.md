---
title: 'EM_POSFROMCHAR 訊息 (Winuser .h) '
description: 抓取編輯控制項中所指定字元的工作區座標。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- EM_POSFROMCHAR message Windows 控制項
topic_type:
- apiref
api_name:
- EM_POSFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d98968873ad006b2e91cf3add2429bf7630fae1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508711"
---
# <a name="em_posfromchar-message"></a>EM \_ POSFROMCHAR 訊息

抓取編輯控制項中所指定字元的工作區座標。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 1.0 和3.0：**[**POINTL**](/previous-versions//dd162807(v=vs.85))結構的指標，此結構會接收字元的工作區座標。 座標是在螢幕單元中，相對於控制項工作區的左上角。

**編輯控制項和 Rich edit 2.0：** 以零為基底的字元索引。

</dd> <dt>

*lParam* 
</dt> <dd>

**Rich Edit 1.0 和3.0：** 以零為基底的字元索引。

**編輯控制項和 Rich edit 2.0：** 未使用此參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

**Rich Edit 1.0 和3.0：** 未使用傳回值。

**編輯控制項和 Rich edit 2.0：** 傳回值包含字元的工作區座標。 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含水準座標，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))包含垂直座標。

## <a name="remarks"></a>備註

如果指定的字元未顯示在編輯控制項的工作區中，則傳回的座標可以是負值。 座標會截斷為整數值。

如果字元是行分隔符號，則傳回的座標表示該行中最後一個可見字元以外的某個點。 如果指定的索引大於控制項中最後一個字元的索引，控制項會傳回-1。

**Rich Edit 3.0 和更新版本：** 為了回溯相容性，Microsoft Rich Edit 3.0 支援 Microsoft Rich Edit 2.0 所使用的語法。 如果 Microsoft Rich Edit 3.0 偵測到 *wParam* 不是有效的 [**POINTL**](/previous-versions//dd162807(v=vs.85)) 指標，則會假設訊息是使用 Microsoft Rich Edit 2.0 語法來傳送。 在此情況下，它會使用傳回值傳回座標。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ CHARFROMPOS**](em-charfrompos.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**POINTL**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

