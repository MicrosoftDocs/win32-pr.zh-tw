---
title: 'TCM_GETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 抓取目前用於索引標籤控制項的延伸樣式。 您可以使用 TabCtrl GetExtendedStyle 宏明確地傳送此訊息 \_ 。
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- TCM_GETEXTENDEDSTYLE message Windows 控制項
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
ms.openlocfilehash: 8280b7043591dd4fdd0b453c5baea5fe014bd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934947"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md)
</dt> </dl>

 

 





