---
title: 'UDM_SETBASE 訊息 (Commctrl .h) '
description: 設定上下按鈕控制項的基本基底。 基底值會決定合作者視窗是否以十進位或十六進位數字顯示數位。 十六進位數位一律不帶正負號，而且會簽署十進位數。
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- UDM_SETBASE message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_SETBASE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6bcd7d6154b4ba732e5ffbbec889b326ec8176
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934700"
---
# <a name="udm_setbase-message"></a>UDM \_ SETBASE 訊息

設定上下按鈕控制項的基本基底。 基底值會決定合作者視窗是否以十進位或十六進位數字顯示數位。 十六進位數位一律不帶正負號，而且會簽署十進位數。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

控制項的新基底值。 針對十六進位，此參數可以是十進位或16的10。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是先前的基底值。 如果指定了不正確基底，則傳回值為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





