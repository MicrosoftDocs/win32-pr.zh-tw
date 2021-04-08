---
title: VML TextPathOK 屬性
description: VML TextPathOK 屬性
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06046a4f29c147ef109f0e4670d9965bab77a9fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842340"
---
# <a name="vml-textpathok-attribute"></a><span data-ttu-id="e719d-103">VML TextPathOK 屬性</span><span class="sxs-lookup"><span data-stu-id="e719d-103">VML TextPathOK Attribute</span></span>

<span data-ttu-id="e719d-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="e719d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e719d-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="e719d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e719d-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="e719d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e719d-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="e719d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e719d-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="e719d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e719d-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="e719d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e719d-110">決定是否將顯示文字路徑。</span><span class="sxs-lookup"><span data-stu-id="e719d-110">Determines whether a text path will be displayed.</span></span> <span data-ttu-id="e719d-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e719d-111">Read/write.</span></span> <span data-ttu-id="e719d-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="e719d-112">**VgTriState**.</span></span>

<span data-ttu-id="e719d-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="e719d-113">**Applies To**</span></span>

[<span data-ttu-id="e719d-114">路徑</span><span class="sxs-lookup"><span data-stu-id="e719d-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="e719d-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="e719d-115">**Tag Syntax**</span></span>

<span data-ttu-id="e719d-116"><v： *element* textpathok = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="e719d-116"><v: *element* textpathok=" *expression* "></span></span>

<span data-ttu-id="e719d-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="e719d-117">**Script Syntax**</span></span>

<span data-ttu-id="e719d-118">*元素* 。</span><span class="sxs-lookup"><span data-stu-id="e719d-118">*element* .</span></span> <span data-ttu-id="e719d-119">textpathok = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="e719d-119">textpathok= "*expression*"</span></span>

<span data-ttu-id="e719d-120">*運算式* =*元素*。</span><span class="sxs-lookup"><span data-stu-id="e719d-120">*expression*=*element*.</span></span> <span data-ttu-id="e719d-121">textpathok</span><span class="sxs-lookup"><span data-stu-id="e719d-121">textpathok</span></span>

<span data-ttu-id="e719d-122">**備註**</span><span class="sxs-lookup"><span data-stu-id="e719d-122">**Remarks**</span></span>

<span data-ttu-id="e719d-123">如果 **為 False**，則表示路徑不能有文字路徑。</span><span class="sxs-lookup"><span data-stu-id="e719d-123">If **False**, the path cannot have a text path.</span></span> <span data-ttu-id="e719d-124">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="e719d-124">The default is **False**.</span></span> <span data-ttu-id="e719d-125">您必須將此屬性設定為 **True** ，才能在路徑上顯示文字。</span><span class="sxs-lookup"><span data-stu-id="e719d-125">You must have this attribute set to **True** to display text on a path.</span></span>

<span data-ttu-id="e719d-126">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="e719d-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="e719d-127">**範例**</span><span class="sxs-lookup"><span data-stu-id="e719d-127">**Example**</span></span>

<span data-ttu-id="e719d-128">圖形具有文字路徑。</span><span class="sxs-lookup"><span data-stu-id="e719d-128">The shape has a text path.</span></span> <span data-ttu-id="e719d-129">文字 "Hello VML" 會沿著笑臉狀曲線顯示。</span><span class="sxs-lookup"><span data-stu-id="e719d-129">The text "Hello VML" is displayed along a smile-shaped curve.</span></span>


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 