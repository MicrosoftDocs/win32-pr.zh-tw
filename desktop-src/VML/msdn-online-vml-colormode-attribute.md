---
title: VML ColorMode 屬性
description: VML ColorMode 屬性
ms.assetid: 92c885ca-7912-42ff-8f07-e6e779e0ef05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7126a3f5a95910eb85007fe9a80d500c5233e5e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375748"
---
# <a name="vml-colormode-attribute"></a><span data-ttu-id="4713c-103">VML ColorMode 屬性</span><span class="sxs-lookup"><span data-stu-id="4713c-103">VML ColorMode Attribute</span></span>

<span data-ttu-id="4713c-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="4713c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4713c-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="4713c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4713c-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="4713c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4713c-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="4713c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4713c-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="4713c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4713c-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="4713c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4713c-110">決定拉伸色彩的模式。</span><span class="sxs-lookup"><span data-stu-id="4713c-110">Determines the mode of extrusion color.</span></span> <span data-ttu-id="4713c-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4713c-111">Read/write.</span></span> <span data-ttu-id="4713c-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="4713c-112">**VgTriState**.</span></span>

<span data-ttu-id="4713c-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="4713c-113">**Applies To**</span></span>

[<span data-ttu-id="4713c-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="4713c-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="4713c-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="4713c-115">**Tag Syntax**</span></span>

<span data-ttu-id="4713c-116"><o： *element* colormode = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="4713c-116"><o: *element* colormode=" *expression* "></span></span>

<span data-ttu-id="4713c-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="4713c-117">**Script Syntax**</span></span>

<span data-ttu-id="4713c-118"> colormode = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="4713c-118">*element* .colormode="*expression*"</span></span>

<span data-ttu-id="4713c-119">*運算式* =\*\* colormode</span><span class="sxs-lookup"><span data-stu-id="4713c-119">*expression*=*element*.colormode</span></span>

<span data-ttu-id="4713c-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="4713c-120">**Remarks**</span></span>

<span data-ttu-id="4713c-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="4713c-121">Values include:</span></span>



| <span data-ttu-id="4713c-122">值</span><span class="sxs-lookup"><span data-stu-id="4713c-122">Value</span></span>  | <span data-ttu-id="4713c-123">描述</span><span class="sxs-lookup"><span data-stu-id="4713c-123">Description</span></span>                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4713c-124">自動</span><span class="sxs-lookup"><span data-stu-id="4713c-124">auto</span></span>   | <span data-ttu-id="4713c-125">指定拉伸的色彩與圖形的填滿色彩相同。</span><span class="sxs-lookup"><span data-stu-id="4713c-125">Specifies that the color of the extrusion is the same as the fill color of the shape.</span></span> <span data-ttu-id="4713c-126">預設值。</span><span class="sxs-lookup"><span data-stu-id="4713c-126">Default.</span></span>                |
| <span data-ttu-id="4713c-127">自訂</span><span class="sxs-lookup"><span data-stu-id="4713c-127">custom</span></span> | <span data-ttu-id="4713c-128">指定拉伸將會是 [color](color-attribute--extrusion--vml.md) 屬性的色彩。</span><span class="sxs-lookup"><span data-stu-id="4713c-128">Specifies that the extrusion will be the color of the [Color](color-attribute--extrusion--vml.md) attribute.</span></span> |



 

<span data-ttu-id="4713c-129">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="4713c-129">*Microsoft Office Extensions Attribute*</span></span>

 

 