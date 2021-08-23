---
description: 每個合併模組中都需要空白的 FeatureComponents 資料表。 如果目標 .msi 檔案沒有自己的 FeatureComponents 資料表，則此空白資料表會提供合併工具的架構。
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: 撰寫合併模組 FeatureComponents 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b2da3e25d84f4f10edad6566edeba5a10d43c5617340d40c733aa23d31f4b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650297"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a>撰寫合併模組 FeatureComponents 資料表

每個合併模組中都需要空白的 [FeatureComponents 資料表](featurecomponents-table.md) 。 如果目標 .msi 檔案沒有自己的 FeatureComponents 資料表，則此空白資料表會提供合併工具的架構。

如果為，而且只有在，目標 .msi 檔案中沒有任何 FeatureComponents 資料表，則合併工具會使用模組中提供的空白資料表。 在此情況下，合併工具會在目標 .msi 檔案中建立重複的資料表，並將合併模組中的新元件與應用程式安裝套件中的功能建立關聯的資料列。

 

 



