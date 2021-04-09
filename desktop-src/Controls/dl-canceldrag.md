---
title: 'DL_CANCELDRAG (Commctrl 的通知碼) '
description: 藉由按一下滑鼠右鍵或按下 ESC 鍵，表示使用者已取消拖曳作業。
ms.assetid: 62c1377f-41b6-449f-a95e-2689dc1913c6
keywords:
- DL_CANCELDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DL_CANCELDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab10f7c31184c44fabdffd4f611847e550b62cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106691"
---
# <a name="dl_canceldrag-notification-code"></a>DL \_ CANCELDRAG 通知碼

藉由按一下滑鼠右鍵或按下 ESC 鍵，表示使用者已取消拖曳作業。 拖曳清單方塊會將此通知碼以拖曳清單訊息的形式傳送至其父視窗。 如需詳細資訊，請參閱 [拖曳清單方塊訊息](about-list-boxes.md)。


```C++
DL_CANCELDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)結構的指標，其中包含 DL \_ CANCELDRAG 通知碼、拖曳清單方塊的控制碼，以及游標位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

藉由處理 DL \_ CANCELDRAG 通知程式碼，應用程式可以重設其內部狀態，以指出拖曳沒有作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





