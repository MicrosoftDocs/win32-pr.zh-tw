---
title: UI_PKEY_TooltipDescription
description: 識別 UI \_ PKEY \_ TooltipDescription 屬性。
ms.assetid: 658e798a-f41e-4538-94ac-38a9cb20dd74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900610c1302d3cc904dcde2d7c86801982fd4d10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968867"
---
# <a name="ui_pkey_tooltipdescription"></a>UI \_ PKEY \_ TooltipDescription

識別 UI \_ PKEY \_ TooltipDescription 屬性。

```
propertyDescription
   name = UI_PKEY_TooltipDescription
   shellPKey = UI_PKEY_TooltipDescription
   formatID = 00000005-7363-696e-8441798acf5aebb7
   propID = 5
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>備註

\_ \_ 應用程式會使用 ui PKEY TooltipDescription 來查詢與[UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)相關聯的描述。

屬性值是限制為任何字元序列（包括空白字元和分行符號字元）的字串。

> [!Note]  
> 使用通用字元集 (UCS) XML 字元參考 `&#xA;` 來指定分行符號。

 

UI PKEY TooltipDescription 的最大長度未系結 \_ \_ 。

不支援靠右對齊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源屬性](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)
</dt> <dt>

[UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 




