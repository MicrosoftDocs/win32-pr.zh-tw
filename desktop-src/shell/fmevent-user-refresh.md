---
description: 當使用者從 [檔案管理員] 的 [View] 功能表選擇 [重新整理] 命令時，會傳送至擴充 DLL。 延伸模組可以使用此通知來更新其功能表。
title: 'FMEVENT_USER_REFRESH 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_USER_REFRESH
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b8fb4ce8-d284-4558-82a4-488d4d833bcb
ms.openlocfilehash: 9e2f514494ae8040c7bdb97f556555bd7f32794e4259300da240956ff6fcfe98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094143"
---
# <a name="fmevent_user_refresh-message"></a>FMEVENT \_ 使用者重新整理 \_ 訊息

當使用者從 [檔案管理員] 的 [ **View** ] 功能表選擇 [重新整理 **] 命令時，會** 傳送至擴充 DLL。 延伸模組可以使用此通知來更新其功能表。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果延伸模組 DLL 處理此訊息，則應該傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




