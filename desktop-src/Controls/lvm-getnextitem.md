---
title: 'LVM_GETNEXTITEM 訊息 (Commctrl .h) '
description: 搜尋具有指定屬性的清單視圖專案，並將指定的關聯性帶到指定的專案。 您可以明確地傳送此訊息，或使用 ListView \_ GetNextItem 宏來傳送。
ms.assetid: 2d458f12-b9d3-4b9e-bcb4-927c14c16537
keywords:
- LVM_GETNEXTITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETNEXTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40e8e6fdf068f06176d6965a2fb885b349a74ea5cde73c5952d16d7c76512ae8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002558"
---
# <a name="lvm_getnextitem-message"></a>LVM \_ GETNEXTITEM 訊息

搜尋具有指定屬性的清單視圖專案，並將指定的關聯性帶到指定的專案。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetNextItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnextitem) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要開始搜尋的專案索引，或-1 以尋找符合指定旗標的第一個專案。 從搜尋中排除指定的專案本身。

</dd> <dt>

*lParam* 
</dt> <dd>

指定 *wParam* 中指定之專案的關聯性。 這可以是下列其中一個值或下列值的組合：



| 值                                                                                                                                                                                                                                                             | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>依索引搜尋。</dt> </dl>                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_ALL"></span><span id="_______________lvni_all"></span><dl> <dt> **LVNI \_ 全部**</dt><dt></dt> </dl>                               | 依索引（預設值）搜尋後續專案。<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="_______________LVNI_PREVIOUS"></span><span id="_______________lvni_previous"></span><dl> <dt> **LVNI \_ 上一步**</dt><dt></dt> </dl>                | **Windows Vista 和更新版本：** 搜尋在 *wParam* 中指定的專案之前排序的專案。 LVNI \_ 上一個旗標不是方向 (LVNI \_ 上述的專案會尋找上面所述的專案，而 LVNI 之前的 \_ 版本則會尋找之前排序的專案。 ) LVNI \_ 先前的旗標基本上會反轉 **LVM \_ GETNEXTITEM** 或 [**lvm \_ GETNEXTITEMINDEX**](lvm-getnextitemindex.md) 訊息所執行之搜尋的邏輯。<br/> |
| <dl> <dt></dt><dt>依實體關聯性搜尋開始搜尋的專案索引。</dt> </dl>                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_ABOVE"></span><span id="_______________lvni_above"></span><dl> <dt> **LVNI \_ 以上**</dt><dt></dt> </dl>                         | 搜尋指定專案上方的專案。<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_BELOW"></span><span id="_______________lvni_below"></span><dl> <dt> **LVNI \_ 如下**</dt><dt></dt> </dl>                         | 搜尋位於指定之專案底下的專案。<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_TOLEFT"></span><span id="_______________lvni_toleft"></span><dl> <dt> **LVNI \_ TOLEFT**</dt><dt></dt> </dl>                      | 搜尋指定專案左邊的專案。<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="_______________LVNI_TORIGHT"></span><span id="_______________lvni_toright"></span><dl> <dt> **LVNI \_ TORIGHT**</dt><dt></dt> </dl>                   | 搜尋指定專案右邊的專案。<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_DIRECTIONMASK"></span><span id="_______________lvni_directionmask"></span><dl> <dt> **LVNI \_ DIRECTIONMASK**</dt><dt></dt> </dl> | **Windows Vista 和更新版本：** 具有以下值的方向旗標遮罩： LVNI \_ 在 \| \_ \| LVNI \_ TOLEFT \| LVNI \_ TORIGHT 的上方 LVNI。<br/>                                                                                                                                                                                                                                                                                                   |
| <dl> <dt></dt>您 <dt>可以使用下列其中一個或多個值的組合來指定要尋找的專案狀態：</dt> </dl>                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_CUT"></span><span id="_______________lvni_cut"></span><dl> <dt> **LVNI \_ 剪**</dt>下 <dt></dt> </dl>                               | 此專案已設定 [**LVIS \_ 剪**](list-view-item-states.md) 下狀態旗標。<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_DROPHILITED"></span><span id="_______________lvni_drophilited"></span><dl> <dt> **LVNI \_ DROPHILITED**</dt><dt></dt> </dl>       | 此專案已設定 [**LVIS \_ DROPHILITED**](list-view-item-states.md) 狀態旗標<br/>                                                                                                                                                                                                                                                                                                                                        |
| <span id="_______________LVNI_FOCUSED"></span><span id="_______________lvni_focused"></span><dl> <dt> **LVNI \_ 焦點**</dt><dt></dt> </dl>                   | 此專案已設定 [**LVIS \_ 聚焦**](list-view-item-states.md) 狀態旗標。<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="_______________LVNI_SELECTED"></span><span id="_______________lvni_selected"></span><dl> <dt> **LVNI 已 \_ 選取**</dt><dt></dt> </dl>                | 此專案已設定 [**LVIS \_ 選取**](list-view-item-states.md) 狀態旗標。<br/>                                                                                                                                                                                                                                                                                                                                             |
| <span id="_______________LVNI_STATEMASK"></span><span id="_______________lvni_statemask"></span><dl> <dt> **LVNI \_ STATEMASK**</dt><dt></dt> </dl>             | **Windows Vista 和更新版本：** 具有下列值的狀態旗標遮罩： LVNI \_ 焦點 \| LVNI \_ 選取的 \| LVNI \_ 剪下 \| LVNI \_ DROPHILITED。<br/>                                                                                                                                                                                                                                                                                                   |
| <dl> <dt></dt><dt>依專案的外觀或依群組搜尋</dt> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_VISIBLEORDER"></span><span id="_______________lvni_visibleorder"></span><dl> <dt> **LVNI \_ VISIBLEORDER**</dt><dt></dt> </dl>    | **Windows Vista 和更新版本：** 搜尋可見的順序。<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_VISIBLEONLY"></span><span id="_______________lvni_visibleonly"></span><dl> <dt> **LVNI \_ VISIBLEONLY**</dt><dt></dt> </dl>       | **Windows Vista 和更新版本：** 搜尋可見的專案。<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_SAMEGROUPONLY"></span><span id="_______________lvni_samegrouponly"></span><dl> <dt> **LVNI \_ SAMEGROUPONLY**</dt><dt></dt> </dl> | **Windows Vista 和更新版本：** 搜尋目前的群組。<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt></dt><dt>如果專案未設定所有指定的狀態旗標，則會繼續搜尋下一個專案。</dt> </dl>                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回下一個專案的索引，否則傳回-1。

## <a name="remarks"></a>備註

請注意，下列旗標（僅適用于 Windows Vista）與使用中的任何其他旗標互斥： LVNI \_ VISIBLEONLY、LVNI \_ SAMEGROUPONLY、LVNI \_ VISIBLEORDER、LVNI \_ DIRECTIONMASK 和 LVNI \_ STATEMASK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





