---
title: 'CB_GETTOPINDEX 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ GETTOPINDEX 訊息，以抓取下拉式方塊的清單方塊部分中第一個可見專案的以零為起始的索引。
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- CB_GETTOPINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d5d6834dd954261822c8b1cb1a449d16398284
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934360"
---
# <a name="cb_gettopindex-message"></a>CB \_ GETTOPINDEX 訊息

應用程式會傳送 **CB \_ GETTOPINDEX** 訊息，以抓取下拉式方塊的清單方塊部分中第一個可見專案的以零為起始的索引。 一開始，索引0的專案會在清單方塊的頂端，但是如果清單方塊內容已經過滾動，則其他專案可能會位於頂端。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值是下拉式方塊清單方塊中第一個可見專案的索引。

如果訊息失敗，則傳回值為 CB \_ ERR。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CB \_ SETTOPINDEX**](cb-settopindex.md)
</dt> </dl>

 

 





