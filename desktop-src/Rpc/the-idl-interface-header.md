---
title: IDL 介面標頭
description: IDL 介面標頭會指定整個介面的相關資訊。 不同于 ACF，介面標頭包含的屬性與平臺無關。
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c176078c370819331405b070ffa832384584a944b65fae771b9a2044a178e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924267"
---
# <a name="the-idl-interface-header"></a>IDL 介面標頭

IDL 介面標頭會指定整個介面的相關資訊。 不同于 ACF，介面標頭包含的屬性與平臺無關。

介面標頭中的屬性是整個介面的通用屬性。 亦即，它們會套用至介面及其所有部分。 這些屬性會以方括弧括住介面定義的開頭。 下列介面定義中會顯示一個範例：

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

請注意，介面標頭包含 **\[** [**uuid**](/windows/desktop/Midl/uuid) **\]** 和 **\[** [**version**](/windows/desktop/Midl/version) **\]** 屬性。 因為這些分別代表介面的 UUID 和版本號碼，所以它們是整個介面的屬性。

介面主體也可以包含屬性。 不過，它們並不適用于整個介面。 它們參考介面中的特定專案，例如遠端過程參數。

如需 IDL 標頭屬性的完整討論，請參閱 [MIDL 語言參考](/windows/desktop/Midl/midl-language-reference)。

 

 