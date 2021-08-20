---
title: 保留模式與立即模式
description: 圖形 Api 可以分為保留模式 Api 和立即模式 Api。
ms.assetid: 0a98e8ee-4bc1-490c-867e-42bceae8a1f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42d981aafad39c8f8a1e9cd82a90c9b23ad83313822181caae01468465e92fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117993124"
---
# <a name="retained-mode-versus-immediate-mode"></a>保留模式與立即模式

圖形 Api 可以分為 *保留模式* api 和 *立即模式* api。 Direct2D 是立即模式的 API。 Windows Presentation Foundation (WPF) 是保留模式 API 的範例。

保留模式 API 是宣告式。 應用程式會從圖形基本專案（例如圖形和線條）來建立場景。 圖形程式庫會將場景的模型儲存在記憶體中。 為了繪製框架，圖形程式庫會將場景轉換成一組繪圖命令。 在框架之間，圖形程式庫會將場景保留在記憶體中。 為了變更轉譯的內容，應用程式會發出命令以更新場景，例如，加入或移除圖形。 然後，程式庫會負責重繪場景。

![顯示保留模式圖形的圖表。](images/graphics06.png)

立即模式 API 是程式性的。 每次繪製新的框架時，應用程式就會直接發出繪製命令。 圖形程式庫不會在畫面格之間儲存場景模型。 相反地，應用程式會持續追蹤場景。

![顯示立即模式圖形的圖表。](images/graphics07.png)

保留模式 Api 可能更容易使用，因為 API 會為您執行更多工作，例如初始化、狀態維護和清除。 另一方面，它們通常較不具彈性，因為 API 會有自己的場景模型。 此外，保留模式 API 可能具有較高的記憶體需求，因為它需要提供一般用途的場景模型。 使用立即模式 API，您可以執行目標優化。

## <a name="next"></a>下一個

[您的第一個 Direct2D 計畫](your-first-direct2d-program.md)

 

 




