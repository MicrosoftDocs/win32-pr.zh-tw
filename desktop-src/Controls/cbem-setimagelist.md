---
title: 'CBEM_SETIMAGELIST 訊息 (Commctrl .h) '
description: 設定 ComboBoxEx 控制項的影像清單。
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- CBEM_SETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33816abe36e2d1e1593e6365061a500d072c155b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935017"
---
# <a name="cbem_setimagelist-message"></a>CBEM \_ SETIMAGELIST 訊息

設定 ComboBoxEx 控制項的影像清單。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

要為控制項設定之影像清單的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

將控制碼傳回至先前與控制項相關聯的影像清單，如果先前未設定任何影像清單，則傳回 **Null** 。

## <a name="remarks"></a>備註

> [!IMPORTANT]
> 影像清單中的影像高度可能會變更 ComboBoxEx 控制項的大小需求。 建議您在傳送此訊息之後調整控制項的大小，以確保顯示正確。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





