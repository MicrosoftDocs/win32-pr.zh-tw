---
title: 'LVM_SETITEMCOUNT 訊息 (Commctrl .h) '
description: 讓清單視圖控制項配置記憶體給指定的專案數，或設定虛擬清單視圖控制項中的虛擬專案數。
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- LVM_SETITEMCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e390e7ae5913053f91f7f2f8d197af1cf4b7a40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094176"
---
# <a name="lvm_setitemcount-message"></a>LVM \_ SETITEMCOUNT 訊息

讓清單視圖控制項配置記憶體給指定的專案數，或設定 [虛擬清單視圖控制項](list-view-controls-overview.md)中的虛擬專案數。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

清單視圖控制項最終將包含的專案數目。

</dd> <dt>

*lParam* 
</dt> <dd>

[版本 4.70](common-control-versions.md)。 值，指定在重設專案計數之後，清單視圖控制項的行為。 這個值可以是下列各項的組合：



| 值                                                                                                                                                                                    | 意義                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <dt>**LVSICF \_ NOINVALIDATEALL**</dt> </dl> | 除非受影響的專案目前為 view，否則不會重新繪製清單視圖控制項。<br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <dt>**LVSICF \_ NOSCROLL**</dt> </dl>                      | 當專案計數變更時，清單視圖控制項不會變更捲軸位置。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

記憶體的配置方式取決於建立清單視圖控制項的方式。 您可以明確地傳送此訊息，或使用 [**listview \_ SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) 或 [**listview \_ SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) 宏。 如需詳細資訊，請參閱 [虛擬 List-View 樣式](/windows/desktop/Controls/list-view-controls-overview)。

如果未在 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式下建立清單視圖控制項，則傳送此訊息會導致控制項為指定的專案數配置其內部資料結構。 這可防止控制項在每次加入專案時都必須配置資料結構。

如果使用 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式建立清單視圖控制項 (虛擬清單視圖) ，則傳送此訊息會設定控制項包含的虛擬專案數目。

*LParam* 參數僅適用于使用 [**Lvs) \_ OWNERDATA**](list-view-window-styles.md)和 [**lvs) \_ 報表**](list-view-window-styles.md)或 [**lvs) \_ 清單**](list-view-window-styles.md)樣式的清單視圖控制項。

當通用控制項清單視圖為虛擬化清單-view ([**lvs) \_ OWNERDATA**](list-view-window-styles.md)) 時，清單視圖上會有100000000專案的限制。 在此案例中，當 **LVM \_ SETITEMCOUNT** 的 *wParam* 為100000001時，會傳回 FALSE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

