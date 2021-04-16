---
title: 'Title 屬性 (Shape)  (VML) '
description: 'Title 屬性 (Shape)  (VML) '
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075b1cf078617abd3486ba55008794e1342efa63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463664"
---
# <a name="title-attribute-shapevml"></a><span data-ttu-id="0deb6-103">Title 屬性 (Shape)  (VML) </span><span class="sxs-lookup"><span data-stu-id="0deb6-103">Title Attribute (Shape)(VML)</span></span>

<span data-ttu-id="0deb6-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="0deb6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0deb6-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="0deb6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0deb6-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="0deb6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0deb6-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="0deb6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0deb6-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="0deb6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0deb6-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="0deb6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0deb6-110">定義滑鼠指標移至圖形上方時所顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="0deb6-110">Defines the text displayed when the mouse pointer moves over the shape.</span></span> <span data-ttu-id="0deb6-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0deb6-111">Read/write.</span></span> <span data-ttu-id="0deb6-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="0deb6-112">**String**.</span></span>

<span data-ttu-id="0deb6-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="0deb6-113">**Applies To**</span></span>

[<span data-ttu-id="0deb6-114">形狀</span><span class="sxs-lookup"><span data-stu-id="0deb6-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="0deb6-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="0deb6-115">**Tag Syntax**</span></span>

<span data-ttu-id="0deb6-116"><v： *element* title = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="0deb6-116"><v: *element* title=" *expression* "></span></span>

<span data-ttu-id="0deb6-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="0deb6-117">**Script Syntax**</span></span>

<span data-ttu-id="0deb6-118">*element* 。 title = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="0deb6-118">*element* .title="*expression*"</span></span>

<span data-ttu-id="0deb6-119">*運算式* =*元素*。標題</span><span class="sxs-lookup"><span data-stu-id="0deb6-119">*expression*=*element*.title</span></span>

<span data-ttu-id="0deb6-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="0deb6-120">**Remarks**</span></span>

<span data-ttu-id="0deb6-121">**標題** 屬性類似于標準 HTML **標題** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0deb6-121">The **Title** attribute is similar to the standard HTML **Title** attribute.</span></span> <span data-ttu-id="0deb6-122">標題的行為類似于 Microsoft Windows 工具提示。</span><span class="sxs-lookup"><span data-stu-id="0deb6-122">The behavior of a title is similar to a Microsoft Windows ToolTip.</span></span>

<span data-ttu-id="0deb6-123">**VML 標準屬性**</span><span class="sxs-lookup"><span data-stu-id="0deb6-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="0deb6-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="0deb6-124">**Example**</span></span>

<span data-ttu-id="0deb6-125">圖形的標題是「工具提示顯示」，並會在滑鼠指標移至圖形上方時顯示。</span><span class="sxs-lookup"><span data-stu-id="0deb6-125">The title of the shape is "ToolTip display" and will appear when the mouse pointer moves over the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="0deb6-126">[Title 屬性範例](/previous-versions/bb264097(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0deb6-126">[Title Attribute Example](/previous-versions/bb264097(v=vs.85)).</span></span> <span data-ttu-id="0deb6-127"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="0deb6-127">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 