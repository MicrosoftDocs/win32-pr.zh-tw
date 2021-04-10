---
title: '矩陣屬性 (扭曲)  (VML) '
description: '矩陣屬性 (扭曲)  (VML) '
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8327acfebfe4d968e673060f2f3cbef69d3e9db6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024000"
---
# <a name="matrix-attribute-skewvml"></a><span data-ttu-id="208ad-103">矩陣屬性 (扭曲)  (VML) </span><span class="sxs-lookup"><span data-stu-id="208ad-103">Matrix Attribute (Skew)(VML)</span></span>

<span data-ttu-id="208ad-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="208ad-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="208ad-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="208ad-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="208ad-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="208ad-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="208ad-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="208ad-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="208ad-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="208ad-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="208ad-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="208ad-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="208ad-110">定義扭曲的觀點轉換。</span><span class="sxs-lookup"><span data-stu-id="208ad-110">Defines a perspective transform of a skew.</span></span> <span data-ttu-id="208ad-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="208ad-111">Read/write.</span></span> <span data-ttu-id="208ad-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="208ad-112">**String**.</span></span>

<span data-ttu-id="208ad-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="208ad-113">**Applies To**</span></span>

[<span data-ttu-id="208ad-114">斜</span><span class="sxs-lookup"><span data-stu-id="208ad-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="208ad-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="208ad-115">**Tag Syntax**</span></span>

<span data-ttu-id="208ad-116"><o： *element* matrix = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="208ad-116"><o: *element* matrix=" *expression* "></span></span>

<span data-ttu-id="208ad-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="208ad-117">**Script Syntax**</span></span>

<span data-ttu-id="208ad-118">*element* . matrix = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="208ad-118">*element* .matrix="*expression*"</span></span>

<span data-ttu-id="208ad-119">*運算式* =*元素*。矩陣</span><span class="sxs-lookup"><span data-stu-id="208ad-119">*expression*=*element*.matrix</span></span>

<span data-ttu-id="208ad-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="208ad-120">**Remarks**</span></span>

<span data-ttu-id="208ad-121">矩陣是以 "sxx，sxy，syx，syy，px，.py" 形式的字串，其中 s 是 scale、p 是觀點，而 x 和 y 是 x 和 y 值。</span><span class="sxs-lookup"><span data-stu-id="208ad-121">The matrix is a string in the form "sxx, sxy, syx, syy, px, py" where s is scale, p is perspective, and x and y are x and y values.</span></span> <span data-ttu-id="208ad-122">如果 [Offset](offset-attribute--skew--vml.md) 是絕對單位，則 px 和 .py 是以 emu ^-1 [單位](msdn-online-vml-units.md) (否則為圖形大小) 的反向分數。</span><span class="sxs-lookup"><span data-stu-id="208ad-122">If [Offset](offset-attribute--skew--vml.md) is in absolute units, then px and py are in emu^-1 [units](msdn-online-vml-units.md) (otherwise they are an inverse fraction of the shape size).</span></span> <span data-ttu-id="208ad-123">預設值為 "1，0，0，1，0，0"。</span><span class="sxs-lookup"><span data-stu-id="208ad-123">The default value is "1,0,0,1,0,0".</span></span>

<span data-ttu-id="208ad-124">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="208ad-124">*Microsoft Office Extensions Attribute*</span></span>

 

 