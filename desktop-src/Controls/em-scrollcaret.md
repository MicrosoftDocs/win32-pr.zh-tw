---
title: 'EM_SCROLLCARET 訊息 (Winuser .h) '
description: 將插入號滾動至編輯控制項中的 view。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 7a33034d-9369-49f8-a881-0c1d2cedff6a
keywords:
- EM_SCROLLCARET 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SCROLLCARET
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fd3a752d9f8c8cf0fed812d10a4d18633fb682f3f127c6fc7f2f47744ae861b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171377"
---
# <a name="em_scrollcaret-message"></a>EM \_ SCROLLCARET 訊息

將插入號滾動至編輯控制項中的 view。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

此參數已保留備用。 它應該設定為零。

</dd> <dt>

*lParam* 
</dt> <dd>

此參數已保留備用。 它應該設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值沒有意義。

## <a name="remarks"></a>備註

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

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

[**EM \_ LINESCROLL**](em-linescroll.md)
</dt> <dt>

[**EM \_ 捲軸**](em-scroll.md)
</dt> <dt>

[**WM \_ VSCROLL**](wm-vscroll.md)
</dt> </dl>

 

 





