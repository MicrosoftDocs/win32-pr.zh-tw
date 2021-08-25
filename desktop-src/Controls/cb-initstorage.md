---
title: 'CB_INITSTORAGE 訊息 (Winuser .h) '
description: 應用程式會先傳送 CB \_ INITSTORAGE 訊息，然後再將大量專案新增至下拉式方塊的清單方塊部分。 這則訊息會配置記憶體來儲存清單方塊專案。
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- CB_INITSTORAGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be1aeccdde2c81c87956a42e72440732ff9eb2732cbd066f51308816c01f64a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089088"
---
# <a name="cb_initstorage-message"></a>CB \_ INITSTORAGE 訊息

應用程式會先傳送 **CB \_ INITSTORAGE** 訊息，然後再將大量專案新增至下拉式方塊的清單方塊部分。 這則訊息會配置記憶體來儲存清單方塊專案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要加入的專案數目。

</dd> <dt>

*lParam* 
</dt> <dd>

要配置給專案字串的記憶體數量（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，傳回值就是已預先配置記憶體的專案總數，也就是所有成功的 **CB \_ INITSTORAGE** 訊息新增的專案總數。

如果訊息失敗，則傳回值為 CB \_ ERRSPACE。

此訊息會配置記憶體，並傳回上述的成功和錯誤值。

## <a name="remarks"></a>備註

**CB \_ INITSTORAGE** 訊息可協助加速初始化具有大量專案 (超過 100) 的下拉式方塊。 它會保留指定的記憶體數量，讓後續的 [**CB \_ ADDSTRING**](cb-addstring.md)、 [**cb \_ INSERTSTRING**](cb-insertstring.md)和 [**CB \_ DIR**](cb-dir.md) 訊息能以最短的時間進行。 您可以使用 *wParam* 和 *lParam* 參數的估計值。 如果您高估值，系統會配置額外的記憶體，如果低估了，則會將一般配置用於超出要求數量的專案。

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

[**CB \_ 目錄**](cb-dir.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> </dl>

 

 





