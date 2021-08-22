---
title: 'STM_SETICON 訊息 (Winuser .h) '
description: 應用程式會傳送 STM \_ SETICON 訊息，以將圖示與圖示控制項產生關聯。
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- STM_SETICON 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- STM_SETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ff1cbaa6a1083751b3619392fbb0d3b60695e829907c2dfe27fdb41170e167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119281418"
---
# <a name="stm_seticon-message"></a>STM \_ SETICON 訊息

應用程式會傳送 **STM \_ SETICON** 訊息，以將圖示與圖示控制項產生關聯。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要與圖示控制項相關聯之圖示的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是先前與圖示控制項相關聯之圖示的控制碼; 如果發生錯誤，則為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**STM \_ GETICON**](stm-geticon.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**LoadIcon**](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

