---
title: VML 簡介
description: VML 簡介
ms.assetid: 8b603e95-3f02-47d6-9c5c-c781fa5d8459
keywords:
- Vector Markup Language (VML) ，參考
- VML (Vector Markup Language) ，參考
- 向量圖形、VML 參考
- '向量圖形、Vector Markup Language (VML) '
- Vector Markup Language (VML) 的參考
- VML 參考
- Vector Markup Language (VML) 、Shape 元素
- VML (Vector Markup Language) ，Shape 元素
- 向量圖形、圖形元素
- Shape 元素
- VML 元素，圖形
- Vector Markup Language (VML) 、VBScript
- VML (Vector Markup Language) 、VBScript
- Vector Markup Language (VML) 、JAVAscript
- VML (Vector Markup Language) ，JAVAscript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7a370519e3f173e7418f1aa0510cac768ff46c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375629"
---
# <a name="vml-introduction"></a><span data-ttu-id="4fcd0-118">VML 簡介</span><span class="sxs-lookup"><span data-stu-id="4fcd0-118">VML Introduction</span></span>

<span data-ttu-id="4fcd0-119">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-119">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4fcd0-120">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-120">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4fcd0-121">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-121">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4fcd0-122">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-122">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4fcd0-123">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-123">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4fcd0-124">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-124">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4fcd0-125">本檔提供 Microsoft Office 2000 隨附的 Vector Markup Language (VML) 之執行的完整詳細參考。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-125">This document gives a complete detailed reference to the implementation of the Vector Markup Language (VML) that is shipped with Microsoft Office 2000.</span></span> <span data-ttu-id="4fcd0-126">其他實施可能會有所不同。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-126">Other implementations may vary.</span></span> <span data-ttu-id="4fcd0-127">如需 VML 的詳細資訊，請參閱 [vml 規格](https://www.w3.org/TR/NOTE-datetime.html) 。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-127">Consult the [VML specification](https://www.w3.org/TR/NOTE-datetime.html) for more information about VML as a standard.</span></span>

<span data-ttu-id="4fcd0-128">VML 定義為一組 XML 元素，以及每個專案的對應屬性。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-128">VML is defined as a set of XML elements and the corresponding attributes for each element.</span></span> <span data-ttu-id="4fcd0-129">由於 **Shape** 元素是 VML 的基本組建區塊，請按一下 [這裡](shape-element--vml.md) 開始參考。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-129">Since the **Shape** element is the basic building block of VML, click [here](shape-element--vml.md) to begin the reference.</span></span>

<span data-ttu-id="4fcd0-130">請注意，此參考包含數個範例和示範。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-130">Note that this reference contains several examples and demos.</span></span> <span data-ttu-id="4fcd0-131">您必須安裝 Microsoft Internet Explorer 5.0 或更高版本，才能查看即時的 VML。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-131">You must have Microsoft Internet Explorer 5.0 or greater installed to view the live VML.</span></span>

<span data-ttu-id="4fcd0-132">除了使用專案和屬性作為擴充 HTML 的 XML 標記的相關資訊之外，此參考還包含語法及範例，說明如何使用腳本和 Internet Explorer 5 或更新版本的檔物件模型功能。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-132">In addition to the information about using elements and attributes as XML tags that extend HTML, this reference contains syntax and examples that show how to use the scripting and the Document Object Model features of Internet Explorer 5 or greater.</span></span> <span data-ttu-id="4fcd0-133">使用具有 VML 的腳本可讓您即時建立元素，並即時操作屬性。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-133">Using script with VML enables you to create elements "on the fly" and manipulate attributes in real time.</span></span>

<span data-ttu-id="4fcd0-134">這項參考中的範例會使用 VBScript 和 JAVAscript。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-134">This examples in this reference uses VBScript and Javascript.</span></span> <span data-ttu-id="4fcd0-135">如果您使用的指令碼語言與範例所示的不同，則您必須符合所有元素和屬性名稱的大小寫。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-135">If you use use a different scripting language than the one shown in an example, you must match the case of all element and attribute names.</span></span> <span data-ttu-id="4fcd0-136">參考提供正確的腳本語法，適用于區分大小寫的語言，例如 JavaScript。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-136">The reference gives scripting syntax that is correct for case-sensitive languages such as JavaScript.</span></span> <span data-ttu-id="4fcd0-137">如果不確定是否有正確的字元大小寫，請使用物件瀏覽器 (例如 OLEView) 流覽 VGX.DLL 來判斷元素或屬性的確切大小寫。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-137">If in doubt regarding the correct character case, use an object browser (such as OLEView) to explore the VGX.DLL to determine the exact case of an element or attribute.</span></span> <span data-ttu-id="4fcd0-138">請注意，當使用 VML 作為 XML 標記時，區分大小寫取決於基礎檔的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-138">Note that when VML is used as XML tags, case sensitivity depends on the document type of you underlying document.</span></span> <span data-ttu-id="4fcd0-139">如果您使用 strict 模式！DOCTYPE、元素和屬性會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="4fcd0-139">If you are using a strict mode !DOCTYPE, elements and attributes will be case sensitive.</span></span>

[<span data-ttu-id="4fcd0-140">VML 參考</span><span class="sxs-lookup"><span data-stu-id="4fcd0-140">The VML Reference</span></span>](shape-element--vml.md)

 

 