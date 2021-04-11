---
title: VML FitPath 屬性
description: VML FitPath 屬性
ms.assetid: f15775ed-f7b7-45d9-83ed-e307daf7451b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1805e59a50c63248ed936f6a849869057a34a6e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186097"
---
# <a name="vml-fitpath-attribute"></a><span data-ttu-id="707a9-103">VML FitPath 屬性</span><span class="sxs-lookup"><span data-stu-id="707a9-103">VML FitPath Attribute</span></span>

<span data-ttu-id="707a9-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="707a9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="707a9-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="707a9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="707a9-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="707a9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="707a9-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="707a9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="707a9-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="707a9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="707a9-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="707a9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="707a9-110">定義文字是否符合圖形的路徑。</span><span class="sxs-lookup"><span data-stu-id="707a9-110">Defines whether the text fits the path of a shape.</span></span> <span data-ttu-id="707a9-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="707a9-111">Read/write.</span></span> <span data-ttu-id="707a9-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="707a9-112">**VgTriState**.</span></span>

<span data-ttu-id="707a9-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="707a9-113">**Applies To**</span></span>

[<span data-ttu-id="707a9-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="707a9-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="707a9-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="707a9-115">**Tag Syntax**</span></span>

<span data-ttu-id="707a9-116"><v： *element* fitpath = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="707a9-116"><v: *element* fitpath=" *expression* "></span></span>

<span data-ttu-id="707a9-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="707a9-117">**Script Syntax**</span></span>

<span data-ttu-id="707a9-118"> fitpath = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="707a9-118">*element* .fitpath="*expression*"</span></span>

<span data-ttu-id="707a9-119">*運算式* =\*\* fitpath</span><span class="sxs-lookup"><span data-stu-id="707a9-119">*expression*=*element*.fitpath</span></span>

<span data-ttu-id="707a9-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="707a9-120">**Remarks**</span></span>

<span data-ttu-id="707a9-121">若 **為 True**，則會調整文字大小以填滿其所在的路徑。</span><span class="sxs-lookup"><span data-stu-id="707a9-121">If **True**, sizes the text to fill the path it lies out on.</span></span> <span data-ttu-id="707a9-122">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="707a9-122">The default is **False**.</span></span>

<span data-ttu-id="707a9-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="707a9-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="707a9-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="707a9-124">**Example**</span></span>

<span data-ttu-id="707a9-125">文字會符合路徑。</span><span class="sxs-lookup"><span data-stu-id="707a9-125">The text will fit the path.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitpath="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 