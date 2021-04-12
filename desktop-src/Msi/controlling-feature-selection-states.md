---
description: 您可以藉由撰寫 Feature 資料表和元件表格，來控制可供使用者和應用程式選取的功能安裝選項。
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: 控制特徵選取狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadedf4b6038f8257d06671e0774afc258391898
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194948"
---
# <a name="controlling-feature-selection-states"></a>控制特徵選取狀態

您可以藉由撰寫 [feature 資料表](feature-table.md) 和 [元件表格](component-table.md)，來控制可供使用者和應用程式選取的功能安裝選項。

-   若要防止選取某項功能的公告狀態，請在 [功能資料表](feature-table.md)的 [屬性] 欄位中包含 **msidbFeatureAttributesDisallowAdvertise** 。
-   若要防止針對某個功能選取 [從來源執行] 或 [從網路執行] 狀態，請在 [元件資料表](component-table.md)的 [屬性] 欄位中，針對屬於該功能的每個元件包含 **msidbComponentAttributesLocalOnly** 。 如果某項功能沒有元件，則此功能一律會有從來源執行和可執行檔「我的電腦」選項。
-   若要防止選取某項功能的 [從我的電腦] 狀態，請在 [元件資料表](component-table.md)的 [屬性] 欄位中，針對屬於該功能的每個元件包含 **msidbComponentAttributesSourceOnly** 。 如果某項功能沒有元件，則此功能一律會有從來源執行和可執行檔「我的電腦」選項。
-   您可以在 [功能資料表](feature-table.md)的 [屬性] 欄位中包含 **msidbFeatureAttributesFollowParent** 和 **msidbFeatureAttributesUIDisallowAbsent** ，以撰寫新的子功能。

 

 



