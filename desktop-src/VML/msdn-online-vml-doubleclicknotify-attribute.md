---
title: VML DoubleClickNotify 屬性
description: VML DoubleClickNotify 屬性
ms.assetid: 003a87f5-29c1-484e-ac15-2e4cb8e854ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16be329952cfff23957f961fb6d29198ad173898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315235"
---
# <a name="vml-doubleclicknotify-attribute"></a><span data-ttu-id="49f69-103">VML DoubleClickNotify 屬性</span><span class="sxs-lookup"><span data-stu-id="49f69-103">VML DoubleClickNotify Attribute</span></span>

<span data-ttu-id="49f69-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="49f69-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="49f69-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="49f69-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="49f69-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="49f69-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="49f69-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="49f69-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="49f69-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="49f69-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="49f69-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="49f69-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="49f69-110">按兩下圖形時傳送事件訊息。</span><span class="sxs-lookup"><span data-stu-id="49f69-110">Sends an event message when a shape is double-clicked.</span></span> <span data-ttu-id="49f69-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="49f69-111">Read/write.</span></span> <span data-ttu-id="49f69-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="49f69-112">**VgTriState**.</span></span>

<span data-ttu-id="49f69-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="49f69-113">**Applies To**</span></span>

[<span data-ttu-id="49f69-114">形狀</span><span class="sxs-lookup"><span data-stu-id="49f69-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="49f69-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="49f69-115">**Tag Syntax**</span></span>

<span data-ttu-id="49f69-116"><v： *element* o:doubleclicknotify = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="49f69-116"><v: *element* o:doubleclicknotify=" *expression* "></span></span>

<span data-ttu-id="49f69-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="49f69-117">**Remarks**</span></span>

<span data-ttu-id="49f69-118">預設值為 **False**，表示不會引發事件。</span><span class="sxs-lookup"><span data-stu-id="49f69-118">The default value is **False**, indicating that the event will not be fired.</span></span>

<span data-ttu-id="49f69-119">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="49f69-119">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="49f69-120">**範例**</span><span class="sxs-lookup"><span data-stu-id="49f69-120">**Example**</span></span>

<span data-ttu-id="49f69-121">按兩下時，圖形將會觸發按兩下事件。</span><span class="sxs-lookup"><span data-stu-id="49f69-121">The shape will trigger a double-click event when double-clicked.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:doubleclicknotify="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 