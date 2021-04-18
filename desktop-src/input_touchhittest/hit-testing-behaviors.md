---
title: 觸控點擊測試行為
description: 應用程式或 UI 架構會使用下列常數，來識別透過 RegisterTouchHitTestingWindow 函式註冊的 windows 如何處理觸控點擊測試的訊息。
ms.assetid: D1ECCBFA-CD01-401E-A42E-4F954F5F0A32
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965928"
---
# <a name="touch-hit-testing-behaviors"></a>觸控點擊測試行為

應用程式或 UI 架構會使用下列常數，來識別透過 [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) 函式註冊的 windows 如何處理觸控點擊測試的訊息。

| 常數/值 | Description |
|---|---|
| **TOUCH_HIT_TESTING_DEFAULT** </dt><dt>0 (0x0)  | 指出 [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) 的訊息不會傳送至目標視窗，而是傳送至子視窗。<br/> |
| **TOUCH_HIT_TESTING_CLIENT** </dt><dt>1 (0x1)     | 指出 [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) 的訊息會傳送至目標視窗。<br/>                                   |
| **TOUCH_HIT_TESTING_NONE** </dt><dt>2 (0x2)           | 指出 [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) 的訊息不會傳送至目標視窗或子視窗。<br/>              |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 標頭<br/>                   | <dl> <dt>Winuser。h |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[常數](constants.md)
