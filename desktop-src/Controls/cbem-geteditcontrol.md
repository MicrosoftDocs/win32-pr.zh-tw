---
title: 'CBEM_GETEDITCONTROL 訊息 (Commctrl .h) '
description: 取得 ComboBoxEx 控制項之編輯控制項部分的控制碼。 當 ComboBoxEx 控制項設定為 CBS 下拉式樣式時，會使用編輯方塊 \_ 。
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- CBEM_GETEDITCONTROL 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885a90a1b37fab7cd8e4a492bd00ad349f96202e13ee25a404f7f4aa41f623e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414068"
---
# <a name="cbem_geteditcontrol-message"></a>CBEM \_ GETEDITCONTROL 訊息

取得 ComboBoxEx 控制項之編輯控制項部分的控制碼。 當 ComboBoxEx 控制項設定為 [**CBS \_ 下拉式**](combo-box-styles.md) 樣式時，會使用編輯方塊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 ComboBoxEx 控制項中編輯控制項的控制碼（如果它使用 [**CBS \_ 下拉式清單**](combo-box-styles.md) 樣式）。 否則，訊息會傳回 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





