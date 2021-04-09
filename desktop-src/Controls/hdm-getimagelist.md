---
title: 'HDM_GETIMAGELIST 訊息 (Commctrl .h) '
description: 取得已針對現有標題控制項設定之影像清單的控制碼。 您可以明確地傳送此訊息，或使用標頭 \_ GetImageList 或標頭 \_ GetStateImageList 宏。
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- HDM_GETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e199d603af873f1957d33855ccf5c59a90a4002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686102"
---
# <a name="hdm_getimagelist-message"></a>HDM \_ GETIMAGELIST 訊息

取得已針對現有標題控制項設定之影像清單的控制碼。 您可以明確地傳送此訊息，或使用 [**標頭 \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) 或 [**標頭 \_ GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) 宏。

## <a name="parameters"></a>參數

<dl> <dt>*wParam*</dt> <dd>下列其中一個值：

| 值                                                                                                                                                      | 意義                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ 正常**</dt> </dl> | 表示這是一般的影像清單。<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**HDSIL \_ 狀態**</dt> </dl>    | 表示這是狀態影像清單。<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回標題控制項之影像清單集的控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





