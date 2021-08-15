---
title: 'LVM_GETGROUPRECT 訊息 (Commctrl .h) '
description: 取得指定群組的矩形。 明確地傳送此訊息，或使用 ListView \_ GetGroupRect 宏。
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- LVM_GETGROUPRECT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETGROUPRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89340015972799b059e4568b5e87be511b7fc3718e7e7494d1bf46296886f030
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540918"
---
# <a name="lvm_getgrouprect-message"></a>LVM \_ GETGROUPRECT 訊息

取得指定群組的矩形。 明確地傳送此訊息，或使用 [**ListView \_ GetGroupRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

指定 group by **iGroupId** (參閱 [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) 結構) 。

</dd> <dt>

*lParam* \[in、out\]
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，用來接收 *wParam* 所指定之群組的資訊。 訊息接收者負責為結構成員設定 *wParam* 所指定之群組的資訊。

呼叫進程負責為結構配置記憶體。 將矩形的 **頂端** 成員設定 [**為下列**](/previous-versions//dd162897(v=vs.85)) 其中一個旗標，以指定要取得的矩形座標。



| 值                                                                                                                                                                  | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <dt>**LVGGR \_ 群組**</dt> </dl>                | 整個展開群組的座標。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <dt>**LVGGR \_ 標頭**</dt> </dl>             | 僅 (折迭的群組) 的標頭座標。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <dt>**LVGGR \_ 標籤**</dt> </dl>                | 標籤的座標。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <dt>**LVGGR \_ SUBSETLINK**</dt> </dl> | 子集連結的座標只 (標記子集) 。 清單視圖控制項可以限制每個群組中顯示的可見專案數目。 使用者會看到連結，讓使用者可以展開群組。 如果群組是 LVGS SUBSETED 的子集 (群組狀態，此旗標將會傳回子集連結的周框 \_ ，請參閱結構 [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)、成員 **狀態**) 。 提供此旗標，讓協助工具應用程式可以找到連結。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

