---
title: 'LB_INITSTORAGE 訊息 (Winuser .h) '
description: 配置用來儲存清單方塊專案的記憶體。 在應用程式將大量專案加入清單方塊之前，會使用此訊息。
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- LB_INITSTORAGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe873244358bf171c3fcedc994facd36e194edf38e0ee0442f12556cc4342514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544268"
---
# <a name="lb_initstorage-message"></a>LB \_ INITSTORAGE 訊息

配置用來儲存清單方塊專案的記憶體。 在應用程式將大量專案加入清單方塊之前，會使用此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要加入的專案數目。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

要配置給專案字串的記憶體數量（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值會是已預先配置記憶體的專案總數，也就是所有成功 **LB \_ INITSTORAGE** 訊息新增的專案總數。

如果訊息失敗，則傳回值為 LB \_ ERRSPACE。

Microsoft Windows NT 4.0：此訊息不會配置指定的記憶體數量;但是，它一律會傳回在 *wParam* 參數中指定的值。

## <a name="remarks"></a>備註

**LB \_ INITSTORAGE** 訊息有助於加速初始化具有大量專案 (超過 100) 的清單方塊。 它會保留指定的記憶體數量，讓後續 [**的 \_ LB ADDSTRING**](lb-addstring.md)、 [**lb \_ INSERTSTRING**](lb-insertstring.md)、 [**lb \_ DIR**](lb-dir.md)和 [**LB \_ ADDFILE**](lb-addfile.md) 訊息都能以最短的時間進行。 您可以使用 *wParam* 和 *lParam* 參數的估計值。 如果您高估值，則會配置額外的記憶體;如果您低估了，一般配置會用於超出要求數量的專案。

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

[**LB \_ ADDFILE**](lb-addfile.md)
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ 目錄**](lb-dir.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> </dl>

 

 





