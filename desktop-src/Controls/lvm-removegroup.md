---
title: 'LVM_REMOVEGROUP 訊息 (Commctrl .h) '
description: 從清單視圖控制項移除群組。
ms.assetid: c6f4f54c-4cf8-47d0-8e96-fa8a1df0501b
keywords:
- LVM_REMOVEGROUP 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_REMOVEGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c644a0367747ad63eb15a2b83a8df3078c1c89ca1c51875b178aa22d054de2b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062318"
---
# <a name="lvm_removegroup-message"></a>LVM \_ REMOVEGROUP 訊息

從清單視圖控制項移除群組。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>指定要移除之群組的識別碼。</dd> <dt>

*lParam* 
</dt> <dd>

必須是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回群組的索引，否則傳回-1。

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





