---
description: 動態存取控制 (DAC) 案例可針對企業檔案伺服器案例啟用集中式存取控制管理。
ms.assetid: 5A06B8D8-F14B-4D9E-9ED6-4246A26BF945
title: 集中式授權原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1e5798c477a69e80f325a35fd443df101a148c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945496"
---
# <a name="centralized-authorization-policy"></a>集中式授權原則

[動態存取控制 (DAC) 案例](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)可針對企業檔案伺服器案例啟用集中式存取控制管理。 大部分的組織都有多個區域，他們想要控制存取權。

範例包括：

-   控制機密資訊的存取，其中標示為機密的檔案會有特定許可權
-   控制存取包含個人識別資訊的檔案 (PII. ) 
-   根據組織的保留原則來限制對檔的存取。

提供數個新的授權原則抽象概念，可讓系統管理員集中定義這些原則，並允許個別定義和維護每個存取需求，但套用為一個原則，以簡化定義流程。

有兩個新的 Active Directory 原則物件： [集中授權原則](central-authorization-policies.md) (cap) 和 [集中授權原則規則](central-authorization-policy-rule.md) (capr) 是在 windows 8 中引進，可根據宣告和資源屬性的運算式來定義及套用集中式授權原則。 在使用這些物件時，系統管理員會將 capr 定義為特定的授權原則，以套用至具有特定屬性或符合特定適用性條件的資源。 例如，標示為「高度業務衝擊」的檔。 您可以針對可以表示的組織中每個所需的存取控制原則來定義 capes，而且可以識別其應套用的資源（就 windows 8 dac 運算式而言）。 端點是可在資源上一起套用的 caprs 集合。 下圖顯示帽和維德角的關聯性，以及在定義和套用這些物件至檔案資源時所牽涉到的概念步驟。 ![capes 和 cap 的關聯性](images/cap.png)

 

 
