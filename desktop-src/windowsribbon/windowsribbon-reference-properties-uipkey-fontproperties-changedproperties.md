---
title: UI_PKEY_FontProperties_ChangedProperties
description: 識別 UI \_ PKEY \_ FontProperties \_ ChangedProperties 屬性。
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124b36d5e24f4e0c0122cffdbbed11669a4ea510
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376220"
---
# <a name="ui_pkey_fontproperties_changedproperties"></a>UI \_ PKEY \_ FontProperties \_ ChangedProperties

識別 UI \_ PKEY \_ FontProperties \_ ChangedProperties 屬性。

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a>備註

UI \_ PKEY \_ FontProperties \_ ChangedProperties 是由應用程式用來查詢 [ui \_ PKEY \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md)中的已變更屬性。

在這個 [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)物件上呼叫 [**IUISimplePropertySet：： GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)方法會傳回 [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

UI \_ PKEY \_ FontProperties \_ ChangedProperties 會作為 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) 呼叫的最後一個參數傳遞至功能區主機應用程式。

這個屬性索引鍵是唯讀的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字型控制項屬性](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[字型控制項](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 