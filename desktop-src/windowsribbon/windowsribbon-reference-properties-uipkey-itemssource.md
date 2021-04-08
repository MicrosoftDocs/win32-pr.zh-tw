---
title: UI_PKEY_ItemsSource
description: 識別 UI \_ PKEY \_ ItemsSource 屬性。
ms.assetid: f5e99d2a-f50a-4932-ae77-581037cb9ac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bdc52a7688648f59be74c22516ee790d109dd2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682900"
---
# <a name="ui_pkey_itemssource"></a><span data-ttu-id="bba4e-103">UI \_ PKEY \_ ItemsSource</span><span class="sxs-lookup"><span data-stu-id="bba4e-103">UI\_PKEY\_ItemsSource</span></span>

<span data-ttu-id="bba4e-104">識別 UI \_ PKEY \_ ItemsSource 屬性。</span><span class="sxs-lookup"><span data-stu-id="bba4e-104">Identifies the UI\_PKEY\_ItemsSource property.</span></span>

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a><span data-ttu-id="bba4e-105">備註</span><span class="sxs-lookup"><span data-stu-id="bba4e-105">Remarks</span></span>

<span data-ttu-id="bba4e-106">\_ \_ 應用程式會使用 UI PKEY ItemsSource 來查詢資源庫控制項中的專案集合，例如快速存取工具列 (QAT) 。</span><span class="sxs-lookup"><span data-stu-id="bba4e-106">UI\_PKEY\_ItemsSource is used by an application to query the collection of items in a gallery control, such as the Quick Access Toolbar (QAT).</span></span>

<span data-ttu-id="bba4e-107">屬性值是 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 物件。</span><span class="sxs-lookup"><span data-stu-id="bba4e-107">The property value is an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="bba4e-108">此 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 中的每個專案都必須執行 [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) ，以公開與該專案相關聯的唯讀屬性，例如標籤或影像。</span><span class="sxs-lookup"><span data-stu-id="bba4e-108">Each item in this [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) must implement [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) to expose the read-only properties associated with the item, such as the label or image.</span></span>

<span data-ttu-id="bba4e-109">若要在執行時間加入或刪除資源庫控制項中的專案，請使用 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 方法。</span><span class="sxs-lookup"><span data-stu-id="bba4e-109">To add or delete items in a gallery control at run time, use the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) methods.</span></span>

<span data-ttu-id="bba4e-110">下列螢幕擷取畫面說明 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 功能表中的專案集合。</span><span class="sxs-lookup"><span data-stu-id="bba4e-110">The following screen shot illustrates a collection of items in a [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) menu.</span></span>

![顯示功能區圖庫中類別的螢幕擷取畫面。](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a><span data-ttu-id="bba4e-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="bba4e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bba4e-113">集合屬性</span><span class="sxs-lookup"><span data-stu-id="bba4e-113">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 