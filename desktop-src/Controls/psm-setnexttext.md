---
title: 'PSM_SETNEXTTEXT 訊息 (Prsht.idl .h) '
description: 設定 wizard 中 [下一步] 按鈕的文字。 您可以使用 PropSheet SetNextText 宏明確地傳送此訊息 \_ 。
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- PSM_SETNEXTTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d781a8d76fca5c1e74bcda452b6ab7e03a32aacc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685556"
---
# <a name="psm_setnexttext-message"></a>PSM \_ SETNEXTTEXT 訊息

設定 wizard 中 [ **下一步** ] 按鈕的文字。 您可以使用 [**PropSheet \_ SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

包含文字之緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有有意義的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **PSM \_SETNEXTTEXTW** (Unicode) <br/>                                         |



 

 





