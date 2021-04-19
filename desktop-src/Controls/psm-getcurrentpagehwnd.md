---
title: 'PSM_GETCURRENTPAGEHWND 訊息 (Prsht.idl .h) '
description: 抓取屬性工作表目前頁面的視窗控制碼。 您可以使用 PropSheet GetCurrentPageHwnd 宏明確地傳送此訊息 \_ 。
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- PSM_GETCURRENTPAGEHWND message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_GETCURRENTPAGEHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9ac89e6bc60317f2caf31ea92754d10983e11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965926"
---
# <a name="psm_getcurrentpagehwnd-message"></a>PSM \_ GETCURRENTPAGEHWND 訊息

抓取屬性工作表目前頁面的視窗控制碼。 您可以使用 [**PropSheet \_ GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回目前屬性工作表頁面的視窗控制碼。

## <a name="remarks"></a>備註

使用具有非強制回應屬性工作表的 **PSM \_ GETCURRENTPAGEHWND** 訊息，以判斷何時要終結對話方塊。 當使用者按一下 [ **確定]** 或 [ **取消** ] 按鈕時， **PSM \_ GETCURRENTPAGEHWND** 會傳回 **Null**，然後您可以使用 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) 函數來終結對話方塊。

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

