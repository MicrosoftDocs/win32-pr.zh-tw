---
title: 'CB_GETCURSEL 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ GETCURSEL 訊息，以抓取下拉式方塊清單方塊中目前選取之專案的索引（如果有的話）。
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- CB_GETCURSEL 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bc51f43fd28563be4bc3f024bf6afd35c297648aa6c6cad677aca4582c3737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089258"
---
# <a name="cb_getcursel-message"></a>CB \_ GETCURSEL 訊息

應用程式會傳送 **CB \_ GETCURSEL** 訊息，以抓取下拉式方塊清單方塊中目前選取之專案的索引（如果有的話）。

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

傳回值是目前選取專案的以零為基底的索引。 如果未選取任何專案，則會是 CB \_ 錯誤。

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

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> </dl>

 

 





