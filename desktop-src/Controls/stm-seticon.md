---
title: 'STM_SETICON 訊息 (Winuser .h) '
description: 應用程式會傳送 STM \_ SETICON 訊息，以將圖示與圖示控制項產生關聯。
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- STM_SETICON message Windows 控制項
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
ms.openlocfilehash: cb9c7e2a007c1f866a1c73b3a1c1a55b157add47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024648"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



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

 

