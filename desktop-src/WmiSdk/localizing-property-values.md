---
description: CIM 架構當地語系化模型提供當地語系化限定詞的機制。 它不支援直接當地語系化屬性值。
ms.assetid: a88bd873-7132-45b6-831e-64f9bb254c6e
ms.tgt_platform: multiple
title: 當地語系化屬性值
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ccec714557934ca32a878e21fb2a75d24a211a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318935"
---
# <a name="localizing-property-values"></a>當地語系化屬性值

CIM 架構當地語系化模型提供當地語系化限定詞的機制。 它不支援直接當地語系化屬性值。

不過，在某些情況下，靜態實例中的字串屬性值可以由列舉整數型別取代，而且可以在類別定義中為屬性定義值對應。 在這些情況下，應該將 **值** 限定詞當地語系化。 使用列舉限定詞是當地語系化屬性值的主要機制。 不支援任何其他形式的屬性值當地語系化。

下列範例顯示如何使用部分值對應搭配正則運算式來當地語系化靜態屬性。 在此範例中，預先定義的值子集會使用靜態實例在架構中初始化。 其餘的值是動態提供的。

``` syntax
[abstract]
class DataGroup
{
   [key] string GUID;
   [Description("data group display name"): Amended,
                     ValueMap{"Logical Disk",
                     "CPU Utilization", ".+"}]
                     string GroupDisplayName;
   [ValueMap{"Monitors percentage of disk free space",
                  "Monitors percentage CPU utilization", ".+"}] 
                   string GroupDescription;
};

[static, Description ("pre-configured parameters") :amended]
class InitialGroup : DataGroup {
};

[dynamic, provider("HMProvider"),
    Description ("user-defined parameters") :amended]
class UserDefionedGroup : DataGroup {
};

instance of InitialGroup {
   GUID = "abc";
   GroupDisplayName = "Logical Disk";
   GroupDescription = "Monitors percentage of disk free space";
};

instance of InitialGroup {
   GUID = "def";
   GroupDisplayName = "CPU Utilization";
   GroupDescription = "Monitors percentage CPU utilization";
};
```

如需詳細資訊，請參閱 [當地語系化靜態屬性](localizing-static-properties.md)。

 

 



