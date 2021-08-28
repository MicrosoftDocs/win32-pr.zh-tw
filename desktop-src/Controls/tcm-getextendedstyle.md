---
title: 'TCM_GETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 抓取目前用於索引標籤控制項的延伸樣式。 您可以使用 TabCtrl GetExtendedStyle 宏明確地傳送此訊息 \_ 。
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- TCM_GETEXTENDEDSTYLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5c4618fe039fcd05a73e409f0e8ddd7042694d526f902d432d2513bbef96e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876568"
---
# <a name="tcm_getextendedstyle-message"></a>TCM \_ GETEXTENDEDSTYLE 訊息

抓取目前用於索引標籤控制項的延伸樣式。 您可以使用 [**TabCtrl \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **DWORD** 值，表示目前用於索引標籤控制項的延伸樣式。 此值為索引標籤控制項 [擴充樣式](tab-control-extended-styles.md)的組合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md)
</dt> </dl>

 

 





