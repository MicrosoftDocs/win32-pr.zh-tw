---
description: 您可以使用 GetDC 函式來執行必須立即發生的繪圖，而不是在 \_ 處理 WM 油漆訊息時。
ms.assetid: 75525e26-72f5-4a58-a663-0bbdc2034759
title: 使用 GetDC 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c018228eccbce7b487444341481165e24214b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973060"
---
# <a name="using-the-getdc-function"></a>使用 GetDC 函式

您可以使用 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 函式來執行必須立即發生的繪圖，而不是在處理 [**WM \_ 油漆**](wm-paint.md) 訊息時。 這類繪圖通常是為了回應使用者的動作，例如使用滑鼠進行選取或繪製。 在這種情況下，使用者應該會收到立即的意見反應，而且不得強制停止選取或繪製，讓應用程式顯示結果。 下列各節說明如何使用 GetDC 在視窗中繪製：

-   [使用滑鼠繪圖](drawing-with-the-mouse.md)
-   [以計時間隔繪製](drawing-at-timed-intervals.md)

 

 



