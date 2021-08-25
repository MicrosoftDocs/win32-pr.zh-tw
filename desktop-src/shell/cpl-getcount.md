---
description: 傳送至主控台應用程式的 CPlApplet 函式，以取得應用程式所支援的對話方塊數目。
title: 'CPL_GETCOUNT 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6b88b56c-aad7-4144-ab95-15d7eef21861
api_name:
- CPL_GETCOUNT
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58f95a62d17ccafd308666a5632a1f7a42ebfda6ca0a54dfb6dfa9d9eda9b684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715478"
---
# <a name="cpl_getcount-message"></a>CPL \_ GETCOUNT 訊息

傳送至主控台應用程式的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式，以取得應用程式所支援的對話方塊數目。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

[**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc)函式會傳回主控台應用程式所支援的對話方塊數目。

## <a name="remarks"></a>備註

這則訊息會緊接在 [**CPL \_ 初始**](cpl-init.md) 訊息之後傳送。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Cpl。h</dt> </dl> |



 

 
