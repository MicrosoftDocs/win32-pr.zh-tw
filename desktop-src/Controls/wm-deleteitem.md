---
title: 'WM_DELETEITEM 訊息 (Winuser .h) '
description: 當清單方塊或下拉式方塊終結時，或是當 LB \_ DELETESTRING、lb \_ RESETCONTENT、CB \_ DELETESTRING 或 CB \_ RESETCONTENT 訊息移除專案時，傳送給清單方塊或下拉式方塊的擁有者。
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- WM_DELETEITEM message Windows 控制項
topic_type:
- apiref
api_name:
- WM_DELETEITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf37f8a367d23353903bd3cda85b573f6884ff2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465145"
---
# <a name="wm_deleteitem-message"></a>WM \_ DELETEITEM 訊息

當清單方塊或下拉式方塊終結時，或是當 [**lb \_ DELETESTRING**](lb-deletestring.md)、 [**lb \_ RESETCONTENT**](lb-resetcontent.md)、 [**CB \_ DELETESTRING**](cb-deletestring.md)或 [**CB \_ RESETCONTENT**](cb-resetcontent.md) 訊息移除專案時，傳送給清單方塊或下拉式方塊的擁有者。 系統會為每個已刪除的專案傳送 **WM \_ DELETEITEM** 訊息。 系統會傳送包含非零專案資料之任何已刪除清單方塊或下拉式方塊專案的 **WM \_ DELETEITEM** 訊息。


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定傳送 **WM \_ DELETEITEM** 訊息之控制項的識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

[**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)結構的指標，其中包含從清單方塊中刪除之專案的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回 **TRUE** 。

## <a name="remarks"></a>備註

Microsoft Windows NT 和更新版本： Windows 僅針對從主控描繪清單方塊中刪除的專案傳送 **WM \_ DELETEITEM** 訊息 (具有 [**磅 \_ OWNERDRAWFIXED**](list-box-styles.md) 或 [**磅 \_ OWNERDRAWVARIABLE**](list-box-styles.md) 樣式) 或擁有者繪製的下拉式列示方塊， (使用 [**cbs \_ OWNERDRAWFIXED**](combo-box-styles.md) 或 [**cbs \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式) 。

Windows 95： Windows 傳送包含非零專案資料之任何已刪除清單方塊或下拉式方塊專案的 **WM \_ DELETEITEM** 訊息。

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

[**CB \_ RESETCONTENT**](cb-resetcontent.md)
</dt> <dt>

[**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[**LB \_ DELETESTRING**](lb-deletestring.md)
</dt> <dt>

[**LB \_ RESETCONTENT**](lb-resetcontent.md)
</dt> </dl>

 

 





