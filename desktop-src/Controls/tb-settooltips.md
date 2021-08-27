---
title: 'TB_SETTOOLTIPS 訊息 (Commctrl .h) '
description: 將工具提示控制項與工具列產生關聯。
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- TB_SETTOOLTIPS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a75827df49eeaf8b6175cd14180ebb26ddbb642588ee77d625c701eee457baaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061228"
---
# <a name="tb_settooltips-message"></a>TB \_ SETTOOLTIPS 訊息

將工具提示控制項與工具列產生關聯。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

工具提示控制項的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

在傳送 **TB \_ SETTOOLTIPS** 訊息之前新增至工具列的任何按鈕，都不會向工具提示控制項註冊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





