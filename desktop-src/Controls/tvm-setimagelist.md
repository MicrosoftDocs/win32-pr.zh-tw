---
title: 'TVM_SETIMAGELIST 訊息 (Commctrl .h) '
description: 設定樹狀檢視控制項的 [一般] 或 [狀態] 影像清單，然後使用新的影像來重新繪製控制項。 您可以使用 TreeView SetImageList 宏明確地傳送此訊息 \_ 。
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- TVM_SETIMAGELIST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df79089c7a2071c6af702da9ef862178738ede3dccff312c3fbae7dbefe4de56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018676"
---
# <a name="tvm_setimagelist-message"></a>TVM \_ SETIMAGELIST 訊息

設定樹狀檢視控制項的 [一般] 或 [狀態] 影像清單，然後使用新的影像來重新繪製控制項。 您可以使用 [**TreeView \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要設定之影像清單的類型。 這個參數可以是下列其中一個值：



| 值                                                                                                                                                      | 意義                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**TVSIL \_ 正常**</dt> </dl> | 指出一般影像清單，其中包含樹狀檢視控制項專案的已選取、nonselected 和重迭影像。<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**TVSIL \_ 狀態**</dt> </dl>    | 表示狀態影像清單。 您可以使用狀態影像來表示應用程式定義的專案狀態。 狀態影像會顯示在專案的選取專案或 nonselected 影像的左邊。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

影像清單的控制碼。 如果 *lParam* 為 **Null**，則訊息會從樹狀檢視控制項中移除指定的影像清單。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回上一個影像清單的控制碼（如果有的話），否則傳回 **Null** 。

## <a name="remarks"></a>備註

樹狀檢視控制項將不會損毀以此訊息指定的影像清單。 當您的應用程式不再需要時，您的應用程式必須損毀映射清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ GETIMAGELIST**](tvm-getimagelist.md)
</dt> </dl>

 

 





