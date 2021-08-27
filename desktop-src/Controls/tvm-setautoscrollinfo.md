---
title: 'TVM_SETAUTOSCROLLINFO 訊息 (Commctrl .h) '
description: 設定用來判斷自動滾動特性的資訊。 您可以使用 TreeView SetAutoScrollInfo 宏明確地傳送此訊息 \_ 。
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- TVM_SETAUTOSCROLLINFO 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETAUTOSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8840045900fdbd63930219d199889cde018406779426cd767b49ab41a399efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060158"
---
# <a name="tvm_setautoscrollinfo-message"></a>TVM \_ SETAUTOSCROLLINFO 訊息

設定用來判斷自動滾動特性的資訊。 您可以使用 [**TreeView \_ SetAutoScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

指定每秒的圖元數。 滾動的位移會除以 *wParam* ，以決定自動捲軸的總持續時間。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

指定重繪時間間隔。 在每個 elasped 間隔重繪，直到專案滾動到視野為止。 指定 *wParam* 時，會計算專案的位置，並進行重新繪製。 設定此值以建立平滑滾動。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE**。

## <a name="remarks"></a>備註

Autoscroll 資訊可用來將看不見專案滾動到視野中。 控制項必須有 [**tv \_ EX \_ AUTOHSCROLL**](tree-view-control-window-extended-styles.md) 延伸樣式。 如需擴充樣式的詳細資訊，請參閱 Tree-View 控制延伸樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





