---
description: FeatureComponents 資料表會定義功能和元件之間的關聯性。 針對每個功能，此表格會列出構成該功能的所有元件。
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: FeatureComponents 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c93a7c020f179843916b063b48e2e4d19f7bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691791"
---
# <a name="featurecomponents-table"></a>FeatureComponents 資料表

FeatureComponents 資料表會定義功能和元件之間的關聯性。 針對每個功能，此表格會列出構成該功能的所有元件。

FeatureComponents 資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 功能\_   | [識別碼](identifier.md) | Y   | N        |
| 元件\_ | [識別碼](identifier.md) | Y   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_
</dt> <dd>

功能 [資料表](feature-table.md)第一個資料行中的外部索引鍵。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

[元件資料表](component-table.md)的第一個資料行中的外部索引鍵。

</dd> </dl>

## <a name="remarks"></a>備註

每項功能有1600個元件的最大限制。

元件可以由兩個以上的功能共用，也就是相同元件可由多項功能參考。

當執行 [PublishFeatures 動作](publishfeatures-action.md) 或 [UnpublishFeatures 動作](unpublishfeatures-action.md) 時，就會參考此資料表。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE21](ice21.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE47](ice47.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE69](ice69.md)  
</dl>

 

 



