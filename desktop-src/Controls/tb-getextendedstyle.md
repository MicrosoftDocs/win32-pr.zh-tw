---
title: 'TB_GETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 抓取工具列控制項的延伸樣式。
ms.assetid: d9e31a8e-5e5a-4d2d-bc3b-65ac40e8592f
keywords:
- TB_GETEXTENDEDSTYLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab059933c2019009ebc746cc59df6affb840f09c40a201a4ee4048dc2498a17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918858"
---
# <a name="tb_getextendedstyle-message"></a>TB \_ GETEXTENDEDSTYLE 訊息

抓取工具列控制項的延伸樣式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **DWORD** ，表示目前在工具列控制項中使用的樣式。 這個值可以是 [擴充樣式](toolbar-extended-styles.md)的組合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md)
</dt> </dl>

 

 





