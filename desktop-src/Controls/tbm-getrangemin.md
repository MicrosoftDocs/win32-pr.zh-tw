---
title: 'TBM_GETRANGEMIN 訊息 (Commctrl .h) '
description: 抓取捲軸中滑杆的最小位置。
ms.assetid: 64334aed-0403-4785-829e-693292734d10
keywords:
- TBM_GETRANGEMIN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b79cfcf589dcd246699e0eb79c30368a3cad0e72eb74a76528967d3a0683d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046538"
---
# <a name="tbm_getrangemin-message"></a>TBM \_ GETRANGEMIN 訊息

抓取捲軸中滑杆的最小位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回32位值，這個值會指定在最小至最大滑杆位置的最小值範圍中，最小位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**TBM \_ GETRANGEMAX**](tbm-getrangemax.md)
</dt> <dt>

[**TBM \_ SETRANGE**](tbm-setrange.md)
</dt> <dt>

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> </dl>

 

 





