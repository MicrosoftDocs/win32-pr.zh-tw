---
title: 'CB_RESETCONTENT 訊息 (Winuser .h) '
description: 從清單方塊中移除所有專案，並編輯下拉式方塊的控制項。
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- CB_RESETCONTENT message Windows 控制項
topic_type:
- apiref
api_name:
- CB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3567f31ef98fffe42e53c4811acc786d41ae9f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843564"
---
# <a name="cb_resetcontent-message"></a>CB \_ RESETCONTENT 訊息

從清單方塊中移除所有專案，並編輯下拉式方塊的控制項。

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

此訊息一律會傳回 CB \_ ok。

## <a name="remarks"></a>備註

如果您建立具有主控描繪樣式的下拉式方塊，但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式，則下拉式方塊的擁有者會收到下拉式方塊中每個專案的 [**WM \_ DELETEITEM**](wm-deleteitem.md) 訊息。

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

[**CB \_ DELETESTRING**](cb-deletestring.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





