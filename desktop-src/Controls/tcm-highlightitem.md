---
title: 'TCM_HIGHLIGHTITEM 訊息 (Commctrl .h) '
description: 設定索引標籤專案的醒目提示狀態。 您可以使用 TabCtrl HighlightItem 宏明確地傳送此訊息 \_ 。
ms.assetid: b0d0850a-62d9-46a1-8846-81f67a886ea8
keywords:
- TCM_HIGHLIGHTITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_HIGHLIGHTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b355b1a0ad4d228fc8f67051497b0327885f7cafc3860af9c74bac0812b344ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876508"
---
# <a name="tcm_highlightitem-message"></a>TCM \_ HIGHLIGHTITEM 訊息

設定索引標籤專案的醒目提示狀態。 您可以使用 [**TabCtrl \_ HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**INT** 值，指定索引標籤控制項專案的以零為基底的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 **布林** 值，指定要設定的醒目提示狀態。 如果這個值為 **TRUE**，則會反白顯示索引標籤;如果 **為 FALSE**，則索引標籤會設定為其預設狀態。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

在 Comctl32.dll 6.0 版中，當主題為作用中時，此訊息沒有任何可見效果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

