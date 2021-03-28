---
description: 應用程式會使部分視窗失效，並使用 InvalidateRect 或 InvalidateRgn 函數來設定更新區域。
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: 使更新區域失效並進行驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba895875f9ec1350b6eb28ccb8f1721df6999ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972661"
---
# <a name="invalidating-and-validating-the-update-region"></a>使更新區域失效並進行驗證

應用程式會使部分視窗失效，並使用 [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) 或 [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) 函數來設定更新區域。 這些函式會將用戶端座標中的指定矩形或區域 (新增) 至更新區域，將矩形或區域與系統或應用程式先前新增至更新區域中的任何一項結合。

[**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect)和 [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn)函式不會產生 [**WM \_ 繪製**](wm-paint.md)訊息。 相反地，系統會累積這些函式所做的變更及其本身的變更，而視窗則會在其訊息佇列中處理其他訊息。 藉由累積變更，視窗會一次處理所有變更，而不是一次更新位和片段。

[**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect)和 [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn)函式會從更新區域中移除指定的矩形或區域，藉以驗證視窗的一部分。 這些函式通常是在視窗已更新更新區域中的特定螢幕部分，然後收到 [**WM \_ 油漆**](wm-paint.md) 訊息時使用。

 

 



