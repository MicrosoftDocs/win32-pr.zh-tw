---
title: 'HDM_GETITEM 訊息 (Commctrl .h) '
description: 取得標題控制項中的專案相關資訊。 您可以明確地傳送此訊息，或使用標頭 \_ GetItem 宏。
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- HDM_GETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETITEM
- HDM_GETITEMA
- HDM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2073602121480930e0f7d9d2e5a904c0dea77ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103776"
---
# <a name="hdm_getitem-message"></a>HDM \_ GETITEM 訊息

取得標題控制項中的專案相關資訊。 您可以明確地傳送此訊息，或使用 [**標頭 \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要取得其資訊之專案的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema)結構的指標。 傳送訊息時， **遮罩** 成員會指出所要求的資訊類型。 當訊息傳回時，其他成員會收到要求的資訊。 如果 **遮罩** 成員指定為零，則訊息會傳回 **TRUE** ，但不會將任何資訊複製到結構中。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

如果在 \_ [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema)結構的 **MASK** 成員中設定 HDI 文字旗標，控制項可能會變更結構的 **pszText** 成員以指向新的文字，而不是以要求的文字填滿緩衝區。 應用程式不應假設文字一定會放在要求的緩衝區中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **HDM \_GETITEMW** (Unicode) 和 **HDM \_ GETITEMA** (ANSI) <br/>                   |



 

 





