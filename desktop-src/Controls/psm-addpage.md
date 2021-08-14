---
title: 'PSM_ADDPAGE 訊息 (Prsht.idl .h) '
description: 將新頁面加入現有屬性工作表的結尾。 您可以使用 PropSheet AddPage 宏明確地傳送此訊息 \_ 。
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- PSM_ADDPAGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PSM_ADDPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17e9da965e5e45c6fe11bc319436c00663fdc6348d3d2457b3c15472f6f3868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169824"
---
# <a name="psm_addpage-message"></a>PSM \_ ADDPAGE 訊息

將新頁面加入現有屬性工作表的結尾。 您可以使用 [**PropSheet \_ AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

要加入之頁面的控制碼。 頁面必須已由先前對 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) 函式的呼叫所建立。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

新頁面應該不會大於目前屬性工作表中最大的頁面，因為未調整內容工作表的大小以符合新頁面。

當屬性工作表正在動作頁面清單時，會發生一些訊息和一個函式呼叫。 當此動作執行時，嘗試修改頁面清單將會產生無法預期的結果。 因此，您不應該 \_ 在 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)的執行中或在處理下列通知並 Windows 訊息時，使用 PSM ADDPAGE 訊息。

-   [PSN \_ APPLY](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [PSN \_ 重設](psn-reset.md)
-   [PSN \_ ADVANCED.FIELD.SETACTIVE](psn-setactive.md)
-   [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)

如果您在處理其中一個訊息時，或當 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)正在進行時需要修改屬性工作表頁面，請自行張貼私用 Windows 訊息。 在屬性工作表管理員完成其工作之前，您的應用程式將不會收到該訊息。 然後您可以修改頁面清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

