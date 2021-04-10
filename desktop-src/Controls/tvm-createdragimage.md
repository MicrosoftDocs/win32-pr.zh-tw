---
title: 'TVM_CREATEDRAGIMAGE 訊息 (Commctrl .h) '
description: 在樹狀檢視控制項中，為指定的專案建立拖曳點陣圖。
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- TVM_CREATEDRAGIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189b37affc6a4382541faea13199cacfcb9b7df5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103902"
---
# <a name="tvm_createdragimage-message"></a>TVM \_ CREATEDRAGIMAGE 訊息

在樹狀檢視控制項中，為指定的專案建立拖曳點陣圖。 此訊息也會建立點陣圖的影像清單，並將點陣圖加入影像清單中。 應用程式可以在使用影像清單函式拖曳專案時顯示影像。 您可以使用 [**TreeView \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

接收新拖曳點陣圖之專案的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回已加入拖曳點陣圖之影像清單的控制碼，否則為 **Null** 。

## <a name="remarks"></a>備註

如果您在沒有相關聯影像清單的情況下建立樹狀檢視控制項，則無法使用 **TVM \_ CREATEDRAGIMAGE** 訊息來建立要在拖曳作業期間顯示的影像。 您必須執行您自己的方法來建立拖曳游標。

當不再需要時，您的應用程式會負責終結影像清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





