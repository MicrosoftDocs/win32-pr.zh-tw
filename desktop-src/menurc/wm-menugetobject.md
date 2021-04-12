---
title: 'WM_MENUGETOBJECT 訊息 (Winuser .h) '
description: 當滑鼠游標進入功能表項目，或從專案的中央移至專案的頂端或底部時，傳送至拖放功能表的擁有者。
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- WM_MENUGETOBJECT 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_MENUGETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e124c7f2757a0d6d1d2ac0904052b6d3c255ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509463"
---
# <a name="wm_menugetobject-message"></a>WM \_ MENUGETOBJECT 訊息

當滑鼠游標進入功能表項目，或從專案的中央移至專案的頂端或底部時，傳送至拖放功能表的擁有者。


```C++
#define WM_MENUGETOBJECT                0x0124
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

應用程式應該會傳回下列其中一個值。



| 傳回碼/值                                                                                                                                                | Description                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNGO \_>AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR**</dt> <dt>0x00000001</dt> </dl>     | 在 [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)的 **pvObj** 成員中傳回介面指標<br/> |
| <dl> <dt>**MNGO \_NOINTERFACE**</dt> <dt>0x00000000</dt> </dl> | 不支援此介面。<br/>                                                                             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[功能表總覽](menus.md)
</dt> </dl>

 

 





