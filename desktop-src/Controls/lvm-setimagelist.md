---
title: 'LVM_SETIMAGELIST 訊息 (Commctrl .h) '
description: 將影像清單指派給清單視圖控制項。 您可以明確地傳送此訊息，或使用 ListView \_ SetImageList 宏來傳送。
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- LVM_SETIMAGELIST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4151f7d6e3736e6fe28faa28bc258fb4f85bfb57622b1ec77c02ed83ea187941
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919958"
---
# <a name="lvm_setimagelist-message"></a>LVM \_ SETIMAGELIST 訊息

將影像清單指派給清單視圖控制項。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

影像清單的類型。 這個參數可以是下列其中一個值：



| 值                                                                                                                                                                     | 意義                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ 正常**</dt> </dl>                | 具有大型圖示的影像清單。<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ SMALL**</dt> </dl>                   | 具有小圖示的影像清單。<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**LVSIL \_ 狀態**</dt> </dl>                   | 具有狀態影像的影像清單。<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**LVSIL \_ GROUPHEADER**</dt> </dl> | 群組頁首的影像清單。<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

要指派之影像清單的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回與控制項相關聯之影像清單的控制碼; 否則為 **Null** 。

## <a name="remarks"></a>備註

除非設定了 [**lvs) \_ SHAREIMAGELISTS**](list-view-window-styles.md) 樣式，否則當清單視圖控制項終結時，目前的影像清單將會終結。 如果您使用此訊息將一個影像清單取代為另一個，則您的應用程式必須明確地終結目前以外的所有影像清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





