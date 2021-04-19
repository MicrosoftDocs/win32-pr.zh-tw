---
description: 家長監護 SKU 可用性
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: 家長監護 SKU 可用性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b858bc62e8f10a3b06313befd99d67e497b8d442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981554"
---
# <a name="parental-controls-sku-availability"></a>家長監護 SKU 可用性

本章節中所述的「家長監護」、「功能」和「Api」目前計畫僅適用于以取用者為焦點的 Sku，例如：

-   Windows Vista Starter
-   Windows Vista Home Basic
-   Windows Vista Home Premium
-   Windows Vista Ultimate

家長監護只會安裝在這些 Sku 上。 需要部署至商務 Sku 的解決方案必須：

-   偵測並不供應商務 Sku 的家長監護功能。
-   偵測並提供設定、記錄和限制的替代方法。

建議解決方案透過檢查合規性 API 上的 COM CoCreateInstance 是否成功，來偵測家長監護基礎結構的可用性。

以 Windows Vista 基礎結構為依據的可感知應用程式，也可能想要在支援的 SKU 上隱藏家長監護的 UI 時，隱藏任何自己的 UI 公開設定或其他功能。 為可見度判斷提供的函式，涵蓋已加入網域的隱藏專案。

 

 



