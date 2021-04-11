---
title: VML Master 屬性
description: VML Master 屬性
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d6c34fe49c107ed7ee1b4c1fb90d31bb07f17a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093275"
---
# <a name="vml-master-attribute"></a><span data-ttu-id="954cf-103">VML Master 屬性</span><span class="sxs-lookup"><span data-stu-id="954cf-103">VML Master Attribute</span></span>

<span data-ttu-id="954cf-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="954cf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="954cf-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="954cf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="954cf-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="954cf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="954cf-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="954cf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="954cf-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="954cf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="954cf-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="954cf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="954cf-110">判斷 **ShapeType** 元素是否為主要元素。</span><span class="sxs-lookup"><span data-stu-id="954cf-110">Determines whether a **ShapeType** element is a master element.</span></span> <span data-ttu-id="954cf-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="954cf-111">Read/write.</span></span> <span data-ttu-id="954cf-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="954cf-112">**VgTriState**.</span></span>

<span data-ttu-id="954cf-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="954cf-113">**Applies To**</span></span>

[<span data-ttu-id="954cf-114">ShapeType</span><span class="sxs-lookup"><span data-stu-id="954cf-114">ShapeType</span></span>](msdn-online-vml-shapetype-element.md)

<span data-ttu-id="954cf-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="954cf-115">**Tag Syntax**</span></span>

<span data-ttu-id="954cf-116"><v： *element* o:master = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="954cf-116"><v: *element* o:master=" *expression* "></span></span>

<span data-ttu-id="954cf-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="954cf-117">**Remarks**</span></span>

<span data-ttu-id="954cf-118">若 **為 True**，表示 **ShapeType** 圖形是由轉譯引擎轉譯。</span><span class="sxs-lookup"><span data-stu-id="954cf-118">If **True**, the **ShapeType** shape is rendered by the rendering engine.</span></span> <span data-ttu-id="954cf-119">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="954cf-119">The default value is **False**.</span></span>

<span data-ttu-id="954cf-120">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="954cf-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="954cf-121">**範例**</span><span class="sxs-lookup"><span data-stu-id="954cf-121">**Example**</span></span>

<span data-ttu-id="954cf-122">**ShapeType** 元素是主要圖形。</span><span class="sxs-lookup"><span data-stu-id="954cf-122">The **ShapeType** element is a master shape.</span></span>


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 