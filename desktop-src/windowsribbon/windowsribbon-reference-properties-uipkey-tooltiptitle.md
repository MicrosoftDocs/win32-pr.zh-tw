---
title: UI_PKEY_TooltipTitle
description: 識別 UI \_ PKEY \_ TooltipTitle 屬性。
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e62fe9ebdb6418f5790e0073e32e81d7f7aba75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969664"
---
# <a name="ui_pkey_tooltiptitle"></a>UI \_ PKEY \_ TooltipTitle

識別 UI \_ PKEY \_ TooltipTitle 屬性。

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>備註

\_ \_ 應用程式會使用 [UI PKEY TooltipTitle] 來查詢索引標籤、群組、按鈕、圖庫專案和其他功能區控制項的工具提示。

屬性值是限制為任何字元序列（包括空白字元和分行符號字元）的字串。

> [!Note]  
> 使用通用字元集 (UCS) XML 字元參考 `&#xA;` 來指定分行符號。

 

不支援靠右對齊。

UI PKEY TooltipTitle 的最大長度未系結 \_ \_ 。

若要在工具提示中顯示 & 符號，請將特殊字元指定以雙字元符號 (`&&`) ，如下列範例所示。


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源屬性](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




