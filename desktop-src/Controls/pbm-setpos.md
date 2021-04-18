---
title: 'PBM_SETPOS 訊息 (Commctrl .h) '
description: 設定進度列的目前位置，並重新繪製橫條以反映新的位置。
ms.assetid: 9ebeaa19-0f42-4af7-85d8-aae22498fd6f
keywords:
- PBM_SETPOS message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a157f6a220f4932d39d13f08df79afa99d7348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968576"
---
# <a name="pbm_setpos-message"></a>PBM \_ SETPOS 訊息

設定進度列的目前位置，並重新繪製橫條以反映新的位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

成為新位置的帶正負號的整數。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前的位置。

## <a name="remarks"></a>備註

如果 *wParam* 超出控制項的範圍，則位置會設定為最接近的界限。

請勿將此訊息傳送至具有 [**PBS \_ 字幕**](progress-bar-control-styles.md) 樣式的控制項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





