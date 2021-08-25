---
title: 'PSM_SETCURSELID 訊息 (Prsht.idl .h) '
description: 根據頁面的資源識別碼，啟用屬性工作表中的指定頁面。 您可以使用 PropSheet SetCurSelByID 宏明確地傳送此訊息 \_ 。
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- PSM_SETCURSELID 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETCURSELID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be1d21b5153d480e409c6e9e7f4204746b5509b058bc292509e24ad9e03b538
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877018"
---
# <a name="psm_setcurselid-message"></a>PSM \_ SETCURSELID 訊息

根據頁面的資源識別碼，啟用屬性工作表中的指定頁面。 您可以使用 [**PropSheet \_ SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

要啟動之頁面的資源識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

遺失啟用的視窗會收到 [PSN \_ KILLACTIVE](psn-killactive.md) 通知程式碼，而取得啟用的視窗則會接收 [PSN \_ advanced.field.setactive](psn-setactive.md) 通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

 





