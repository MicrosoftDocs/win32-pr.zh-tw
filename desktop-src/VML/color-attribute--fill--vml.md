---
title: '色彩屬性 (填滿)  (的 VML) '
description: '色彩屬性 (填滿)  (的 VML) '
ms.assetid: 38e75bf5-4da9-4c58-af86-3554d03a6b7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480b3a013add36533a82b31338fba301e8353db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463197"
---
# <a name="color-attribute-fillvml"></a><span data-ttu-id="ea3a3-103">色彩屬性 (填滿)  (的 VML) </span><span class="sxs-lookup"><span data-stu-id="ea3a3-103">Color Attribute (Fill)(VML)</span></span>

<span data-ttu-id="ea3a3-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="ea3a3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ea3a3-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="ea3a3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ea3a3-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="ea3a3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ea3a3-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="ea3a3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ea3a3-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="ea3a3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ea3a3-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="ea3a3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ea3a3-110">定義填滿的色彩。</span><span class="sxs-lookup"><span data-stu-id="ea3a3-110">Defines the color of a fill.</span></span> <span data-ttu-id="ea3a3-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ea3a3-111">Read/write.</span></span> <span data-ttu-id="ea3a3-112">**VgColor**。</span><span class="sxs-lookup"><span data-stu-id="ea3a3-112">**VgColor**.</span></span>

<span data-ttu-id="ea3a3-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="ea3a3-113">**Applies To**</span></span>

[<span data-ttu-id="ea3a3-114">填滿</span><span class="sxs-lookup"><span data-stu-id="ea3a3-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="ea3a3-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="ea3a3-115">**Tag Syntax**</span></span>

<span data-ttu-id="ea3a3-116"><v： *element* color = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ea3a3-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="ea3a3-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="ea3a3-117">**Script Syntax**</span></span>

<span data-ttu-id="ea3a3-118">*element* 。 color = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ea3a3-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="ea3a3-119">*運算式* =*元素*。色彩</span><span class="sxs-lookup"><span data-stu-id="ea3a3-119">*expression*=*element*.color</span></span>

<span data-ttu-id="ea3a3-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="ea3a3-120">**Remarks**</span></span>

<span data-ttu-id="ea3a3-121">覆寫圖形的 **FillColor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ea3a3-121">Overrides the **FillColor** attribute of a shape.</span></span> <span data-ttu-id="ea3a3-122">預設值為 **白色**。</span><span class="sxs-lookup"><span data-stu-id="ea3a3-122">The default value is **White**.</span></span>

<span data-ttu-id="ea3a3-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="ea3a3-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="ea3a3-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="ea3a3-124">**Example**</span></span>

<span data-ttu-id="ea3a3-125">圖形的填滿色彩為綠色。</span><span class="sxs-lookup"><span data-stu-id="ea3a3-125">The fill color of the shape is green.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="green"/>
   </v:shape>
```



 

 