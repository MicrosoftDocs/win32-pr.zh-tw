---
title: 'LVM_GETNEXTITEMINDEX 訊息 (Commctrl .h) '
description: 抓取指定的清單視圖控制項中，符合指定的屬性和與另一個專案之關聯性之專案的索引。 明確地傳送此訊息，或使用 ListView \_ GetNextItemIndex 宏。
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getnextitemindex.htm
keywords:
- LVM_GETNEXTITEMINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETNEXTITEMINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cfc393aee4f275e941a04bb3f23ee4c2c3ac529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105498"
---
# <a name="lvm_getnextitemindex-message"></a>LVM \_ GETNEXTITEMINDEX 訊息

抓取指定的清單視圖控制項中，符合指定的屬性和與另一個專案之關聯性之專案的索引。 明確地傳送此訊息，或使用 [**ListView \_ GetNextItemIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnextitemindex) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[in、out\]
</dt> <dd>

要開始搜尋之專案的 [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) 結構指標，或-1 會尋找符合指定旗標的第一個專案。 呼叫進程負責配置此結構並設定其成員。

</dd> <dt>

*lParam* 
</dt> <dd>

指定 [參數 *wParam*] 中所列專案的關聯性。 這可以是下列其中一個值或下列值的組合：



| 值                                                                                                                                                                                                                                                             | 意義                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>依索引搜尋。</dt> </dl>                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_ALL"></span><span id="_______________lvni_all"></span><dl> <dt> **LVNI \_ 全部**</dt><dt></dt> </dl>                               | 依索引（預設值）搜尋後續專案。<br/>                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt></dt><dt>依實體關聯性搜尋開始搜尋的專案索引。</dt> </dl>                                         |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_ABOVE"></span><span id="_______________lvni_above"></span><dl> <dt> **LVNI \_ 以上**</dt><dt></dt> </dl>                         | 搜尋指定專案上方的專案。<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_BELOW"></span><span id="_______________lvni_below"></span><dl> <dt> **LVNI \_ 如下**</dt><dt></dt> </dl>                         | 搜尋位於指定之專案底下的專案。<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_TOLEFT"></span><span id="_______________lvni_toleft"></span><dl> <dt> **LVNI \_ TOLEFT**</dt><dt></dt> </dl>                      | 搜尋指定專案左邊的專案。<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="_______________LVNI_PREVIOUS"></span><span id="_______________lvni_previous"></span><dl> <dt> **LVNI \_ 上一步**</dt><dt></dt> </dl>                | **Windows Vista 和更新版本：** 搜尋在 *wParam* 中指定的專案之前排序的專案。 LVNI \_ 上一個旗標不是方向 (LVNI \_ 上述的專案會尋找上面所述的專案，而 LVNI 之前的 \_ 版本則會尋找之前排序的專案。 ) LVNI \_ 先前的旗標基本上會反轉 LVM \_ GETNEXTITEM 或 lvm \_ GETNEXTITEMINDEX 訊息所執行之搜尋的邏輯。<br/> |
| <span id="_______________LVNI_TORIGHT"></span><span id="_______________lvni_toright"></span><dl> <dt> **LVNI \_ TORIGHT**</dt><dt></dt> </dl>                   | 搜尋指定專案右邊的專案。<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="_______________LVNI_DIRECTIONMASK"></span><span id="_______________lvni_directionmask"></span><dl> <dt> **LVNI \_ DIRECTIONMASK**</dt><dt></dt> </dl> | **Windows Vista 和更新版本：** 具有以下值的方向旗標遮罩： LVNI \_ 在 \| \_ \| LVNI \_ TOLEFT \| LVNI \_ TORIGHT 的上方 LVNI。<br/>                                                                                                                                                                                                                                                               |
| <dl> <dt></dt>您 <dt>可以使用下列其中一個或多個值的組合來指定要尋找的專案狀態：</dt> </dl>                                |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_CUT"></span><span id="_______________lvni_cut"></span><dl> <dt> **LVNI \_ 剪**</dt>下 <dt></dt> </dl>                               | 此專案已設定 [**LVIS \_ 剪**](list-view-item-states.md) 下狀態旗標。<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_DROPHILITED"></span><span id="_______________lvni_drophilited"></span><dl> <dt> **LVNI \_ DROPHILITED**</dt><dt></dt> </dl>       | 此專案已設定 [**LVIS \_ DROPHILITED**](list-view-item-states.md) 狀態旗標<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="_______________LVNI_FOCUSED"></span><span id="_______________lvni_focused"></span><dl> <dt> **LVNI \_ 焦點**</dt><dt></dt> </dl>                   | 此專案已設定 [**LVIS \_ 聚焦**](list-view-item-states.md) 狀態旗標。<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="_______________LVNI_SELECTED"></span><span id="_______________lvni_selected"></span><dl> <dt> **LVNI 已 \_ 選取**</dt><dt></dt> </dl>                | 此專案已設定 [**LVIS \_ 選取**](list-view-item-states.md) 狀態旗標。<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="_______________LVNI_STATEMASK"></span><span id="_______________lvni_statemask"></span><dl> <dt> **LVNI \_ STATEMASK**</dt><dt></dt> </dl>             | **Windows Vista 和更新版本：** 具有下列值的狀態旗標遮罩： LVNI \_ 焦點 \| LVNI \_ 選取的 \| LVNI \_ 剪下 \| LVNI \_ DROPHILITED。<br/>                                                                                                                                                                                                                                                               |
| <dl> <dt></dt><dt>依專案的外觀或依群組進行搜尋。</dt> </dl>                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_VISIBLEORDER"></span><span id="_______________lvni_visibleorder"></span><dl> <dt> **LVNI \_ VISIBLEORDER**</dt><dt></dt> </dl>    | **Windows Vista 和更新版本：** 搜尋可見的順序。<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_VISIBLEONLY"></span><span id="_______________lvni_visibleonly"></span><dl> <dt> **LVNI \_ VISIBLEONLY**</dt><dt></dt> </dl>       | **Windows Vista 和更新版本：** 搜尋可見的專案。<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_SAMEGROUPONLY"></span><span id="_______________lvni_samegrouponly"></span><dl> <dt> **LVNI \_ SAMEGROUPONLY**</dt><dt></dt> </dl> | **Windows Vista 和更新版本：** 搜尋目前的群組。<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt></dt><dt>如果專案未設定所有指定的狀態旗標，則會繼續搜尋下一個專案。</dt> </dl>                          |                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

請注意，下列旗標（僅適用于 Windows Vista）與使用中的任何其他旗標互斥： LVNI \_ PREVIOUS、LVNI \_ VISIBLEONLY、LVNI \_ SAMEGROUPONLY、LVNI \_ VISIBLEORDER、LVNI \_ DIRECTIONMASK 和 LVNI \_ STATEMASK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LVM \_ GETNEXTITEM**](lvm-getnextitem.md)
</dt> </dl>

 

 





