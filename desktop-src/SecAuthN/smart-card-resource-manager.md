---
description: 智慧卡 Resource Manager
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: 智慧卡 Resource Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3ee8e0bf311539863502d3e789544717e6dff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987718"
---
# <a name="smart-card-resource-manager"></a>智慧卡 Resource Manager

[*智慧卡*](../secgloss/s-gly.md)[*資源管理員*](../secgloss/r-gly.md)管理對 [*讀者*](../secgloss/r-gly.md)和 *智慧卡* 的存取。 為了管理這些資源，它會執行下列功能。

-   識別和追蹤資源。
-   跨多個應用程式分配讀取器和資源。
-   支援存取指定卡片上可用之服務的 [*交易*](../secgloss/t-gly.md) 基本專案。
    > [!Note]  
    > 這是很重要的一點，因為目前的卡片是單一執行緒裝置，通常需要執行多個命令才能完成單一函式。 [*交易*](../secgloss/t-gly.md) 可讓您在不中斷的情況下執行多個命令，以確保中繼 [*狀態*](../secgloss/s-gly.md) 資訊未損毀。

     

您可以透過 resource manager API 直接存取資源管理員，或透過任何智慧卡 [*服務提供者*](../secgloss/s-gly.md)間接存取資源管理員。

資源管理員 API 是一組 Windows 功能，可直接存取 resource manager 的服務。 如需 API 所提供的 Windows 函式總覽，請參閱 [智慧卡 RESOURCE MANAGER api](smart-card-resource-manager-api.md)。 相較之下，智慧卡服務提供者會使用 COM 介面。

資源管理員 API 中的許多 Windows 函式在智慧卡服務提供者的 COM 介面的屬性和方法中都有對等專案。 雖然大部分的應用程式開發人員會發現 COM 更容易使用，但有些應用程式仍然需要使用 Windows 功能來執行某些工作。 例如，需要操作 [*智慧卡資料庫*](../secgloss/s-gly.md)中讀取器或讀者群組清單的應用程式，以及需要直接控制讀取器的應用程式，都必須使用 RESOURCE manager API。 提供這些功能的服務僅適用于 Windows 函式，而不是在服務提供者提供的 COM 中。

如需有關如何在 Windows 中執行 [*資源管理員*](../secgloss/r-gly.md) 的詳細資訊，請參閱 [Resource Manager 執行](resource-manager-implementation.md)。

 

 
