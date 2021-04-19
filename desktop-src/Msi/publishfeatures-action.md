---
description: PublishFeatures 動作會將每個功能的狀態寫入系統登錄。
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: PublishFeatures 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5356ef89aa2651c470917a9b8d81b79ee83d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986921"
---
# <a name="publishfeatures-action"></a>PublishFeatures 動作

PublishFeatures 動作會將每個功能的狀態寫入系統登錄。 功能狀態可能是不存在、已公告或已安裝。 PublishFeatures 動作也會針對每個已安裝的功能，將功能元件對應寫入系統登錄。

PublishFeatures 動作會查詢 [FeatureComponents 資料表](featurecomponents-table.md)、 [功能資料表](feature-table.md)和 [元件資料表](component-table.md)。

## <a name="sequence-restrictions"></a>順序限制

PublishFeatures 動作必須在 [PublishProduct](publishproduct-action.md)之前。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述        |
|-------|-----------------------------------|
| \[1\] | 已公告功能的識別碼。 |



 

## <a name="remarks"></a>備註

PublishFeatures 動作會發佈所有已選取要公告或安裝的功能組合。

 

 



