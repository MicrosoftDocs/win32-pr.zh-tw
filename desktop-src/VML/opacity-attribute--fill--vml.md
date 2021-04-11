---
title: '不透明度屬性 (填滿)  (的 VML) '
description: '不透明度屬性 (填滿)  (的 VML) '
ms.assetid: abd2fe4d-6391-4413-80f0-549bcc74f42e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b913498705e65fa7211db4b4cef039894d573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683066"
---
# <a name="opacity-attribute-fillvml"></a><span data-ttu-id="dfc5e-103">不透明度屬性 (填滿)  (的 VML) </span><span class="sxs-lookup"><span data-stu-id="dfc5e-103">Opacity Attribute (Fill)(VML)</span></span>

<span data-ttu-id="dfc5e-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="dfc5e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="dfc5e-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="dfc5e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="dfc5e-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="dfc5e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="dfc5e-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="dfc5e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="dfc5e-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="dfc5e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="dfc5e-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="dfc5e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="dfc5e-110">定義填滿的透明度。</span><span class="sxs-lookup"><span data-stu-id="dfc5e-110">Defines the transparency of a fill.</span></span> <span data-ttu-id="dfc5e-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="dfc5e-111">Read/write.</span></span> <span data-ttu-id="dfc5e-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="dfc5e-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span>

<span data-ttu-id="dfc5e-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="dfc5e-113">**Applies To**</span></span>

[<span data-ttu-id="dfc5e-114">填滿</span><span class="sxs-lookup"><span data-stu-id="dfc5e-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="dfc5e-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="dfc5e-115">**Tag Syntax**</span></span>

<span data-ttu-id="dfc5e-116"><v： *element* opacity = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="dfc5e-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="dfc5e-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="dfc5e-117">**Script Syntax**</span></span>

<span data-ttu-id="dfc5e-118">*元素* 。不透明度 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="dfc5e-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="dfc5e-119">*運算式* =*元素*。不透明度</span><span class="sxs-lookup"><span data-stu-id="dfc5e-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="dfc5e-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="dfc5e-120">**Remarks**</span></span>

<span data-ttu-id="dfc5e-121">預設值為 1.0。</span><span class="sxs-lookup"><span data-stu-id="dfc5e-121">The default value is 1.0.</span></span>

<span data-ttu-id="dfc5e-122">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="dfc5e-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="dfc5e-123">**範例**</span><span class="sxs-lookup"><span data-stu-id="dfc5e-123">**Example**</span></span>

<span data-ttu-id="dfc5e-124">圖形填滿會是50% 的透明。</span><span class="sxs-lookup"><span data-stu-id="dfc5e-124">The fill of the shape will be 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill opacity="50%" color="red"/>
   </v:shape>
```



 

 