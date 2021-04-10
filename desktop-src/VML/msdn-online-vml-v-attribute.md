---
title: VML V 屬性
description: VML V 屬性
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690518e998163f7e47fb326b3037e6a4ec397e8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092827"
---
# <a name="vml-v-attribute"></a><span data-ttu-id="f8cc4-103">VML V 屬性</span><span class="sxs-lookup"><span data-stu-id="f8cc4-103">VML V Attribute</span></span>

<span data-ttu-id="f8cc4-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="f8cc4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f8cc4-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="f8cc4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f8cc4-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="f8cc4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f8cc4-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="f8cc4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f8cc4-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="f8cc4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f8cc4-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="f8cc4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f8cc4-110">定義組成路徑的命令。</span><span class="sxs-lookup"><span data-stu-id="f8cc4-110">Defines the commands that make up a path.</span></span> <span data-ttu-id="f8cc4-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f8cc4-111">Read/write.</span></span> <span data-ttu-id="f8cc4-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="f8cc4-112">**String**.</span></span>

<span data-ttu-id="f8cc4-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="f8cc4-113">**Applies To**</span></span>

[<span data-ttu-id="f8cc4-114">路徑</span><span class="sxs-lookup"><span data-stu-id="f8cc4-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="f8cc4-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="f8cc4-115">**Tag Syntax**</span></span>

<span data-ttu-id="f8cc4-116"><v： *element* v = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="f8cc4-116"><v: *element* v=" *expression* "></span></span>

<span data-ttu-id="f8cc4-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="f8cc4-117">**Script Syntax**</span></span>

<span data-ttu-id="f8cc4-118">*元素* . v = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="f8cc4-118">*element* .v="*expression*"</span></span>

<span data-ttu-id="f8cc4-119">*運算式* =*元素*. v</span><span class="sxs-lookup"><span data-stu-id="f8cc4-119">*expression*=*element*.v</span></span>

<span data-ttu-id="f8cc4-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="f8cc4-120">**Remarks**</span></span>

<span data-ttu-id="f8cc4-121">覆寫圖形的 **Path** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f8cc4-121">Overrides the **Path** attribute of a shape.</span></span> <span data-ttu-id="f8cc4-122">座標可以是固定數位、相對值或公式的參考 (使用 "" 格式， @n 其中 n 是公式編號，例如，" @2 " 代表公式陣列中的第二個公式) 。</span><span class="sxs-lookup"><span data-stu-id="f8cc4-122">Coordinates can be fixed numbers, relative numbers, or references to formulas (by using the format of "@n" where n is a formula number; for example, "@2" refers to the second formula in the formula array).</span></span>

<span data-ttu-id="f8cc4-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="f8cc4-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="f8cc4-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="f8cc4-124">**Example**</span></span>

<span data-ttu-id="f8cc4-125">使用 **V** 屬性來建立矩形。</span><span class="sxs-lookup"><span data-stu-id="f8cc4-125">A rectangle is created using the **V** attribute.</span></span> <span data-ttu-id="f8cc4-126">請注意，在第一組以逗號分隔的座標之後，會使用小寫字母 L (**lineto** 命令) 。</span><span class="sxs-lookup"><span data-stu-id="f8cc4-126">Note that a lowercase letter L (**lineto** command) is used after the first set of comma-delimited coordinates.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 