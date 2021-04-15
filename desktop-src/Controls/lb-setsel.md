---
title: 'LB_SETSEL 訊息 (Winuser .h) '
description: 在多重選取清單方塊中選取專案，並視需要將專案滾動至 [view]。
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- LB_SETSEL message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd50f12c4190ba9ecafad11b167c1ac60adf691d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466521"
---
# <a name="lb_setsel-message"></a>LB \_ SETSEL 訊息

在多重選取清單方塊中選取專案，並視需要將專案滾動至 [view]。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定如何設定選取專案。 如果此參數為 **TRUE**，則會選取並反白顯示專案;如果為 **FALSE**，則會移除反白顯示，且不會再選取專案。

</dd> <dt>

*lParam* 
</dt> <dd>

指定要設定之專案的以零為基底的索引。 如果此參數為-1，則會根據 *wParam* 的值，在所有專案中加入或移除選取範圍，且不會發生任何滾動。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果發生錯誤，傳回值為 LB \_ ERR。

## <a name="remarks"></a>備註

此訊息只能搭配多重選取清單方塊使用。

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

[**LB \_ GETSEL**](lb-getsel.md)
</dt> <dt>

[**LB \_ SELITEMRANGE**](lb-selitemrange.md)
</dt> </dl>

 

 





