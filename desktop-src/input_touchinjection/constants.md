---
title: 觸控式插入常數
description: 本節提供觸控式插入常數的參考規格。
ms.assetid: 52941DF1-88AF-452B-BF3E-838ADBDBC9B2
topic_type:
- apiref
api_name:
- MAX_TOUCH_COUNT
- TOUCH_FEEDBACK_DEFAULT
- TOUCH_FEEDBACK_INDIRECT
- TOUCH_FEEDBACK_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: d86af0d67c48218e8cb3f5909b647ff59d8b0cdddddef24057e02521a7f253ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451738"
---
# <a name="touch-injection-constants"></a>觸控式插入常數

本節提供 [觸控式插入](touch-injection-portal.md) 常數的參考規格。

| 常數/值 | 描述 |
|---|---|
| **MAX_TOUCH_COUNT** 256                            | 指定同時連絡人的最大數目。<br/> |
| **TOUCH_FEEDBACK_DEFAULT** 0x1    | 指定預設觸控視覺效果。<br/>                |
| **TOUCH_FEEDBACK_INDIRECT** 0x2 | 指定間接觸控視覺效果。<br/>               |
| **TOUCH_FEEDBACK_NONE** 0x3             | 指定無觸控視覺效果。<br/>                     |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 8 \[僅限桌面應用程式\]                                           |
| 最低支援的伺服器 | Windows Server 2012 \[僅限桌面應用程式\]                                 |
| 標頭                   | Winuser。h |

## <a name="see-also"></a>另請參閱

[觸控式插入參考](touch-injection-reference.md)
