---
title: 'PSM_INSERTPAGE 訊息 (Prsht.idl .h) '
description: 將新頁面插入現有的屬性工作表中。 頁面可以插入指定的索引或指定的頁面之後。 您可以使用 PropSheet InsertPage 宏明確地傳送此訊息 \_ 。
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- PSM_INSERTPAGE message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_INSERTPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afdd58536a5cdd18d39a331df4b18c9bbae93842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968361"
---
# <a name="psm_insertpage-message"></a>PSM \_ INSERTPAGE 訊息

將新頁面插入現有的屬性工作表中。 頁面可以插入指定的索引或指定的頁面之後。 您可以使用 [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要插入頁面的位置。 將此參數設定為 **Null** ，以將新頁面設為第一頁。 若要指定要插入新頁面的位置，您可以傳遞索引或現有頁面的 HPROPSHEETPAGE 控制碼。



| 值                                                                                                                                             | 意義                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>索引</dt> </dl>            | 如果 *wParam* 參數小於 MAXUSHORT () 最大不帶正負號的短整數，則 *wParam* 會為新頁面指定以零為基底的索引。 例如，若要將插入的頁面設為屬性工作表上的第三頁，請將 *wParam* 設定為2。 若要將它設為第一頁，請將 *wParam* 設定為0。 如果 *wParam* 的值大於頁面數目且小於 MAXUSHORT，則會附加該頁面。<br/> |
| <dl> <dt></dt><dt>hpageInsertAfter</dt> </dl> | 如果您將 *wParam* 參數設定為現有頁面的 HPROPSHEETPAGE 控制碼，就會在新頁面之後插入新頁面。<br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

要插入之頁面的控制碼。 頁面必須先透過呼叫 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) 函數來建立。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功插入頁面，則會傳回非零值，否則會傳回零。

## <a name="remarks"></a>備註

插入點之後的頁面會向右移動，以容納新的頁面。

屬性工作表未調整大小以符合新的頁面。 不要讓新的頁面大於屬性工作表的最大頁面。

當屬性工作表正在動作頁面清單時，會發生一些訊息和一個函式呼叫。 當此動作執行時，嘗試修改頁面清單將會產生無法預期的結果。 因此，您不應該 \_ 在 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 的執行中或在處理下列通知和 Windows 訊息時使用 PSM INSERTPAGE 訊息。

-   [PSN \_ APPLY](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [PSN \_ 重設](psn-reset.md)
-   [PSN \_ ADVANCED.FIELD.SETACTIVE](psn-setactive.md)
-   [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)

如果您在處理其中一個訊息時，或當 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 正在運作時需要修改屬性工作表頁面，請自行張貼私用 Windows 訊息。 在屬性工作表管理員完成其工作之前，您的應用程式將不會收到該訊息。 然後您可以修改頁面清單。

下列通知也會受到屬性工作表修改的影響。

-   [PSN \_ WIZBACK](psn-wizback.md)
-   [PSN \_ WIZNEXT](psn-wiznext.md)

您可以新增或移除頁面，以回應這些通知，前提是您透過 DWL MSGRESULT 傳回 (， \_) 非零值來指定所需的新頁面。 但是請注意，如果您插入的頁面是在目前的頁面 (，其索引小於目前的頁面) ， [PSN \_ KILLACTIVE](psn-killactive.md) 可能會傳送至錯誤的頁面。

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

