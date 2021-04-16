---
title: 'WM_COMPAREITEM 訊息 (Winuser .h) '
description: 傳送來判斷新專案在主控描繪下拉式方塊或清單方塊的排序清單中的相對位置。
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- WM_COMPAREITEM message Windows 控制項
topic_type:
- apiref
api_name:
- WM_COMPAREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f269b90f00e69cce2fb84e6b4efa76e554ad96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464240"
---
# <a name="wm_compareitem-message"></a>WM \_ COMPAREITEM 訊息

傳送來判斷新專案在主控描繪下拉式方塊或清單方塊的排序清單中的相對位置。 每當應用程式加入新的專案時，系統會將此訊息傳送給以 [**CBS \_ 排序**](combo-box-styles.md) 或 [**磅 \_ 排序**](list-box-styles.md) 樣式建立的下拉式方塊或清單方塊的擁有者。


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定傳送 **WM \_ COMPAREITEM** 訊息之控制項的識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

[**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct)結構的指標，其中包含組合或清單方塊中兩個專案的識別碼和應用程式提供的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值指出兩個專案的相對位置。 它可能是下表所示的任何值。



| 傳回碼                                                                          | Description                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**值**</dt> </dl> | 意義<br/>                                           |
| <dl> <dt>**-1**</dt> </dl>    | 專案1在專案2之前的排序次序。<br/>       |
| <dl> <dt>**0**</dt> </dl>     | 專案1和2在排序的順序中是相等的。<br/> |
| <dl> <dt>**1**</dt> </dl>     | 專案1會依照排序次序來追蹤專案2。<br/>        |



 

## <a name="remarks"></a>備註

當主控描繪下拉式方塊或清單方塊的擁有者收到此訊息時，擁有者會傳回值，指出 [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) 結構所指定的專案會出現在另一個專案之前。 一般而言，系統會傳送此訊息數次，直到它決定新專案的確切位置。

如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **布林** 值，並直接傳回值。 \_ [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 DWL MSGRESULT 值會被忽略。

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

[**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

**其他資源**
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 

