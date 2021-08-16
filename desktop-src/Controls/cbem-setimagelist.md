---
title: 'CBEM_SETIMAGELIST 訊息 (Commctrl .h) '
description: 設定 ComboBoxEx 控制項的影像清單。
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- CBEM_SETIMAGELIST 訊息 Windows 控制項
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
ms.openlocfilehash: fbd83336d27bf8e47900554a6f3c36d2d767e5e8ddd4b8680b50050d87da79bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699258"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





