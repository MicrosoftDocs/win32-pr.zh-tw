---
title: 'STM_GETICON 訊息 (Winuser .h) '
description: 應用程式會傳送 STM \_ GETICON 訊息，以抓取與具有 SS 圖示樣式之靜態控制項相關聯的圖示控制碼 \_ 。
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- STM_GETICON message Windows 控制項
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
ms.openlocfilehash: f64f55d2a2f8315b99526e51a69891f6f0056e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094075"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**STM \_ SETICON**](stm-seticon.md)
</dt> </dl>

 

 





