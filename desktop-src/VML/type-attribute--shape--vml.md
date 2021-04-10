---
title: '類型屬性 (圖形)  (VML) '
description: '類型屬性 (圖形)  (VML) '
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e53b275d6b6327b3d3783704dbd06156e643f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023634"
---
# <a name="type-attribute-shapevml"></a><span data-ttu-id="be03a-103">類型屬性 (圖形)  (VML) </span><span class="sxs-lookup"><span data-stu-id="be03a-103">Type Attribute (Shape)(VML)</span></span>

<span data-ttu-id="be03a-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="be03a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="be03a-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="be03a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="be03a-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="be03a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="be03a-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="be03a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="be03a-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="be03a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="be03a-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="be03a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="be03a-110">定義 [ShapeType](msdn-online-vml-shapetype-element.md) 元素之識別碼的參考。</span><span class="sxs-lookup"><span data-stu-id="be03a-110">Defines a reference to the ID of a [ShapeType](msdn-online-vml-shapetype-element.md) element.</span></span> <span data-ttu-id="be03a-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="be03a-111">Read/write.</span></span> <span data-ttu-id="be03a-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="be03a-112">**String**.</span></span>

<span data-ttu-id="be03a-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="be03a-113">**Applies To**</span></span>

[<span data-ttu-id="be03a-114">形狀</span><span class="sxs-lookup"><span data-stu-id="be03a-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="be03a-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="be03a-115">**Tag Syntax**</span></span>

``` syntax
<v:
          element 
          type=" expression ">
```

<span data-ttu-id="be03a-116">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="be03a-116">**Script Syntax**</span></span>

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

<span data-ttu-id="be03a-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="be03a-117">**Remarks**</span></span>

<span data-ttu-id="be03a-118">如果 **Type** 屬性參考 **SHAPETYPE** 元素的識別碼，則會使用 **ShapeType** 的填滿、路徑和筆劃做為範本來建立圖形。</span><span class="sxs-lookup"><span data-stu-id="be03a-118">If the **Type** attribute references the ID of a **ShapeType** element, the fills, paths, and strokes of the **ShapeType** are used as templates to create the shape.</span></span> <span data-ttu-id="be03a-119">衍生自 **ShapeType** 的值可以由個別圖形值覆寫。</span><span class="sxs-lookup"><span data-stu-id="be03a-119">Values derived from **ShapeType** can be overridden by individual shape values.</span></span>

<span data-ttu-id="be03a-120">如果用於標記中，字串值的開頭必須是數位記號 (\#) 符號。</span><span class="sxs-lookup"><span data-stu-id="be03a-120">If used in tags, the string value must begin with a number sign (\#) symbol.</span></span>

<span data-ttu-id="be03a-121">**VML 標準屬性**</span><span class="sxs-lookup"><span data-stu-id="be03a-121">**VML Standard Attribute**</span></span>

<span data-ttu-id="be03a-122">**範例**</span><span class="sxs-lookup"><span data-stu-id="be03a-122">**Example**</span></span>

<span data-ttu-id="be03a-123">使用 "mytype" 做為識別碼來建立 **ShapeType** 圖形。</span><span class="sxs-lookup"><span data-stu-id="be03a-123">A **ShapeType** shape is created with the "mytype" as an ID.</span></span>


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



<span data-ttu-id="be03a-124">然後，如果您使用 **ShapeType** 值建立圖形，此圖形將會有 "Mytype" **ShapeType** 的屬性;亦即，"shape01" 會有藍色筆劃的紅色填滿。</span><span class="sxs-lookup"><span data-stu-id="be03a-124">Then if you create a shape using the **ShapeType** values, the shape will have the attributes of the "mytype" **ShapeType**; that is, "shape01" will have a red fill with a blue stroke.</span></span>


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



<span data-ttu-id="be03a-125">您可以覆寫繼承的值，例如，將色彩變更為綠色。</span><span class="sxs-lookup"><span data-stu-id="be03a-125">You can override the inherited values, for example, by changing the color to green.</span></span>


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



<span data-ttu-id="be03a-126">[Type 屬性範例](/previous-versions/bb264099(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="be03a-126">[Type Attribute Example](/previous-versions/bb264099(v=vs.85)).</span></span> <span data-ttu-id="be03a-127"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="be03a-127">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 