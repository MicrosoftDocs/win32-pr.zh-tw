---
title: 'HDM_EDITFILTER 訊息 (Commctrl .h) '
description: 當篩選按鈕具有焦點時，將輸入焦點移至編輯方塊。
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- HDM_EDITFILTER 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- HDM_EDITFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8636c17bfa9043891e5037df79be9c72c1ddc8f3aa2b4d13520f4289205b5099
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006158"
---
# <a name="hdm_editfilter-message"></a>HDM \_ EDITFILTER 訊息

當篩選按鈕具有焦點時，將輸入焦點移至編輯方塊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

值，指定要編輯的資料行。

</dd> <dt>

*lParam* 
</dt> <dd>

指定如何處理使用者編輯變更的旗標。 使用此旗標來指定當使用者在傳送訊息時編輯篩選器的過程中，該怎麼辦。



| 值                                                                                                                                      | 意義                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt></dt><dt> **TRUE**</dt> </dl>  | 捨棄使用者所做的變更。 <br/> |
| <dl> <dt></dt><dt> **FALSE**</dt> </dl> | 接受使用者所做的變更。 <br/>  |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回整數。 **LRESULT** 會轉換為整數，表示 **TRUE** (1) 或 **FALSE** (0) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**HDM \_ CLEARFILTER**](hdm-clearfilter.md)
</dt> </dl>

 

 





