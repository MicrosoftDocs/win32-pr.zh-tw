---
title: 'EM_CHARFROMPOS 訊息 (Winuser .h) '
description: 取得最接近編輯控制項工作區中指定點之字元的相關資訊。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- EM_CHARFROMPOS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_CHARFROMPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a133907b29857abdc1663d3283bc4b4164878f3fa0976769e6d42daef2c4cb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915958"
---
# <a name="em_charfrompos-message"></a>EM \_ CHARFROMPOS 訊息

取得最接近編輯控制項工作區中指定點之字元的相關資訊。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

控制項工作區中某個點的座標。 座標是在螢幕單元中，相對於控制項工作區的左上角。

**Rich edit 控制項：** 包含水準和垂直座標之 [**POINTL**](/previous-versions//dd162807(v=vs.85)) 結構的指標。

**編輯控制項：**[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含水準座標。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))包含垂直座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

**Rich edit 控制項：** 傳回值會指定最接近指定點的字元之以零為基底的字元索引。 如果指定的點超過控制項的最後一個字元，則傳回值會指出編輯控制項中的最後一個字元。

**編輯控制項：**[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定最接近指定點的字元之以零為起始的索引。 此索引是相對於控制項的開頭，而不是行的開頭。 如果指定的點超過編輯控制項中的最後一個字元，則傳回值會指出控制項中的最後一個字元。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定包含字元之行的以零為起始的索引。 針對單行編輯控制項，此值為零。 如果指定的點超過行的最後一個可見字元，則索引會指出行分隔符號。

## <a name="remarks"></a>備註

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

如果某個點傳遞至 **EM \_ CHARFROMPOS** 做為 *lParam* ，且該點超出編輯控制項的界限，則 *lResult* 為 (65535，65535) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ POSFROMCHAR**](em-posfromchar.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**POINTL**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

