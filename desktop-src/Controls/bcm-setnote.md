---
title: 'BCM_SETNOTE 訊息 (Commctrl .h) '
description: 設定與命令連結按鈕相關聯的備註文字。 您可以明確地傳送此訊息，或使用按鈕 \_ SetNote 宏。
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- BCM_SETNOTE message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_SETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f544a7fb9dd89346cc2aa9725d36122746a8f608
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934364"
---
# <a name="bcm_setnote-message"></a>BCM \_ SETNOTE 訊息

設定與命令連結按鈕相關聯的備註文字。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

包含附注之以 null 終止的 **WCHAR** 字串指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

從 comctl32.dll DLL 6.01 版開始，命令連結按鈕可能具有附注。

[ **BCM \_ SETNOTE** ] 訊息只適用于 [ [**BS \_ COMMANDLINK**](button-styles.md) ] 和 [ [**BS \_ DEFCOMMANDLINK**](button-styles.md) ] 按鈕樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[按鈕樣式](button-styles.md)
</dt> <dt>

**概念**
</dt> <dt>

[按鈕類型](button-types-and-styles.md)
</dt> </dl>

 

 





