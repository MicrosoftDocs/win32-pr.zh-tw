---
title: 'Color 屬性 (Shadow)  (VML) '
description: 'Color 屬性 (Shadow)  (VML) '
ms.assetid: 677615b7-b4a4-411f-b04e-3ed0399f4c05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73df77e65a3ae0f74c6e79b9c179c31da27698f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967668"
---
# <a name="color-attribute-shadowvml"></a><span data-ttu-id="4c2ac-103">Color 屬性 (Shadow)  (VML) </span><span class="sxs-lookup"><span data-stu-id="4c2ac-103">Color Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="4c2ac-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4c2ac-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4c2ac-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4c2ac-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4c2ac-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4c2ac-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4c2ac-110">定義陰影的色彩。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-110">Defines the color of the shadow.</span></span> <span data-ttu-id="4c2ac-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4c2ac-111">Read/write.</span></span> <span data-ttu-id="4c2ac-112">**VgColor**。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-112">**VgColor**.</span></span>

<span data-ttu-id="4c2ac-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="4c2ac-113">**Applies To**</span></span>

[<span data-ttu-id="4c2ac-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="4c2ac-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="4c2ac-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="4c2ac-115">**Tag Syntax**</span></span>

<span data-ttu-id="4c2ac-116"><v： *element* color = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="4c2ac-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="4c2ac-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="4c2ac-117">**Script Syntax**</span></span>

<span data-ttu-id="4c2ac-118">*element* 。 color = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="4c2ac-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="4c2ac-119">*運算式* =*元素*。色彩</span><span class="sxs-lookup"><span data-stu-id="4c2ac-119">*expression*=*element*.color</span></span>

<span data-ttu-id="4c2ac-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="4c2ac-120">**Remarks**</span></span>

<span data-ttu-id="4c2ac-121">使用 color 屬性來設定或取得陰影的色彩。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-121">Use the color attribute to set or get the color of a shadow.</span></span>

<span data-ttu-id="4c2ac-122">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="4c2ac-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="4c2ac-123">**範例**</span><span class="sxs-lookup"><span data-stu-id="4c2ac-123">**Example**</span></span>

<span data-ttu-id="4c2ac-124">陰影為綠色。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-124">The shadow is green.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green"/>
   </v:shape>
```



 

 