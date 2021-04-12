---
title: 'PSM_SETCURSEL 訊息 (Prsht.idl .h) '
description: 啟用屬性工作表中的指定頁面。 您可以使用 PropSheet SetCurSel 宏明確地傳送此訊息 \_ 。
ms.assetid: 800aadde-cabc-424e-8e63-60fc7ce952d7
keywords:
- PSM_SETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETCURSEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f41f0ba2ec8d13a7bfc932b553b355399f76b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094419"
---
# <a name="psm_setcursel-message"></a>PSM \_ SETCURSEL 訊息

啟用屬性工作表中的指定頁面。 您可以使用 [**PropSheet \_ SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的頁面索引。 應用程式可以指定索引或控制碼或兩者。 如果同時指定這兩者， *lParam* 會優先使用。

</dd> <dt>

*lParam* 
</dt> <dd>

要啟用之頁面的控制碼。 應用程式可以指定索引或控制碼或兩者。 如果同時指定這兩者， *lParam* 會優先使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

遺失啟用的視窗會收到 [PSN \_ KILLACTIVE](psn-killactive.md) 通知程式碼，而取得啟用的視窗則會接收 [PSN \_ advanced.field.setactive](psn-setactive.md) 通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

 





