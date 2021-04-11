---
title: 'RB_SETPARENT 訊息 (Commctrl .h) '
description: 設定 Rebar 控制項的父視窗。
ms.assetid: bb8036d4-cab8-4887-86c6-66460bdbe64b
keywords:
- RB_SETPARENT message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6fafd054d9438b6aedd268620097847b42f3d60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843919"
---
# <a name="rb_setparent-message"></a>RB \_ SETPARENT 訊息

設定 Rebar 控制項的父視窗。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要設定之父視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回前一個父視窗的控制碼; 如果沒有上一個父系，則傳回 **Null** 。

## <a name="remarks"></a>備註

Rebar 控制項會將通知訊息傳送至您使用此訊息指定的視窗。 此訊息不會實際變更 Rebar 控制項的父代。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





