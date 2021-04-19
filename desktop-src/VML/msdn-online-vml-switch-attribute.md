---
title: VML 參數屬性
description: VML 參數屬性
ms.assetid: fc099c0a-6789-41e8-ab08-36f4fd2d3bfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d102d6af20e698d8ec281cb1be6fae9690de4e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967262"
---
# <a name="vml-switch-attribute"></a><span data-ttu-id="49f43-103">VML 參數屬性</span><span class="sxs-lookup"><span data-stu-id="49f43-103">VML Switch Attribute</span></span>

<span data-ttu-id="49f43-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="49f43-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="49f43-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="49f43-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="49f43-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="49f43-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="49f43-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="49f43-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="49f43-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="49f43-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="49f43-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="49f43-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="49f43-110">決定是否要交換控制碼方向。</span><span class="sxs-lookup"><span data-stu-id="49f43-110">Determines whether the handle directions are swapped.</span></span> <span data-ttu-id="49f43-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="49f43-111">Read/write.</span></span> <span data-ttu-id="49f43-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="49f43-112">**VgTriState**.</span></span>

<span data-ttu-id="49f43-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="49f43-113">**Applies To**</span></span>

<span data-ttu-id="49f43-114">[H](msdn-online-vml-h-element.md) ([控制碼](msdn-online-vml-handles-element.md) 的子項目) </span><span class="sxs-lookup"><span data-stu-id="49f43-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="49f43-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="49f43-115">**Tag Syntax**</span></span>

<span data-ttu-id="49f43-116"><v： *element* switch = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="49f43-116"><v: *element* switch=" *expression* "></span></span>

<span data-ttu-id="49f43-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="49f43-117">**Remarks**</span></span>

<span data-ttu-id="49f43-118">若 **為 True**，則當圖形高度高於寬度時，會在 x 和 y 方向之間切換控制碼。</span><span class="sxs-lookup"><span data-stu-id="49f43-118">If **True**, the handle is switched between the x and y directions if the shape is taller than it is wide.</span></span> <span data-ttu-id="49f43-119">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="49f43-119">The default value is **False**.</span></span>

<span data-ttu-id="49f43-120">這個屬性會用於具有 limo 延展行為的圖形。</span><span class="sxs-lookup"><span data-stu-id="49f43-120">This attribute is used for shapes with limo stretch behavior.</span></span>

<span data-ttu-id="49f43-121">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="49f43-121">*VML Standard Attribute*</span></span>

 

 