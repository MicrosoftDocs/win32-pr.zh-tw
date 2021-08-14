---
title: 'Windows觸控手勢常數 (Winuser) '
description: 此區段會列出 Windows Touch 手勢所使用的常數。
ms.assetid: C5C3C533-A781-47EF-8209-2D94A94C9097
topic_type:
- apiref
api_name:
- GESTURECONFIGMAXCOUNT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/18/2020
ms.openlocfilehash: 3e980619a4f0f2a0df83ebfbe2fb8e8a767ef5f988e2bb3b769bde64e714eb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435224"
---
# <a name="windows-touch-gestures-constants"></a>Windows觸控手勢常數

此區段會列出 Windows Touch 手勢所使用的常數。

<dl> <dt>

**GESTURECONFIGMAXCOUNT**
</dt> <dd> <dl> <dt>

256
</dt> <dt>

定義可以在 [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) 或 [**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig)的單一呼叫中包含的手勢設定的最大數目。

</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |

## <a name="see-also"></a>另請參閱

[**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig)、 [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)、 [Windows Touch 手勢](multi-touch-gestures.md)
