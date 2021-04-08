---
title: 'TVM_GETIMAGELIST 訊息 (Commctrl .h) '
description: 抓取與樹狀檢視控制項相關聯之一般或狀態影像清單的控制碼。 您可以使用 TreeView GetImageList 宏明確地傳送此訊息 \_ 。
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- TVM_GETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e4e2503d9c6d57743059ee1da3049a36ed17f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686380"
---
# <a name="tvm_getimagelist-message"></a>TVM \_ GETIMAGELIST 訊息

抓取與樹狀檢視控制項相關聯之一般或狀態影像清單的控制碼。 您可以使用 [**TreeView \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要取出的影像清單類型。 這個參數可以是下列其中一個值：



| 值                                                                                                                                                      | 意義                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**TVSIL \_ 正常**</dt> </dl> | 指出一般影像清單，其中包含樹狀檢視控制項專案的已選取、nonselected 和重迭影像。<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**TVSIL \_ 狀態**</dt> </dl>    | 表示狀態影像清單。 您可以使用狀態影像來表示應用程式定義的專案狀態。 狀態影像會顯示在專案的選取專案或 nonselected 影像的左邊。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回指定之影像清單的 HIMAGELIST 控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ SETIMAGELIST**](tvm-setimagelist.md)
</dt> </dl>

 

 





