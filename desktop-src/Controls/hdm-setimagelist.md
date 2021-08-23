---
title: 'HDM_SETIMAGELIST 訊息 (Commctrl .h) '
description: 將影像清單指派給現有的標題控制項。 您可以明確地傳送此訊息，或使用標頭 \_ SetImageList 或標頭 \_ SetStateImageList 宏。
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- HDM_SETIMAGELIST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2034a6880721914961b3bd75907df2e7b4e53360ccb3b10162f238068d85031d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435808"
---
# <a name="hdm_setimagelist-message"></a>HDM \_ SETIMAGELIST 訊息

將影像清單指派給現有的標題控制項。 您可以明確地傳送此訊息，或使用 [**標頭 \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) 或 [**標頭 \_ SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) 宏。

## <a name="parameters"></a>參數

<dl> <dt>*wParam*</dt> <dd>下列其中一個值：

| 值                                                                                                                                                      | 意義                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ 正常**</dt> </dl> | 表示這是一般的影像清單。<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**HDSIL \_ 狀態**</dt> </dl>    | 表示這是狀態影像清單。<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

影像清單的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

將控制碼傳回至先前與控制項相關聯的影像清單。 失敗時傳回 Null，如果先前未設定任何影像清單，則傳回 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





