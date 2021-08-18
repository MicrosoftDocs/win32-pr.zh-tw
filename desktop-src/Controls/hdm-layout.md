---
title: 'HDM_LAYOUT 訊息 (Commctrl .h) '
description: 抓取用來在父視窗的目標矩形內設定標題控制項大小和位置的資訊。 您可以明確地傳送此訊息，或使用標頭 \_ 版面配置宏。
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- HDM_LAYOUT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- HDM_LAYOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff4194ad5aa1847aa977bac1269a7ab88d36a571824387e07264713726135f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435928"
---
# <a name="hdm_layout-message"></a>HDM \_ 版面配置訊息

抓取用來在父視窗的目標矩形內設定標題控制項大小和位置的資訊。 您可以明確地傳送此訊息，或使用 [**標頭 \_ 版面**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) 配置宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout)結構的指標。 **Prc** 成員會指定矩形的座標，而 **pwpos** 成員會收到矩形內標題控制項的大小和位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

*LParam* 結構的 **pwpos** 成員會收到適當的大小和位置值，以便將控制項放在指定矩形的上方。 高度值是控制項的水準框線高度，以及目前在控制項裝置內容中所選取之字型的平均高度。

若要使用 **HDM \_ 版面** 配置來設定標題控制項的初始大小和位置，請設定控制項的初始可見度狀態，使其隱藏。 傳送 HDM 配置以抓取大小和位置值之後，請使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)函式來設定新的大小、位置和可見度狀態。 **\_**

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

