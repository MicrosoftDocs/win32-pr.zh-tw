---
title: 'CB_SETTOPINDEX 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETTOPINDEX 訊息，確保下拉式方塊的清單方塊中會顯示特定的專案。
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- CB_SETTOPINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f402cbd16cd61a829a2221600bd3c548829f348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685562"
---
# <a name="cb_settopindex-message"></a>CB \_ SETTOPINDEX 訊息

應用程式會傳送 **CB \_ SETTOPINDEX** 訊息，確保下拉式方塊的清單方塊中會顯示特定的專案。 系統會將清單方塊內容滾動，讓指定的專案出現在清單方塊的頂端，或達到最大捲軸範圍。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定清單專案的以零為基底的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值為零。

如果訊息失敗，則傳回值為 CB \_ ERR。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CB \_ GETTOPINDEX**](cb-gettopindex.md)
</dt> </dl>

 

 





