---
title: 'STM_GETICON 訊息 (Winuser .h) '
description: 應用程式會傳送 STM \_ GETICON 訊息，以抓取與具有 SS 圖示樣式之靜態控制項相關聯的圖示控制碼 \_ 。
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- STM_GETICON 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- STM_GETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d33aab01e668f4b77e36a0a62b8eab75f3ee5db82188416c295c04cdf9bcb078
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084948"
---
# <a name="stm_geticon-message"></a>STM \_ GETICON 訊息

應用程式會傳送 **STM \_ GETICON** 訊息，以抓取與具有 SS 圖示樣式之靜態控制項相關聯的圖示控制碼 \_ 。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是圖示的控制碼; 如果靜態控制項沒有相關聯的圖示或發生錯誤，則為 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**STM \_ SETICON**](stm-seticon.md)
</dt> </dl>

 

 





