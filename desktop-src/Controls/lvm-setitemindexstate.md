---
title: 'LVM_SETITEMINDEXSTATE 訊息 (Commctrl .h) '
description: 設定清單視圖專案的狀態。 明確地傳送此訊息，或使用 ListView \_ SetItemIndexState 宏。
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- LVM_SETITEMINDEXSTATE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETITEMINDEXSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18094986f5a57713e842b51b31c74ccfe4987d1c1fe62380ea8a986762e20c7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062208"
---
# <a name="lvm_setitemindexstate-message"></a>LVM \_ SETITEMINDEXSTATE 訊息

設定清單視圖專案的狀態。 明確地傳送此訊息，或使用 [**ListView \_ SetItemIndexState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

專案之 [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) 結構的指標。 呼叫進程負責配置此結構及設定成員。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的指標。 呼叫進程負責為結構配置記憶體。 將 **狀態** 成員設定為一或多個 (為 [清單視圖專案狀態](list-view-item-states.md) 旗標的位合) 。 設定結構的 **stateMask** 成員，以表示 **狀態** 成員的有效位。 如需詳細資訊，請參閱 **LVITEM** 結構的 **stateMask** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 型別的值。



| 傳回碼                                                                                  | 描述                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**E \_ 失敗**</dt> </dl>       | 無法設定狀態。<br/>                            |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | 清單視圖控制項尚未準備好進行操作。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 作業成功。<br/>                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





