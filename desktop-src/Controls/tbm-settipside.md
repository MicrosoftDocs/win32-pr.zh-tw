---
title: 'TBM_SETTIPSIDE 訊息 (Commctrl .h) '
description: 放置 [提示] 控制項所使用的工具提示控制項。 使用 [TBS \_ 工具提示] 樣式的 [顯示工具提示] 控制項。
ms.assetid: 40a0eeb0-7bb4-4102-98ea-ee664799b934
keywords:
- TBM_SETTIPSIDE message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETTIPSIDE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c3ab1f6c601d9b243977d147f7503ce99788e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384262"
---
# <a name="tbm_settipside-message"></a>TBM \_ SETTIPSIDE 訊息

放置 [提示] 控制項所使用的工具提示控制項。 使用 [ [**TBS \_ 工具提示**](trackbar-control-styles.md) ] 樣式的 [顯示工具提示] 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

值，表示要顯示工具提示控制項的位置。 這個值可以是下列其中一個值：



| 值                                                                                                                                                   | 意義                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBTS_TOP"></span><span id="tbts_top"></span><dl> <dt>**TBTS \_ TOP**</dt> </dl>          | 工具提示控制項將定位在 [並排] 上方。 此旗標用於水準 trackbars。<br/>         |
| <span id="TBTS_LEFT"></span><span id="tbts_left"></span><dl> <dt>**\_左 TBTS**</dt> </dl>       | 工具提示控制項將放置在 [並排] 的左邊。 此旗標用於垂直 trackbars。<br/>  |
| <span id="TBTS_BOTTOM"></span><span id="tbts_bottom"></span><dl> <dt>**TBTS \_ 底部**</dt> </dl> | 工具提示控制項將放置在 [並排] 下方。 此旗標用於水準 trackbars。<br/>         |
| <span id="TBTS_RIGHT"></span><span id="tbts_right"></span><dl> <dt>**TBTS \_ RIGHT**</dt> </dl>    | 工具提示控制項將放置在 [程式提示] 右邊。 此旗標用於垂直 trackbars。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值，這個值表示工具提示控制項先前的位置。 傳回值等於 *wParam* 的其中一個可能值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





