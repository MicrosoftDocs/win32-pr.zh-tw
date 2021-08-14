---
title: UI_PKEY_ItemsSource
description: 識別 UI \_ PKEY \_ ItemsSource 屬性。
ms.assetid: f5e99d2a-f50a-4932-ae77-581037cb9ac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017a3fc8f05c24c8d1996202b1db08a459f1a3747e3f787b521a70e6e3a25df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201566"
---
# <a name="ui_pkey_itemssource"></a>UI \_ PKEY \_ ItemsSource

識別 UI \_ PKEY \_ ItemsSource 屬性。

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>備註

\_ \_ 應用程式會使用 UI PKEY ItemsSource 來查詢資源庫控制項中的專案集合，例如快速存取工具列 (QAT) 。

屬性值是 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 物件。

此 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 中的每個專案都必須執行 [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) ，以公開與該專案相關聯的唯讀屬性，例如標籤或影像。

若要在執行時間加入或刪除資源庫控制項中的專案，請使用 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 方法。

下列螢幕擷取畫面說明 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 功能表中的專案集合。

![顯示功能區圖庫中類別的螢幕擷取畫面。](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[集合屬性](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 