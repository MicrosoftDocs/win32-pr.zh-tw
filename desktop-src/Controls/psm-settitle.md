---
title: 'PSM_SETTITLE 訊息 (Prsht.idl .h) '
description: 設定屬性工作表的標題。 您可以使用 PropSheet SetTitle 宏明確地傳送此訊息 \_ 。
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- PSM_SETTITLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETTITLE
- PSM_SETTITLEA
- PSM_SETTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 782d5ebf3e7fe0850b89d9f52f0dc5c406dbd41c9bdad694b41b8ae9ea4c8b0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985448"
---
# <a name="psm_settitle-message"></a>PSM \_ SETTITLE 訊息

設定屬性工作表的標題。 您可以使用 [**PropSheet \_ SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

旗標，指出是否要包含前置詞 "Properties" 或後置詞 "Properties" (視具有指定之標題字串的版本) 而定。 如果此值為 PSH \_ PROPTITLE，則會包含前置詞或尾碼。

</dd> <dt>

*lParam* 
</dt> <dd>

包含標題字串的緩衝區指標。 如果此參數的 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 為 **Null**，則屬性工作表會載入 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))中指定的字串資源。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

在 Aero Wizard 中，此訊息可以用來動態變更內部頁面的標題;例如，在處理 [PSN \_ advanced.field.setactive](psn-setactive.md) 通知時。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **PSM \_SETTITLEW** (Unicode) 和 **PSM \_ SETTITLEA** (ANSI) <br/>              |



 

