---
title: 觸控點擊測試分數
description: 下列常數會識別物件的可能點擊測試分數（相對於與 touch contact 區域交集的其他物件）。
ms.assetid: EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_PROXIMITY_CLOSEST
- TOUCH_HIT_TESTING_PROXIMITY_FARTHEST
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: f6590e7d56c1c9d92f0ff20524b6e4222d8655b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508468"
---
# <a name="touch-hit-testing-scores"></a>觸控點擊測試分數

下列常數會識別物件的可能點擊測試分數（相對於與 touch contact 區域交集的其他物件）。

| 常數/值 | Description |
|---|---|
| **TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0      | 物件是最可能的目標。<br/>  |
| **TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF | 物件是最不可能的目標。<br/> |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 標頭<br/>                   | Winuser。h |
