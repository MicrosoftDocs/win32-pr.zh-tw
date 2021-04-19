---
title: VML 列印屬性
description: VML 列印屬性
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55925621ab56f011c998f3feac21a892a4d7ea66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106983299"
---
# <a name="vml-print-attribute"></a><span data-ttu-id="22e8b-103">VML 列印屬性</span><span class="sxs-lookup"><span data-stu-id="22e8b-103">VML Print Attribute</span></span>

<span data-ttu-id="22e8b-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="22e8b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="22e8b-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="22e8b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="22e8b-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="22e8b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="22e8b-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="22e8b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="22e8b-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="22e8b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="22e8b-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="22e8b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="22e8b-110">決定是否要列印圖形。</span><span class="sxs-lookup"><span data-stu-id="22e8b-110">Determines whether the shape will be printed.</span></span> <span data-ttu-id="22e8b-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="22e8b-111">Read/write.</span></span> <span data-ttu-id="22e8b-112">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="22e8b-112">[VgTriState](msdn-online-vml-vgtristate.md).</span></span>

<span data-ttu-id="22e8b-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="22e8b-113">**Applies To**</span></span>

[<span data-ttu-id="22e8b-114">形狀</span><span class="sxs-lookup"><span data-stu-id="22e8b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="22e8b-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="22e8b-115">**Tag Syntax**</span></span>

<span data-ttu-id="22e8b-116"><v： *element* print = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="22e8b-116"><v: *element* print=" *expression* "></span></span>

<span data-ttu-id="22e8b-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="22e8b-117">**Script Syntax**</span></span>

<span data-ttu-id="22e8b-118">*element* = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="22e8b-118">*element* .print="*expression*"</span></span>

<span data-ttu-id="22e8b-119">*運算式* =*元素*。列印</span><span class="sxs-lookup"><span data-stu-id="22e8b-119">*expression*=*element*.print</span></span>

<span data-ttu-id="22e8b-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="22e8b-120">**Remarks**</span></span>

<span data-ttu-id="22e8b-121">提供以指定是否列印圖形的方式。</span><span class="sxs-lookup"><span data-stu-id="22e8b-121">Provided as a way to specify whether shapes will be printed.</span></span> <span data-ttu-id="22e8b-122">請注意，即使在這個屬性為 **False** 的情況下，圖形仍可以顯示在螢幕上。</span><span class="sxs-lookup"><span data-stu-id="22e8b-122">Note that a shape can still be displayed on the screen, even if it is not printed as a result of this attribute being **False**.</span></span> <span data-ttu-id="22e8b-123">預設值是 **True**。</span><span class="sxs-lookup"><span data-stu-id="22e8b-123">The default value is **True**.</span></span>

<span data-ttu-id="22e8b-124">Microsoft Office 會使用這個屬性，但 Microsoft Internet Explorer 不會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="22e8b-124">This attribute is used by Microsoft Office but is not used by Microsoft Internet Explorer.</span></span>

<span data-ttu-id="22e8b-125">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="22e8b-125">*Microsoft Office Extensions Attribute*</span></span>

 

 