---
description: 每個 Windows Installer 功能都會使用一或多個 Windows Installer 元件，而功能可以共用元件。
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: 指定 Feature-Component 關聯性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1d7a79e35822d5a0ad67f43297ec461eb3c2fd766c946cc414a571c148de5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627868"
---
# <a name="specifying-feature-component-relationships"></a>指定 Feature-Component 關聯性

每個[Windows Installer 功能](windows-installer-features.md)都會使用一或多個[Windows Installer 元件](windows-installer-components.md)，而功能可以共用元件。 [FeatureComponents 資料表](featurecomponents-table.md)會定義功能和元件之間的關聯性。 請參閱 Windows Installer 總覽中的[核心資料表群組](core-tables-group.md)和[元件和功能](components-and-features.md)。 在本節中，您會將資訊新增至記事本範例的 FeatureComponents 資料表。

使用資料庫編輯器開啟 MNP2000.msi，並將下列資料輸入空白的 FeatureComponents 資料表中。

[FeatureComponents 資料表](featurecomponents-table.md)



| 特徵\_ | 元件\_ |
|-----------|-------------|
| 棒球  | 棒球    |
| 演唱會   | 演唱會     |
| 舞蹈     | 舞蹈       |
| 足球  | 足球    |
| 說明      | 說明        |
| 一月   | 一月     |
| NewYears  | NewYears    |
| [記事本]   | [記事本]     |
| 讀我檔案    | [記事本]     |



 

[繼續](adding-registry-information.md)

 

 



