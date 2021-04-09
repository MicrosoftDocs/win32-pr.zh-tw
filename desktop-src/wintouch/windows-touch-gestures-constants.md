---
title: 'Windows Touch 筆勢常數 (Winuser) '
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
ms.openlocfilehash: be1d8fe9354c7160643dcefb2d35938453ad5b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934421"
---
# <a name="windows-touch-gestures-constants"></a>Windows Touch 手勢常數

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
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |

## <a name="see-also"></a>另請參閱

[**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig)、 [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)、 [Windows Touch 手勢](multi-touch-gestures.md)
