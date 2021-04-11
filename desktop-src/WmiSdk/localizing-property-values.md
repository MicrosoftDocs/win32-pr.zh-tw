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
# <a name="localizing-property-values"></a><span data-ttu-id="2b0d8-104">當地語系化屬性值</span><span class="sxs-lookup"><span data-stu-id="2b0d8-104">Localizing Property Values</span></span>

<span data-ttu-id="2b0d8-105">CIM 架構當地語系化模型提供當地語系化限定詞的機制。</span><span class="sxs-lookup"><span data-stu-id="2b0d8-105">The CIM schema localization model provides a mechanism for localizing qualifiers.</span></span> <span data-ttu-id="2b0d8-106">它不支援直接當地語系化屬性值。</span><span class="sxs-lookup"><span data-stu-id="2b0d8-106">It does not support direct localization of property values.</span></span>

<span data-ttu-id="2b0d8-107">不過，在某些情況下，靜態實例中的字串屬性值可以由列舉整數型別取代，而且可以在類別定義中為屬性定義值對應。</span><span class="sxs-lookup"><span data-stu-id="2b0d8-107">In some cases, however, the string properties values in the static instances can be replaced by an enumerated integer type and a value map can be defined for the property in the class definition.</span></span> <span data-ttu-id="2b0d8-108">在這些情況下，應該將 **值** 限定詞當地語系化。</span><span class="sxs-lookup"><span data-stu-id="2b0d8-108">In these cases, the **Values** qualifier should be localized.</span></span> <span data-ttu-id="2b0d8-109">使用列舉限定詞是當地語系化屬性值的主要機制。</span><span class="sxs-lookup"><span data-stu-id="2b0d8-109">Using enumeration qualifiers is the primary mechanism for localizing property values.</span></span> <span data-ttu-id="2b0d8-110">不支援任何其他形式的屬性值當地語系化。</span><span class="sxs-lookup"><span data-stu-id="2b0d8-110">Any other forms of property value localization are not supported.</span></span>

<span data-ttu-id="2b0d8-111">下列範例顯示如何使用部分值對應搭配正則運算式來當地語系化靜態屬性。</span><span class="sxs-lookup"><span data-stu-id="2b0d8-111">The following example shows how static properties can be localized using partial value maps with regular expressions.</span></span> <span data-ttu-id="2b0d8-112">在此範例中，預先定義的值子集會使用靜態實例在架構中初始化。</span><span class="sxs-lookup"><span data-stu-id="2b0d8-112">In this example, the predefined subset of values is initialized in the schema using static instances.</span></span> <span data-ttu-id="2b0d8-113">其餘的值是動態提供的。</span><span class="sxs-lookup"><span data-stu-id="2b0d8-113">The rest of the values are provided dynamically.</span></span>

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

<span data-ttu-id="2b0d8-114">如需詳細資訊，請參閱 [當地語系化靜態屬性](localizing-static-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="2b0d8-114">For more information, see [Localizing Static Properties](localizing-static-properties.md).</span></span>

 

 



