---
title: 'Vector Markup Language (VML) '
description: 'Vector Markup Language (VML) '
ms.assetid: 1f30d60f-3d4f-43e4-9a2b-424a5ee8f852
keywords:
- Vector Markup Language (VML) ，關於
- VML (Vector Markup Language) ，關於
- 向量圖形，關於
- '向量圖形、Vector Markup Language (VML) '
- 'Vector Markup Language (VML) ，全球資訊網協會 (W3C) '
- 'VML (Vector Markup Language) ，全球資訊網協會 (W3C) '
- '向量圖形，全球資訊網協會 (W3C) '
- 向量圖形，VML 優點
- Vector Markup Language (VML) ，優點
- VML (Vector Markup Language) ，優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4637fff0550ce9c93e295c51fc529f62c370b8aa
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910259"
---
# <a name="vector-markup-language-vml"></a><span data-ttu-id="30924-113">Vector Markup Language (VML) </span><span class="sxs-lookup"><span data-stu-id="30924-113">Vector Markup Language (VML)</span></span>

<span data-ttu-id="30924-114">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="30924-114">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="30924-115">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="30924-115">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!NOTE]
> <span data-ttu-id="30924-116">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="30924-116">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="30924-117">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="30924-117">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="30924-118">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="30924-118">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="30924-119">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="30924-119">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

<span data-ttu-id="30924-120">Vector Markup Language (VML) 是以 XML 為基礎的 exchange、編輯和傳遞格式，適用于 Web 上符合生產力使用者和圖形設計專業人員需求的高品質向量圖形。</span><span class="sxs-lookup"><span data-stu-id="30924-120">Vector Markup Language (VML) is an XML-based exchange, editing, and delivery format for high-quality vector graphics on the Web that meets the needs of both productivity users and graphic design professionals.</span></span> <span data-ttu-id="30924-121">XML 是一種新興的簡單、彈性且開放的文字語言，可補充 HTML。</span><span class="sxs-lookup"><span data-stu-id="30924-121">XML is an emerging simple, flexible, and open text-based language that complements HTML.</span></span> <span data-ttu-id="30924-122">如需 XML 的詳細資訊，請參閱 MSDN Library 的 [XML 一節](/documentation/?frame=true) (。 ) </span><span class="sxs-lookup"><span data-stu-id="30924-122">(See the [XML section](/documentation/?frame=true) of the MSDN Library for detailed information on XML.)</span></span>

<span data-ttu-id="30924-123">目前 Microsoft Internet Explorer 5.0 版或更新版本支援 VML。</span><span class="sxs-lookup"><span data-stu-id="30924-123">VML is currently supported by Microsoft Internet Explorer version 5.0 or later.</span></span>

<span data-ttu-id="30924-124">已將 VML 建議為 W3C 作為 Web 上向量圖形的標準 (請參閱 [Vector Markup Language (VML) ](https://www.w3.org/TR/NOTE-VML)) 。</span><span class="sxs-lookup"><span data-stu-id="30924-124">VML has been proposed to the W3C as a standard for vector graphics on the Web (see [Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-VML)).</span></span> <span data-ttu-id="30924-125">Microsoft 會繼續在開發和實行以 XML 為基礎的技術方面繼續收取費用， (AutoDesk、Hewlett Packard、Macromedia、Visio) 和 W3C 來推動以網路為基礎的標準。</span><span class="sxs-lookup"><span data-stu-id="30924-125">Microsoft is continuing to lead the charge in the development and implementation of XML-based technologies, working with leading industry partners (AutoDesk, Hewlett-Packard, Macromedia, Visio) and the W3C to advance Web-based standards.</span></span> <span data-ttu-id="30924-126">我們預計在 Web 上使用 W3C 到最後一個標準格式的向量圖形。</span><span class="sxs-lookup"><span data-stu-id="30924-126">We expect to work with the W3C to ultimately drive to one standard format for vector graphics on the Web.</span></span>

<span data-ttu-id="30924-127">Microsoft Office 2000 或更新版本也支援 VML。</span><span class="sxs-lookup"><span data-stu-id="30924-127">VML is also supported by Microsoft Office 2000 or later.</span></span> <span data-ttu-id="30924-128">Microsoft Word、Microsoft Excel 和 Microsoft PowerPoint 可以用來建立 VML 圖形。</span><span class="sxs-lookup"><span data-stu-id="30924-128">Microsoft Word, Microsoft Excel, and Microsoft PowerPoint can be used to create VML graphics.</span></span>

### <a name="using-vml"></a><span data-ttu-id="30924-129">使用 VML</span><span class="sxs-lookup"><span data-stu-id="30924-129">Using VML</span></span>

<span data-ttu-id="30924-130">若要在您的網頁中使用 VML，請使用樣式元素來匯入 VML 行為，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="30924-130">To use VML in your web pages, use a style element to import the VML behavior, as shown in the following code.</span></span>

```
<style>v\: * { behavior:url(#default#VML); display:inline-block }</style>
```

<span data-ttu-id="30924-131">接下來，宣告 VML 命名空間，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="30924-131">Next, declare the VML namespace, as shown in the following code sample.</span></span>

```
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v" />
```

<span data-ttu-id="30924-132">最後，新增 VML 元素來定義視覺效果。</span><span class="sxs-lookup"><span data-stu-id="30924-132">Finally, add VML elements to define visuals effects.</span></span> <span data-ttu-id="30924-133">例如，下列 VML 程式碼會建立紅色橢圓。</span><span class="sxs-lookup"><span data-stu-id="30924-133">For example, the following VML code creates a red oval.</span></span>

```
<v:oval style="width:100pt;height:50pt" fillcolor="red">
</v:oval>
```

> [!NOTE]
> <span data-ttu-id="30924-134">若要在使用 strict 模式檔時取得最佳結果，請確定您的標記有效且格式正確。</span><span class="sxs-lookup"><span data-stu-id="30924-134">For best results when using strict mode documents, be sure that your markup is valid and well-formed.</span></span> <span data-ttu-id="30924-135">如需詳細資訊，請參閱！DOCTYPE 參考頁面。</span><span class="sxs-lookup"><span data-stu-id="30924-135">For more information, please see the !DOCTYPE reference page.</span></span>


### <a name="benefits-of-vml"></a><span data-ttu-id="30924-136">VML 的優點</span><span class="sxs-lookup"><span data-stu-id="30924-136">Benefits of VML</span></span>

-   <span data-ttu-id="30924-137">VML 讓生產力使用者和作者更容易撰寫。</span><span class="sxs-lookup"><span data-stu-id="30924-137">VML makes authoring easier for productivity users and authors.</span></span> <span data-ttu-id="30924-138">它可透過剪下和貼上) ，以及在各種生產力和設計應用程式之間進行向量圖形的後續編輯，來促進 exchange (。</span><span class="sxs-lookup"><span data-stu-id="30924-138">It facilitates the exchange (via cut and paste) and subsequent editing of vector graphics between a wide variety of productivity and design applications.</span></span>
-   <span data-ttu-id="30924-139">VML 可提供更快速的圖形下載及更好的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="30924-139">VML provides faster graphic downloads and a better user experience.</span></span> <span data-ttu-id="30924-140">它可讓您使用以文字為基礎的開放格式，將高品質、完全整合、可擴充的向量圖形傳遞至 Web。</span><span class="sxs-lookup"><span data-stu-id="30924-140">It allows the delivery of high-quality, fully integrated, scalable vector graphics to the Web, in an open text-based format.</span></span> <span data-ttu-id="30924-141">VML 圖形會與 HTML 網頁一起以內嵌方式傳遞，而不是以外部檔案的形式參考圖形，可讓它們與使用者互動進行互動及調整。</span><span class="sxs-lookup"><span data-stu-id="30924-141">Rather than referencing graphics as external files, VML graphics are delivered inline with the HTML page, allowing them to interact and scale with user interaction.</span></span>
-   <span data-ttu-id="30924-142">VML 是開放且以標準為基礎。</span><span class="sxs-lookup"><span data-stu-id="30924-142">VML is open and standards-based.</span></span> <span data-ttu-id="30924-143">它是以 XML 為基礎的格式。</span><span class="sxs-lookup"><span data-stu-id="30924-143">It is an XML-based format.</span></span> <span data-ttu-id="30924-144">XML 1.0 是一種開放、簡單、以文字為基礎的語言，用來描述 Web 上的結構化資料，並補充 HTML 來顯示。</span><span class="sxs-lookup"><span data-stu-id="30924-144">XML 1.0 is an open, simple, text-based language for describing structured data on the Web, and complements HTML for display.</span></span> <span data-ttu-id="30924-145">VML 也支援其他 W3C 標準，例如階層式樣式表 2.0 (CSS) ，它會指定樣式資訊和2D 定位，以及檔物件模型 (DOM) ，可讓開發人員以頁面元素一致地與物件互動。</span><span class="sxs-lookup"><span data-stu-id="30924-145">VML also supports other W3C standards, such as Cascading Style Sheets 2.0 (CSS), which specifies style information and 2-D positioning, as well as the Document Object Model (DOM), which allows developers to interact consistently with page elements as objects.</span></span>

### <a name="for-additional-information"></a><span data-ttu-id="30924-146">其他資訊</span><span class="sxs-lookup"><span data-stu-id="30924-146">For additional information</span></span>

<span data-ttu-id="30924-147">請參閱下列連結：</span><span class="sxs-lookup"><span data-stu-id="30924-147">See the links below:</span></span>

-   <span data-ttu-id="30924-148">如需 VML 常見問題的解答，請參閱 [VML 常見問題](frequently-asked-questions-about-vml.yml)。</span><span class="sxs-lookup"><span data-stu-id="30924-148">For answers to frequently asked questions about VML, see the [VML FAQ](frequently-asked-questions-about-vml.yml).</span></span>
-   <span data-ttu-id="30924-149">如需在 Web 網頁上使用 VML 的教學課程，請參閱 [如何在網頁上使用 vml](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)，以補充提交給 W3C 的 [vml 規格](https://www.w3.org/TR/NOTE-datetime.html) 。</span><span class="sxs-lookup"><span data-stu-id="30924-149">For a tutorial on using VML on Web pages, see [How to Use VML on Web Pages](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), which complements the [VML specification](https://www.w3.org/TR/NOTE-datetime.html) submitted to the W3C.</span></span>
-   <span data-ttu-id="30924-150">如需 VML 資料類型的詳細資訊，請參閱 [基本的 Vml 類型](basic-vml-types.md) 檔。</span><span class="sxs-lookup"><span data-stu-id="30924-150">For information on VML data types, see the [Basic VML Types](basic-vml-types.md) document.</span></span>
-   <span data-ttu-id="30924-151">如需 VML 的完整參考，包括如何搭配使用 VML 與標記以及腳本的相關資訊，請參閱 [Vml 參考](msdn-online-vml-introduction.md)。</span><span class="sxs-lookup"><span data-stu-id="30924-151">For the complete reference on VML, including information on how to use VML with tags as well as scripting, see the [VML Reference](msdn-online-vml-introduction.md).</span></span>