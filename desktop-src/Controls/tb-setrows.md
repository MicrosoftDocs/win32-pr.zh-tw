---
title: 'TB_SETROWS 訊息 (Commctrl .h) '
description: 設定工具列中的按鈕列數。
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- TB_SETROWS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2c0e95d6f0f19c2b1c9b76cf22a37da0086987b22fe144603cdb2afa8a1ad83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293638"
---
# <a name="tb_setrows-message"></a>TB \_ SETROWS 訊息

設定工具列中的按鈕列數。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定所要求的資料列數目。 最小的資料列數目是1，而最大的資料列數目等於工具列中的按鈕數目。

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是一個 **布林** 值，指出當系統無法建立 *wParam* 所指定的資料列數目時，是否要建立比所要求更多的資料列。 若 **為 TRUE**，則系統會建立更多資料列。 如果 **為 FALSE**，則系統會建立較少的資料列。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會在設定資料列之後接收工具列的周框。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

因為在設定資料列數目時，系統不會分解按鈕群組，所以產生的資料列數目可能會與要求的數目不同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

