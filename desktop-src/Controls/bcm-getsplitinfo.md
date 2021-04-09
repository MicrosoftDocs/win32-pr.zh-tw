---
title: 'BCM_GETSPLITINFO 訊息 (Commctrl .h) '
description: 取得分割按鈕控制項的資訊。 明確地傳送此訊息，或使用按鈕 \_ GetSplitInfo 宏。
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- BCM_GETSPLITINFO message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162c5522fcb432e3d512f688ae24aa12d4d0d8e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934452"
---
# <a name="bcm_getsplitinfo-message"></a>BCM \_ GETSPLITINFO 訊息

取得分割按鈕控制項的資訊。 明確地傳送此訊息，或使用 [**按鈕 \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* \[in、out\]
</dt> <dd>

[**按鈕 \_ SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo)結構的指標，用來接收按鈕的資訊。 呼叫端負責配置結構的記憶體。 設定此結構的 **遮罩** 成員，以決定要接收的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

此訊息只能搭配 [**BS \_ SPLITBUTTON**](button-styles.md) 和 [**BS \_ DEFSPLITBUTTON**](button-styles.md) 按鈕樣式使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[按鈕樣式](button-styles.md)
</dt> <dt>

**概念**
</dt> <dt>

[按鈕類型](button-types-and-styles.md)
</dt> </dl>

 

 





