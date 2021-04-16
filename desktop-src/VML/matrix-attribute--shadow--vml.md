---
title: '矩陣屬性 (陰影)  (VML) '
description: '矩陣屬性 (陰影)  (VML) '
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d599aa817e87481aefdec43dbe345b7235fc54bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382677"
---
# <a name="matrix-attribute-shadowvml"></a><span data-ttu-id="4d7f3-103">矩陣屬性 (陰影)  (VML) </span><span class="sxs-lookup"><span data-stu-id="4d7f3-103">Matrix Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="4d7f3-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="4d7f3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4d7f3-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="4d7f3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4d7f3-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="4d7f3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4d7f3-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="4d7f3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4d7f3-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="4d7f3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4d7f3-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="4d7f3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4d7f3-110">定義陰影的觀點轉換。</span><span class="sxs-lookup"><span data-stu-id="4d7f3-110">Defines a perspective transform for a shadow.</span></span> <span data-ttu-id="4d7f3-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4d7f3-111">Read/write.</span></span> <span data-ttu-id="4d7f3-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="4d7f3-112">**String**.</span></span>

<span data-ttu-id="4d7f3-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="4d7f3-113">**Applies To**</span></span>

[<span data-ttu-id="4d7f3-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="4d7f3-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="4d7f3-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="4d7f3-115">**Tag Syntax**</span></span>

<span data-ttu-id="4d7f3-116"><v： *element* matrix = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="4d7f3-116"><v: *element* matrix=" *expression* "></span></span>

<span data-ttu-id="4d7f3-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="4d7f3-117">**Script Syntax**</span></span>

<span data-ttu-id="4d7f3-118">*element* . matrix = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="4d7f3-118">*element* .matrix="*expression*"</span></span>

<span data-ttu-id="4d7f3-119">*運算式* =*元素*。矩陣</span><span class="sxs-lookup"><span data-stu-id="4d7f3-119">*expression*=*element*.matrix</span></span>

<span data-ttu-id="4d7f3-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="4d7f3-120">**Remarks**</span></span>

<span data-ttu-id="4d7f3-121">以 "sxx，sxy，syx，syy，px，.py" 形式的透視圖轉換矩陣，其中 s = scale 和 p = 透視圖。</span><span class="sxs-lookup"><span data-stu-id="4d7f3-121">A perspective transform matrix in the form "sxx,sxy,syx,syy,px,py" where s= scale and p = perspective.</span></span> <span data-ttu-id="4d7f3-122">如果位移的單位為絕對單位，則為 px，.py 則為 1/emu 單位;否則是圖形大小的反向分數。</span><span class="sxs-lookup"><span data-stu-id="4d7f3-122">If offset is in absolute units then px, py are in 1/emu units; otherwise they are an inverse fraction of the shape size.</span></span>

<span data-ttu-id="4d7f3-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="4d7f3-123">*VML Standard Attribute*</span></span>

 

 