---
title: 'LB_SETCURSEL 訊息 (Winuser .h) '
description: 視需要選取字串並將它滾動至 view。 選取新的字串時，清單方塊會從先前選取的字串中移除反白顯示。
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- LB_SETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d1305ccece9c220d6a20e72e0ee54a428f8b13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106978599"
---
# <a name="lb_setcursel-message"></a>LB \_ SETCURSEL 訊息

視需要選取字串並將它滾動至 view。 選取新的字串時，清單方塊會從先前選取的字串中移除反白顯示。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定所選取之字串以零為起始的索引。 如果此參數為-1，則會將清單方塊設定為沒有選取專案。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果發生錯誤，傳回值為 LB \_ ERR。 如果 *wParam* 參數為-1，則 \_ 即使未發生任何錯誤，傳回值也會是 LB ERR。

## <a name="remarks"></a>備註

此訊息只適用于單一挑選清單框。 您無法使用它來設定或移除多重選取清單方塊中的選取專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ GETCURSEL**](lb-getcursel.md)
</dt> </dl>

 

 





