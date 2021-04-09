---
title: 'CB_SETCURSEL 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETCURSEL 訊息，以選取下拉式方塊清單中的字串。
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- CB_SETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd130204e6dc8bb4166c21bc9c4d52950182c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025079"
---
# <a name="cb_setcursel-message"></a>CB \_ SETCURSEL 訊息

應用程式會傳送 **CB \_ SETCURSEL** 訊息，以選取下拉式方塊清單中的字串。 如有必要，清單會將字串滾動至 view。 下拉式方塊的編輯控制項中的文字會變更，以反映新的選取專案，並移除清單中的任何先前選取專案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定要選取之字串的以零為基底的索引。 如果此參數為-1，則會移除清單中目前的選取範圍，並清除編輯控制項。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值是所選取專案的索引。 如果 *wParam* 大於清單中的專案數，或 *wParam* 為-1，則傳回值為 CB \_ ERR，並且會清除選取專案。

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

[**CB \_ FINDSTRING**](cb-findstring.md)
</dt> <dt>

[**CB \_ GETCURSEL**](cb-getcursel.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> </dl>

 

 





