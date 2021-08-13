---
title: UI_PKEY_Label
description: 識別 UI \_ PKEY \_ 標籤屬性。
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13506d1609f915c2eab9824a3f5256383c5f2aecf73ed5787e3372f17b44b435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706429"
---
# <a name="ui_pkey_label"></a>UI \_ PKEY \_ 標籤

識別 UI \_ PKEY \_ 標籤屬性。

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>備註

UI \_ PKEY \_ 標籤是由應用程式用來查詢索引標籤、群組、按鈕、圖庫專案和其他功能區控制項的標籤文字。

> [!Note]  
> Windows 8 和更新版本：[應用程式功能表](windowsribbon-controls-applicationmenu.md)按鈕影像已變更為 label： **File**。 建議您不要使用 [檔案] 作為任何您自己的索引標籤的標籤。

 

屬性值是限制為任何字元序列（包括空白字元和分行符號字元）的字串。

> [!Note]  
> 使用通用字元集 (UCS) XML 字元參考 `&#xA;` 來指定分行符號。

 

不支援靠右對齊。

UI PKEY 標籤的最大長度 \_ \_ 為未系結。

如果命令是透過功能表項目公開，而且 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 或 UI \_ PKEY \_ 標籤的值包含前面加上連字號的字母，如下列範例所示，則會將這個字母視為使用者介面的快速鍵，以及功能區架構的鍵盤對應鍵。


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



若要在標籤中顯示 & 符號，請將特殊字元指定換成雙符號 (`&&`) ，如下列範例所示。


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源屬性](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**LabelTitle**](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[UI \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




