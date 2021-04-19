---
title: '函數 (觸控點擊測試) '
description: 本節中的主題提供觸控點擊測試功能的參考規格。
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- 使用者互動
- input
- 指標
- 觸控
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 03fcb4fb3fbe4f56e288703316f4b6e3ff02bba4
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "106996333"
---
# <a name="touch-hit-testing-functions"></a>觸控點擊測試功能

本節中的主題提供 [觸控點擊測試功能](functions.md)的參考規格。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
| --- | --- |
| [**EvaluateProximityToPolygon**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | 將多邊形的分數傳回為可能的觸控目標 (相較于與 touch contact 區域) 相交的其他所有多邊形，以及多邊形內的調整觸控點。 <br/> |
| [**EvaluateProximityToRect**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | 將矩形的分數傳回為可能的觸控目標，相較于所有其他與觸控連絡人區域相交的矩形，以及矩形內調整的觸控點。 <br/> |
| [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | 傳回接近的評估分數，以及調整的觸控點座標作為 [WM_TOUCHHITTESTING 訊息](../inputmsg/wm-touchhittesting.md) 回呼的封裝值。 <br/> |
| [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | 註冊視窗以處理 [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) 通知<br/> |

## <a name="related-topics"></a>相關主題

[觸控點擊測試參考](touchhittest-reference.md)
