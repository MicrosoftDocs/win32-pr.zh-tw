---
title: VML Limo 屬性
description: VML Limo 屬性
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364aebfc2384ac9e19c9dc5f2f0ae52f09228a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375441"
---
# <a name="vml-limo-attribute"></a><span data-ttu-id="a9b4d-103">VML Limo 屬性</span><span class="sxs-lookup"><span data-stu-id="a9b4d-103">VML Limo Attribute</span></span>

<span data-ttu-id="a9b4d-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="a9b4d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a9b4d-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="a9b4d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a9b4d-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="a9b4d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a9b4d-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="a9b4d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a9b4d-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="a9b4d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a9b4d-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="a9b4d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a9b4d-110">定義路徑上的延展點。</span><span class="sxs-lookup"><span data-stu-id="a9b4d-110">Defines a stretch point on the path.</span></span> <span data-ttu-id="a9b4d-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a9b4d-111">Read/write.</span></span> <span data-ttu-id="a9b4d-112">**Vector2D**。</span><span class="sxs-lookup"><span data-stu-id="a9b4d-112">**Vector2D**.</span></span>

<span data-ttu-id="a9b4d-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="a9b4d-113">**Applies To**</span></span>

[<span data-ttu-id="a9b4d-114">路徑</span><span class="sxs-lookup"><span data-stu-id="a9b4d-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="a9b4d-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="a9b4d-115">**Tag Syntax**</span></span>

<span data-ttu-id="a9b4d-116"><v： *element* limo = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a9b4d-116"><v: *element* limo=" *expression* "></span></span>

<span data-ttu-id="a9b4d-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="a9b4d-117">**Script Syntax**</span></span>

<span data-ttu-id="a9b4d-118"> limo = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="a9b4d-118">*element* .limo="*expression*"</span></span>

<span data-ttu-id="a9b4d-119">*運算式* =\*\* limo</span><span class="sxs-lookup"><span data-stu-id="a9b4d-119">*expression*=*element*.limo</span></span>

<span data-ttu-id="a9b4d-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="a9b4d-120">**Remarks**</span></span>

<span data-ttu-id="a9b4d-121">預設值為 "0 0"。</span><span class="sxs-lookup"><span data-stu-id="a9b4d-121">The default value is "0 0".</span></span> <span data-ttu-id="a9b4d-122">Limo 伸展是指圖形邊緣上的點，可定義圖形在圖形化編輯器中的位置和方式。</span><span class="sxs-lookup"><span data-stu-id="a9b4d-122">Limo stretches are points on a shape's edge that define where and how a shape may be stretched by a user in a graphical editor.</span></span>

<span data-ttu-id="a9b4d-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="a9b4d-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="a9b4d-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="a9b4d-124">**Example**</span></span>

<span data-ttu-id="a9b4d-125">Limo 延展點是定義于水平線的中間。</span><span class="sxs-lookup"><span data-stu-id="a9b4d-125">A limo stretch point is defined halfway along the horizontal line.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 