---
title: 'Color2 屬性 (筆觸)  (VML) '
description: 'Color2 屬性 (筆觸)  (VML) '
ms.assetid: 60b8035e-9477-4f8b-817b-dd6c41bdfa79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d577843b7d65de4f6197beabc877c308cf00154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463468"
---
# <a name="color2-attribute-strokevml"></a><span data-ttu-id="31550-103">Color2 屬性 (筆觸)  (VML) </span><span class="sxs-lookup"><span data-stu-id="31550-103">Color2 Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="31550-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="31550-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="31550-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="31550-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="31550-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="31550-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="31550-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="31550-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="31550-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="31550-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="31550-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="31550-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="31550-110">定義筆觸的第二個色彩。</span><span class="sxs-lookup"><span data-stu-id="31550-110">Defines a second color for strokes.</span></span> <span data-ttu-id="31550-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="31550-111">Read/write.</span></span> <span data-ttu-id="31550-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="31550-112">**String**.</span></span>

<span data-ttu-id="31550-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="31550-113">**Applies To**</span></span>

[<span data-ttu-id="31550-114">中風</span><span class="sxs-lookup"><span data-stu-id="31550-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="31550-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="31550-115">**Tag Syntax**</span></span>

<span data-ttu-id="31550-116"><v： *element* color2 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="31550-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="31550-117">指令碼語法</span><span class="sxs-lookup"><span data-stu-id="31550-117">Script Syntax</span></span>

<span data-ttu-id="31550-118"> color2 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="31550-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="31550-119">*運算式* =\*\* color2</span><span class="sxs-lookup"><span data-stu-id="31550-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="31550-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="31550-120">**Remarks**</span></span>

<span data-ttu-id="31550-121">當筆觸的填滿類型為模式時，會使用第二個色彩。</span><span class="sxs-lookup"><span data-stu-id="31550-121">A second color is used when a stroke's fill type is a pattern.</span></span>

<span data-ttu-id="31550-122">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="31550-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="31550-123">**範例**</span><span class="sxs-lookup"><span data-stu-id="31550-123">**Example**</span></span>

<span data-ttu-id="31550-124">圖形的筆觸是一種模式填滿，其填滿是由來源影像所定義，但透明背景則是由第二個色彩定義。</span><span class="sxs-lookup"><span data-stu-id="31550-124">The shape's stroke is a pattern fill where the fill is defined by the source image but the transparent background is defined by the second color.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke filltype="pattern" width="5pt" src="cylinder.gif" color2="green"/>
   </v:shape>
```



 

 