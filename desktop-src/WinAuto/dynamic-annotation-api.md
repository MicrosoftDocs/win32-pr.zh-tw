---
title: 動態注釋 API
description: 動態批註 API 是 Microsoft Active Accessibility 的延伸模組，可讓開發人員自訂現有的 IAccessible 支援，而不需要使用容易出錯的子類別化或包裝技術。
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7f73c1da79784fdd86652128b572fd81904023c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932588"
---
# <a name="dynamic-annotation-api"></a>動態注釋 API

動態批註 API 是 Microsoft Active Accessibility 的延伸模組，可讓開發人員自訂現有的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 支援，而不需要使用容易出錯的子類別化或包裝技術。 這種機制也可讓開發人員將提示或其他有用的資訊傳遞給 Oleacc.dll proxy。

動態注釋通常用來更正或修改現有 Oleacc.dll proxy 所公開的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件不正確的實例。 例如，您可以使用它來覆寫預設 proxy 所提供的 [**名稱**](name-property.md)和 [**角色**](role-property.md)屬性 [**，並提供**](help-property.md)描述和 [**說明**](description-property.md)屬性 (預設 proxy) 可能無法提供。

在 Windows 7 中，開發人員可以使用動態批註 API 來標注 Microsoft 消費者介面自動化屬性，以及 Oleacc.dll 為標準 Windows 控制項建立的 proxy 物件 Microsoft Active Accessibility 屬性。 Oleacc.dll 的 proxy 物件可同時為 Microsoft Active Accessibility 和消費者介面自動化用戶端提供服務。

## <a name="in-this-section"></a>本節內容

-   [背景資訊](background-information.md)
-   [動態注釋的替代方案](alternatives-to-dynamic-annotation.md)
-   [動態注釋的類型](types-of-dynamic-annotation.md)
-   [直接注釋](direct-annotation.md)
-   [值對應注釋](value-map-annotation.md)
-   [伺服器注釋](server-annotation.md)
-   [問題與限制](issues-and-limitations.md)

 

 




