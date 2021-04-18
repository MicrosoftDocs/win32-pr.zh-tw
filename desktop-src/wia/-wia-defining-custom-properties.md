---
description: 定義自訂屬性。
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: 定義自訂屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd91ee4d4e657ce0d6c01330d85e8df4ef57a36d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983504"
---
# <a name="defining-custom-properties"></a><span data-ttu-id="ba0a1-103">定義自訂屬性</span><span class="sxs-lookup"><span data-stu-id="ba0a1-103">Defining Custom Properties</span></span>

<span data-ttu-id="ba0a1-104">**定義自訂屬性**。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-104">**Defining Custom Properties**.</span></span>

<span data-ttu-id="ba0a1-105">如果 Windows 映像取得需要 (WIA) 迷你驅動程式來定義自訂屬性，則應該使用 [WIA \_ 私用 \_ DEVPROP] 屬性作為 [自訂根專案屬性]，而 [wia \_ 私用 \_ ITEMPROP] 屬性則應該用於其他專案屬性。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-105">If it is necessary for the Windows Image Acquisition (WIA) minidriver to define custom properties, the WIA\_PRIVATE\_DEVPROP property should be used for custom root item properties, and the WIA\_PRIVATE\_ITEMPROP" property should be used for other item properties.</span></span> <span data-ttu-id="ba0a1-106">這些常數定義于 *wiadef* 中。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-106">These constants are defined in *wiadef.h*.</span></span>

<span data-ttu-id="ba0a1-107">下列範例程式碼顯示三個根專案屬性的定義。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-107">The following example code shows definitions for three root item properties.</span></span> <span data-ttu-id="ba0a1-108">第一個自訂根項目屬性的屬性識別碼（自訂 \_ 根項目 \_ \_ 1）是根據 WIA 私用 \_ DEVPROP 所定義 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-108">The property ID for the first custom root item property, CUSTOM\_ROOT\_PROP\_1, is defined in terms of WIA\_PRIVATE\_DEVPROP.</span></span> <span data-ttu-id="ba0a1-109">其他根專案屬性的屬性識別碼是根據 WIA \_ 私用 \_ DEVPROP + 1、wia 私用 \_ \_ DEVPROP + 2 等專案來定義。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-109">Property IDs for additional root item properties are defined in terms of WIA\_PRIVATE\_DEVPROP + 1, WIA\_PRIVATE\_DEVPROP + 2, and so on.</span></span> <span data-ttu-id="ba0a1-110">如果需要額外的自訂根專案屬性，則可以繼續模式。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-110">The pattern can be continued if additional custom root item properties are needed.</span></span>


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



<span data-ttu-id="ba0a1-111">下一個範例會顯示三個自訂子專案屬性和屬性識別碼的定義。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-111">The next example shows definitions for three custom child item properties and property IDs.</span></span> <span data-ttu-id="ba0a1-112">第一個自訂子專案屬性的屬性識別碼（自訂子系屬性 \_ \_ \_ 1）是根據 WIA 私用 ITEMPROP 所定義 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-112">The property ID for the first custom child item property, CUSTOM\_CHILD\_PROP\_1, is defined in terms of WIA\_PRIVATE\_ITEMPROP.</span></span> <span data-ttu-id="ba0a1-113">其他子專案屬性的屬性識別碼是根據 WIA \_ 私用 ITEMPROP + 1 等專案來定義 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-113">Property IDs for additional child item properties are defined in terms of WIA\_PRIVATE\_ITEMPROP + 1, and so on.</span></span> <span data-ttu-id="ba0a1-114">如同之前，如果需要更多的自訂子專案屬性，就可以繼續模式。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-114">As before, the pattern can be continued if more of these custom child item properties are needed.</span></span>


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



<span data-ttu-id="ba0a1-115">自訂 WIA 屬性必須有與自訂屬性識別碼相關聯的自訂屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-115">Custom WIA properties must have custom property names that are associated with the custom property IDs.</span></span> <span data-ttu-id="ba0a1-116">下列範例程式碼顯示三個自訂根專案屬性名稱的定義。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-116">The following example code shows definitions for three custom root item property names.</span></span> <span data-ttu-id="ba0a1-117"> (這些屬性名稱會與上一個範例中所建立的自訂屬性識別碼搭配使用，其中自訂的根項目 1 STR 中包含的自訂屬性名稱 \_ \_ \_ \_ 會與自訂根專案屬性識別碼自訂根 \_ 元素1相關聯 \_ \_ 。 ) </span><span class="sxs-lookup"><span data-stu-id="ba0a1-117">(These property names are used with the custom property IDs that were created in a previous example, where the custom property name contained in CUSTOM\_ROOT\_PROP\_1\_STR is associated with the custom root item property ID CUSTOM\_ROOT\_PROP\_1.)</span></span>


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> <span data-ttu-id="ba0a1-118">WIA 屬性名稱 *不* 會以多種語言當地語系化。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-118">WIA property names are *not* localized in multiple languages.</span></span> <span data-ttu-id="ba0a1-119">這是因為使用屬性識別碼或屬性名稱的應用程式可以讀取 WIA 屬性。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-119">This is because WIA properties can be read by applications using the property ID or the property name.</span></span> <span data-ttu-id="ba0a1-120">如果使用名稱，則它必須是常數，就如同屬性識別碼一樣。</span><span class="sxs-lookup"><span data-stu-id="ba0a1-120">If the name is used, it must be a constant, just as the property ID is.</span></span>

 

 

 



