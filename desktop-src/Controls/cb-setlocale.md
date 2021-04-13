---
title: 'CB_SETLOCALE 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETLOCALE 訊息來設定下拉式方塊的目前地區設定。 如果下拉式方塊具有 CBS \_ 排序樣式，且使用 CB ADDSTRING 來新增字串 \_ ，則下拉式方塊的地區設定會影響清單專案的排序方式。
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- CB_SETLOCALE message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025f33dc8ba236965a98ca984446b04846ecd2ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465929"
---
# <a name="cb_setlocale-message"></a>CB \_ SETLOCALE 訊息

應用程式會傳送 **CB \_ SETLOCALE** 訊息來設定下拉式方塊的目前地區設定。 如果下拉式方塊具有 [**CBS \_ 排序**](combo-box-styles.md) 樣式，且使用 [**CB \_ ADDSTRING**](cb-addstring.md)來新增字串，則下拉式方塊的地區設定會影響清單專案的排序方式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定下拉式方塊的地區設定識別碼，以在加入文字時用來排序。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是先前的地區設定識別碼。 如果 *wParam* 指定系統上未安裝的地區設定，則傳回值為 CB \_ ERR，而且目前的下拉式列示方塊地區設定不會變更。

## <a name="remarks"></a>備註

使用 [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) 宏來建立地區設定識別碼，並使用 [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) 宏來建立語言識別項。 語言識別項是由主要語言識別項和子語言識別項所組成。

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

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ GETLOCALE**](cb-getlocale.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

