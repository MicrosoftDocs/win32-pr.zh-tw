---
title: 'LB_SELITEMRANGEEX 訊息 (Winuser .h) '
description: 選取多重選取清單方塊中的一或多個連續專案。
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- LB_SELITEMRANGEEX message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa3ca1335372b7a61c4dfcbc379c36e89ff933e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934907"
---
# <a name="lb_selitemrangeex-message"></a>LB \_ SELITEMRANGEEX 訊息

選取多重選取清單方塊中的一或多個連續專案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定要選取之第一個專案的以零為基底的索引。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

指定要選取之最後一個專案的以零為基底的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果發生錯誤，傳回值為 LB \_ ERR。

## <a name="remarks"></a>備註

如果 *wParam* 參數小於 *lParam* 參數，則會選取指定的專案範圍。 如果 *wParam* 大於或等於 *lParam*，則範圍會從指定的專案範圍中移除。 若只要選取一個專案，請選取兩個專案，然後取消選取不想要的專案。

此訊息只能搭配多重選取清單方塊使用。

此訊息只能選取前65536個專案內的範圍。

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

[**LB \_ SELITEMRANGE**](lb-selitemrange.md)
</dt> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> </dl>

 

 





