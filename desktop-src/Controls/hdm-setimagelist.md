---
title: 'HDM_SETIMAGELIST 訊息 (Commctrl .h) '
description: 將影像清單指派給現有的標題控制項。 您可以明確地傳送此訊息，或使用標頭 \_ SetImageList 或標頭 \_ SetStateImageList 宏。
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- HDM_SETIMAGELIST message Windows 控制項
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
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934317"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





