---
description: 智慧卡 Resource Manager
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: 智慧卡 Resource Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9d78b1d54a4db3fa8146b2689173c264e8320da024d0dc3e165dd648b8a33d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917507"
---
# <a name="smart-card-resource-manager"></a>智慧卡 Resource Manager

[*智慧卡*](../secgloss/s-gly.md)[*資源管理員*](../secgloss/r-gly.md)管理對 [*讀者*](../secgloss/r-gly.md)和 *智慧卡* 的存取。 為了管理這些資源，它會執行下列功能。

-   識別和追蹤資源。
-   跨多個應用程式分配讀取器和資源。
-   支援存取指定卡片上可用之服務的 [*交易*](../secgloss/t-gly.md) 基本專案。
    > [!Note]  
    > 這是很重要的一點，因為目前的卡片是單一執行緒裝置，通常需要執行多個命令才能完成單一函式。 [*交易*](../secgloss/t-gly.md) 可讓您在不中斷的情況下執行多個命令，以確保中繼 [*狀態*](../secgloss/s-gly.md) 資訊未損毀。

     

您可以透過 resource manager API 直接存取資源管理員，或透過任何智慧卡 [*服務提供者*](../secgloss/s-gly.md)間接存取資源管理員。

資源管理員 API 是一組 Windows 函式，可讓您直接存取 resource manager 的服務。 如需 api 所提供之 Windows 函式的總覽，請參閱[智慧卡 Resource Manager api](smart-card-resource-manager-api.md)。 相較之下，智慧卡服務提供者會使用 COM 介面。

資源管理員 API 中的許多 Windows 函式在智慧卡服務提供者的 COM 介面的屬性和方法中都有對等專案。 雖然大部分的應用程式開發人員會發現 COM 更容易使用，但有些應用程式仍然需要使用 Windows 函式來執行特定工作。 例如，需要操作 [*智慧卡資料庫*](../secgloss/s-gly.md)中讀取器或讀者群組清單的應用程式，以及需要直接控制讀取器的應用程式，都必須使用 RESOURCE manager API。 提供這些功能的服務僅適用于 Windows 函式，而不是服務提供者所提供的 COM。

如需有關如何在 Windows 中執行 [*資源管理員*](../secgloss/r-gly.md)的詳細資訊，請參閱 [Resource Manager 執行](resource-manager-implementation.md)。

 

 
