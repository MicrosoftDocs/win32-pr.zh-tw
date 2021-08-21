---
title: UI_PKEY_LabelDescription
description: 識別 UI \_ PKEY \_ LabelDescription 屬性。
ms.assetid: e7dfbe7e-c9c9-44fe-9e2d-39e20f5f7062
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80a2db487988f66fcc393b3ba449dfda789248dabc3cd9e1d3e48acf9ba3473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437993"
---
# <a name="ui_pkey_labeldescription"></a>UI \_ PKEY \_ LabelDescription

識別 UI \_ PKEY \_ LabelDescription 屬性。

```
propertyDescription
   name = UI_PKEY_LabelDescription
   shellPKey = UI_PKEY_LabelDescription
   formatID = 00000002-7363-696e-8441798acf5aebb7
   propID = 2
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>備註

\_ \_ 應用程式會使用 ui PKEY LabelDescription 來查詢與[UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)相關聯的描述。

屬性值是限制為任何字元序列（包括空白字元和分行符號字元）的字串。

> [!Note]  
> 使用通用字元集 (UCS) XML 字元參考 `&#xA;` 來指定分行符號。

 

長度上限為未系結。

不支援靠右對齊。

下列螢幕擷取畫面說明如何在應用程式功能表中使用標籤和相關聯的標籤描述。

![螢幕擷取畫面：顯示應用程式功能表中的標籤和相關聯的標籤描述。](images/properties/ui-pkey-labeldescription.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源屬性](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**LabelDescription**](windowsribbon-element-command-labeldescription.md)
</dt> <dt>

[UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 




