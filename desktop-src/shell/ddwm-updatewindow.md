---
description: 指示使用新的 DROPDESCRIPTION 資訊來更新放置映射視窗。
title: DDWM_UPDATEWINDOW 訊息
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3b74f2e1-8121-4b7c-8d7a-b449cda529da
api_name:
- DDWM_UPDATEWINDOW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a17e015d6dff2ae5133f3ce8245c5ead3c3381f8eb5c48e74946fdf9bcb46ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032836"
---
# <a name="ddwm_updatewindow-message"></a>DDWM \_ UPDATEWINDOW 訊息

指示使用新的 [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) 資訊來更新放置映射視窗。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

未使用。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

未使用。

</dd> </dl>

## <a name="remarks"></a>備註

DDWM \_ UPDATEWINDOW 定義為 WM \_ 使用者 + 3。

當 drop 作業的狀態變更時（例如回應輔助按鍵），[**IDropTarget：:D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) 會傳回新的 [**DROPEFFECT**](../com/dropeffect-constants.md) 值 (這個 **DROPEFFECT** 值也可以透過 [**IDropSource：： system.windows.dragdrop.givefeedback>**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)) 來接收。 在回應中，應用程式會使用新的 [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype)值來更新放置目標的 [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription)結構，以指出要套用至拖曳視窗視覺效果的裝飾;例如，指出檔案正在複製而不是移動，或物件無法卸載至該位置。 不過，在物件收到 **DDWM \_ UPDATEWINDOW** 訊息之前，不會更新視覺效果。

[DragWindow](clipboard.md)剪貼簿格式會將「收件者」視窗的 **HWND** ，提供給 **DDWM \_ UPDATEWINDOW** 訊息的寄件者。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 
