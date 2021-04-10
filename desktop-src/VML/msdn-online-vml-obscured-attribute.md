---
title: VML 遮蔽屬性
description: VML 遮蔽屬性
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e383061d3210c9c52dc8c89322bd617257555e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023680"
---
# <a name="vml-obscured-attribute"></a><span data-ttu-id="58a26-103">VML 遮蔽屬性</span><span class="sxs-lookup"><span data-stu-id="58a26-103">VML Obscured Attribute</span></span>

<span data-ttu-id="58a26-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="58a26-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="58a26-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="58a26-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="58a26-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="58a26-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="58a26-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="58a26-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="58a26-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="58a26-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="58a26-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="58a26-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="58a26-110">判斷陰影是否透明。</span><span class="sxs-lookup"><span data-stu-id="58a26-110">Determines whether a shadow is transparent.</span></span> <span data-ttu-id="58a26-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="58a26-111">Read/write.</span></span> <span data-ttu-id="58a26-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="58a26-112">**VgTriState**.</span></span>

<span data-ttu-id="58a26-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="58a26-113">**Applies To**</span></span>

[<span data-ttu-id="58a26-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="58a26-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="58a26-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="58a26-115">**Tag Syntax**</span></span>

<span data-ttu-id="58a26-116"><v： *element* 遮蔽 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="58a26-116"><v: *element* obscured=" *expression* "></span></span>

<span data-ttu-id="58a26-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="58a26-117">**Script Syntax**</span></span>

<span data-ttu-id="58a26-118">*元素* 。遮蔽 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="58a26-118">*element* .obscured="*expression*"</span></span>

<span data-ttu-id="58a26-119">*運算式* =*元素*。遮蔽</span><span class="sxs-lookup"><span data-stu-id="58a26-119">*expression*=*element*.obscured</span></span>

<span data-ttu-id="58a26-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="58a26-120">**Remarks**</span></span>

<span data-ttu-id="58a26-121">若 **為 True**，可讓您在圖形沒有填滿時，透過陰影查看。</span><span class="sxs-lookup"><span data-stu-id="58a26-121">If **True**, lets you see through the shadow if there is no fill on the shape.</span></span> <span data-ttu-id="58a26-122">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="58a26-122">Default is **False**.</span></span>

<span data-ttu-id="58a26-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="58a26-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="58a26-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="58a26-124">**Example**</span></span>

<span data-ttu-id="58a26-125">背景會透過陰影顯示。</span><span class="sxs-lookup"><span data-stu-id="58a26-125">The background shows through the shadow.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" obscured="True"/>
   </v:shape>
```



 

 