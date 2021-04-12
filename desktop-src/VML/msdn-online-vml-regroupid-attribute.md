---
title: VML ReGroupID 屬性
description: VML ReGroupID 屬性
ms.assetid: 2fbcc8c5-6e31-4301-9fb8-c2618bb17a1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384703d3fc5675013de09c4e3b5dec7505cf4164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375545"
---
# <a name="vml-regroupid-attribute"></a><span data-ttu-id="a41e8-103">VML ReGroupID 屬性</span><span class="sxs-lookup"><span data-stu-id="a41e8-103">VML ReGroupID Attribute</span></span>

<span data-ttu-id="a41e8-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="a41e8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a41e8-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="a41e8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a41e8-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="a41e8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a41e8-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="a41e8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a41e8-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="a41e8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a41e8-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="a41e8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a41e8-110">定義圖形的上一個群組。</span><span class="sxs-lookup"><span data-stu-id="a41e8-110">Defines a previous group for a shape.</span></span> <span data-ttu-id="a41e8-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a41e8-111">Read/write.</span></span> <span data-ttu-id="a41e8-112">**VgInteger**。</span><span class="sxs-lookup"><span data-stu-id="a41e8-112">**VgInteger**.</span></span>

<span data-ttu-id="a41e8-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="a41e8-113">**Applies To**</span></span>

[<span data-ttu-id="a41e8-114">形狀</span><span class="sxs-lookup"><span data-stu-id="a41e8-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a41e8-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="a41e8-115">**Tag Syntax**</span></span>

<span data-ttu-id="a41e8-116"><v： *element* o:regroupid = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a41e8-116"><v: *element* o:regroupid=" *expression* "></span></span>

<span data-ttu-id="a41e8-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="a41e8-117">**Remarks**</span></span>

<span data-ttu-id="a41e8-118">識別碼是用來識別已不再分組之圖形的群組。</span><span class="sxs-lookup"><span data-stu-id="a41e8-118">An ID number is used to identify groups of shapes that are no longer grouped.</span></span> <span data-ttu-id="a41e8-119">允許以程式設計方式 regrouped 圖形。</span><span class="sxs-lookup"><span data-stu-id="a41e8-119">Allows shapes to be regrouped programmatically.</span></span>

<span data-ttu-id="a41e8-120">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="a41e8-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="a41e8-121">**範例**</span><span class="sxs-lookup"><span data-stu-id="a41e8-121">**Example**</span></span>

<span data-ttu-id="a41e8-122">圖形是群組識別碼040754所表示之群組的一部分。</span><span class="sxs-lookup"><span data-stu-id="a41e8-122">The shape was part of a group denoted by the group ID 040754.</span></span>


```HTML
   <v:shape id="rect01" ReGroupID="040754"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 