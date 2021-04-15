---
title: 'HDM_SETITEM 訊息 (Commctrl .h) '
description: 在標題控制項中設定指定專案的屬性。 您可以明確地傳送此訊息，或使用標頭 \_ SetItem 宏。
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- HDM_SETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b03a05b909cf8c7887edd2031f5346c419f1cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466341"
---
# <a name="hdm_setitem-message"></a>HDM \_ SETITEM 訊息

在標題控制項中設定指定專案的屬性。 您可以明確地傳送此訊息，或使用 [**標頭 \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要變更其屬性之專案的目前索引。

</dd> <dt>

*lParam* 
</dt> <dd>

包含專案資訊之 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) 結構的指標。 傳送此訊息時，必須設定結構的 **遮罩** 成員，以指出要設定的屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

在成功時傳回非零值，否則傳回零。

## <a name="remarks"></a>備註

支援此訊息的 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) 結構支援專案順序和影像清單資訊。 藉由使用這些成員，您可以控制顯示專案的順序，並指定要與專案一起顯示的影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **HDM \_SETITEMW** (Unicode) 和 **HDM \_ SETITEMA** (ANSI) <br/>                   |



 

 





