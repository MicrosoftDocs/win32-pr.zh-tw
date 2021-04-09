---
title: 'EM_GETZOOM 訊息 (Richedit .h) '
description: 取得目前的縮放比例。 Zoom 比例一律介於1/64 到64之間。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: d4a1daee-4af7-44d1-80d6-0fcaaf3672a8
keywords:
- EM_GETZOOM message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a88aa96787e1fda5cdeb8f77f478a4d51635cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685606"
---
# <a name="em_getzoom-message"></a>EM \_ GETZOOM 訊息

取得多行編輯控制項或 rich edit 控制項的目前縮放比例。 Zoom 比例一律介於1/64 到64之間。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

接收縮放比例的分子。

</dd> <dt>

*lParam* 
</dt> <dd>

接收縮放比例的分母。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果處理訊息，訊息會傳回 TRUE，如果 *wParam* 和 *lParam* 都不是 **Null**，就會傳回 **TRUE** 。

## <a name="remarks"></a>備註

**編輯：** 在 Windows 10 1809 和更新版本中支援。 編輯控制項必須設定 **ES \_ EX \_ 可** 擴充樣式，此訊息才能有效果，請參閱 [編輯控制項延伸樣式](edit-control-window-extended-styles.md)。 如需編輯控制項的詳細資訊，請參閱 [編輯控制項](edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Rich Edit 3。0<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Richedit .h/Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETZOOM**](em-setzoom.md)
</dt> </dl>

 

 





