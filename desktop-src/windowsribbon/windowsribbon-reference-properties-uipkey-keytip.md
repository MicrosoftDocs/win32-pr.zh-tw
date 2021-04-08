---
title: UI_PKEY_Keytip
description: 識別 UI \_ PKEY \_ Keytip 屬性。
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550bfac9b341d14b495c73e4426e8143d91d8e19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932281"
---
# <a name="ui_pkey_keytip"></a>UI \_ PKEY \_ 按鍵提示

識別 UI \_ PKEY \_ Keytip 屬性。

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>備註

\_ \_ 應用程式會使用 UI PKEY 快捷方式來查詢功能區控制項的鍵盤快速鍵。

這個屬性值是字串，由任何字元序列組成，包括空白字元。

\_ \_ 除非透過功能表項目公開命令，否則 UI PKEY Keytip 的值會當做命令的鍵盤快速鍵。 在此情況下，架構會忽略 UI \_ PKEY \_ Keytip 值，並改為使用 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 或 [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)所指定的字元前面加上連字號。 如果未指定 **LabelTitle** 或 UI \_ PKEY 標籤的連字號 \_ ，則不會公開任何快捷方式或鍵盤快速鍵。

UI PKEY Keytip 的最大長度是無限制的 \_ \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源屬性](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**命令。快速鍵**](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




