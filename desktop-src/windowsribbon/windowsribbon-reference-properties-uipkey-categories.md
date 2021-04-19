---
title: UI_PKEY_Categories
description: 識別 UI \_ PKEY \_ 類別目錄屬性。
ms.assetid: 15f97307-ea3d-407a-a276-46b82f81bdbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7666ee9eba6639f1f39b96f012b464854191ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969113"
---
# <a name="ui_pkey_categories"></a><span data-ttu-id="b120b-103">UI \_ PKEY \_ 類別</span><span class="sxs-lookup"><span data-stu-id="b120b-103">UI\_PKEY\_Categories</span></span>

<span data-ttu-id="b120b-104">識別 UI \_ PKEY \_ 類別目錄屬性。</span><span class="sxs-lookup"><span data-stu-id="b120b-104">Identifies the UI\_PKEY\_Categories property.</span></span>

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a><span data-ttu-id="b120b-105">備註</span><span class="sxs-lookup"><span data-stu-id="b120b-105">Remarks</span></span>

<span data-ttu-id="b120b-106">\_ \_ 應用程式會使用 UI PKEY 類別來查詢用來將資源庫控制項中的相關專案分組的類別。</span><span class="sxs-lookup"><span data-stu-id="b120b-106">UI\_PKEY\_Categories is used by an application to query the categories that are used to group related items in a gallery control.</span></span>

<span data-ttu-id="b120b-107">屬性值是 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 物件，其中集合中的每個專案都代表一個類別目錄。</span><span class="sxs-lookup"><span data-stu-id="b120b-107">The property value is an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object where each item in the collection represents a category.</span></span>

<span data-ttu-id="b120b-108">此 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 中的每個專案都必須執行 [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) ，以公開與該專案相關聯的唯讀屬性，例如標籤或影像。</span><span class="sxs-lookup"><span data-stu-id="b120b-108">Each item in this [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) must implement [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) to expose the read-only properties associated with the item, such as the label or image.</span></span>

<span data-ttu-id="b120b-109">若要在執行時間加入或刪除資源庫控制項中的專案，請使用 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)的各種方法。</span><span class="sxs-lookup"><span data-stu-id="b120b-109">To add or delete items in a gallery control at run time, use the various methods of [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).</span></span>

<span data-ttu-id="b120b-110">下列螢幕擷取畫面說明如何在 [ [**SplitButton**](windowsribbon-element-splitbutton.md) ] 功能表中使用兩個類別目錄、**選取專案圖形** 和 **選擇選項**。</span><span class="sxs-lookup"><span data-stu-id="b120b-110">The following screen shot illustrates the use of two categories, **Selection shapes** and **Selection options**, in a [**SplitButton**](windowsribbon-element-splitbutton.md) menu.</span></span>

![在 splitbuttongallery 控制項中顯示兩個類別、選取專案圖形和選取選項的螢幕擷取畫面。](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a><span data-ttu-id="b120b-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="b120b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b120b-113">集合屬性</span><span class="sxs-lookup"><span data-stu-id="b120b-113">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[<span data-ttu-id="b120b-114">UI \_ PKEY \_ 類別</span><span class="sxs-lookup"><span data-stu-id="b120b-114">UI\_PKEY\_CategoryId</span></span>](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 