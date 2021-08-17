---
description: 家長監護 SKU 可用性
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: 家長監護 SKU 可用性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21184a383a28e3ae06198f203475c1c03334e5d678278bbb3b4988b52971e79e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461198"
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

根據 Windows Vista 基礎結構，可感知家長監護的應用程式可能也會想要在支援的 SKU 上隱藏家長監護的 ui 時，隱藏任何自己的 ui 公開設定或其他功能。 為可見度判斷提供的函式，涵蓋已加入網域的隱藏專案。

 

 



