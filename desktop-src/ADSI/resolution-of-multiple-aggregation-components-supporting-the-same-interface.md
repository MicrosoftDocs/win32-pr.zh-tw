---
title: 支援相同介面的多個匯總元件的解析
description: 這種情況很罕見，這兩個延伸模組會對 ADSI 公開相同的介面。
ms.assetid: 87cb1a17-04f7-4ad0-989a-a9506dfdca05
ms.tgt_platform: multiple
keywords:
- 多個支援相同介面 ADSI 之匯總元件的解析
- 多個支援相同介面 ADSI 之匯總元件的解析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f58b7b606a05543444a172e2f76b436f6048431
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967596"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a>支援相同介面的多個匯總元件的解析

這種情況很罕見，這兩個延伸模組會對 ADSI 公開相同的介面。 如果發生這種情況，則適用下列規則：

-   如果匯總工具 (ADSI) 和任何擴充物件都支援介面（例如 **IMyInterface**），則 **QueryInterface** 一律會傳回 **IMyInterface** for adsi。
-   如果匯總工具 (ADSI) 不支援介面（例如 **IMyInterface**），但有一個以上的擴充物件支援， **QueryInterface** 會傳回登錄中所列的第一個擴充物件的 **IMyInterface** ，以支援該介面。

請注意，登錄中的元件順序也會影響自動化中名稱衝突的解析。 如需詳細資訊，請參閱 [擴充功能的自動化中的函數/屬性名稱衝突的解決方式](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)。

 

 




