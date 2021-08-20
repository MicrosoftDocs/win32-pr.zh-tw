---
title: 'PSM_GETRESULT 訊息 (Prsht.idl .h) '
description: 由非強制回應屬性工作表用來取出 PropertySheet 傳回的強制回應屬性工作表資訊。 您可以明確地傳送此訊息，或使用 PropSheet \_ GetResult 宏。
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- PSM_GETRESULT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PSM_GETRESULT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acc8fed8cdaa1f4282c3ed066ad44f68221330fa9e79b0719db8bba1bca37f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169804"
---
# <a name="psm_getresult-message"></a>PSM \_ GETRESULT 訊息

由非強制回應屬性工作表用來取出 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)傳回的強制回應屬性工作表資訊。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) 宏。

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

如果成功，則傳回正值，否則傳回-1。 下列傳回值具有特殊意義。



| 傳回碼                                                                                         | 描述                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**識別碼 \_ PSREBOOTSYSTEM**</dt> </dl>   | 頁面傳送了 [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) 訊息給屬性工作表。 電腦必須重新開機，使用者的變更才會生效。<br/> |
| <dl> <dt>**識別碼 \_ PSRESTARTWINDOWS**</dt> </dl> | 頁面傳送了 [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) 訊息給屬性工作表。 必須重新開機 Windows，使用者的變更才會生效。<br/>  |



 

## <a name="remarks"></a>備註

若要取出延伸的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

此訊息的傳回值與 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 針對模式屬性工作表傳回的值相同。

[版本5.80。](common-control-versions.md) [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)傳回值會針對強制回應和非強制回應屬性工作表攜帶不同的資訊。 在某些情況下，非強制回應屬性工作表可能需要從 **PropertySheet** 接收的資訊（如果已強制回應）。 尤其是，他們可能需要知道識別碼 \_ PSREBOOTSYSTEM 或識別碼 PSRESTARTWINDOWS 是否 \_ 會傳回。

若為非強制回應屬性工作表，您的訊息迴圈應該使用 [**psm \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md) 將訊息傳遞至 [屬性工作表] 對話方塊，並使用 [ [**psm \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) ] 來判斷何時要終結對話方塊。 當使用者按一下 [ **確定]** 或 [ **取消** ] 按鈕時， **PSM \_ GETCURRENTPAGEHWND** 會傳回 **Null**。 然後，您可以藉由傳送 **PSM \_ GETRESULT** 訊息來取得強制回應屬性工作表從 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)接收的值。

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

