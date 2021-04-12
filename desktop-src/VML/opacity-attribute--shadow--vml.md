---
title: '不透明度屬性 (陰影)  (VML) '
description: '不透明度屬性 (陰影)  (VML) '
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d09ca038a187c4a4ed1f914f5d05bcfd63e4a4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375580"
---
# <a name="opacity-attribute-shadowvml"></a><span data-ttu-id="ef87c-103">不透明度屬性 (陰影)  (VML) </span><span class="sxs-lookup"><span data-stu-id="ef87c-103">Opacity Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="ef87c-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="ef87c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ef87c-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="ef87c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ef87c-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="ef87c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ef87c-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="ef87c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ef87c-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="ef87c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ef87c-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="ef87c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ef87c-110">決定陰影的透明度。</span><span class="sxs-lookup"><span data-stu-id="ef87c-110">Determines the transparency of a shadow.</span></span> <span data-ttu-id="ef87c-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ef87c-111">Read/write.</span></span> <span data-ttu-id="ef87c-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="ef87c-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span></span>

<span data-ttu-id="ef87c-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="ef87c-113">**Applies To**</span></span>

[<span data-ttu-id="ef87c-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="ef87c-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="ef87c-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="ef87c-115">**Tag Syntax**</span></span>

<span data-ttu-id="ef87c-116"><v： *element* opacity = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ef87c-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="ef87c-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="ef87c-117">**Script Syntax**</span></span>

<span data-ttu-id="ef87c-118">*元素* 。不透明度 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ef87c-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="ef87c-119">*運算式* =*元素*。不透明度</span><span class="sxs-lookup"><span data-stu-id="ef87c-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="ef87c-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="ef87c-120">**Remarks**</span></span>

<span data-ttu-id="ef87c-121">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="ef87c-121">The default value is 1.</span></span> <span data-ttu-id="ef87c-122">值為0會產生完全透明的陰影。</span><span class="sxs-lookup"><span data-stu-id="ef87c-122">A value of 0 will make a completely transparent shadow.</span></span>

<span data-ttu-id="ef87c-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="ef87c-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="ef87c-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="ef87c-124">**Example**</span></span>

<span data-ttu-id="ef87c-125">圖形的陰影有50% 的透明。</span><span class="sxs-lookup"><span data-stu-id="ef87c-125">The shape has a shadow that is 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 