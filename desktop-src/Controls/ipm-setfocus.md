---
title: 'IPM_SETFOCUS 訊息 (Commctrl .h) '
description: 將鍵盤焦點設定為 IP 位址控制項中的指定欄位。 將會選取該欄位中的所有文字。
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- IPM_SETFOCUS message Windows 控制項
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d713e0a8b7eb838a2db5c4738c801d4fb76b782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104460"
---
# <a name="ipm_setfocus-message"></a>IPM \_ SETFOCUS 訊息

將鍵盤焦點設定為 IP 位址控制項中的指定欄位。 將會選取該欄位中的所有文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的欄位索引，應設定焦點。 如果這個值大於欄位數目，則焦點會設定為第一個空白欄位。 如果所有欄位都是非空白的，則焦點會設定為第一個欄位。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





