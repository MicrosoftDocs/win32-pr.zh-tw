---
title: 'LVM_GETCOLUMN 訊息 (Commctrl .h) '
description: 取得清單視圖控制項之資料行的屬性。 您可以明確地傳送此訊息，或使用 ListView \_ GetColumn 宏來傳送。
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- LVM_GETCOLUMN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65478d1d249740c630499fd4837e31d4eba7b992cf3ef3682c4e7b72d0706cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411734"
---
# <a name="lvm_getcolumn-message"></a>LVM \_ GETCOLUMN 訊息

取得清單視圖控制項之資料行的屬性。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

資料行的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)結構的指標，指定要取出的資訊，並接收資料行的相關資訊。 **遮罩** 成員會指定要取出的資料行屬性。 如果 **遮罩** 成員指定 LVCF \_ 文字值， **pszText** 成員就必須包含接收專案文字的緩衝區位址，而且 **cchTextMax** 成員必須指定緩衝區的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





