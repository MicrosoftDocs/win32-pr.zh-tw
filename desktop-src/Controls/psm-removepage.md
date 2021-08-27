---
title: 'PSM_REMOVEPAGE 訊息 (Prsht.idl .h) '
description: 從屬性工作表移除頁面。 您可以使用 PropSheet RemovePage 宏明確地傳送此訊息 \_ 。
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- PSM_REMOVEPAGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PSM_REMOVEPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1493fe8a4f6a3b8e8ac93103d27e67ae984221bdc6efd584130879d17249c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088608"
---
# <a name="psm_removepage-message"></a>PSM \_ REMOVEPAGE 訊息

從屬性工作表移除頁面。 您可以使用 [**PropSheet \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要移除之頁面的以零為基底的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

要移除之頁面的 HPROPSHEETPAGE 控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

應用程式可以指定索引或控制碼，或兩者。 如果同時指定這兩者， *lParam* 會優先使用。

傳送 **PSM \_ REMOVEPAGE** 會損毀正在移除的屬性工作表頁面。

當屬性工作表正在動作頁面清單時，會發生一些訊息和一個函式呼叫。 當此動作執行時，嘗試修改頁面清單將會產生無法預期的結果。 因此，您不應該在 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)的執行中或在處理下列通知並 Windows 訊息時，使用 **PSM \_ REMOVEPAGE** 訊息。

-   [PSN \_ APPLY](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [PSN \_ 重設](psn-reset.md)
-   [PSN \_ ADVANCED.FIELD.SETACTIVE](psn-setactive.md)
-   [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)

如果您在處理其中一個訊息時，或當 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)正在進行時需要修改屬性工作表頁面，請自行張貼私用 Windows 訊息。 在屬性工作表管理員完成其工作之前，您的應用程式將不會收到該訊息。 然後您可以修改頁面清單。

下列通知也會受到屬性工作表修改的影響。

-   [PSN \_ WIZBACK](psn-wizback.md)
-   [PSN \_ WIZNEXT](psn-wiznext.md)

您可以新增或移除頁面，以回應這些通知，前提是您透過 DWL MSGRESULT 傳回 (， \_) 非零值來指定所需的新頁面。 但是請注意，如果您移除目前頁面之前的頁面 (，其索引小於目前頁面) 的索引， [PSN \_ KILLACTIVE](psn-killactive.md) 可能會傳送至錯誤的頁面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

