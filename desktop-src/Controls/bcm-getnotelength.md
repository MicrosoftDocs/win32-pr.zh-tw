---
title: 'BCM_GETNOTELENGTH 訊息 (Commctrl .h) '
description: 取得可在 [命令連結] 按鈕的 [描述] 中顯示的附注文字長度。 明確地傳送此訊息，或使用按鈕 \_ GetNoteLength 宏。
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- BCM_GETNOTELENGTH message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_GETNOTELENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b33c5245778481033bd97326c3d66a40bf03210
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024999"
---
# <a name="bcm_getnotelength-message"></a>BCM \_ GETNOTELENGTH 訊息

取得可在 [命令連結] 按鈕的 [描述] 中顯示的附注文字長度。 明確地傳送此訊息，或使用 [**按鈕 \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **WCHARs** 中的附注文字長度，不包括任何結束的 **Null**，或如果沒有附注文字，則為零。

## <a name="remarks"></a>備註

從 comctl32.dll DLL 6.01 版開始，命令連結按鈕可能具有附注。 如需 DLL 版本的詳細資訊，請參閱 [通用控制項版本](common-control-versions.md)。

[ **BCM \_ GETNOTELENGTH** ] 訊息只適用于 [ [**BS \_ COMMANDLINK**](button-styles.md) ] 和 [ [**BS \_ DEFCOMMANDLINK**](button-styles.md) ] 按鈕樣式。

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

 

 





