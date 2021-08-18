---
title: 'CB_GETITEMDATA 訊息 (Winuser .h) '
description: 應用程式會將 CB \_ GETITEMDATA 訊息傳送至下拉式方塊，以抓取與下拉式方塊中指定之專案相關聯的應用程式提供值。
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- CB_GETITEMDATA 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8427e666668303456d16c00ae460a608a51bc31cd59e0ee6fa6851031057695b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019926"
---
# <a name="cb_getitemdata-message"></a>CB \_ GETITEMDATA 訊息

應用程式會將 **CB \_ GETITEMDATA** 訊息傳送至下拉式方塊，以抓取與下拉式方塊中指定之專案相關聯的應用程式提供值。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

項目之以零起始的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是與專案相關聯的值。 如果發生錯誤，則為 CB \_ 錯誤。

如果專案是在建立時沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md)樣式的主控描繪下拉式方塊中，則傳回值是已將專案新增至下拉式方塊之 [**cb \_ ADDSTRING**](cb-addstring.md)或 [**cb \_ INSERTSTRING**](cb-insertstring.md)訊息的 *lParam* 參數中所包含的值。 如果未使用 **CBS \_ HASSTRINGS** 樣式，則傳回值是包含在 [**CB \_ SETITEMDATA**](cb-setitemdata.md)訊息中的 *lParam* 參數。

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

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> <dt>

[**CB \_ SETITEMDATA**](cb-setitemdata.md)
</dt> </dl>

 

 





