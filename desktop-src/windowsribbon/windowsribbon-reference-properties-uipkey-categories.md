---
title: UI_PKEY_Categories
description: 識別 UI \_ PKEY \_ 類別目錄屬性。
ms.assetid: 15f97307-ea3d-407a-a276-46b82f81bdbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4aa812673f289b80b000710dd48a449656368f00d0beb51dcb489e60328e6a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086543"
---
# <a name="ui_pkey_categories"></a>UI \_ PKEY \_ 類別

識別 UI \_ PKEY \_ 類別目錄屬性。

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>備註

\_ \_ 應用程式會使用 UI PKEY 類別來查詢用來將資源庫控制項中的相關專案分組的類別。

屬性值是 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 物件，其中集合中的每個專案都代表一個類別目錄。

此 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 中的每個專案都必須執行 [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) ，以公開與該專案相關聯的唯讀屬性，例如標籤或影像。

若要在執行時間加入或刪除資源庫控制項中的專案，請使用 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)的各種方法。

下列螢幕擷取畫面說明如何在 [ [**SplitButton**](windowsribbon-element-splitbutton.md) ] 功能表中使用兩個類別目錄、**選取專案圖形** 和 **選擇選項**。

![在 splitbuttongallery 控制項中顯示兩個類別、選取專案圖形和選取選項的螢幕擷取畫面。](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[集合屬性](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[UI \_ PKEY \_ 類別](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 