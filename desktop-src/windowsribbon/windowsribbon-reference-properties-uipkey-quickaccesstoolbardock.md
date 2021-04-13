---
title: UI_PKEY_QuickAccessToolbarDock
description: 識別 UI \_ PKEY \_ QuickAccessToolbarDock 屬性。
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ae48cb9ef2ee665739de2f3aacab197b461665
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375480"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a>UI \_ PKEY \_ QuickAccessToolbarDock

識別 UI \_ PKEY \_ QuickAccessToolbarDock 屬性。

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a>備註

\_ \_ 應用程式會使用 UI PKEY QuickAccessToolbarDock 來查詢快速存取工具列 (QAT) 的停駐狀態。

屬性值來自 [**UI \_ CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) 列舉。



|                         |                                                                                                                                                                                                                                                       |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UI \_ CONTROLDOCK \_ TOP    | QAT 會停駐在功能區主機應用程式的非工作區中，如下列螢幕擷取畫面所示。![[快速存取] 工具列的螢幕擷取畫面，停駐在非工作區的功能區上方。](images/properties/qat-docktop.png)<br/> |
| UI \_ CONTROLDOCK \_ 底部 | QAT 會停駐為功能區下方的視覺化整數寬線，如下列螢幕擷取畫面所示。 ![快速存取工具列上停駐于功能區下方的螢幕擷取畫面。](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[功能區屬性](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

