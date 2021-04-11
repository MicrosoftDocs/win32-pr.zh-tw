---
title: 'LVM_GETIMAGELIST 訊息 (Commctrl .h) '
description: 抓取用來繪製清單視圖專案的影像清單控制碼。 您可以明確地傳送此訊息，或使用 ListView \_ GetImageList 宏來傳送。
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- LVM_GETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abc68c5e5dd9a18c3ec203ad7fe3db97a542845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104453"
---
# <a name="lvm_getimagelist-message"></a>LVM \_ GETIMAGELIST 訊息

抓取用來繪製清單視圖專案的影像清單控制碼。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要取出的影像清單。 這個參數可以是下列其中一個值：



| 值                                                                                                                                                                     | 意義                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ 正常**</dt> </dl>                | 具有大型圖示的影像清單。<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ SMALL**</dt> </dl>                   | 具有小圖示的影像清單。<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**LVSIL \_ 狀態**</dt> </dl>                   | 具有狀態影像的影像清單。<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**LVSIL \_ GROUPHEADER**</dt> </dl> | 群組頁首的影像清單。<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回指定之影像清單的控制碼，否則傳回 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





