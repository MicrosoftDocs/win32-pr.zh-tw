---
title: VML 物件模型參考
description: 本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c387935119babc73442e9b8f307672925bdf71d3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444819"
---
# <a name="vml-object-model-reference"></a><span data-ttu-id="63ba0-104">VML 物件模型參考</span><span class="sxs-lookup"><span data-stu-id="63ba0-104">VML Object Model Reference</span></span>

<span data-ttu-id="63ba0-105">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="63ba0-105">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="63ba0-106">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="63ba0-106">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="63ba0-107">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="63ba0-107">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="63ba0-108">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="63ba0-108">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="63ba0-109">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-109">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="63ba0-110">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-110">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="63ba0-111">本主題內容：</span><span class="sxs-lookup"><span data-stu-id="63ba0-111">In this topic:</span></span>

-   [<span data-ttu-id="63ba0-112">簡介</span><span class="sxs-lookup"><span data-stu-id="63ba0-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="63ba0-113">範例</span><span class="sxs-lookup"><span data-stu-id="63ba0-113">Example</span></span>](#example)
-   [<span data-ttu-id="63ba0-114">設定 VML</span><span class="sxs-lookup"><span data-stu-id="63ba0-114">Setting up VML</span></span>](#setting-up-vml)
-   [<span data-ttu-id="63ba0-115">VML OM 參考</span><span class="sxs-lookup"><span data-stu-id="63ba0-115">VML OM Reference</span></span>](#vml-om-reference)
    -   [<span data-ttu-id="63ba0-116">Shape 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-116">Shape element</span></span>](#shape-element)
-   [<span data-ttu-id="63ba0-117">Shape 元素的子項目</span><span class="sxs-lookup"><span data-stu-id="63ba0-117">Subelements of the Shape Element</span></span>](#subelements-of-the-shape-element)
    -   [<span data-ttu-id="63ba0-118">Background 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-118">Background element</span></span>](#background-element)
    -   [<span data-ttu-id="63ba0-119">延伸元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-119">Extrusion element</span></span>](#extrusion-element)
    -   [<span data-ttu-id="63ba0-120">Fill 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-120">Fill element</span></span>](#fill-element)
    -   [<span data-ttu-id="63ba0-121">Group 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-121">Group element</span></span>](#group-element)
    -   [<span data-ttu-id="63ba0-122">Imagedata 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-122">Imagedata element</span></span>](#imagedata-element)
    -   [<span data-ttu-id="63ba0-123">Path 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-123">Path element</span></span>](#path-element)
    -   [<span data-ttu-id="63ba0-124">Shadow 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-124">Shadow element</span></span>](#shadow-element)
    -   [<span data-ttu-id="63ba0-125">扭曲元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-125">Skew element</span></span>](#skew-element)
    -   [<span data-ttu-id="63ba0-126">Stroke 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-126">Stroke element</span></span>](#stroke-element)
    -   [<span data-ttu-id="63ba0-127">TextPath 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-127">TextPath element</span></span>](#textpath-element)
-   [<span data-ttu-id="63ba0-128">在 VML 物件模型中使用的資料類型</span><span class="sxs-lookup"><span data-stu-id="63ba0-128">Data Types Used in the VML Object Model</span></span>](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a><span data-ttu-id="63ba0-129">簡介</span><span class="sxs-lookup"><span data-stu-id="63ba0-129">Introduction</span></span>

<span data-ttu-id="63ba0-130">[Vector Markup Language (VML) ](https://www.w3.org/TR/NOTE-datetime.html) 是以文字為基礎的語言，使用 [XML](https://www.w3.org/TR/REC-xml.mdl) 擴充 HTML 以顯示向量圖形資訊。</span><span class="sxs-lookup"><span data-stu-id="63ba0-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) is a text-based language that uses [XML](https://www.w3.org/TR/REC-xml.mdl) to extend HTML for the purpose of displaying vector graphic information.</span></span> <span data-ttu-id="63ba0-131">[VML 檔物件模型 (DOM) 會定義用於操作檔元素的程式設計介面。</span><span class="sxs-lookup"><span data-stu-id="63ba0-131">The VML Document Object Model (DOM) defines a programmatic interface for the manipulation of the document elements.</span></span> <span data-ttu-id="63ba0-132">這可讓使用者透過平臺和語言中性介面，以動態方式建立和修改向量圖形。</span><span class="sxs-lookup"><span data-stu-id="63ba0-132">This enables the user to dynamically create and modify vector graphics through a platform- and language-neutral interface.</span></span> <span data-ttu-id="63ba0-133">VML DOM 符合 [檔物件模型](https://www.w3.org/TR/REC-DOM-Level-1/) 規格。</span><span class="sxs-lookup"><span data-stu-id="63ba0-133">The VML DOM conforms to the [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specification.</span></span>

<span data-ttu-id="63ba0-134">VML 使用 [Shape](#shape-element) 元素作為向量圖形影像的基本建築物區塊。</span><span class="sxs-lookup"><span data-stu-id="63ba0-134">VML uses the [Shape](#shape-element) element as the basic building block for vector graphic images.</span></span> <span data-ttu-id="63ba0-135">建立圖形之後，您可以透過屬性或附加的子項目來修改圖形。</span><span class="sxs-lookup"><span data-stu-id="63ba0-135">Once a shape is created, you can modify the shape through attributes or by attached subelements.</span></span> <span data-ttu-id="63ba0-136">例如，若要變更圖形的色彩，請將色彩值指派給 **FillColor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="63ba0-136">For example, to change the color of a shape, assign a color value to the **FillColor** attribute.</span></span>


```HTML
myshape.fillcolor = "red"
```



<span data-ttu-id="63ba0-137">圖形的數個屬性也是子 [元素](/windows) ，而且有自己的屬性，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="63ba0-137">Several of the attributes of a shape are also [subelements](/windows) and have their own attributes, including the following:</span></span>

-   [<span data-ttu-id="63ba0-138">背景</span><span class="sxs-lookup"><span data-stu-id="63ba0-138">Background</span></span>](#background-element)
-   [<span data-ttu-id="63ba0-139">擠壓</span><span class="sxs-lookup"><span data-stu-id="63ba0-139">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="63ba0-140">填滿</span><span class="sxs-lookup"><span data-stu-id="63ba0-140">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="63ba0-141">群組</span><span class="sxs-lookup"><span data-stu-id="63ba0-141">Group</span></span>](#group-element)
-   [<span data-ttu-id="63ba0-142">Imagedata</span><span class="sxs-lookup"><span data-stu-id="63ba0-142">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="63ba0-143">路徑</span><span class="sxs-lookup"><span data-stu-id="63ba0-143">Path</span></span>](#path-element)
-   [<span data-ttu-id="63ba0-144">Shadow</span><span class="sxs-lookup"><span data-stu-id="63ba0-144">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="63ba0-145">斜</span><span class="sxs-lookup"><span data-stu-id="63ba0-145">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="63ba0-146">中風</span><span class="sxs-lookup"><span data-stu-id="63ba0-146">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="63ba0-147">TextPath</span><span class="sxs-lookup"><span data-stu-id="63ba0-147">TextPath</span></span>](#textpath-element)

<span data-ttu-id="63ba0-148">VML OM 會使用數個 [資料類型](/windows) 來定義參數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-148">The VML OM uses several [data types](/windows) to define parameters.</span></span> <span data-ttu-id="63ba0-149">前面加上 "Vg" 的資料類型是列舉，而前面加上 "IVg" 的資料類型是物件。</span><span class="sxs-lookup"><span data-stu-id="63ba0-149">Datatypes prefixed with "Vg" are enumerations and those prefixed with "IVg" are objects.</span></span> <span data-ttu-id="63ba0-150">按一下這裡以取得清單。</span><span class="sxs-lookup"><span data-stu-id="63ba0-150">Click here for a list.</span></span> <span data-ttu-id="63ba0-151">次要資料類型會以特定參數列出。</span><span class="sxs-lookup"><span data-stu-id="63ba0-151">Minor datatypes are listed with specific parameters.</span></span>

## <a name="example"></a><span data-ttu-id="63ba0-152">範例</span><span class="sxs-lookup"><span data-stu-id="63ba0-152">Example</span></span>

<span data-ttu-id="63ba0-153">下列 VBScript 程式碼顯示如何建立簡單的圖形：</span><span class="sxs-lookup"><span data-stu-id="63ba0-153">The following VBScript code shows how to create a simple shape:</span></span>


```HTML
        Set MyRect = Document.CreateElement("v:Rect")
        Set R = MyDiv.AppendChild(MyRect)
        R.Style.Position = "absolute"
        R.Style.Width = 20
        R.Style.Height = 20
        R.Style.Top = 50
        R.Style.Left = 50
        R.FillColor = "red"
```



<span data-ttu-id="63ba0-154">在上述範例中，會使用檔物件模型方法 **CreateElement** 來建立圖形。</span><span class="sxs-lookup"><span data-stu-id="63ba0-154">In the above example, a shape is created by using the Document Object Model method **CreateElement**.</span></span> <span data-ttu-id="63ba0-155">圖形是一個 VML 預先定義的矩形圖形。</span><span class="sxs-lookup"><span data-stu-id="63ba0-155">The shape is a VML predefined Rect shape.</span></span> <span data-ttu-id="63ba0-156">雖然物件存在，但是在附加至檔之前，它不能是檔的一部分。</span><span class="sxs-lookup"><span data-stu-id="63ba0-156">Even though the object exists, it cannot be part of the document until it is attached to the document.</span></span> <span data-ttu-id="63ba0-157">使用 **AppendChild** 方法，矩形就會成為名為 MyDiv 的 **DIV** 元素的子系。</span><span class="sxs-lookup"><span data-stu-id="63ba0-157">Using the **AppendChild** method, the Rect is made a child of a **DIV** element called MyDiv.</span></span> <span data-ttu-id="63ba0-158">有幾個最小樣式屬性 (**位置**、 **寬度**、 **高度**、 **Top**、 **左方**) 設定成提供圖形特定的大小。</span><span class="sxs-lookup"><span data-stu-id="63ba0-158">A few minimum style attributes (**Position**, **Width**, **Height**, **Top**, **Left**) are set to give the shape a specific size.</span></span> <span data-ttu-id="63ba0-159">最後，會使用 **FillColor** 屬性來指派色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-159">Finally, a color is assigned with the **FillColor** attribute.</span></span> <span data-ttu-id="63ba0-160">請注意，您可以使用任何可搭配檔物件模型介面使用的指令碼語言或任何語言。</span><span class="sxs-lookup"><span data-stu-id="63ba0-160">Note that any scripting language or any language that can work with Document Object Model interfaces can be used.</span></span>

## <a name="setting-up-vml"></a><span data-ttu-id="63ba0-161">設定 VML</span><span class="sxs-lookup"><span data-stu-id="63ba0-161">Setting up VML</span></span>

<span data-ttu-id="63ba0-162">一個 VML 的執行是透過 Microsoft Internet Explorer 5.0 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="63ba0-162">One implementation of VML is through Microsoft Internet Explorer 5.0 or greater.</span></span> <span data-ttu-id="63ba0-163">若要在網頁中正確設定轉譯物件，必須進行下列新增專案：</span><span class="sxs-lookup"><span data-stu-id="63ba0-163">To set up the rendering object correctly in a Web page, the following additions must be made:</span></span>

1.  <span data-ttu-id="63ba0-164">必須在初始中設定架構</span><span class="sxs-lookup"><span data-stu-id="63ba0-164">The schema must be set up in the initial</span></span> <HTML> <span data-ttu-id="63ba0-165">標記如下：</span><span class="sxs-lookup"><span data-stu-id="63ba0-165">tag as follows:</span></span>
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  <span data-ttu-id="63ba0-166">轉譯行為必須是檔樣式的一部分：</span><span class="sxs-lookup"><span data-stu-id="63ba0-166">The rendering behavior must be part of the document's style:</span></span>
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

<span data-ttu-id="63ba0-167">以下顯示針對顯示動態建立圖形的 VML 正確設定的 HTML 網頁範例。</span><span class="sxs-lookup"><span data-stu-id="63ba0-167">The following shows a sample HTML Web page set up correctly for VML showing the dynamic creation of a shape.</span></span>


```HTML
<HTML xmlns:v="urn:schemas-microsoft-com:vml">
<HEAD>
<STYLE>
v\:* { behavior: url(#default#VML); display:inline-block}
</STYLE>
<TITLE>VML Sample</TITLE>
</HEAD>
<BODY>
<DIV id="MyDiv"></DIV>
<SCRIPT ID="MYSCRIPT" LANGUAGE="VBScript">
<!--
Set MyRect = Document.CreateElement("v:Rect")
Set R = MyDiv.AppendChild(MyRect)
R.Style.Position = "absolute"
R.Style.Width = 20
R.Style.Height = 20
R.Style.Top = 50
R.Style.Left = 50
R.FillColor = "red"
-->
</SCRIPT>
</BODY>
</HTML>
```



<span data-ttu-id="63ba0-168">請注意，在 Beta 版中，必須要有 ActiveX 物件標記和不同的行為樣式。</span><span class="sxs-lookup"><span data-stu-id="63ba0-168">Note that in beta versions, an ActiveX object tag and a different behavior style was required.</span></span>

## <a name="vml-om-reference"></a><span data-ttu-id="63ba0-169">VML OM 參考</span><span class="sxs-lookup"><span data-stu-id="63ba0-169">VML OM Reference</span></span>

<span data-ttu-id="63ba0-170">這個參考定義了 VML 的物件模型所使用的 [Shape](#shape-element) 元素、子 [元素](/windows)和 [資料類型](/windows) 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-170">This reference defines the [Shape](#shape-element) element, [subelements](/windows), and [data types](/windows) that are used by the object model of VML.</span></span>

### <a name="shape-element"></a><span data-ttu-id="63ba0-171">Shape 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-171">Shape element</span></span>

<span data-ttu-id="63ba0-172">圖形是 Vector Markup Language (VML) 所定義之圖形影像的建立區塊。</span><span class="sxs-lookup"><span data-stu-id="63ba0-172">Shapes are the building blocks of graphical images defined by Vector Markup Language (VML).</span></span> <span data-ttu-id="63ba0-173">圖形是最上層元素，而數個子項目可協助定義每個圖形的本質。</span><span class="sxs-lookup"><span data-stu-id="63ba0-173">The shape is the top-level element and several subelements help define the nature of each shape.</span></span>

<span data-ttu-id="63ba0-174">VML 提供預先定義的圖形：</span><span class="sxs-lookup"><span data-stu-id="63ba0-174">VML provides predefined shapes:</span></span>

<span data-ttu-id="63ba0-175">**圖形屬性**</span><span class="sxs-lookup"><span data-stu-id="63ba0-175">**Shape Attributes**</span></span>

-   <span data-ttu-id="63ba0-176">**Arc**</span><span class="sxs-lookup"><span data-stu-id="63ba0-176">**Arc**</span></span>
-   <span data-ttu-id="63ba0-177">**曲線**</span><span class="sxs-lookup"><span data-stu-id="63ba0-177">**Curve**</span></span>
-   <span data-ttu-id="63ba0-178">**線條**</span><span class="sxs-lookup"><span data-stu-id="63ba0-178">**Line**</span></span>
-   <span data-ttu-id="63ba0-179">**折線**</span><span class="sxs-lookup"><span data-stu-id="63ba0-179">**PolyLine**</span></span>
-   <span data-ttu-id="63ba0-180">**Rect**</span><span class="sxs-lookup"><span data-stu-id="63ba0-180">**Rect**</span></span>
-   <span data-ttu-id="63ba0-181">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="63ba0-181">**RoundRect**</span></span>



|   <span data-ttu-id="63ba0-182">Subelement</span><span class="sxs-lookup"><span data-stu-id="63ba0-182">Subelement</span></span>           |    <span data-ttu-id="63ba0-183">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-183">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba0-184">形容詞</span><span class="sxs-lookup"><span data-stu-id="63ba0-184">Adj</span></span>          | <span data-ttu-id="63ba0-185">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-185">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span></span> <span data-ttu-id="63ba0-186">以逗號分隔的數位清單，這些是用來定義圖形路徑之指南公式的參數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-186">A comma-delimited list of numbers that are the parameters for the guide formulas that define the path of the shape.</span></span> <span data-ttu-id="63ba0-187">可能會省略值以允許使用預設值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-187">Values may be omitted to allow for using defaults.</span></span> <span data-ttu-id="63ba0-188">最多可以有8個調整值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-188">There can be up to 8 adjustment values.</span></span>                                                                                                   |
| <span data-ttu-id="63ba0-189">Alt</span><span class="sxs-lookup"><span data-stu-id="63ba0-189">Alt</span></span>          | <span data-ttu-id="63ba0-190">字串。</span><span class="sxs-lookup"><span data-stu-id="63ba0-190">String.</span></span> <span data-ttu-id="63ba0-191">與圖形相關聯的替代文字。</span><span class="sxs-lookup"><span data-stu-id="63ba0-191">Alternative text associated with shape.</span></span> <span data-ttu-id="63ba0-192">用於非圖形化流覽。</span><span class="sxs-lookup"><span data-stu-id="63ba0-192">Used for non-graphical browsing.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="63ba0-193">按鈕</span><span class="sxs-lookup"><span data-stu-id="63ba0-193">Button</span></span>       | <span data-ttu-id="63ba0-194">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-194">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-195">按一下時，會顯示按鈕的行為。</span><span class="sxs-lookup"><span data-stu-id="63ba0-195">Displays button behavior on click.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="63ba0-196">BWMode</span><span class="sxs-lookup"><span data-stu-id="63ba0-196">BWMode</span></span>       | <span data-ttu-id="63ba0-197">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-197">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="63ba0-198">決定在應用程式中，或列印到黑白印表機時，圖形會以黑白方式呈現。</span><span class="sxs-lookup"><span data-stu-id="63ba0-198">Determines how shape will render in black-and-white view in apps or when printed to black-and-white printers.</span></span> <span data-ttu-id="63ba0-199">值包括： **Color**、 **Auto**、 **灰階**、 **LightGrayScale**、 **InverseGray**、 **GrayOutline**、 **BlackTextAndLines**、 **systeminformation.highcontrast**、 **黑色**、 **白色**、 **Undrawn**。</span><span class="sxs-lookup"><span data-stu-id="63ba0-199">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="63ba0-200">預設值： **Auto**。</span><span class="sxs-lookup"><span data-stu-id="63ba0-200">Default: **Auto**.</span></span> |
| <span data-ttu-id="63ba0-201">BWNormal</span><span class="sxs-lookup"><span data-stu-id="63ba0-201">BWNormal</span></span>     | <span data-ttu-id="63ba0-202">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="63ba0-202">VgBlackWhiteMode.</span></span> <span data-ttu-id="63ba0-203">當 BWMode 為 Auto 時，會參考此屬性以瞭解如何以一般黑色和白色呈現圖形。</span><span class="sxs-lookup"><span data-stu-id="63ba0-203">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span> <span data-ttu-id="63ba0-204">值包括： **Color**、 **Auto**、 **灰階**、 **LightGrayScale**、 **InverseGray**、 **GrayOutline**、 **BlackTextAndLines**、 **systeminformation.highcontrast**、 **黑色**、 **白色**、 **Undrawn**。</span><span class="sxs-lookup"><span data-stu-id="63ba0-204">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="63ba0-205">預設值： **Auto**。</span><span class="sxs-lookup"><span data-stu-id="63ba0-205">Default: **Auto**.</span></span>                                                |
| <span data-ttu-id="63ba0-206">BWPure</span><span class="sxs-lookup"><span data-stu-id="63ba0-206">BWPure</span></span>       | <span data-ttu-id="63ba0-207">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="63ba0-207">VgBlackWhiteMode.</span></span> <span data-ttu-id="63ba0-208">當 BWMode 為 Auto 時，會參考此屬性以瞭解如何以純 B/W 呈現圖形。</span><span class="sxs-lookup"><span data-stu-id="63ba0-208">When BWMode is Auto, this property is consulted for how to render the shape in pure B/W.</span></span> <span data-ttu-id="63ba0-209">值包括： **Color**、 **Auto**、 **灰階**、 **LightGrayScale**、 **InverseGray**、 **GrayOutline**、 **BlackTextAndLines**、 **systeminformation.highcontrast**、 **黑色**、 **白色**、 **Undrawn**。</span><span class="sxs-lookup"><span data-stu-id="63ba0-209">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="63ba0-210">預設值： **Auto**。</span><span class="sxs-lookup"><span data-stu-id="63ba0-210">Default: **Auto**.</span></span>                                                              |
| <span data-ttu-id="63ba0-211">ChildShapes</span><span class="sxs-lookup"><span data-stu-id="63ba0-211">ChildShapes</span></span>  | <span data-ttu-id="63ba0-212">IVgGroupShapes.</span><span class="sxs-lookup"><span data-stu-id="63ba0-212">IVgGroupShapes.</span></span> <span data-ttu-id="63ba0-213">此群組中其他圖形的集合。</span><span class="sxs-lookup"><span data-stu-id="63ba0-213">A collection of other shapes in this group.</span></span> <span data-ttu-id="63ba0-214">此集合支援標準長度和專案方法。</span><span class="sxs-lookup"><span data-stu-id="63ba0-214">This collection supports the standard Length and Item methods.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="63ba0-215">Chromakey</span><span class="sxs-lookup"><span data-stu-id="63ba0-215">Chromakey</span></span>    | <span data-ttu-id="63ba0-216">[IVgColor](msdn-online-vml-ivgcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-216">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="63ba0-217">將會是透明的色彩值，並顯示圖形背後的任何事物。</span><span class="sxs-lookup"><span data-stu-id="63ba0-217">A color value that will be transparent and show anything behind the shape.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="63ba0-218">Control1</span><span class="sxs-lookup"><span data-stu-id="63ba0-218">Control1</span></span>     | <span data-ttu-id="63ba0-219">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-219">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="63ba0-220">曲線的控制點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-220">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="63ba0-221">Control2</span><span class="sxs-lookup"><span data-stu-id="63ba0-221">Control2</span></span>     | <span data-ttu-id="63ba0-222">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-222">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="63ba0-223">曲線的控制點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-223">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="63ba0-224">CoordOrigin</span><span class="sxs-lookup"><span data-stu-id="63ba0-224">CoordOrigin</span></span>  | <span data-ttu-id="63ba0-225">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) 容器矩形左上角的座標。</span><span class="sxs-lookup"><span data-stu-id="63ba0-225">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) The coordinates at the top left corner of the container rectangle.</span></span> <span data-ttu-id="63ba0-226">範圍從0到無限大。</span><span class="sxs-lookup"><span data-stu-id="63ba0-226">Range from 0 to infinity.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="63ba0-227">CoordSize</span><span class="sxs-lookup"><span data-stu-id="63ba0-227">CoordSize</span></span>    | <span data-ttu-id="63ba0-228">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-228">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="63ba0-229">此圖形之參考矩形內的座標空間的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-229">The width and height of the coordinate space inside the reference rectangle of this shape.</span></span> <span data-ttu-id="63ba0-230">如果未指定，則與矩形的寬度和高度相同。</span><span class="sxs-lookup"><span data-stu-id="63ba0-230">If it is not specified, it is the same as the width and height of the rectangle.</span></span> <span data-ttu-id="63ba0-231">範圍從0到無限大。</span><span class="sxs-lookup"><span data-stu-id="63ba0-231">Range from 0 to infinity.</span></span> <span data-ttu-id="63ba0-232">預設值： "1000，1000"。</span><span class="sxs-lookup"><span data-stu-id="63ba0-232">Default: "1000,1000".</span></span>                                                                                               |
| <span data-ttu-id="63ba0-233">EndAngle</span><span class="sxs-lookup"><span data-stu-id="63ba0-233">EndAngle</span></span>     | <span data-ttu-id="63ba0-234">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-234">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="63ba0-235">圖形的結束角度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-235">End angle of shape.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="63ba0-236">擠壓</span><span class="sxs-lookup"><span data-stu-id="63ba0-236">Extrusion</span></span>    | <span data-ttu-id="63ba0-237">IVgExtrusion.</span><span class="sxs-lookup"><span data-stu-id="63ba0-237">IVgExtrusion.</span></span> <span data-ttu-id="63ba0-238">指定此圖形的延伸物件值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-238">Specifies the Extrusion object value for this shape.</span></span> <span data-ttu-id="63ba0-239">如需詳細資訊，請參閱「 [延伸](msdn-online-vml-extrusion-element.md) 」元素。</span><span class="sxs-lookup"><span data-stu-id="63ba0-239">See the [Extrusion](msdn-online-vml-extrusion-element.md) element for details.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="63ba0-240">填滿</span><span class="sxs-lookup"><span data-stu-id="63ba0-240">Fill</span></span>         | <span data-ttu-id="63ba0-241">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="63ba0-241">VgFillFormat.</span></span> <span data-ttu-id="63ba0-242">指定此圖形的填滿值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-242">Specifies the fill value for this shape.</span></span> <span data-ttu-id="63ba0-243">如需詳細資訊，請參閱 [Fill](msdn-online-vml-fill-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="63ba0-243">See the [Fill](msdn-online-vml-fill-element.md) element for more details.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="63ba0-244">FillColor</span><span class="sxs-lookup"><span data-stu-id="63ba0-244">FillColor</span></span>    | <span data-ttu-id="63ba0-245">[IVgColor](msdn-online-vml-ivgcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-245">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="63ba0-246">要用來填滿此圖形路徑之筆刷的主要色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-246">The primary color of the brush to use to fill the path of this shape.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="63ba0-247">已</span><span class="sxs-lookup"><span data-stu-id="63ba0-247">Filled</span></span>       | <span data-ttu-id="63ba0-248">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-248">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-249">若為 True，則會填滿定義圖形的路徑。</span><span class="sxs-lookup"><span data-stu-id="63ba0-249">If True, the path defining the shape will be filled.</span></span> <span data-ttu-id="63ba0-250">根據預設，除非有指定更複雜填滿屬性的 Fill 子項目，否則它將會以純色填滿。</span><span class="sxs-lookup"><span data-stu-id="63ba0-250">By default, it will be filled using a solid color unless there is a Fill subelement that specifies more complex fill properties.</span></span> <span data-ttu-id="63ba0-251">如果為 False，則填滿是透明的。</span><span class="sxs-lookup"><span data-stu-id="63ba0-251">If False, the fill is transparent.</span></span>                                                                                                           |
| <span data-ttu-id="63ba0-252">翻轉</span><span class="sxs-lookup"><span data-stu-id="63ba0-252">Flip</span></span>         | <span data-ttu-id="63ba0-253">VgFlipOrientation.</span><span class="sxs-lookup"><span data-stu-id="63ba0-253">VgFlipOrientation.</span></span> <span data-ttu-id="63ba0-254">值為： X Y XY YX</span><span class="sxs-lookup"><span data-stu-id="63ba0-254">Values are: X Y XY YX</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="63ba0-255">ForceDash</span><span class="sxs-lookup"><span data-stu-id="63ba0-255">ForceDash</span></span>    | <span data-ttu-id="63ba0-256">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-256">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-257">指出當圖形沒有線條且沒有填滿時，應該呈現虛線外框。</span><span class="sxs-lookup"><span data-stu-id="63ba0-257">Indication that a dashed outline should be rendered when there is no line and no fill for a shape.</span></span> <span data-ttu-id="63ba0-258">這種行為通常適用于在編輯應用程式中顯示隱藏式圖形，因此可以在影像對應中加以選取和操作。</span><span class="sxs-lookup"><span data-stu-id="63ba0-258">This behavior is generally useful for making invisible shapes visible in editing applications so they can be selected and operated on, such as in an image map.</span></span>                                                                 |
| <span data-ttu-id="63ba0-259">公式</span><span class="sxs-lookup"><span data-stu-id="63ba0-259">Formulas</span></span>     | <span data-ttu-id="63ba0-260">IVgFormulas.</span><span class="sxs-lookup"><span data-stu-id="63ba0-260">IVgFormulas.</span></span> <span data-ttu-id="63ba0-261">定義圖形的公式陣列。</span><span class="sxs-lookup"><span data-stu-id="63ba0-261">An array of formulas that defines a shape.</span></span>                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="63ba0-262">寄件者</span><span class="sxs-lookup"><span data-stu-id="63ba0-262">From</span></span>         | <span data-ttu-id="63ba0-263">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-263">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="63ba0-264">行的起點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-264">Starting point of line.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="63ba0-265">Href</span><span class="sxs-lookup"><span data-stu-id="63ba0-265">HRef</span></span>         | <span data-ttu-id="63ba0-266">[字串](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-266">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-267">如果按一下此圖形，要跳到的 URL。</span><span class="sxs-lookup"><span data-stu-id="63ba0-267">The URL to jump to if this shape is clicked.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="63ba0-268">ImageData</span><span class="sxs-lookup"><span data-stu-id="63ba0-268">ImageData</span></span>    | <span data-ttu-id="63ba0-269">IVgImageData.</span><span class="sxs-lookup"><span data-stu-id="63ba0-269">IVgImageData.</span></span> <span data-ttu-id="63ba0-270">影像資訊（如果圖形是圖片的話）。</span><span class="sxs-lookup"><span data-stu-id="63ba0-270">Image information if the shape is a picture.</span></span> <span data-ttu-id="63ba0-271">如需詳細資訊，請參閱 ImageData 元素。</span><span class="sxs-lookup"><span data-stu-id="63ba0-271">See the ImageData element for more information.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="63ba0-272">OnEd</span><span class="sxs-lookup"><span data-stu-id="63ba0-272">OnEd</span></span>         | <span data-ttu-id="63ba0-273">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-273">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-274">隱藏左上角和右下方以外的所有控制碼，如同直線線段的控制碼一樣。</span><span class="sxs-lookup"><span data-stu-id="63ba0-274">Hides all handles except the top left and bottom right, as in the handles for a straight line segment.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="63ba0-275">不透明度</span><span class="sxs-lookup"><span data-stu-id="63ba0-275">Opacity</span></span>      | <span data-ttu-id="63ba0-276">[VgFraction](msdn-online-vml-vgfraction-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-276">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="63ba0-277">整個圖形的不透明度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-277">The opacity of the entire shape.</span></span> <span data-ttu-id="63ba0-278">介於0.0 到1.0 之間的數位。</span><span class="sxs-lookup"><span data-stu-id="63ba0-278">A number between 0.0 and 1.0.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="63ba0-279">路徑</span><span class="sxs-lookup"><span data-stu-id="63ba0-279">Path</span></span>         | <span data-ttu-id="63ba0-280">IVgPath.</span><span class="sxs-lookup"><span data-stu-id="63ba0-280">IVgPath.</span></span> <span data-ttu-id="63ba0-281">字串，包含定義路徑的命令。</span><span class="sxs-lookup"><span data-stu-id="63ba0-281">A string containing the commands that define the path.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="63ba0-282">點</span><span class="sxs-lookup"><span data-stu-id="63ba0-282">Points</span></span>       | <span data-ttu-id="63ba0-283">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-283">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span></span> <span data-ttu-id="63ba0-284">定義圖形的點集合。</span><span class="sxs-lookup"><span data-stu-id="63ba0-284">A collection of points defining a shape.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="63ba0-285">列印</span><span class="sxs-lookup"><span data-stu-id="63ba0-285">Print</span></span>        | <span data-ttu-id="63ba0-286">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-286">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-287">若為 True，表示要列印此圖形。</span><span class="sxs-lookup"><span data-stu-id="63ba0-287">If True, this shape is meant to be printed.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="63ba0-288">旋轉</span><span class="sxs-lookup"><span data-stu-id="63ba0-288">Rotation</span></span>     | <span data-ttu-id="63ba0-289">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-289">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="63ba0-290">設定圖形的旋轉。</span><span class="sxs-lookup"><span data-stu-id="63ba0-290">Sets rotation of shape.</span></span> <span data-ttu-id="63ba0-291">值會傳播至圖形樣式。</span><span class="sxs-lookup"><span data-stu-id="63ba0-291">Value is propagated to the shape style.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="63ba0-292">調整</span><span class="sxs-lookup"><span data-stu-id="63ba0-292">Scale</span></span>        | <span data-ttu-id="63ba0-293">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-293">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="63ba0-294">圖形的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="63ba0-294">Scale of shape.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="63ba0-295">陰影</span><span class="sxs-lookup"><span data-stu-id="63ba0-295">Shadow</span></span>       | <span data-ttu-id="63ba0-296">IVgShadow.</span><span class="sxs-lookup"><span data-stu-id="63ba0-296">IVgShadow.</span></span> <span data-ttu-id="63ba0-297">指定此圖形的陰影。</span><span class="sxs-lookup"><span data-stu-id="63ba0-297">Specifies the shadow for this shape.</span></span> <span data-ttu-id="63ba0-298">如需詳細資料，請參閱 [Shadow](msdn-online-vml-shadow-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="63ba0-298">See the [Shadow](msdn-online-vml-shadow-element.md) element for details.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="63ba0-299">Spt</span><span class="sxs-lookup"><span data-stu-id="63ba0-299">Spt</span></span>          | <span data-ttu-id="63ba0-300">保留的。</span><span class="sxs-lookup"><span data-stu-id="63ba0-300">Reserved.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="63ba0-301">>startangle</span><span class="sxs-lookup"><span data-stu-id="63ba0-301">StartAngle</span></span>   | <span data-ttu-id="63ba0-302">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-302">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="63ba0-303">圖形的開始角度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-303">Start angle of shape.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="63ba0-304">筆勢</span><span class="sxs-lookup"><span data-stu-id="63ba0-304">Stroke</span></span>       | <span data-ttu-id="63ba0-305">VgStrokeFormat.</span><span class="sxs-lookup"><span data-stu-id="63ba0-305">VgStrokeFormat.</span></span> <span data-ttu-id="63ba0-306">如需詳細資料，請參閱 Stroke 元素。</span><span class="sxs-lookup"><span data-stu-id="63ba0-306">See Stroke element for details.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="63ba0-307">StrokeColor</span><span class="sxs-lookup"><span data-stu-id="63ba0-307">StrokeColor</span></span>  | <span data-ttu-id="63ba0-308">[IVgColor](msdn-online-vml-ivgcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-308">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="63ba0-309">用來將此圖形的路徑進行筆劃之筆刷的主要色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-309">The primary color of the brush to use to stroke the path of this shape.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="63ba0-310">撫摸</span><span class="sxs-lookup"><span data-stu-id="63ba0-310">Stroked</span></span>      | <span data-ttu-id="63ba0-311">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-311">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-312">若為 True，則會將定義圖形的路徑進行筆劃。</span><span class="sxs-lookup"><span data-stu-id="63ba0-312">If True, the path defining the shape will be stroked.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="63ba0-313">StrokeWeight</span><span class="sxs-lookup"><span data-stu-id="63ba0-313">StrokeWeight</span></span> | <span data-ttu-id="63ba0-314">[VGLength](msdn-online-vml-vglength.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-314">[VGLength](msdn-online-vml-vglength.md).</span></span> <span data-ttu-id="63ba0-315">用來對路徑進行筆劃的筆刷寬度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-315">The width of the brush to use to stroke the path.</span></span> <span data-ttu-id="63ba0-316">介於0與1584之間的範圍。</span><span class="sxs-lookup"><span data-stu-id="63ba0-316">Ranges between 0 and 1584.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="63ba0-317">TextPath</span><span class="sxs-lookup"><span data-stu-id="63ba0-317">TextPath</span></span>     | <span data-ttu-id="63ba0-318">IVgTextPath.</span><span class="sxs-lookup"><span data-stu-id="63ba0-318">IVgTextPath.</span></span> <span data-ttu-id="63ba0-319">指定圖形的 TextPath 物件。</span><span class="sxs-lookup"><span data-stu-id="63ba0-319">Specifies the TextPath object of the shape.</span></span> <span data-ttu-id="63ba0-320">如需詳細資訊，請參閱 [TextPath](msdn-online-vml-textpath-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="63ba0-320">See the [TextPath](msdn-online-vml-textpath-element.md) element for more information.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="63ba0-321">收件者</span><span class="sxs-lookup"><span data-stu-id="63ba0-321">To</span></span>           | <span data-ttu-id="63ba0-322">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-322">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="63ba0-323">行的結束點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-323">End point of line.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="63ba0-324">類型</span><span class="sxs-lookup"><span data-stu-id="63ba0-324">Type</span></span>         | <span data-ttu-id="63ba0-325">字串。</span><span class="sxs-lookup"><span data-stu-id="63ba0-325">String.</span></span> <span data-ttu-id="63ba0-326">圖形類型。</span><span class="sxs-lookup"><span data-stu-id="63ba0-326">Type of shape.</span></span>                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a><span data-ttu-id="63ba0-327">Shape 元素的子項目</span><span class="sxs-lookup"><span data-stu-id="63ba0-327">Subelements of the Shape Element</span></span>

<span data-ttu-id="63ba0-328">下列子項目是 VML 物件模型的一部分。</span><span class="sxs-lookup"><span data-stu-id="63ba0-328">The following subelements are part of the VML object model.</span></span>

-   [<span data-ttu-id="63ba0-329">背景</span><span class="sxs-lookup"><span data-stu-id="63ba0-329">Background</span></span>](#background-element)
-   [<span data-ttu-id="63ba0-330">擠壓</span><span class="sxs-lookup"><span data-stu-id="63ba0-330">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="63ba0-331">填滿</span><span class="sxs-lookup"><span data-stu-id="63ba0-331">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="63ba0-332">群組</span><span class="sxs-lookup"><span data-stu-id="63ba0-332">Group</span></span>](#group-element)
-   [<span data-ttu-id="63ba0-333">Imagedata</span><span class="sxs-lookup"><span data-stu-id="63ba0-333">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="63ba0-334">路徑</span><span class="sxs-lookup"><span data-stu-id="63ba0-334">Path</span></span>](#path-element)
-   [<span data-ttu-id="63ba0-335">Shadow</span><span class="sxs-lookup"><span data-stu-id="63ba0-335">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="63ba0-336">斜</span><span class="sxs-lookup"><span data-stu-id="63ba0-336">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="63ba0-337">中風</span><span class="sxs-lookup"><span data-stu-id="63ba0-337">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="63ba0-338">TextPath</span><span class="sxs-lookup"><span data-stu-id="63ba0-338">TextPath</span></span>](#textpath-element)

### <a name="background-element"></a><span data-ttu-id="63ba0-339">Background 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-339">Background element</span></span>

<span data-ttu-id="63ba0-340">描述使用 VML 填滿的頁面背景填滿。</span><span class="sxs-lookup"><span data-stu-id="63ba0-340">Describes the fill of the background of a page using VML fills.</span></span>


|   <span data-ttu-id="63ba0-341">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-341">Attribute</span></span>        |   <span data-ttu-id="63ba0-342">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-342">Description</span></span>                                                                                                                                                                                      |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba0-343">BWMode</span><span class="sxs-lookup"><span data-stu-id="63ba0-343">BWMode</span></span>    | <span data-ttu-id="63ba0-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="63ba0-345">決定圖形在應用程式中的黑白外觀或列印時的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="63ba0-345">Determines how shape will render in black-and-white view in applications or when printed.</span></span>                                     |
| <span data-ttu-id="63ba0-346">BWNormal</span><span class="sxs-lookup"><span data-stu-id="63ba0-346">BWNormal</span></span>  | <span data-ttu-id="63ba0-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="63ba0-348">當 BWMode 為 Auto 時，會參考此屬性以瞭解如何以一般黑色和白色呈現圖形。</span><span class="sxs-lookup"><span data-stu-id="63ba0-348">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span>                        |
| <span data-ttu-id="63ba0-349">BWPure</span><span class="sxs-lookup"><span data-stu-id="63ba0-349">BWPure</span></span>    | <span data-ttu-id="63ba0-350">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-350">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="63ba0-351">當 BWMode 為 Auto 時，會參考此屬性以瞭解如何以純黑色和白色呈現圖形。</span><span class="sxs-lookup"><span data-stu-id="63ba0-351">When BWMode is Auto, this property is consulted for how to render the shape in pure black and white.</span></span>                          |
| <span data-ttu-id="63ba0-352">填滿</span><span class="sxs-lookup"><span data-stu-id="63ba0-352">Fill</span></span>      | <span data-ttu-id="63ba0-353">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="63ba0-353">VgFillFormat.</span></span> <span data-ttu-id="63ba0-354">指定此圖形的填滿。</span><span class="sxs-lookup"><span data-stu-id="63ba0-354">Specifies the fill for this shape.</span></span> <span data-ttu-id="63ba0-355">如需詳細資訊，請參閱 [Fill](msdn-online-vml-fill-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="63ba0-355">See [Fill](msdn-online-vml-fill-element.md) element for more information.</span></span>                                                             |
| <span data-ttu-id="63ba0-356">FillColor</span><span class="sxs-lookup"><span data-stu-id="63ba0-356">FillColor</span></span> | <span data-ttu-id="63ba0-357">[IVgColor](msdn-online-vml-ivgcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-357">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="63ba0-358">要用來填滿此圖形路徑之筆刷的主要色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-358">The primary color of the brush to use to fill the path of this shape.</span></span> <span data-ttu-id="63ba0-359">Fill 元素中的色彩值重複。</span><span class="sxs-lookup"><span data-stu-id="63ba0-359">Duplicate of the Color value in the Fill element.</span></span> <span data-ttu-id="63ba0-360">預設為白色。</span><span class="sxs-lookup"><span data-stu-id="63ba0-360">The default is white.</span></span> |



 

### <a name="extrusion-element"></a><span data-ttu-id="63ba0-361">延伸元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-361">Extrusion element</span></span>

<span data-ttu-id="63ba0-362">描述圖形的立體延伸。</span><span class="sxs-lookup"><span data-stu-id="63ba0-362">Describes a 3-D extrusion of the shape.</span></span>

<span data-ttu-id="63ba0-363">**屬性**</span><span class="sxs-lookup"><span data-stu-id="63ba0-363">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-364">AutoRotationCenter</span><span class="sxs-lookup"><span data-stu-id="63ba0-364">AutoRotationCenter</span></span></td>
<td><span data-ttu-id="63ba0-365"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-365"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="63ba0-366">若為 True，則3D 物件群組的旋轉中心 (事實上，群組中只有一個物件) 會自動判斷為群組的中心;否則，它是由 RotationCenter 參數決定，這是圖形的一部分，0、0、0是中心。</span><span class="sxs-lookup"><span data-stu-id="63ba0-366">If True, the center of rotation of the group of 3-D objects (in fact there is only ever one object in the group) is determined automatically to be the center of the group; otherwise it is determined by the RotationCenter parameters, which are a fraction of the shape with 0,0,0 being the center.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-367">BackDepth</span><span class="sxs-lookup"><span data-stu-id="63ba0-367">BackDepth</span></span></td>
<td><span data-ttu-id="63ba0-368"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-368"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span></span> <span data-ttu-id="63ba0-369">反向拉伸的數量。</span><span class="sxs-lookup"><span data-stu-id="63ba0-369">Amount of backward extrusion.</span></span> <span data-ttu-id="63ba0-370">範圍從0到32767。</span><span class="sxs-lookup"><span data-stu-id="63ba0-370">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-371">亮度</span><span class="sxs-lookup"><span data-stu-id="63ba0-371">Brightness</span></span></td>
<td><span data-ttu-id="63ba0-372"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-372"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="63ba0-373">場景的整體亮度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-373">Overall brightness of the scene.</span></span> <span data-ttu-id="63ba0-374">預設值為 &quot; 20000 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-374">Default is &quot;20,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-375">Color</span><span class="sxs-lookup"><span data-stu-id="63ba0-375">Color</span></span></td>
<td><span data-ttu-id="63ba0-376"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-376"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="63ba0-377">拉伸的色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-377">The color of the extrusion.</span></span> <span data-ttu-id="63ba0-378">只有在 ColorMode 為 Custom 時才會使用。</span><span class="sxs-lookup"><span data-stu-id="63ba0-378">Only used if ColorMode is Custom.</span></span> <span data-ttu-id="63ba0-379">否則，會自動將 [拉伸效果] 色彩設定為與 FillColor 相同。</span><span class="sxs-lookup"><span data-stu-id="63ba0-379">Otherwise, Auto sets the extrusion effect color to the same as FillColor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-380">ColorMode</span><span class="sxs-lookup"><span data-stu-id="63ba0-380">ColorMode</span></span></td>
<td><span data-ttu-id="63ba0-381">Vg3DColorMode.</span><span class="sxs-lookup"><span data-stu-id="63ba0-381">Vg3DColorMode.</span></span> <span data-ttu-id="63ba0-382">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-382">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-383">Auto (預設值)</span><span class="sxs-lookup"><span data-stu-id="63ba0-383">Auto (default)</span></span></li>
<li><span data-ttu-id="63ba0-384">自訂</span><span class="sxs-lookup"><span data-stu-id="63ba0-384">Custom</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-385">Diffusity</span><span class="sxs-lookup"><span data-stu-id="63ba0-385">Diffusity</span></span></td>
<td><span data-ttu-id="63ba0-386"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-386"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="63ba0-387">要擴散的事件比率反映燈光。</span><span class="sxs-lookup"><span data-stu-id="63ba0-387">The ratio of incident to diffusely reflected light.</span></span> <span data-ttu-id="63ba0-388">小於1.0 的值是正常的，但大於1的值可能會產生有趣的效果。</span><span class="sxs-lookup"><span data-stu-id="63ba0-388">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-389">Edge</span><span class="sxs-lookup"><span data-stu-id="63ba0-389">Edge</span></span></td>
<td><span data-ttu-id="63ba0-390"><a href="msdn-online-vml-vglength.md">VgLength</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-390"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="63ba0-391">設定模擬圓角斜面邊緣的大小。</span><span class="sxs-lookup"><span data-stu-id="63ba0-391">Sets the size of a simulated rounded beveled edge.</span></span> <span data-ttu-id="63ba0-392">浮點數中的範圍介於0到32767之間。</span><span class="sxs-lookup"><span data-stu-id="63ba0-392">Ranges from 0 to 32767 in floating point pts.</span></span> <span data-ttu-id="63ba0-393">預設值為 &quot; 1pt &quot; 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-393">Default is &quot;1pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-394">Facet</span><span class="sxs-lookup"><span data-stu-id="63ba0-394">Facet</span></span></td>
<td><span data-ttu-id="63ba0-395"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-395"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="63ba0-396">設定場景的 facet。</span><span class="sxs-lookup"><span data-stu-id="63ba0-396">Sets the facet of the scene.</span></span> <span data-ttu-id="63ba0-397">預設值為 &quot; 30000 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-397">Default is &quot;30,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-398">ForeDepth</span><span class="sxs-lookup"><span data-stu-id="63ba0-398">ForeDepth</span></span></td>
<td><span data-ttu-id="63ba0-399"><a href="msdn-online-vml-vglength.md">VgLength</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-399"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="63ba0-400">向前延伸的數量。</span><span class="sxs-lookup"><span data-stu-id="63ba0-400">Amount of forward extrusion.</span></span> <span data-ttu-id="63ba0-401">範圍從0到32767。</span><span class="sxs-lookup"><span data-stu-id="63ba0-401">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-402">LightFace</span><span class="sxs-lookup"><span data-stu-id="63ba0-402">LightFace</span></span></td>
<td><span data-ttu-id="63ba0-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="63ba0-404">Determimes 物件的正面臉部是否會回應3-d 照明的變更，例如，當物件旋轉時。</span><span class="sxs-lookup"><span data-stu-id="63ba0-404">Determimes whether the front face of the object will respond to changes in the 3-D lighting, e.g., when an object rotates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-405">LightHarsh</span><span class="sxs-lookup"><span data-stu-id="63ba0-405">LightHarsh</span></span></td>
<td><span data-ttu-id="63ba0-406"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-406"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="63ba0-407">主要光源的光源。</span><span class="sxs-lookup"><span data-stu-id="63ba0-407">Harsh lighting for the primary light source.</span></span> <span data-ttu-id="63ba0-408">預設值是 False。</span><span class="sxs-lookup"><span data-stu-id="63ba0-408">Default is False.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-409">LightHarsh2</span><span class="sxs-lookup"><span data-stu-id="63ba0-409">LightHarsh2</span></span></td>
<td><span data-ttu-id="63ba0-410"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-410"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="63ba0-411">次要燈光來源的粗糙光源。</span><span class="sxs-lookup"><span data-stu-id="63ba0-411">Harsh lighting for the secondary light source.</span></span> <span data-ttu-id="63ba0-412">預設值是 False。</span><span class="sxs-lookup"><span data-stu-id="63ba0-412">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-413">LightLevel</span><span class="sxs-lookup"><span data-stu-id="63ba0-413">LightLevel</span></span></td>
<td><span data-ttu-id="63ba0-414"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-414"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="63ba0-415">主要燈光來源的濃度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-415">Intensity of the primary light source.</span></span> <span data-ttu-id="63ba0-416">預設值為 &quot; 38000 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-416">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-417">LightLevel2</span><span class="sxs-lookup"><span data-stu-id="63ba0-417">LightLevel2</span></span></td>
<td><span data-ttu-id="63ba0-418"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-418"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="63ba0-419">次要燈光來源的濃度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-419">Intensity of the secondary light source.</span></span> <span data-ttu-id="63ba0-420">預設值為 &quot; 38000 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-420">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-421">LightPosition</span><span class="sxs-lookup"><span data-stu-id="63ba0-421">LightPosition</span></span></td>
<td><span data-ttu-id="63ba0-422">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="63ba0-422">Vector3D.</span></span> <span data-ttu-id="63ba0-423">主要光源來源的位置。</span><span class="sxs-lookup"><span data-stu-id="63ba0-423">Position of the primary light source.</span></span> <span data-ttu-id="63ba0-424">預設值為 &quot; 50000、0、10000 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-424">Default is &quot;50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-425">LightPosition2</span><span class="sxs-lookup"><span data-stu-id="63ba0-425">LightPosition2</span></span></td>
<td><span data-ttu-id="63ba0-426">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="63ba0-426">Vector3D.</span></span> <span data-ttu-id="63ba0-427">次要燈光來源的位置。</span><span class="sxs-lookup"><span data-stu-id="63ba0-427">Position of the secondary light source.</span></span> <span data-ttu-id="63ba0-428">預設值為 &quot; -50000、0、10000 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-428">Default is &quot;-50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-429">LockRotationCenter</span><span class="sxs-lookup"><span data-stu-id="63ba0-429">LockRotationCenter</span></span></td>
<td><span data-ttu-id="63ba0-430"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-430"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="63ba0-431">&quot;Lockrotationcenter &quot; 表示群組的旋轉會依照頁面上 y 軸的旋轉角度 [1] 角度定義，後面接著 X 軸的旋轉角度 [0] 角度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-431">&quot;Lockrotationcenter&quot; means that the rotation of the group is defined to be by rotation-angle[1] degrees about the y-axis on the page followed by rotation-angle[0] degrees about the x-axis.</span></span> <span data-ttu-id="63ba0-432">當 LockRotationCenter 為 False 時，就會根據方向定義的向量，將旋轉定義為面向角度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-432">When LockRotationCenter is False, the rotation is defined to be by orientation-angle degrees about the vector defined by orientation.</span></span> <span data-ttu-id="63ba0-433">因此，例如，lockrotationcenter = false orientationangle = 45 方向 = (0，1，0) 相當於 lockrotationcenter = true rotationangle = (0，45) 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-433">So, for example, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) is equivalent to lockrotationcenter=true rotationangle=(0,45).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-434">金屬</span><span class="sxs-lookup"><span data-stu-id="63ba0-434">Metal</span></span></td>
<td><span data-ttu-id="63ba0-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="63ba0-436">使反射反映的光線成為材質色彩，而不是光線來源色彩，讓物件看起來更材質。</span><span class="sxs-lookup"><span data-stu-id="63ba0-436">Causes specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-437">開啟</span><span class="sxs-lookup"><span data-stu-id="63ba0-437">On</span></span></td>
<td><span data-ttu-id="63ba0-438"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-438"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="63ba0-439">開啟和關閉延伸效果的顯示。</span><span class="sxs-lookup"><span data-stu-id="63ba0-439">Turns the display of the extrusion effect on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-440">Orientation</span><span class="sxs-lookup"><span data-stu-id="63ba0-440">Orientation</span></span></td>
<td><span data-ttu-id="63ba0-441">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="63ba0-441">Vector3D.</span></span> <span data-ttu-id="63ba0-442">攝影機的方向。</span><span class="sxs-lookup"><span data-stu-id="63ba0-442">Orientation of the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-443">OrientationAngle</span><span class="sxs-lookup"><span data-stu-id="63ba0-443">OrientationAngle</span></span></td>
<td><span data-ttu-id="63ba0-444"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-444"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="63ba0-445">攝影機方向與 xy 平面之間的角度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-445">Angle between the orientation of the camera and the xy plane.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-446">飛機</span><span class="sxs-lookup"><span data-stu-id="63ba0-446">Plane</span></span></td>
<td><span data-ttu-id="63ba0-447">Vg3DExtrudePlane.</span><span class="sxs-lookup"><span data-stu-id="63ba0-447">Vg3DExtrudePlane.</span></span> <span data-ttu-id="63ba0-448">允許從平面與螢幕平面垂直的拉伸。</span><span class="sxs-lookup"><span data-stu-id="63ba0-448">Allows extrusion from planes orthogonal to the screen plane.</span></span> <span data-ttu-id="63ba0-449">需要以繪圖單位（而非 emus）指定 ForeDepth 和 BackDepth。</span><span class="sxs-lookup"><span data-stu-id="63ba0-449">Requires ForeDepth and BackDepth to be specified in drawing units instead of emus.</span></span> <span data-ttu-id="63ba0-450">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-450">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-451">Xy</span><span class="sxs-lookup"><span data-stu-id="63ba0-451">XY</span></span></li>
<li><span data-ttu-id="63ba0-452">Zx</span><span class="sxs-lookup"><span data-stu-id="63ba0-452">ZX</span></span></li>
<li><span data-ttu-id="63ba0-453">YZ</span><span class="sxs-lookup"><span data-stu-id="63ba0-453">YZ</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-454">轉譯</span><span class="sxs-lookup"><span data-stu-id="63ba0-454">Render</span></span></td>
<td><span data-ttu-id="63ba0-455">Vg3DRenderMode.</span><span class="sxs-lookup"><span data-stu-id="63ba0-455">Vg3DRenderMode.</span></span> <span data-ttu-id="63ba0-456">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-456">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-457">Solid (預設值)</span><span class="sxs-lookup"><span data-stu-id="63ba0-457">Solid (default)</span></span></li>
<li><span data-ttu-id="63ba0-458">著色</span><span class="sxs-lookup"><span data-stu-id="63ba0-458">WireFrame</span></span></li>
<li><span data-ttu-id="63ba0-459">BoundingCube</span><span class="sxs-lookup"><span data-stu-id="63ba0-459">BoundingCube</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-460">RotationAngle</span><span class="sxs-lookup"><span data-stu-id="63ba0-460">RotationAngle</span></span></td>
<td><span data-ttu-id="63ba0-461"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-461"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="63ba0-462">System.windows.media.skewtransform.anglex、System.windows.media.skewtransform.angley 或 AngleZ 是由 ShapeRotation 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="63ba0-462">AngleX, AngleY, or AngleZ is controlled by the ShapeRotation attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-463">RotationCenter</span><span class="sxs-lookup"><span data-stu-id="63ba0-463">RotationCenter</span></span></td>
<td><span data-ttu-id="63ba0-464">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="63ba0-464">Vector3D.</span></span> <span data-ttu-id="63ba0-465">旋轉的中心。</span><span class="sxs-lookup"><span data-stu-id="63ba0-465">Center of rotation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-466">增</span><span class="sxs-lookup"><span data-stu-id="63ba0-466">Shininess</span></span></td>
<td><span data-ttu-id="63ba0-467"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-467"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="63ba0-468">決定集中或分佈反射反映的方式。</span><span class="sxs-lookup"><span data-stu-id="63ba0-468">Determines how concentrated or spread out specular reflection is.</span></span> <span data-ttu-id="63ba0-469">高值會是8到10，而且近似于鏡像，而較低的值會是2至3，而且大約 sequined 服裝。</span><span class="sxs-lookup"><span data-stu-id="63ba0-469">A high value would be 8 to 10 and would approximate a mirror, and a low value would be 2 to 3 and would approximate sequined clothing.</span></span> <span data-ttu-id="63ba0-470">建議使用3到7之間的值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-470">Values of 3 to 7 are recommended.</span></span> <span data-ttu-id="63ba0-471">較高的值會反映出燈燈的來源。</span><span class="sxs-lookup"><span data-stu-id="63ba0-471">High values will reflect pinpoint light sources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-472">SkewAmt</span><span class="sxs-lookup"><span data-stu-id="63ba0-472">SkewAmt</span></span></td>
<td><span data-ttu-id="63ba0-473"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-473"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span></span> <span data-ttu-id="63ba0-474">如果 Type 是 Parallel，屬性會決定扭曲量。</span><span class="sxs-lookup"><span data-stu-id="63ba0-474">If Type is Parallel, attribute determines the amount of skew.</span></span> <span data-ttu-id="63ba0-475">範圍從0到100。</span><span class="sxs-lookup"><span data-stu-id="63ba0-475">Ranges from 0 to 100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-476">SkewAngle</span><span class="sxs-lookup"><span data-stu-id="63ba0-476">SkewAngle</span></span></td>
<td><span data-ttu-id="63ba0-477"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-477"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="63ba0-478">如果 Type 是 Parallel，屬性會決定扭曲的程度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-478">If Type is Parallel, attribute determines the degree of skew.</span></span> <span data-ttu-id="63ba0-479">預設值為 &quot; -45 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-479">Default is &quot;-45&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-480">Specularity</span><span class="sxs-lookup"><span data-stu-id="63ba0-480">Specularity</span></span></td>
<td><span data-ttu-id="63ba0-481"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-481"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="63ba0-482">要反射的事件比率反映燈光。</span><span class="sxs-lookup"><span data-stu-id="63ba0-482">The ratio of incident to specularly reflected light.</span></span> <span data-ttu-id="63ba0-483">小於1.0 的值是正常的，但大於1的值可能會產生有趣的效果。</span><span class="sxs-lookup"><span data-stu-id="63ba0-483">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-484">類型</span><span class="sxs-lookup"><span data-stu-id="63ba0-484">Type</span></span></td>
<td><span data-ttu-id="63ba0-485">VgExtrusionType.</span><span class="sxs-lookup"><span data-stu-id="63ba0-485">VgExtrusionType.</span></span> <span data-ttu-id="63ba0-486">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-486">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-487">平行 (預設) </span><span class="sxs-lookup"><span data-stu-id="63ba0-487">Parallel (default)</span></span></li>
<li><span data-ttu-id="63ba0-488">檢視方塊</span><span class="sxs-lookup"><span data-stu-id="63ba0-488">Perspective</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-489">觀點</span><span class="sxs-lookup"><span data-stu-id="63ba0-489">Viewpoint</span></span></td>
<td><span data-ttu-id="63ba0-490">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="63ba0-490">Vector3D.</span></span> <span data-ttu-id="63ba0-491">從中查看場景的位置。</span><span class="sxs-lookup"><span data-stu-id="63ba0-491">The point where the scene is being viewed from.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-492">ViewpointOrigin</span><span class="sxs-lookup"><span data-stu-id="63ba0-492">ViewpointOrigin</span></span></td>
<td><span data-ttu-id="63ba0-493"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-493"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="63ba0-494">可以有從0.5 到-0.5 的值，以定點陣圖形周框方塊內的觀點原點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-494">Can have values from 0.5 to -0.5 to position the origin of the viewpoint within the shape bounding box.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a><span data-ttu-id="63ba0-495">Fill 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-495">Fill element</span></span>

<span data-ttu-id="63ba0-496">說明如何針對填滿較純色的填滿路徑。</span><span class="sxs-lookup"><span data-stu-id="63ba0-496">Describes how a path should be filled for fills more complex than a solid color.</span></span>

<span data-ttu-id="63ba0-497">**屬性**</span><span class="sxs-lookup"><span data-stu-id="63ba0-497">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-498">AlignShape</span><span class="sxs-lookup"><span data-stu-id="63ba0-498">AlignShape</span></span></td>
<td><span data-ttu-id="63ba0-499"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-499"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="63ba0-500">將影像與圖形對齊。</span><span class="sxs-lookup"><span data-stu-id="63ba0-500">Align the image with the shape.</span></span> <span data-ttu-id="63ba0-501">如果為 False，則會將影像與視窗對齊。</span><span class="sxs-lookup"><span data-stu-id="63ba0-501">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-502">角度</span><span class="sxs-lookup"><span data-stu-id="63ba0-502">Angle</span></span></td>
<td><span data-ttu-id="63ba0-503"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-503"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="63ba0-504">漸層沿著的角度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-504">The angle along which the gradient goes.</span></span> <span data-ttu-id="63ba0-505">0度是沿著水準軸從左至右。</span><span class="sxs-lookup"><span data-stu-id="63ba0-505">0 degrees is along the horizontal axis from left to right.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-506">層面</span><span class="sxs-lookup"><span data-stu-id="63ba0-506">Aspect</span></span></td>
<td><span data-ttu-id="63ba0-507"><strong>VgAspectType</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-507"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="63ba0-508">ImageSize 屬性將會調整，以保留影像的外觀。</span><span class="sxs-lookup"><span data-stu-id="63ba0-508">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="63ba0-509">數值包括：</span><span class="sxs-lookup"><span data-stu-id="63ba0-509">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="63ba0-510">值</span><span class="sxs-lookup"><span data-stu-id="63ba0-510">Value</span></span></th>
<th><span data-ttu-id="63ba0-511">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-511">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-512">忽略</span><span class="sxs-lookup"><span data-stu-id="63ba0-512">Ignore</span></span></td>
<td><span data-ttu-id="63ba0-513">略過外觀問題。</span><span class="sxs-lookup"><span data-stu-id="63ba0-513">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-514">至少</span><span class="sxs-lookup"><span data-stu-id="63ba0-514">AtLeast</span></span></td>
<td><span data-ttu-id="63ba0-515">映射大小至少與影像大小一樣大。</span><span class="sxs-lookup"><span data-stu-id="63ba0-515">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-516">有</span><span class="sxs-lookup"><span data-stu-id="63ba0-516">AtMost</span></span></td>
<td><span data-ttu-id="63ba0-517">影像的大小不會大於影像大小。</span><span class="sxs-lookup"><span data-stu-id="63ba0-517">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-518">Color</span><span class="sxs-lookup"><span data-stu-id="63ba0-518">Color</span></span></td>
<td><span data-ttu-id="63ba0-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> 主要填滿色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> The main fill color.</span></span> <span data-ttu-id="63ba0-520">與 shape 中的 FillColor 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="63ba0-520">Same as FillColor attribute in shape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-521">Color2</span><span class="sxs-lookup"><span data-stu-id="63ba0-521">Color2</span></span></td>
<td><span data-ttu-id="63ba0-522"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-522"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="63ba0-523">當影像類型為模式或漸層填滿時，填滿的次要色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-523">The secondary color for a fill when image type is Pattern or a gradient fill.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-524">色彩</span><span class="sxs-lookup"><span data-stu-id="63ba0-524">Colors</span></span></td>
<td><span data-ttu-id="63ba0-525"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-525"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span></span> <span data-ttu-id="63ba0-526">漸層中的中繼色彩及其沿著漸層的相對位置，例如 &quot; 30% 紅色、70% 藍色、90% 綠色 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-526">Intermediate colors in the gradient and their relative positions along the gradient, e.g., &quot;30% red, 70% blue, 90% green&quot;.</span></span> <span data-ttu-id="63ba0-527">圖形) 中的主要色彩 (色彩屬性為0%，次要色彩 (Color2 屬性) 為100%。</span><span class="sxs-lookup"><span data-stu-id="63ba0-527">Primary color (Color attribute in shape) is 0% and secondary color (Color2 attribute) is 100%.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-528">焦點</span><span class="sxs-lookup"><span data-stu-id="63ba0-528">Focus</span></span></td>
<td><span data-ttu-id="63ba0-529"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-529"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span></span> <span data-ttu-id="63ba0-530">線性漸層填滿的焦點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-530">Focal point for linear gradient fill.</span></span> <span data-ttu-id="63ba0-531">值從-100 到 + 100。</span><span class="sxs-lookup"><span data-stu-id="63ba0-531">Values go from -100 to +100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-532">FocusPosition</span><span class="sxs-lookup"><span data-stu-id="63ba0-532">FocusPosition</span></span></td>
<td><span data-ttu-id="63ba0-533"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-533"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="63ba0-534">放射狀漸層的最內部矩形位置。</span><span class="sxs-lookup"><span data-stu-id="63ba0-534">Position of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="63ba0-535">向量是圖形寬度和高度 (0.0-1.0) 的分數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-535">The vector is a fraction (0.0 - 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-536">FocusSize</span><span class="sxs-lookup"><span data-stu-id="63ba0-536">FocusSize</span></span></td>
<td><span data-ttu-id="63ba0-537"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> 放射狀漸層的最內部矩形大小。</span><span class="sxs-lookup"><span data-stu-id="63ba0-537"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Size of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="63ba0-538">向量是圖形寬度和高度 (0.0 至 1.0) 的分數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-538">The vector is a fraction (0.0 to 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-539">方法</span><span class="sxs-lookup"><span data-stu-id="63ba0-539">Method</span></span></td>
<td><span data-ttu-id="63ba0-540">VgSigmaType.</span><span class="sxs-lookup"><span data-stu-id="63ba0-540">VgSigmaType.</span></span> <span data-ttu-id="63ba0-541">數值包括：</span><span class="sxs-lookup"><span data-stu-id="63ba0-541">Values include:</span></span>
<ul>
<li><span data-ttu-id="63ba0-542">None</span><span class="sxs-lookup"><span data-stu-id="63ba0-542">None</span></span></li>
<li><span data-ttu-id="63ba0-543">線性</span><span class="sxs-lookup"><span data-stu-id="63ba0-543">Linear</span></span></li>
<li><span data-ttu-id="63ba0-544">Sigma</span><span class="sxs-lookup"><span data-stu-id="63ba0-544">Sigma</span></span></li>
<li><span data-ttu-id="63ba0-545">任意</span><span class="sxs-lookup"><span data-stu-id="63ba0-545">Any</span></span></li>
</ul>
<p><span data-ttu-id="63ba0-546">預設值為 Sigma。</span><span class="sxs-lookup"><span data-stu-id="63ba0-546">Default is Sigma.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-547">開啟</span><span class="sxs-lookup"><span data-stu-id="63ba0-547">On</span></span></td>
<td><span data-ttu-id="63ba0-548"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-548"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="63ba0-549">開啟填滿顯示。</span><span class="sxs-lookup"><span data-stu-id="63ba0-549">Turns fill display on.</span></span> <span data-ttu-id="63ba0-550">與 shape 中的 Fill 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="63ba0-550">Same as Fill attribute in shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-551">不透明度</span><span class="sxs-lookup"><span data-stu-id="63ba0-551">Opacity</span></span></td>
<td><span data-ttu-id="63ba0-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="63ba0-553">填滿的不透明度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-553">Opacity of the fill.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-554">Opacity2</span><span class="sxs-lookup"><span data-stu-id="63ba0-554">Opacity2</span></span></td>
<td><span data-ttu-id="63ba0-555"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-555"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="63ba0-556">漸層的次要不透明度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-556">The secondary opacity for gradients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-557">來源</span><span class="sxs-lookup"><span data-stu-id="63ba0-557">Origin</span></span></td>
<td><span data-ttu-id="63ba0-558"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-558"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="63ba0-559">視為影像來源之影像左上角的相對點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-559">Point relative to upper left corner of the image that is treated as the origin of the image.</span></span> <span data-ttu-id="63ba0-560">預設值是影像的中心。</span><span class="sxs-lookup"><span data-stu-id="63ba0-560">Default is the center of the image.</span></span> <span data-ttu-id="63ba0-561">向量是從0.0 到 1.0) 影像寬度和高度 (的分數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-561">The vector is a fraction (from 0.0 to 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-562">位置</span><span class="sxs-lookup"><span data-stu-id="63ba0-562">Position</span></span></td>
<td><span data-ttu-id="63ba0-563"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-563"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="63ba0-564">指向圖形的參考矩形，以放置影像的來源。</span><span class="sxs-lookup"><span data-stu-id="63ba0-564">Point in the reference rectangle of the shape to position the origin of the image.</span></span> <span data-ttu-id="63ba0-565">預設值為容器矩形的中心。</span><span class="sxs-lookup"><span data-stu-id="63ba0-565">Default is the center of the container rectangle.</span></span> <span data-ttu-id="63ba0-566">向量是影像寬度和高度 (0.0-1.0) 的分數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-566">The vector is a fraction (0.0 - 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-567">大小</span><span class="sxs-lookup"><span data-stu-id="63ba0-567">Size</span></span></td>
<td><span data-ttu-id="63ba0-568"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-568"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="63ba0-569">影像的大小。</span><span class="sxs-lookup"><span data-stu-id="63ba0-569">The size of the image.</span></span> <span data-ttu-id="63ba0-570">預設值是影像的圖元大小。</span><span class="sxs-lookup"><span data-stu-id="63ba0-570">Default is pixel size of the image.</span></span> <span data-ttu-id="63ba0-571">可以用絕對座標或百分比來指定。</span><span class="sxs-lookup"><span data-stu-id="63ba0-571">May be specified in absolute coordinates or percentage.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-572">來源</span><span class="sxs-lookup"><span data-stu-id="63ba0-572">Src</span></span></td>
<td><span data-ttu-id="63ba0-573"><a href="#data-types-used-in-the-vml-object-model">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-573"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="63ba0-574">影像的 URL，以載入影像和模式填滿。</span><span class="sxs-lookup"><span data-stu-id="63ba0-574">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="63ba0-575">這個屬性必須一律存在，並指向有效的影像資料，圖片才會出現。</span><span class="sxs-lookup"><span data-stu-id="63ba0-575">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-576">類型</span><span class="sxs-lookup"><span data-stu-id="63ba0-576">Type</span></span></td>
<td><span data-ttu-id="63ba0-577">VgFillType.</span><span class="sxs-lookup"><span data-stu-id="63ba0-577">VgFillType.</span></span> <span data-ttu-id="63ba0-578">可以是下列其中一個類型：</span><span class="sxs-lookup"><span data-stu-id="63ba0-578">May be one of the following types:</span></span>
<ul>
<li><span data-ttu-id="63ba0-579">背景</span><span class="sxs-lookup"><span data-stu-id="63ba0-579">Background</span></span></li>
<li><span data-ttu-id="63ba0-580">Frame</span><span class="sxs-lookup"><span data-stu-id="63ba0-580">Frame</span></span></li>
<li><span data-ttu-id="63ba0-581">漸層</span><span class="sxs-lookup"><span data-stu-id="63ba0-581">Gradient</span></span></li>
<li><span data-ttu-id="63ba0-582">GradientCenter</span><span class="sxs-lookup"><span data-stu-id="63ba0-582">GradientCenter</span></span></li>
<li><span data-ttu-id="63ba0-583">GradientRadial</span><span class="sxs-lookup"><span data-stu-id="63ba0-583">GradientRadial</span></span></li>
<li><span data-ttu-id="63ba0-584">GradientTitle</span><span class="sxs-lookup"><span data-stu-id="63ba0-584">GradientTitle</span></span></li>
<li><span data-ttu-id="63ba0-585">GradientUnscaled</span><span class="sxs-lookup"><span data-stu-id="63ba0-585">GradientUnscaled</span></span></li>
<li><span data-ttu-id="63ba0-586">模式</span><span class="sxs-lookup"><span data-stu-id="63ba0-586">Pattern</span></span></li>
<li><span data-ttu-id="63ba0-587">實線</span><span class="sxs-lookup"><span data-stu-id="63ba0-587">Solid</span></span></li>
<li><span data-ttu-id="63ba0-588">磚</span><span class="sxs-lookup"><span data-stu-id="63ba0-588">Tile</span></span></li>
</ul>
<span data-ttu-id="63ba0-589">磚、模式和框架都需要提供影像屬性。</span><span class="sxs-lookup"><span data-stu-id="63ba0-589">Tile, Pattern, and Frame require the image attributes to be supplied.</span></span> <span data-ttu-id="63ba0-590">漸層和 GradientRadial 需要提供漸層屬性。</span><span class="sxs-lookup"><span data-stu-id="63ba0-590">Gradient and GradientRadial require the gradient attributes to be supplied.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a><span data-ttu-id="63ba0-591">Group 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-591">Group element</span></span>

<span data-ttu-id="63ba0-592">群組是個別圖形的集合，可作為單位來定位和轉換。</span><span class="sxs-lookup"><span data-stu-id="63ba0-592">A group is a collection of individual shapes that can be positioned and transformed as a unit.</span></span>



|   <span data-ttu-id="63ba0-593">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-593">Attribute</span></span>        |   <span data-ttu-id="63ba0-594">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-594">Description</span></span>                                                                                                                                                                                      |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba0-595">Item</span><span class="sxs-lookup"><span data-stu-id="63ba0-595">Item</span></span>   | <span data-ttu-id="63ba0-596">[IVgShape](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-596">[IVgShape](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-597">圖形陣列中的指定專案。</span><span class="sxs-lookup"><span data-stu-id="63ba0-597">Specified item in the array of shapes.</span></span> |
| <span data-ttu-id="63ba0-598">長度</span><span class="sxs-lookup"><span data-stu-id="63ba0-598">Length</span></span> | <span data-ttu-id="63ba0-599">[Integer](#data-types-used-in-the-vml-object-model) (整數)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-599">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-600">此群組中的圖形數目。</span><span class="sxs-lookup"><span data-stu-id="63ba0-600">Number of shapes in this group.</span></span>         |



 

### <a name="imagedata-element"></a><span data-ttu-id="63ba0-601">Imagedata 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-601">Imagedata element</span></span>

<span data-ttu-id="63ba0-602">描述要在圖形之上呈現的圖片。</span><span class="sxs-lookup"><span data-stu-id="63ba0-602">Describes a picture to be rendered on top of a shape.</span></span>



|   <span data-ttu-id="63ba0-603">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-603">Attribute</span></span>        |   <span data-ttu-id="63ba0-604">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-604">Description</span></span>                                                                                                                                                                                      |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba0-605">雙層</span><span class="sxs-lookup"><span data-stu-id="63ba0-605">BiLevel</span></span>     | <span data-ttu-id="63ba0-606">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-606">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-607">只以兩種色彩顯示圖片 (通常是黑色和白色) 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-607">Display picture in only two colors (usually black and white).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="63ba0-608">BlackLevel</span><span class="sxs-lookup"><span data-stu-id="63ba0-608">BlackLevel</span></span>  | <span data-ttu-id="63ba0-609">[VgFraction](msdn-online-vml-vgfraction-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-609">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="63ba0-610">可進行調整以設定層級，讓黑色顯示為 true 黑色，而其他所有色彩則會顯示為黑色以上的陰影。</span><span class="sxs-lookup"><span data-stu-id="63ba0-610">Allows adjustment to set the level so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="63ba0-611">Chromakey</span><span class="sxs-lookup"><span data-stu-id="63ba0-611">Chromakey</span></span>   | <span data-ttu-id="63ba0-612">[IVgColor](msdn-online-vml-ivgcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-612">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="63ba0-613">圖片的透明色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-613">Transparent color of picture.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="63ba0-614">CropBottom</span><span class="sxs-lookup"><span data-stu-id="63ba0-614">CropBottom</span></span>  | <span data-ttu-id="63ba0-615">[VgNumber](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-616">從圖片底部裁剪距離，以圖片大小的百分比表示。</span><span class="sxs-lookup"><span data-stu-id="63ba0-616">Crop distance from bottom of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="63ba0-617">CropLeft</span><span class="sxs-lookup"><span data-stu-id="63ba0-617">CropLeft</span></span>    | <span data-ttu-id="63ba0-618">[VgNumber](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-619">從圖片的左邊緣裁剪距離，以圖片大小的比例表示 (從0.0 到 1.0) 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-619">Crop distance from left edge of picture expressed as a fraction of picture size (from 0.0 to 1.0).</span></span> <span data-ttu-id="63ba0-620">不過，支援「退出裁剪」，因此支援小於0且大於1的值。例如，-5、20會將圖片大小25X 在圖片的一端，以4/5 來裁剪界限。</span><span class="sxs-lookup"><span data-stu-id="63ba0-620">However, "out-cropping" is supported and thus values of less than 0 and greater than 1 are supported; e.g., -5, 20 would out-crop the bounds 25X the picture size with 4/5 on one side of the picture.</span></span> |
| <span data-ttu-id="63ba0-621">CropRight</span><span class="sxs-lookup"><span data-stu-id="63ba0-621">CropRight</span></span>   | <span data-ttu-id="63ba0-622">[VgNumber](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-622">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-623">從圖片右邊裁剪的距離，以圖片大小的百分比表示。</span><span class="sxs-lookup"><span data-stu-id="63ba0-623">Crop distance from right of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="63ba0-624">CropTop</span><span class="sxs-lookup"><span data-stu-id="63ba0-624">CropTop</span></span>     | <span data-ttu-id="63ba0-625">[VgNumber](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-625">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-626">從圖片頂端裁剪的距離，以圖片大小的百分比表示。</span><span class="sxs-lookup"><span data-stu-id="63ba0-626">Crop distance from top of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="63ba0-627">EmbossColor</span><span class="sxs-lookup"><span data-stu-id="63ba0-627">EmbossColor</span></span> | <span data-ttu-id="63ba0-628">[IVgColor](msdn-online-vml-ivgcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-628">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="63ba0-629">這會設定為陰影色彩的百分比，以建立浮凸圖片效果。</span><span class="sxs-lookup"><span data-stu-id="63ba0-629">This is set to a percentage of the shadow color to create an embossed picture effect.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="63ba0-630">獲得</span><span class="sxs-lookup"><span data-stu-id="63ba0-630">Gain</span></span>        | <span data-ttu-id="63ba0-631">[VgPositiveNumber](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-631">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-632">調整所有色彩的濃度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-632">Adjusts the intensity of all colors.</span></span> <span data-ttu-id="63ba0-633">基本上會設定白色的明暗程度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-633">Essentially sets how bright white will be.</span></span> <span data-ttu-id="63ba0-634">範圍從0到32767。</span><span class="sxs-lookup"><span data-stu-id="63ba0-634">Ranges from 0 to 32767.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="63ba0-635">色差補正</span><span class="sxs-lookup"><span data-stu-id="63ba0-635">Gamma</span></span>       | <span data-ttu-id="63ba0-636">[VgFraction](msdn-online-vml-vgfraction-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-636">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="63ba0-637">Gamma 修正。</span><span class="sxs-lookup"><span data-stu-id="63ba0-637">Gamma correction.</span></span> <span data-ttu-id="63ba0-638">增加它可讓影像更對比。</span><span class="sxs-lookup"><span data-stu-id="63ba0-638">Increasing it gives an image more contrast.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="63ba0-639">GrayScale</span><span class="sxs-lookup"><span data-stu-id="63ba0-639">GrayScale</span></span>   | <span data-ttu-id="63ba0-640">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-640">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-641">顯示灰階色彩的圖片。</span><span class="sxs-lookup"><span data-stu-id="63ba0-641">Display picture in grayscale colors.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="63ba0-642">來源</span><span class="sxs-lookup"><span data-stu-id="63ba0-642">Src</span></span>         | <span data-ttu-id="63ba0-643">[字串](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-643">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-644">影像的 URL，以載入影像和模式填滿。</span><span class="sxs-lookup"><span data-stu-id="63ba0-644">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="63ba0-645">這個屬性必須一律存在，並指向有效的影像資料，圖片才會出現。</span><span class="sxs-lookup"><span data-stu-id="63ba0-645">This attribute must always be present and point to valid image data for a picture to appear.</span></span>                                                                                                                                                           |



 

### <a name="path-element"></a><span data-ttu-id="63ba0-646">Path 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-646">Path element</span></span>

<span data-ttu-id="63ba0-647">使用包含一組豐富的「畫筆移動」命令的字串，定義組成圖形的路徑。</span><span class="sxs-lookup"><span data-stu-id="63ba0-647">Defines the path that makes up the shape, using a string that contains a rich set of "pen movement" commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-648">豪華 轎車</span><span class="sxs-lookup"><span data-stu-id="63ba0-648">Limo</span></span></td>
<td><span data-ttu-id="63ba0-649"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-649"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span></span> <span data-ttu-id="63ba0-650">定義圖案伸展的點;例如，針對 giraffe 圖形，limo 點會在頸部上，因此當調整形狀大小時，頸部將會延展，而圖形的其餘部分將會維持其尺寸。</span><span class="sxs-lookup"><span data-stu-id="63ba0-650">Defines the point where the shape is stretched; e.g., for a giraffe shape, the limo point would be on the neck so when the shape is resized, the neck will stretch and the rest of the shape will maintain its dimensions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-651">TextBoxRect</span><span class="sxs-lookup"><span data-stu-id="63ba0-651">TextBoxRect</span></span></td>
<td><span data-ttu-id="63ba0-652"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-652"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span></span> <span data-ttu-id="63ba0-653">陣列，包含定義文字應該移至何處的矩形。</span><span class="sxs-lookup"><span data-stu-id="63ba0-653">Array containing the rectangles that define where text should go.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-654">V</span><span class="sxs-lookup"><span data-stu-id="63ba0-654">V</span></span></td>
<td><span data-ttu-id="63ba0-655"><a href="#data-types-used-in-the-vml-object-model">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-655"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="63ba0-656">符合路徑標記上的 v 屬性。</span><span class="sxs-lookup"><span data-stu-id="63ba0-656">Matches the v attribute on the Path tag.</span></span> <span data-ttu-id="63ba0-657">請注意，路徑可能對應至 Path 屬性或元素。</span><span class="sxs-lookup"><span data-stu-id="63ba0-657">Note that path may correspond to Path attribute or element.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-658">值</span><span class="sxs-lookup"><span data-stu-id="63ba0-658">Value</span></span></td>
<td><span data-ttu-id="63ba0-659"><a href="#data-types-used-in-the-vml-object-model">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-659"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="63ba0-660">定義路徑的命令文字表示。</span><span class="sxs-lookup"><span data-stu-id="63ba0-660">A text representation of the commands that define the path.</span></span> <span data-ttu-id="63ba0-661">X 或 y 座標值可以是表單中公式的參考 &quot; @# &quot; ，其中 # 是公式的序數，例如， &quot; @2 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-661">X or y-coordinate values can be a reference to a formula in the form &quot;@#&quot; where # is the formula's ordinal number, e.g., &quot;@2&quot;.</span></span> <span data-ttu-id="63ba0-662">這個屬性字串是由一組豐富的命令所組成，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="63ba0-662">This attribute string is made up of a rich set of commands including the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="63ba0-663">命令</span><span class="sxs-lookup"><span data-stu-id="63ba0-663">Command</span></span></th>
<th><span data-ttu-id="63ba0-664">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-664">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-665">ae (angleellipseto) </span><span class="sxs-lookup"><span data-stu-id="63ba0-665">ae (angleellipseto)</span></span></td>
<td><span data-ttu-id="63ba0-666"><strong>中央</strong> (x、y) <strong>大小</strong> (w、h) <strong>開始角度</strong>、 <strong>終點</strong></span><span class="sxs-lookup"><span data-stu-id="63ba0-666"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span></span><br/> <span data-ttu-id="63ba0-667">繪製橢圓形的線段。</span><span class="sxs-lookup"><span data-stu-id="63ba0-667">Draw a segment of an ellipse.</span></span> <span data-ttu-id="63ba0-668">從目前的點將直線繪製到區段的起點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-668">A straight line is drawn from the current point to the start point of the segment.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-669">al (angleelipse) </span><span class="sxs-lookup"><span data-stu-id="63ba0-669">al (angleelipse)</span></span></td>
<td><span data-ttu-id="63ba0-670">與 ae 相同，不同之處在于區段的起點有隱含的 m。</span><span class="sxs-lookup"><span data-stu-id="63ba0-670">Same as ae except that there is an implied m to the starting point of the segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-671">ar (arc) </span><span class="sxs-lookup"><span data-stu-id="63ba0-671">ar (arc)</span></span></td>
<td><span data-ttu-id="63ba0-672">與相同。</span><span class="sxs-lookup"><span data-stu-id="63ba0-672">Same as at.</span></span> <span data-ttu-id="63ba0-673">不過，新的子路徑會由隱含的 m 啟動至弧線的起點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-673">However, a new subpath is started by an implied m to the start point of the arc.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-674">在 (arcto) </span><span class="sxs-lookup"><span data-stu-id="63ba0-674">at (arcto)</span></span></td>
<td><span data-ttu-id="63ba0-675"><strong>左</strong>、 <strong>上</strong>、 <strong>右</strong>、 <strong>下</strong>、 <strong>開始</strong> (x、y) <strong>end</strong> (x，y) </span><span class="sxs-lookup"><span data-stu-id="63ba0-675"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="63ba0-676">前四個值會定義橢圓形的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="63ba0-676">The first four values define the bounding box of an ellipse.</span></span> <span data-ttu-id="63ba0-677">最後四個定義兩個放射狀向量。</span><span class="sxs-lookup"><span data-stu-id="63ba0-677">The last four define two radial vectors.</span></span> <span data-ttu-id="63ba0-678">繪製的橢圓形區段會從開始半徑向量所定義的角度開始，並以結束向量所定義的角度結束。</span><span class="sxs-lookup"><span data-stu-id="63ba0-678">A segment of the ellipse is drawn that starts at the angle defined by the start radius vector and ends at the angle defined by the end vector.</span></span> <span data-ttu-id="63ba0-679">從目前的點到弧形開頭繪製直線。弧線一律會以逆時針方向繪製。</span><span class="sxs-lookup"><span data-stu-id="63ba0-679">A straight line is drawn from the current point to the start of the arc. The arc is always drawn in a counterclockwise direction.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-680">c (curveto) </span><span class="sxs-lookup"><span data-stu-id="63ba0-680">c (curveto)</span></span></td>
<td><span data-ttu-id="63ba0-681"><strong>control1</strong> (x，y) <strong>control2</strong> (x，y) <strong>至</strong> (x，y) </span><span class="sxs-lookup"><span data-stu-id="63ba0-681"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y)</span></span> <br/> <span data-ttu-id="63ba0-682">從目前的點繪製三次方貝茲曲線到最後兩個參數所指定的座標，也就是前四個參數所指定的控制點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-682">Draw a cubic bezier curve from the current point to the coordinate given by the final two parameters, the control points given by the first four parameters.</span></span> <span data-ttu-id="63ba0-683">目前的點會成為貝塞爾的端點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-683">The current point becomes the endpoint of the bezier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-684">e (結束) </span><span class="sxs-lookup"><span data-stu-id="63ba0-684">e (end)</span></span></td>
<td><span data-ttu-id="63ba0-685">結束目前的子路徑集。</span><span class="sxs-lookup"><span data-stu-id="63ba0-685">End the current set of subpaths.</span></span> <span data-ttu-id="63ba0-686">會使用 eofill 填滿一組指定的子路徑，並以 end) 分隔 (。</span><span class="sxs-lookup"><span data-stu-id="63ba0-686">A given set of subpaths (as delimited by end) are filled using eofill.</span></span> <span data-ttu-id="63ba0-687">後續的子路徑集合會獨立填入，並在現有的子路徑上重迭。</span><span class="sxs-lookup"><span data-stu-id="63ba0-687">Subsequent sets of subpaths are filled independently and superimposed on existing ones.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-688">l (lineto) </span><span class="sxs-lookup"><span data-stu-id="63ba0-688">l (lineto)</span></span></td>
<td><span data-ttu-id="63ba0-689">x、y</span><span class="sxs-lookup"><span data-stu-id="63ba0-689">x,y</span></span><br/> <span data-ttu-id="63ba0-690">從目前的點將直線繪製到指定的 x，y 座標，以成為新的目前點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-690">Draw a line from the current point to the given x,y-coordinate, which becomes the new current point.</span></span> <span data-ttu-id="63ba0-691">您可以指定其他座標配對來形成聚合線條，例如， &quot; l 10、13、45、27、89、-12 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-691">Additional coordinate pairs may be specified to form a polyline, e.g., &quot;l 10,13,45,27,89,-12&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-692">m (moveto) </span><span class="sxs-lookup"><span data-stu-id="63ba0-692">m (moveto)</span></span></td>
<td><span data-ttu-id="63ba0-693">x、y</span><span class="sxs-lookup"><span data-stu-id="63ba0-693">x,y</span></span><br/> <span data-ttu-id="63ba0-694">在指定的 x，y 座標開始新的子路徑。</span><span class="sxs-lookup"><span data-stu-id="63ba0-694">Start a new subpath at the given x,y-coordinate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-695">nofill) 的 nf-e (</span><span class="sxs-lookup"><span data-stu-id="63ba0-695">nf (nofill)</span></span></td>
<td><span data-ttu-id="63ba0-696">將不會填入以 end) 分隔 (目前的子路徑集合。</span><span class="sxs-lookup"><span data-stu-id="63ba0-696">The current set of subpaths (delimited by end) will not be filled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-697">ns (nostroke) </span><span class="sxs-lookup"><span data-stu-id="63ba0-697">ns (nostroke)</span></span></td>
<td><span data-ttu-id="63ba0-698">將不會對目前的子路徑組合 (以 end) 分隔。</span><span class="sxs-lookup"><span data-stu-id="63ba0-698">The current set of subpaths (delimited by end) will not be stroked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-699">qb (quadraticbezier) </span><span class="sxs-lookup"><span data-stu-id="63ba0-699">qb (quadraticbezier)</span></span></td>
<td><span data-ttu-id="63ba0-700"> (<strong>controlpoint</strong> (x、y) )\ *、<strong>end</strong> (x、y) </span><span class="sxs-lookup"><span data-stu-id="63ba0-700">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="63ba0-701">藉由控制點和端點，定義一或多個二次方貝茲曲線。</span><span class="sxs-lookup"><span data-stu-id="63ba0-701">Defines one or more quadratic bezier curves by means of control points and an endpoint.</span></span> <span data-ttu-id="63ba0-702">中間的 (曲線) 點是透過類似 TrueType 字型的連續控制點來取得。</span><span class="sxs-lookup"><span data-stu-id="63ba0-702">Intermediate (on-curve) points are obtained by interpolation between successive control points similar to TrueType fonts.</span></span> <span data-ttu-id="63ba0-703">子路徑不需要是開始的，在此情況下，會關閉子路徑，而最後一個點則會定義起始點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-703">The subpath need not be a start, in which case the subpath is closed and the last point defines the start point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-704">qx (ellipticalquadrantx) </span><span class="sxs-lookup"><span data-stu-id="63ba0-704">qx (ellipticalquadrantx)</span></span></td>
<td><span data-ttu-id="63ba0-705"><strong>end</strong> (x，y) </span><span class="sxs-lookup"><span data-stu-id="63ba0-705"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="63ba0-706">從目前的點到指定端點繪製的四分之一橢圓形。</span><span class="sxs-lookup"><span data-stu-id="63ba0-706">A quarter ellipse is drawn from the current point to the given endpoint.</span></span> <span data-ttu-id="63ba0-707">橢圓區段一開始會與 X 軸平行的直線相切;亦即，區段開始水準。</span><span class="sxs-lookup"><span data-stu-id="63ba0-707">The elliptical segment is initially tangential to a line parallel to the x-axis; i.e., the segment starts out horizontal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-708">qy (ellipticalquadranty) </span><span class="sxs-lookup"><span data-stu-id="63ba0-708">qy (ellipticalquadranty)</span></span></td>
<td><span data-ttu-id="63ba0-709"><strong>end</strong> (x，y) </span><span class="sxs-lookup"><span data-stu-id="63ba0-709"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="63ba0-710">與 qx 相同，不同之處在于橢圓區段一開始會與 y 軸平行的直線相切;亦即，區段開始垂直。</span><span class="sxs-lookup"><span data-stu-id="63ba0-710">Same as qx except that the elliptical segment is initially tangential to a line parallel to the y-axis; i.e., the segment starts out vertical.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-711">r (rlineto) </span><span class="sxs-lookup"><span data-stu-id="63ba0-711">r (rlineto)</span></span></td>
<td><span data-ttu-id="63ba0-712">x、y</span><span class="sxs-lookup"><span data-stu-id="63ba0-712">x,y</span></span> <br/> <span data-ttu-id="63ba0-713">從目前的點繪製一條直線到相對座標 (cpx + x，cpy + y) 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-713">Draw a line from the current point to the relative coordinate (cpx + x, cpy + y).</span></span> <span data-ttu-id="63ba0-714">如果指定了其他座標組，每個新點都會相對於最後一個點來計算。</span><span class="sxs-lookup"><span data-stu-id="63ba0-714">If additional coordinate pairs are given, each new point is computed relative to the last one.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-715">t (rmoveto) </span><span class="sxs-lookup"><span data-stu-id="63ba0-715">t (rmoveto)</span></span></td>
<td><span data-ttu-id="63ba0-716">x、y</span><span class="sxs-lookup"><span data-stu-id="63ba0-716">x,y</span></span><br/> <span data-ttu-id="63ba0-717">在相對座標開始新的子路徑 ( cpx + x，cpy + y) 其中 cpx，cpy 是目前的位置。</span><span class="sxs-lookup"><span data-stu-id="63ba0-717">Start a new subpath at the relative coordinates ( cpx + x, cpy + y) where cpx, cpy is the current position.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-718">v (curveto) </span><span class="sxs-lookup"><span data-stu-id="63ba0-718">v (curveto)</span></span></td>
<td><span data-ttu-id="63ba0-719"><strong>control1</strong> (x，y) <strong>control2</strong> (x，y) <strong>至</strong> (x，y) </span><span class="sxs-lookup"><span data-stu-id="63ba0-719"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span></span> <br/> <span data-ttu-id="63ba0-720">使用相對於目前點之指定座標的三次方貝茲曲線。</span><span class="sxs-lookup"><span data-stu-id="63ba0-720">Cubic bezier curve using the given coordinates relative to the current point.</span></span> <span data-ttu-id="63ba0-721">所有點都是相對於相同的起點來計算。</span><span class="sxs-lookup"><span data-stu-id="63ba0-721">All the points are computed relative to the same starting point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-722">wa (clockwisearcto) </span><span class="sxs-lookup"><span data-stu-id="63ba0-722">wa (clockwisearcto)</span></span></td>
<td><span data-ttu-id="63ba0-723">與相同，但弧線以順時針方向繪製。</span><span class="sxs-lookup"><span data-stu-id="63ba0-723">Same as at but the arc is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-724">wr (clockwisearc) </span><span class="sxs-lookup"><span data-stu-id="63ba0-724">wr (clockwisearc)</span></span></td>
<td><span data-ttu-id="63ba0-725">與 ar 相同，但以順時針方向繪製。</span><span class="sxs-lookup"><span data-stu-id="63ba0-725">Same as ar but is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-726">x (關閉) </span><span class="sxs-lookup"><span data-stu-id="63ba0-726">x (close)</span></span></td>
<td><span data-ttu-id="63ba0-727">從目前點到原始的 moveto 點繪製一條直線，以關閉目前的子路徑。</span><span class="sxs-lookup"><span data-stu-id="63ba0-727">Close the current subpath by drawing a straight line from the current point to the original moveto point.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a><span data-ttu-id="63ba0-728">Shadow 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-728">Shadow element</span></span>

<span data-ttu-id="63ba0-729">描述圖形上的陰影效果。</span><span class="sxs-lookup"><span data-stu-id="63ba0-729">Describes a shadow effect on a shape.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-730">Color</span><span class="sxs-lookup"><span data-stu-id="63ba0-730">Color</span></span></td>
<td><span data-ttu-id="63ba0-731"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-731"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="63ba0-732">主要陰影的色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-732">Color of the primary shadow.</span></span> <span data-ttu-id="63ba0-733">預設值為 RGB (128128128) </span><span class="sxs-lookup"><span data-stu-id="63ba0-733">Default is RGB(128,128,128)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-734">Color2</span><span class="sxs-lookup"><span data-stu-id="63ba0-734">Color2</span></span></td>
<td><span data-ttu-id="63ba0-735"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-735"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="63ba0-736">第二個陰影的色彩，或反白顯示于浮凸或陰文的陰影。</span><span class="sxs-lookup"><span data-stu-id="63ba0-736">Color of the second shadow, or highlight in an embossed or engraved shadow.</span></span> <span data-ttu-id="63ba0-737">預設值為 RGB (203203203) 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-737">Default is RGB(203,203,203).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-738">矩陣</span><span class="sxs-lookup"><span data-stu-id="63ba0-738">Matrix</span></span></td>
<td><span data-ttu-id="63ba0-739"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-739"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span></span> <span data-ttu-id="63ba0-740">&quot;Sxx、sxy、syx、syy、px、.py &quot; [s = scale、p = 透視圖] 格式的透視圖轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="63ba0-740">A perspective transform matrix in the form, &quot;sxx,sxy,syx,syy,px,py&quot; [s=scale, p=perspective].</span></span> <span data-ttu-id="63ba0-741">專案指定陰影應該如何隨著圖形而調整，而 p 專案則指定陰影應該如何與圖形相對應的扭曲。</span><span class="sxs-lookup"><span data-stu-id="63ba0-741">The s items specify how the shadow should scale with respect to the shape, and the p items specify how the shadow should skew with respect to the shape.</span></span> <span data-ttu-id="63ba0-742">例如，下列矩陣會以2的因數來調整圖形的大小，並以4的因數將其傾斜：</span><span class="sxs-lookup"><span data-stu-id="63ba0-742">For example, the following matrix resizes the shape by a factor of 2 and skews it by a factor of 4 in all directions:</span></span> <br/> <span data-ttu-id="63ba0-743">&quot;2、2、2、2、4、4&quot;</span><span class="sxs-lookup"><span data-stu-id="63ba0-743">&quot;2,2,2,2,4,4&quot;</span></span><br/> <span data-ttu-id="63ba0-744">只有當陰影的類型設定為 [透視圖] 時，才會使用這個矩陣。</span><span class="sxs-lookup"><span data-stu-id="63ba0-744">This matrix is only used if the type of the shadow is set to perspective.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-745">遮蔽</span><span class="sxs-lookup"><span data-stu-id="63ba0-745">Obscured</span></span></td>
<td><span data-ttu-id="63ba0-746"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-746"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="63ba0-747">如果圖形沒有填滿，就可以看到陰影。</span><span class="sxs-lookup"><span data-stu-id="63ba0-747">The shadow can be seen through if there is no fill on the shape.</span></span> <span data-ttu-id="63ba0-748">預設值是 False。</span><span class="sxs-lookup"><span data-stu-id="63ba0-748">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-749">Offset</span><span class="sxs-lookup"><span data-stu-id="63ba0-749">Offset</span></span></td>
<td><span data-ttu-id="63ba0-750"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-750"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span></span> <span data-ttu-id="63ba0-751">X 的數量，y 位移自圖形的位置。</span><span class="sxs-lookup"><span data-stu-id="63ba0-751">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="63ba0-752">預設值為 &quot; 2pt、2pt &quot; 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-752">Default is &quot;2pt,2pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-753">Offset2</span><span class="sxs-lookup"><span data-stu-id="63ba0-753">Offset2</span></span></td>
<td><span data-ttu-id="63ba0-754"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-754"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="63ba0-755">X 的數量，y 第二個從圖形的位置位移。</span><span class="sxs-lookup"><span data-stu-id="63ba0-755">Amount of x,y second offset from the shape?s location.</span></span> <span data-ttu-id="63ba0-756">值可以是絕對測量值，或是 shape (-0.5 到 + 0.5) 的小數值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-756">Values are either an absolute measurement, or a fractional value of shape (-0.5 to +0.5).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-757">開啟</span><span class="sxs-lookup"><span data-stu-id="63ba0-757">On</span></span></td>
<td><span data-ttu-id="63ba0-758"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-758"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="63ba0-759">開啟和關閉陰影的顯示。</span><span class="sxs-lookup"><span data-stu-id="63ba0-759">Turns the display of the shadow on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-760">不透明度</span><span class="sxs-lookup"><span data-stu-id="63ba0-760">Opacity</span></span></td>
<td><span data-ttu-id="63ba0-761"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-761"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="63ba0-762">陰影效果的不透明度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-762">Opacity of the shadow effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-763">來源</span><span class="sxs-lookup"><span data-stu-id="63ba0-763">Origin</span></span></td>
<td><span data-ttu-id="63ba0-764"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> 從-0.5 到 + 0.5 之圖形的一對小數值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-764"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> A pair of fractional values of shape from -0.5 to +0.5.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-765">類型</span><span class="sxs-lookup"><span data-stu-id="63ba0-765">Type</span></span></td>
<td><span data-ttu-id="63ba0-766"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-766"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span></span> <span data-ttu-id="63ba0-767">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-767">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-768">單一 (預設) </span><span class="sxs-lookup"><span data-stu-id="63ba0-768">Single (default)</span></span></li>
<li><span data-ttu-id="63ba0-769">Double</span><span class="sxs-lookup"><span data-stu-id="63ba0-769">Double</span></span></li>
<li><span data-ttu-id="63ba0-770">檢視方塊</span><span class="sxs-lookup"><span data-stu-id="63ba0-770">Perspective</span></span></li>
<li><span data-ttu-id="63ba0-771">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="63ba0-771">ShapeRelative</span></span></li>
<li><span data-ttu-id="63ba0-772">DrawingRelative</span><span class="sxs-lookup"><span data-stu-id="63ba0-772">DrawingRelative</span></span></li>
<li><span data-ttu-id="63ba0-773">Emboss</span><span class="sxs-lookup"><span data-stu-id="63ba0-773">Emboss</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a><span data-ttu-id="63ba0-774">扭曲元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-774">Skew element</span></span>

<span data-ttu-id="63ba0-775">描述圖形上的觀點扭曲效果。</span><span class="sxs-lookup"><span data-stu-id="63ba0-775">Describes a perspective skew effect on a shape.</span></span> <span data-ttu-id="63ba0-776">扭曲會套用至向量圖形資料，而不會套用至影像資料。</span><span class="sxs-lookup"><span data-stu-id="63ba0-776">The skew is applied to vector graphic data, not image data.</span></span>



|   <span data-ttu-id="63ba0-777">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-777">Attribute</span></span>        |   <span data-ttu-id="63ba0-778">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-778">Description</span></span>                                                                                                                                                                                      |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba0-779">矩陣</span><span class="sxs-lookup"><span data-stu-id="63ba0-779">Matrix</span></span> | <span data-ttu-id="63ba0-780">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-780">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-781">以 "sxx，sxy，syx，syy，px，.py" \[ s = scale，p = 透視圖形式的觀點轉換矩陣 \] 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-781">A perspective transform matrix in the form, "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective\].</span></span> <span data-ttu-id="63ba0-782">如果位移的單位為絕對單位，則為 px，.py 則為 emu ^-1 個單位;否則是圖形大小的反向分數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-782">If offset is in absolute units then px,py are in emu ^ -1 units; otherwise they are an inverse fraction of shape size.</span></span> |
| <span data-ttu-id="63ba0-783">Offset</span><span class="sxs-lookup"><span data-stu-id="63ba0-783">Offset</span></span> | <span data-ttu-id="63ba0-784">[IvgSkewOffset](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-784">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-785">X 的數量，y 位移自圖形的位置。</span><span class="sxs-lookup"><span data-stu-id="63ba0-785">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="63ba0-786">預設值為 "2pt，2pt"。</span><span class="sxs-lookup"><span data-stu-id="63ba0-786">Default is "2pt,2pt".</span></span>                                                                                                                                                   |
| <span data-ttu-id="63ba0-787">開啟</span><span class="sxs-lookup"><span data-stu-id="63ba0-787">On</span></span>     | <span data-ttu-id="63ba0-788">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-788">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-789">開啟或關閉扭曲的顯示。</span><span class="sxs-lookup"><span data-stu-id="63ba0-789">Turns the display of the skew on or off.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="63ba0-790">來源</span><span class="sxs-lookup"><span data-stu-id="63ba0-790">Origin</span></span> | <span data-ttu-id="63ba0-791">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-791">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="63ba0-792">從-0.5 到 + 0.5 之圖形的一對小數值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-792">A pair of fractional values of shape from -0.5 to +0.5.</span></span>                                                                                                                                                                     |



 

### <a name="stroke-element"></a><span data-ttu-id="63ba0-793">Stroke 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-793">Stroke element</span></span>

<span data-ttu-id="63ba0-794">描述如何在需要純色的實線之外繪製路徑。</span><span class="sxs-lookup"><span data-stu-id="63ba0-794">Describes how to draw the path if something beyond a solid line with a solid color is desired.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-795">Color</span><span class="sxs-lookup"><span data-stu-id="63ba0-795">Color</span></span></td>
<td><span data-ttu-id="63ba0-796"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-796"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="63ba0-797">線條的色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-797">The color of the line.</span></span> <span data-ttu-id="63ba0-798">與 Shape 中的 StrokeColor 屬性相同，但會覆寫它。</span><span class="sxs-lookup"><span data-stu-id="63ba0-798">Same as StrokeColor attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-799">Color2</span><span class="sxs-lookup"><span data-stu-id="63ba0-799">Color2</span></span></td>
<td><span data-ttu-id="63ba0-800"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-800"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="63ba0-801">次要色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-801">Secondary color.</span></span> <span data-ttu-id="63ba0-802">當 FillType 為模式時使用。</span><span class="sxs-lookup"><span data-stu-id="63ba0-802">Used when FillType is Pattern.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-803">DashStyle</span><span class="sxs-lookup"><span data-stu-id="63ba0-803">DashStyle</span></span></td>
<td><span data-ttu-id="63ba0-804"><strong>VgLineDashStyle</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-804"><strong>VgLineDashStyle</strong>.</span></span> <span data-ttu-id="63ba0-805">虛線樣式格式。</span><span class="sxs-lookup"><span data-stu-id="63ba0-805">Dash style format.</span></span> <span data-ttu-id="63ba0-806">可能是特定的值，或是具有使用者定義虛線模式的數位序列。</span><span class="sxs-lookup"><span data-stu-id="63ba0-806">May be a specific value or a sequence of numbers with a user-defined dash pattern.</span></span> <span data-ttu-id="63ba0-807">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-807">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-808">Solid (預設值)</span><span class="sxs-lookup"><span data-stu-id="63ba0-808">Solid (default)</span></span></li>
<li><span data-ttu-id="63ba0-809">ShortDash</span><span class="sxs-lookup"><span data-stu-id="63ba0-809">ShortDash</span></span></li>
<li><span data-ttu-id="63ba0-810">ShortDot</span><span class="sxs-lookup"><span data-stu-id="63ba0-810">ShortDot</span></span></li>
<li><span data-ttu-id="63ba0-811">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="63ba0-811">ShortDashDot</span></span></li>
<li><span data-ttu-id="63ba0-812">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="63ba0-812">ShortDashDotDot</span></span></li>
<li><span data-ttu-id="63ba0-813">點</span><span class="sxs-lookup"><span data-stu-id="63ba0-813">Dot</span></span></li>
<li><span data-ttu-id="63ba0-814">虛線</span><span class="sxs-lookup"><span data-stu-id="63ba0-814">Dash</span></span></li>
<li><span data-ttu-id="63ba0-815">DashDot</span><span class="sxs-lookup"><span data-stu-id="63ba0-815">DashDot</span></span></li>
<li><span data-ttu-id="63ba0-816">LongDash</span><span class="sxs-lookup"><span data-stu-id="63ba0-816">LongDash</span></span></li>
<li><span data-ttu-id="63ba0-817">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="63ba0-817">LongDashDot</span></span></li>
<li><span data-ttu-id="63ba0-818">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="63ba0-818">LongDashDotDot</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-819">EndArrow</span><span class="sxs-lookup"><span data-stu-id="63ba0-819">EndArrow</span></span></td>
<td><span data-ttu-id="63ba0-820"><strong>VgArrowheadStyle</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-820"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="63ba0-821">行尾的箭頭。</span><span class="sxs-lookup"><span data-stu-id="63ba0-821">Arrowhead for the end of the line.</span></span> <span data-ttu-id="63ba0-822">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-822">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-823">[無] (預設值)</span><span class="sxs-lookup"><span data-stu-id="63ba0-823">None (default)</span></span></li>
<li><span data-ttu-id="63ba0-824">封鎖</span><span class="sxs-lookup"><span data-stu-id="63ba0-824">Block</span></span></li>
<li><span data-ttu-id="63ba0-825">傳統</span><span class="sxs-lookup"><span data-stu-id="63ba0-825">Classic</span></span></li>
<li><span data-ttu-id="63ba0-826">菱形</span><span class="sxs-lookup"><span data-stu-id="63ba0-826">Diamond</span></span></li>
<li><span data-ttu-id="63ba0-827">橢圓形</span><span class="sxs-lookup"><span data-stu-id="63ba0-827">Oval</span></span></li>
<li><span data-ttu-id="63ba0-828">開啟</span><span class="sxs-lookup"><span data-stu-id="63ba0-828">Open</span></span></li>
<li><span data-ttu-id="63ba0-829">&gt; 形箭號</span><span class="sxs-lookup"><span data-stu-id="63ba0-829">Chevron</span></span></li>
<li><span data-ttu-id="63ba0-830">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="63ba0-830">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-831">EndArrowLength</span><span class="sxs-lookup"><span data-stu-id="63ba0-831">EndArrowLength</span></span></td>
<td><span data-ttu-id="63ba0-832"><strong>VgArrowHeadLength</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-832"><strong>VgArrowHeadLength</strong>.</span></span> <span data-ttu-id="63ba0-833">線條結尾的箭頭長度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-833">Arrowhead length for the end of the line.</span></span> <span data-ttu-id="63ba0-834">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-834">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-835">Short</span><span class="sxs-lookup"><span data-stu-id="63ba0-835">Short</span></span></li>
<li><span data-ttu-id="63ba0-836">中 (預設)</span><span class="sxs-lookup"><span data-stu-id="63ba0-836">Medium (default)</span></span></li>
<li><span data-ttu-id="63ba0-837">long</span><span class="sxs-lookup"><span data-stu-id="63ba0-837">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-838">EndArrowWidth</span><span class="sxs-lookup"><span data-stu-id="63ba0-838">EndArrowWidth</span></span></td>
<td><span data-ttu-id="63ba0-839"><strong>VgArrowheadWidth</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-839"><strong>VgArrowheadWidth</strong>.</span></span> <span data-ttu-id="63ba0-840">線條結尾的箭頭寬度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-840">Arrowhead width for the end of the line.</span></span> <span data-ttu-id="63ba0-841">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-841">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-842">狹窄</span><span class="sxs-lookup"><span data-stu-id="63ba0-842">Narrow</span></span></li>
<li><span data-ttu-id="63ba0-843">中 (預設)</span><span class="sxs-lookup"><span data-stu-id="63ba0-843">Medium (default)</span></span></li>
<li><span data-ttu-id="63ba0-844">寬</span><span class="sxs-lookup"><span data-stu-id="63ba0-844">Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-845">EndCap</span><span class="sxs-lookup"><span data-stu-id="63ba0-845">EndCap</span></span></td>
<td><span data-ttu-id="63ba0-846"><strong>VgLineEndCapStyle</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-846"><strong>VgLineEndCapStyle</strong>.</span></span> <span data-ttu-id="63ba0-847">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-847">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-848">一般</span><span class="sxs-lookup"><span data-stu-id="63ba0-848">Flat</span></span></li>
<li><span data-ttu-id="63ba0-849">Square</span><span class="sxs-lookup"><span data-stu-id="63ba0-849">Square</span></span></li>
<li><span data-ttu-id="63ba0-850">Round</span><span class="sxs-lookup"><span data-stu-id="63ba0-850">Round</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-851">FillType</span><span class="sxs-lookup"><span data-stu-id="63ba0-851">FillType</span></span></td>
<td><span data-ttu-id="63ba0-852"><strong>VgLineFillType</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-852"><strong>VgLineFillType</strong>.</span></span> <span data-ttu-id="63ba0-853">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-853">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-854">Solid (預設值)</span><span class="sxs-lookup"><span data-stu-id="63ba0-854">Solid (default)</span></span></li>
<li><span data-ttu-id="63ba0-855">磚</span><span class="sxs-lookup"><span data-stu-id="63ba0-855">Tile</span></span></li>
<li><span data-ttu-id="63ba0-856">模式</span><span class="sxs-lookup"><span data-stu-id="63ba0-856">Pattern</span></span></li>
<li><span data-ttu-id="63ba0-857">Frame</span><span class="sxs-lookup"><span data-stu-id="63ba0-857">Frame</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-858">ImageAlignShape</span><span class="sxs-lookup"><span data-stu-id="63ba0-858">ImageAlignShape</span></span></td>
<td><span data-ttu-id="63ba0-859"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-859"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="63ba0-860">將影像與圖形對齊。</span><span class="sxs-lookup"><span data-stu-id="63ba0-860">Align the image with the shape.</span></span> <span data-ttu-id="63ba0-861">如果為 False，則會將影像與視窗對齊。</span><span class="sxs-lookup"><span data-stu-id="63ba0-861">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-862">ImageAspect</span><span class="sxs-lookup"><span data-stu-id="63ba0-862">ImageAspect</span></span></td>
<td><span data-ttu-id="63ba0-863"><strong>VgAspectType</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-863"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="63ba0-864">ImageSize 屬性將會調整，以保留影像的外觀。</span><span class="sxs-lookup"><span data-stu-id="63ba0-864">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="63ba0-865">數值包括：</span><span class="sxs-lookup"><span data-stu-id="63ba0-865">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="63ba0-866">值</span><span class="sxs-lookup"><span data-stu-id="63ba0-866">Value</span></span></th>
<th><span data-ttu-id="63ba0-867">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-867">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-868">忽略</span><span class="sxs-lookup"><span data-stu-id="63ba0-868">Ignore</span></span></td>
<td><span data-ttu-id="63ba0-869">略過外觀問題。</span><span class="sxs-lookup"><span data-stu-id="63ba0-869">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-870">至少</span><span class="sxs-lookup"><span data-stu-id="63ba0-870">AtLeast</span></span></td>
<td><span data-ttu-id="63ba0-871">映射大小至少與影像大小一樣大。</span><span class="sxs-lookup"><span data-stu-id="63ba0-871">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-872">有</span><span class="sxs-lookup"><span data-stu-id="63ba0-872">AtMost</span></span></td>
<td><span data-ttu-id="63ba0-873">影像的大小不會大於影像大小。</span><span class="sxs-lookup"><span data-stu-id="63ba0-873">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-874">ImageSize</span><span class="sxs-lookup"><span data-stu-id="63ba0-874">ImageSize</span></span></td>
<td><span data-ttu-id="63ba0-875"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-875"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="63ba0-876">用來形成筆刷的影像大小。</span><span class="sxs-lookup"><span data-stu-id="63ba0-876">Size of the image to form the brush with.</span></span> <span data-ttu-id="63ba0-877">預設值是影像的大小。</span><span class="sxs-lookup"><span data-stu-id="63ba0-877">Default is the size of the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-878">JoinStyle</span><span class="sxs-lookup"><span data-stu-id="63ba0-878">JoinStyle</span></span></td>
<td><span data-ttu-id="63ba0-879"><strong>VgLineJoinStyle</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-879"><strong>VgLineJoinStyle</strong>.</span></span> <span data-ttu-id="63ba0-880">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-880">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-881">舍入 (圓角接合) </span><span class="sxs-lookup"><span data-stu-id="63ba0-881">Round (rounded joint)</span></span></li>
<li><span data-ttu-id="63ba0-882">斜面 (斜角接點) </span><span class="sxs-lookup"><span data-stu-id="63ba0-882">Bevel (beveled joint)</span></span></li>
<li><span data-ttu-id="63ba0-883">斜接 (斜接接點) </span><span class="sxs-lookup"><span data-stu-id="63ba0-883">Miter (miter joint)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-884">線條樣式</span><span class="sxs-lookup"><span data-stu-id="63ba0-884">LineStyle</span></span></td>
<td><span data-ttu-id="63ba0-885"><strong>VgLineStyle</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-885"><strong>VgLineStyle</strong>.</span></span> <span data-ttu-id="63ba0-886">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-886">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-887">Single</span><span class="sxs-lookup"><span data-stu-id="63ba0-887">Single</span></span></li>
<li><span data-ttu-id="63ba0-888">ThinThin (1:1:1) </span><span class="sxs-lookup"><span data-stu-id="63ba0-888">ThinThin (1:1:1)</span></span></li>
<li><span data-ttu-id="63ba0-889">ThinThick (1:1:2) </span><span class="sxs-lookup"><span data-stu-id="63ba0-889">ThinThick (1:1:2)</span></span></li>
<li><span data-ttu-id="63ba0-890">ThickThin (2:1:1) </span><span class="sxs-lookup"><span data-stu-id="63ba0-890">ThickThin (2:1:1)</span></span></li>
<li><span data-ttu-id="63ba0-891">ThickBetweenThin (1:1:2:1:1) </span><span class="sxs-lookup"><span data-stu-id="63ba0-891">ThickBetweenThin (1:1:2:1:1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-892">MiterLimit</span><span class="sxs-lookup"><span data-stu-id="63ba0-892">MiterLimit</span></span></td>
<td><span data-ttu-id="63ba0-893"><a href="msdn-online-vml-vglength.md">長度</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-893"><a href="msdn-online-vml-vglength.md">Length</a>.</span></span> <span data-ttu-id="63ba0-894">聯合的內部點和外部點之間的最大距離。</span><span class="sxs-lookup"><span data-stu-id="63ba0-894">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="63ba0-895">此數位是線條粗細的倍數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-895">This number is a multiple of the thickness of the line.</span></span> <span data-ttu-id="63ba0-896">範圍從0到32767。</span><span class="sxs-lookup"><span data-stu-id="63ba0-896">Ranges from 0 to 32,767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-897">開啟</span><span class="sxs-lookup"><span data-stu-id="63ba0-897">On</span></span></td>
<td><span data-ttu-id="63ba0-898"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-898"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="63ba0-899">開啟和關閉行的顯示。</span><span class="sxs-lookup"><span data-stu-id="63ba0-899">Turns the display of the line on and off.</span></span> <span data-ttu-id="63ba0-900">與 Shape 中的 Stroke 屬性相同，但會覆寫它。</span><span class="sxs-lookup"><span data-stu-id="63ba0-900">Same as Stroke attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-901">不透明度</span><span class="sxs-lookup"><span data-stu-id="63ba0-901">Opacity</span></span></td>
<td><span data-ttu-id="63ba0-902"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-902"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="63ba0-903">筆劃的不透明度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-903">Opacity of the stroke.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-904">來源</span><span class="sxs-lookup"><span data-stu-id="63ba0-904">Src</span></span></td>
<td><span data-ttu-id="63ba0-905">字串。</span><span class="sxs-lookup"><span data-stu-id="63ba0-905">String.</span></span> <span data-ttu-id="63ba0-906">影像的 URL，以載入影像和模式填滿。</span><span class="sxs-lookup"><span data-stu-id="63ba0-906">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="63ba0-907">這個屬性必須一律存在，並指向有效的影像資料，圖片才會出現。</span><span class="sxs-lookup"><span data-stu-id="63ba0-907">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-908">StartArrow</span><span class="sxs-lookup"><span data-stu-id="63ba0-908">StartArrow</span></span></td>
<td><span data-ttu-id="63ba0-909"><strong>VgArrowheadStyle</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-909"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="63ba0-910">直線開頭的箭頭。</span><span class="sxs-lookup"><span data-stu-id="63ba0-910">Arrowhead for the start of the line.</span></span> <span data-ttu-id="63ba0-911">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-911">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-912">[無] (預設值)</span><span class="sxs-lookup"><span data-stu-id="63ba0-912">None (default)</span></span></li>
<li><span data-ttu-id="63ba0-913">封鎖</span><span class="sxs-lookup"><span data-stu-id="63ba0-913">Block</span></span></li>
<li><span data-ttu-id="63ba0-914">傳統</span><span class="sxs-lookup"><span data-stu-id="63ba0-914">Classic</span></span></li>
<li><span data-ttu-id="63ba0-915">菱形</span><span class="sxs-lookup"><span data-stu-id="63ba0-915">Diamond</span></span></li>
<li><span data-ttu-id="63ba0-916">橢圓形</span><span class="sxs-lookup"><span data-stu-id="63ba0-916">Oval</span></span></li>
<li><span data-ttu-id="63ba0-917">開啟</span><span class="sxs-lookup"><span data-stu-id="63ba0-917">Open</span></span></li>
<li><span data-ttu-id="63ba0-918">&gt; 形箭號</span><span class="sxs-lookup"><span data-stu-id="63ba0-918">Chevron</span></span></li>
<li><span data-ttu-id="63ba0-919">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="63ba0-919">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-920">StartArrowLength</span><span class="sxs-lookup"><span data-stu-id="63ba0-920">StartArrowLength</span></span></td>
<td><span data-ttu-id="63ba0-921">VgArrowHeadLength.</span><span class="sxs-lookup"><span data-stu-id="63ba0-921">VgArrowHeadLength.</span></span> <span data-ttu-id="63ba0-922">直線開頭的箭頭長度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-922">Arrowhead length for the start of the line.</span></span> <span data-ttu-id="63ba0-923">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-923">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-924">Short</span><span class="sxs-lookup"><span data-stu-id="63ba0-924">Short</span></span></li>
<li><span data-ttu-id="63ba0-925">中 (預設)</span><span class="sxs-lookup"><span data-stu-id="63ba0-925">Medium (default)</span></span></li>
<li><span data-ttu-id="63ba0-926">long</span><span class="sxs-lookup"><span data-stu-id="63ba0-926">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-927">StartArrowWidth</span><span class="sxs-lookup"><span data-stu-id="63ba0-927">StartArrowWidth</span></span></td>
<td><span data-ttu-id="63ba0-928">VgArrowheadWidth.</span><span class="sxs-lookup"><span data-stu-id="63ba0-928">VgArrowheadWidth.</span></span> <span data-ttu-id="63ba0-929">線條開頭的箭頭寬度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-929">Arrowhead width for the start of the line.</span></span> <span data-ttu-id="63ba0-930">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-930">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-931">窄中型 (預設) 寬</span><span class="sxs-lookup"><span data-stu-id="63ba0-931">Narrow Medium (default) Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-932">Weight</span><span class="sxs-lookup"><span data-stu-id="63ba0-932">Weight</span></span></td>
<td><span data-ttu-id="63ba0-933"><a href="msdn-online-vml-vglength.md">VgLength</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-933"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="63ba0-934">線條的寬度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-934">Width of line.</span></span> <span data-ttu-id="63ba0-935">範圍從0到1584。</span><span class="sxs-lookup"><span data-stu-id="63ba0-935">Ranges from 0 to 1584.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="63ba0-936">DashStyle 屬性可讓使用者指定自訂定義的虛線模式。</span><span class="sxs-lookup"><span data-stu-id="63ba0-936">The DashStyle attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="63ba0-937">這是使用一連串的數位來完成。</span><span class="sxs-lookup"><span data-stu-id="63ba0-937">This is done using a series of numbers.</span></span> <span data-ttu-id="63ba0-938">虛線樣式是以虛線的長度來定義， (筆觸的繪製部分) 和虛線之間的空間長度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-938">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="63ba0-939">長度是相對於線條寬度;長度為 &quot; 1 &quot; 等於線條寬度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-939">The lengths are relative to the line width; a length of &quot;1&quot; is equal to the line width.</span></span> <span data-ttu-id="63ba0-940">EndCap 樣式會套用至每個虛線，而箭號樣式則不適用。</span><span class="sxs-lookup"><span data-stu-id="63ba0-940">The EndCap style is applied to each dash, arrow styles are not.</span></span> <span data-ttu-id="63ba0-941">字串會先定義虛線的長度，然後再定義空間的長度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-941">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="63ba0-942">這可能會重複形成複雜的虛線樣式。</span><span class="sxs-lookup"><span data-stu-id="63ba0-942">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="63ba0-943">字串應該一律包含成對的數位;如果它包含奇數數目的數位，則可能會忽略最後一個。</span><span class="sxs-lookup"><span data-stu-id="63ba0-943">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span> <span data-ttu-id="63ba0-944">下表列出一些一般值和預期效果的描述。</span><span class="sxs-lookup"><span data-stu-id="63ba0-944">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="63ba0-945">&quot;0 &quot; 表示應該 epirus 對稱的點 (使用 round endcaps，它應該是圓形) 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-945">&quot;0&quot; implies a dot that should be fourfold symmetrical (with round endcaps it should be a circle).</span></span> <span data-ttu-id="63ba0-946">如果行 endcap 是平面的，則檢視器應該 (盡可能選擇內建的作業系統虛線，也就是可快速繪製) 的東西。</span><span class="sxs-lookup"><span data-stu-id="63ba0-946">If the line endcap is Flat, a viewer should choose a built-in operating system dash where possible (i.e., something that is fast to draw).</span></span> <span data-ttu-id="63ba0-947">以下顯示一些範例。</span><span class="sxs-lookup"><span data-stu-id="63ba0-947">The following shows some examples.</span></span>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-948">&quot;2 2&quot;</span><span class="sxs-lookup"><span data-stu-id="63ba0-948">&quot;2 2&quot;</span></span></td>
<td><span data-ttu-id="63ba0-949">虛線 (每個虛線，而介於兩者之間的空格是線條寬度的兩倍) </span><span class="sxs-lookup"><span data-stu-id="63ba0-949">short-dashes (each dash and the space in between is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-950">&quot;1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="63ba0-950">&quot;1 2&quot;</span></span></td>
<td><span data-ttu-id="63ba0-951">點 (每個虛線都是線條的寬度，而每個空格是線條寬度的兩倍) </span><span class="sxs-lookup"><span data-stu-id="63ba0-951">dot (each dash is the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-952">&quot;4 2&quot;</span><span class="sxs-lookup"><span data-stu-id="63ba0-952">&quot;4 2&quot;</span></span></td>
<td><span data-ttu-id="63ba0-953">虛線 (每個虛線的寬度會是線條寬度的四倍，而每個空格是線條寬度的兩倍) </span><span class="sxs-lookup"><span data-stu-id="63ba0-953">dash (each dash is four times the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-954">&quot;8 2&quot;</span><span class="sxs-lookup"><span data-stu-id="63ba0-954">&quot;8 2&quot;</span></span></td>
<td><span data-ttu-id="63ba0-955">長虛線</span><span class="sxs-lookup"><span data-stu-id="63ba0-955">long-dash</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-956">&quot;4 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="63ba0-956">&quot;4 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="63ba0-957">虛線點</span><span class="sxs-lookup"><span data-stu-id="63ba0-957">dash dot</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-958">&quot;8 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="63ba0-958">&quot;8 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="63ba0-959">長虛線點</span><span class="sxs-lookup"><span data-stu-id="63ba0-959">long-dash dot</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-960">&quot;8 2 1 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="63ba0-960">&quot;8 2 1 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="63ba0-961">長虛線點點</span><span class="sxs-lookup"><span data-stu-id="63ba0-961">long-dash dot dot</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a><span data-ttu-id="63ba0-962">TextPath 元素</span><span class="sxs-lookup"><span data-stu-id="63ba0-962">TextPath element</span></span>

<span data-ttu-id="63ba0-963">描述以提供的文字資料、字型和樣式為基礎的向量路徑。</span><span class="sxs-lookup"><span data-stu-id="63ba0-963">Describes a vector path based on the text data, font, and styles supplied.</span></span> <span data-ttu-id="63ba0-964">如果有提供，則會扭曲文字路徑以符合 **路徑** 元素。</span><span class="sxs-lookup"><span data-stu-id="63ba0-964">The text path is warped to conform to a **Path** element if supplied.</span></span>



|   <span data-ttu-id="63ba0-965">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-965">Attribute</span></span>        |   <span data-ttu-id="63ba0-966">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-966">Description</span></span>                                                                                                                                                                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba0-967">FitPath</span><span class="sxs-lookup"><span data-stu-id="63ba0-967">FitPath</span></span>  | <span data-ttu-id="63ba0-968">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-968">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-969">調整文字大小以填滿其所在的路徑。</span><span class="sxs-lookup"><span data-stu-id="63ba0-969">Sizes the text to fill the path it lies out on.</span></span>                                 |
| <span data-ttu-id="63ba0-970">FitShape</span><span class="sxs-lookup"><span data-stu-id="63ba0-970">FitShape</span></span> | <span data-ttu-id="63ba0-971">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-971">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-972">將文字路徑延伸至圖形方塊的邊緣。</span><span class="sxs-lookup"><span data-stu-id="63ba0-972">Stretches the text path out to the edges of the shape box.</span></span>                      |
| <span data-ttu-id="63ba0-973">開啟</span><span class="sxs-lookup"><span data-stu-id="63ba0-973">On</span></span>       | <span data-ttu-id="63ba0-974">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-974">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-975">決定是否要顯示字元路徑。</span><span class="sxs-lookup"><span data-stu-id="63ba0-975">Determines whether the character paths are displayed or not.</span></span>                    |
| <span data-ttu-id="63ba0-976">String</span><span class="sxs-lookup"><span data-stu-id="63ba0-976">String</span></span>   | <span data-ttu-id="63ba0-977">字串。</span><span class="sxs-lookup"><span data-stu-id="63ba0-977">String.</span></span> <span data-ttu-id="63ba0-978">要轉譯為文字路徑的文字。</span><span class="sxs-lookup"><span data-stu-id="63ba0-978">The text to render as a text path.</span></span>                                                                                    |
| <span data-ttu-id="63ba0-979">Trim</span><span class="sxs-lookup"><span data-stu-id="63ba0-979">Trim</span></span>     | <span data-ttu-id="63ba0-980">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-980">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-981">如果未使用，則移除保留給 ascenders 和下行的任何其他空間。</span><span class="sxs-lookup"><span data-stu-id="63ba0-981">Removes any additional space reserved for ascenders and descenders if not used.</span></span> |
| <span data-ttu-id="63ba0-982">XScale</span><span class="sxs-lookup"><span data-stu-id="63ba0-982">XScale</span></span>   | <span data-ttu-id="63ba0-983">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-983">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-984">使用直接 x 度量，而不是沿著路徑進行測量。</span><span class="sxs-lookup"><span data-stu-id="63ba0-984">Use straight x measurement instead of measuring along the path.</span></span>                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a><span data-ttu-id="63ba0-985">在 VML 物件模型中使用的資料類型</span><span class="sxs-lookup"><span data-stu-id="63ba0-985">Data Types Used in the VML Object Model</span></span>

<span data-ttu-id="63ba0-986">VML 物件模型會使用下列資料類型。</span><span class="sxs-lookup"><span data-stu-id="63ba0-986">The following data types are used by the VML Object Model.</span></span>

-   [<span data-ttu-id="63ba0-987">Double</span><span class="sxs-lookup"><span data-stu-id="63ba0-987">Double</span></span>](/windows)
-   [<span data-ttu-id="63ba0-988">固定</span><span class="sxs-lookup"><span data-stu-id="63ba0-988">Fixed</span></span>](/windows)
-   [<span data-ttu-id="63ba0-989">整數</span><span class="sxs-lookup"><span data-stu-id="63ba0-989">Integer</span></span>](/windows)
-   [<span data-ttu-id="63ba0-990">IVgAdjustments</span><span class="sxs-lookup"><span data-stu-id="63ba0-990">IVgAdjustments</span></span>](/windows)
-   [<span data-ttu-id="63ba0-991">IVgColor</span><span class="sxs-lookup"><span data-stu-id="63ba0-991">IVgColor</span></span>](/windows)
-   [<span data-ttu-id="63ba0-992">IVgEquation</span><span class="sxs-lookup"><span data-stu-id="63ba0-992">IVgEquation</span></span>](/windows)
-   [<span data-ttu-id="63ba0-993">IVgFixedRectangle</span><span class="sxs-lookup"><span data-stu-id="63ba0-993">IVgFixedRectangle</span></span>](/windows)
-   [<span data-ttu-id="63ba0-994">IVgFixedRectangleArray</span><span class="sxs-lookup"><span data-stu-id="63ba0-994">IVgFixedRectangleArray</span></span>](/windows)
-   [<span data-ttu-id="63ba0-995">IVgFormula</span><span class="sxs-lookup"><span data-stu-id="63ba0-995">IVgFormula</span></span>](/windows)
-   [<span data-ttu-id="63ba0-996">IVgFormulas</span><span class="sxs-lookup"><span data-stu-id="63ba0-996">IVgFormulas</span></span>](/windows)
-   [<span data-ttu-id="63ba0-997">IVgGradientColorArray</span><span class="sxs-lookup"><span data-stu-id="63ba0-997">IVgGradientColorArray</span></span>](/windows)
-   [<span data-ttu-id="63ba0-998">IVgPoints</span><span class="sxs-lookup"><span data-stu-id="63ba0-998">IVgPoints</span></span>](/windows)
-   [<span data-ttu-id="63ba0-999">IVgSkewMatrix</span><span class="sxs-lookup"><span data-stu-id="63ba0-999">IVgSkewMatrix</span></span>](/windows)
-   [<span data-ttu-id="63ba0-1000">IVgSkewOffset</span><span class="sxs-lookup"><span data-stu-id="63ba0-1000">IVgSkewOffset</span></span>](/windows)
-   [<span data-ttu-id="63ba0-1001">IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="63ba0-1001">IVgVector2D</span></span>](/windows)
-   [<span data-ttu-id="63ba0-1002">IVgVector3D</span><span class="sxs-lookup"><span data-stu-id="63ba0-1002">IVgVector3D</span></span>](/windows)
-   [<span data-ttu-id="63ba0-1003">長度</span><span class="sxs-lookup"><span data-stu-id="63ba0-1003">Length</span></span>](/windows)
-   [<span data-ttu-id="63ba0-1004">Measure</span><span class="sxs-lookup"><span data-stu-id="63ba0-1004">Measure</span></span>](/windows)
-   [<span data-ttu-id="63ba0-1005">String</span><span class="sxs-lookup"><span data-stu-id="63ba0-1005">String</span></span>](/windows)
-   [<span data-ttu-id="63ba0-1006">VgBlackWhiteMode</span><span class="sxs-lookup"><span data-stu-id="63ba0-1006">VgBlackWhiteMode</span></span>](/windows)
-   [<span data-ttu-id="63ba0-1007">VgFraction</span><span class="sxs-lookup"><span data-stu-id="63ba0-1007">VgFraction</span></span>](/windows)
-   [<span data-ttu-id="63ba0-1008">VgTriState</span><span class="sxs-lookup"><span data-stu-id="63ba0-1008">VgTriState</span></span>](/windows)

<span data-ttu-id="63ba0-1009">**Double 資料類型**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1009">**Double data type**</span></span>

<span data-ttu-id="63ba0-1010">雙精確度整數，其範圍從-無限大到無限大。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1010">A double precision integer with range from -infinity to infinity.</span></span>

<span data-ttu-id="63ba0-1011">**固定資料類型**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1011">**Fixed data type**</span></span>

<span data-ttu-id="63ba0-1012">浮點數，範圍從-32766.0 到32766.0。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1012">Floating point number with range from -32,766.0 to 32,766.0.</span></span>

<span data-ttu-id="63ba0-1013">**整數資料類型**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1013">**Integer data type**</span></span>

<span data-ttu-id="63ba0-1014">範圍從-無限大到無限大的整數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1014">An integer with a range from -infinity to infinity.</span></span>

<span data-ttu-id="63ba0-1015">**IVgAdjustments 資料類型**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1015">**IVgAdjustments data type**</span></span>

<span data-ttu-id="63ba0-1016">圖形的調整集合，可以用來變更圖形的維度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1016">Collection of adjustments to a shape that can be used to change the dimensions of a shape.</span></span> <span data-ttu-id="63ba0-1017">調整可用來作為暫時預留位置，或因任何原因而使用變數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1017">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="63ba0-1018">集合中只有8項調整。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1018">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="63ba0-1019">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-1019">Attribute</span></span> | <span data-ttu-id="63ba0-1020">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1020">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba0-1021">Exists</span><span class="sxs-lookup"><span data-stu-id="63ba0-1021">Exists</span></span>     | <span data-ttu-id="63ba0-1022">[IVgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1022">[IVgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="63ba0-1023">判斷指定的調整是否存在。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1023">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="63ba0-1024">請注意，必須使用索引;也就是說， ( 專案 ) 必須用來取出專案的存在。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1024">Note that an index must be used; that is, exists( item ) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="63ba0-1025">項目</span><span class="sxs-lookup"><span data-stu-id="63ba0-1025">Item</span></span>       | <span data-ttu-id="63ba0-1026">[Long](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1026">[Long](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1027">從0到7的索引調整陣列。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1027">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="63ba0-1028">請注意，可能會 sparcely 指定調整;也就是說，中繼陣列值可能不一定會填滿。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1028">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="63ba0-1029">例如，專案1、3和5的值可能是3，而專案 (0) 、專案 (2) 和專案 (4) 指定。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1029">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="63ba0-1030">若要查看專案是否存在，請使用 Exists 屬性。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1030">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="63ba0-1031">長度</span><span class="sxs-lookup"><span data-stu-id="63ba0-1031">Length</span></span>     | <span data-ttu-id="63ba0-1032">[Integer](#data-types-used-in-the-vml-object-model) (整數)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1032">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1033">調整的數目。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1033">Number of adjustments.</span></span> <span data-ttu-id="63ba0-1034">不能大於8。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1034">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="63ba0-1035">值</span><span class="sxs-lookup"><span data-stu-id="63ba0-1035">Value</span></span>      | <span data-ttu-id="63ba0-1036">[字串](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1036">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1037">數值的文字標記法，每個數位之間都有逗號。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1037">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="63ba0-1038">**IVgColor**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1038">**IVgColor**</span></span>

<span data-ttu-id="63ba0-1039">指定色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1039">Specifies a color.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63ba0-1040">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-1040">Attributes</span></span></th>
<th><span data-ttu-id="63ba0-1041">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1041">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-1042">RGB</span><span class="sxs-lookup"><span data-stu-id="63ba0-1042">RGB</span></span></td>
<td><span data-ttu-id="63ba0-1043"><strong>VgRGBType</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1043"><strong>VgRGBType</strong>.</span></span> <span data-ttu-id="63ba0-1044">RGB 值 (色彩的長) 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1044">RGB value (Long) of the color.</span></span> <span data-ttu-id="63ba0-1045">只有當類型為 RGB 時才有效。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1045">Only valid if Type is RGB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1046">R</span><span class="sxs-lookup"><span data-stu-id="63ba0-1046">R</span></span></td>
<td><span data-ttu-id="63ba0-1047"><a href="#data-types-used-in-the-vml-object-model">Integer</a> (整數)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1047"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="63ba0-1048">色彩的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1048">Red component of the color.</span></span> <span data-ttu-id="63ba0-1049">的範圍可以介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1049">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1050">G</span><span class="sxs-lookup"><span data-stu-id="63ba0-1050">G</span></span></td>
<td><span data-ttu-id="63ba0-1051"><a href="#data-types-used-in-the-vml-object-model">Integer</a> (整數)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1051"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="63ba0-1052">色彩的綠色元件。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1052">Green component of the color.</span></span> <span data-ttu-id="63ba0-1053">的範圍可以介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1053">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1054">B</span><span class="sxs-lookup"><span data-stu-id="63ba0-1054">B</span></span></td>
<td><span data-ttu-id="63ba0-1055"><a href="#data-types-used-in-the-vml-object-model">Integer</a> (整數)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1055"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="63ba0-1056">色彩的藍色元件。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1056">Blue component of the color.</span></span> <span data-ttu-id="63ba0-1057">的範圍可以介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1057">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1058">String</span><span class="sxs-lookup"><span data-stu-id="63ba0-1058">String</span></span></td>
<td><span data-ttu-id="63ba0-1059"><a href="#data-types-used-in-the-vml-object-model">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1059"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="63ba0-1060">色彩的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1060">Text representation of the color.</span></span> <span data-ttu-id="63ba0-1061">以下是支援的命名色彩類型：</span><span class="sxs-lookup"><span data-stu-id="63ba0-1061">The following named color types are supported:</span></span>
<ul>
<li><span data-ttu-id="63ba0-1062">黑色 (#000000) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1062">Black (#000000)</span></span></li>
<li><span data-ttu-id="63ba0-1063">銀級 (#C0C0C0) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1063">Silver (#C0C0C0)</span></span></li>
<li><span data-ttu-id="63ba0-1064">灰色 (#808080) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1064">Gray (#808080)</span></span></li>
<li><span data-ttu-id="63ba0-1065">白色 (#FFFFFF) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1065">White (#FFFFFF)</span></span></li>
<li><span data-ttu-id="63ba0-1066"> (#800000) 的暗紫紅色</span><span class="sxs-lookup"><span data-stu-id="63ba0-1066">Maroon (#800000)</span></span></li>
<li><span data-ttu-id="63ba0-1067">紅色 (#FF0000) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1067">Red (#FF0000)</span></span></li>
<li><span data-ttu-id="63ba0-1068">紫色 (#800080) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1068">Purple (#800080)</span></span></li>
<li><span data-ttu-id="63ba0-1069">Fuchsia (#FF00FF) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1069">Fuchsia (#FF00FF)</span></span></li>
<li><span data-ttu-id="63ba0-1070">綠色 (#008000) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1070">Green (#008000)</span></span></li>
<li><span data-ttu-id="63ba0-1071"> (#00FF00) 的橙色</span><span class="sxs-lookup"><span data-stu-id="63ba0-1071">Lime (#00FF00)</span></span></li>
<li><span data-ttu-id="63ba0-1072">) 的橄欖綠 (#808000</span><span class="sxs-lookup"><span data-stu-id="63ba0-1072">Olive (#808000)</span></span></li>
<li><span data-ttu-id="63ba0-1073">黃色 (#FFFF00) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1073">Yellow (#FFFF00)</span></span></li>
<li><span data-ttu-id="63ba0-1074">Navy (#000080) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1074">Navy (#000080)</span></span></li>
<li><span data-ttu-id="63ba0-1075">藍色 (#0000FF) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1075">Blue (#0000FF)</span></span></li>
<li><span data-ttu-id="63ba0-1076">青色 (#008080) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1076">Teal (#008080)</span></span></li>
<li><span data-ttu-id="63ba0-1077">綠色 (#00FFFF) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1077">Aqua (#00FFFF)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1078">類型</span><span class="sxs-lookup"><span data-stu-id="63ba0-1078">Type</span></span></td>
<td><span data-ttu-id="63ba0-1079"><strong>VgColorType</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1079"><strong>VgColorType</strong>.</span></span> <span data-ttu-id="63ba0-1080">色彩的類型。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1080">Type of color.</span></span> <span data-ttu-id="63ba0-1081">下列其中一種類型：</span><span class="sxs-lookup"><span data-stu-id="63ba0-1081">One of the following types:</span></span>
<ul>
<li><span data-ttu-id="63ba0-1082">Mixed</span><span class="sxs-lookup"><span data-stu-id="63ba0-1082">Mixed</span></span></li>
<li><span data-ttu-id="63ba0-1083">已命名</span><span class="sxs-lookup"><span data-stu-id="63ba0-1083">Named</span></span></li>
<li><span data-ttu-id="63ba0-1084">RGB</span><span class="sxs-lookup"><span data-stu-id="63ba0-1084">RGB</span></span></li>
<li><span data-ttu-id="63ba0-1085">配置</span><span class="sxs-lookup"><span data-stu-id="63ba0-1085">Scheme</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="63ba0-1086">**IVgEquation**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1086">**IVgEquation**</span></span>

<span data-ttu-id="63ba0-1087">用於公式的方程式。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1087">Equations used for formulas.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-1088">作業</span><span class="sxs-lookup"><span data-stu-id="63ba0-1088">Operation</span></span></td>
<td><span data-ttu-id="63ba0-1089"><strong>VgEquationOperationType</strong> 要在參數上執行的作業名稱。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1089"><strong>VgEquationOperationType</strong> Name of operation to perform on the parameters.</span></span> <span data-ttu-id="63ba0-1090">下列作業可用於方程式：</span><span class="sxs-lookup"><span data-stu-id="63ba0-1090">The following operations can be used in an equation:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="63ba0-1091">作業</span><span class="sxs-lookup"><span data-stu-id="63ba0-1091">Operation</span></span></th>
<th><span data-ttu-id="63ba0-1092">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1092">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-1093">Abs</span><span class="sxs-lookup"><span data-stu-id="63ba0-1093">Abs</span></span></td>
<td><span data-ttu-id="63ba0-1094">絕對值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1094">Absolute value.</span></span> <br/> <span data-ttu-id="63ba0-1095"><strong>abs</strong> (v) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1095"><strong>abs</strong>(v)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1096">Atan2</span><span class="sxs-lookup"><span data-stu-id="63ba0-1096">Atan2</span></span></td>
<td><span data-ttu-id="63ba0-1097">極座標：以 fd 單位 (度乘以 65536) 的結果。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1097">Polar arithmetic--results in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="63ba0-1098"><strong>atan2</strong> (p1，v) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1098"><strong>atan2</strong>(p1,v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1099">Cos</span><span class="sxs-lookup"><span data-stu-id="63ba0-1099">Cos</span></span></td>
<td><span data-ttu-id="63ba0-1100">在 fd 單位中的余弦值、引數 (度乘以 65536) 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1100">Cosine, argument in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="63ba0-1101">v \* <strong>cos</strong> (p1) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1101">v \* <strong>cos</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1102">Cosatan2</span><span class="sxs-lookup"><span data-stu-id="63ba0-1102">Cosatan2</span></span></td>
<td><span data-ttu-id="63ba0-1103">在中繼計算中保留完整的精確度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1103">Preserves full accuracy in intermediate calculation.</span></span><br/> <span data-ttu-id="63ba0-1104">v \* <strong>cos (atan2 (</strong> p2，p1 <strong>) ) </strong></span><span class="sxs-lookup"><span data-stu-id="63ba0-1104">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1105">橢圓形</span><span class="sxs-lookup"><span data-stu-id="63ba0-1105">Ellipse</span></span></td>
<td><span data-ttu-id="63ba0-1106">橢圓形</span><span class="sxs-lookup"><span data-stu-id="63ba0-1106">Ellipse</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1107">如果</span><span class="sxs-lookup"><span data-stu-id="63ba0-1107">If</span></span></td>
<td><span data-ttu-id="63ba0-1108">如果條件測試。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1108">If Condition test.</span></span> <span data-ttu-id="63ba0-1109">v > 0 <strong>？</strong></span><span class="sxs-lookup"><span data-stu-id="63ba0-1109">v > 0 <strong>?</strong></span></span> <span data-ttu-id="63ba0-1110">p1： p2</span><span class="sxs-lookup"><span data-stu-id="63ba0-1110">p1 : p2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1111">最大值</span><span class="sxs-lookup"><span data-stu-id="63ba0-1111">Max</span></span></td>
<td><span data-ttu-id="63ba0-1112">兩個值中較大的一個。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1112">The greater of two values.</span></span> <br/> <span data-ttu-id="63ba0-1113"><strong>max</strong> (v，p1) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1113"><strong>max</strong>(v,p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1114">Mid</span><span class="sxs-lookup"><span data-stu-id="63ba0-1114">Mid</span></span></td>
<td><span data-ttu-id="63ba0-1115">平均 ( v + p1) /2</span><span class="sxs-lookup"><span data-stu-id="63ba0-1115">Average ( v + p1)/2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1116">Min</span><span class="sxs-lookup"><span data-stu-id="63ba0-1116">Min</span></span></td>
<td><span data-ttu-id="63ba0-1117">兩個值的較小者。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1117">The lesser of two values.</span></span> <span data-ttu-id="63ba0-1118"><strong>min</strong> (v，p1) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1118"><strong>min</strong>(v,p1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1119">Mod</span><span class="sxs-lookup"><span data-stu-id="63ba0-1119">Mod</span></span></td>
<td><span data-ttu-id="63ba0-1120">模數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1120">Modulus.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1121">產品</span><span class="sxs-lookup"><span data-stu-id="63ba0-1121">Product</span></span></td>
<td><span data-ttu-id="63ba0-1122">用於乘法和除法。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1122">Used for multiplication and division.</span></span> <span data-ttu-id="63ba0-1123">v \* p1/p2</span><span class="sxs-lookup"><span data-stu-id="63ba0-1123">v \* p1 / p2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1124">Sin</span><span class="sxs-lookup"><span data-stu-id="63ba0-1124">Sin</span></span></td>
<td><span data-ttu-id="63ba0-1125">在 fd 單位中的正弦值、引數 (度乘以 65536) 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1125">Sine, argument in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="63ba0-1126">v \* <strong>sin</strong> (p1) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1126">v \* <strong>sin</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1127">Sinatan2</span><span class="sxs-lookup"><span data-stu-id="63ba0-1127">Sinatan2</span></span></td>
<td><span data-ttu-id="63ba0-1128">在中繼計算中保留完整的精確度。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1128">Preserves full accuracy in intermediate calculation.</span></span> <span data-ttu-id="63ba0-1129">v \* <strong>sin</strong> (<strong>atan2</strong> (p2，p1) ) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1129">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1130">Sqrt</span><span class="sxs-lookup"><span data-stu-id="63ba0-1130">Sqrt</span></span></td>
<td><span data-ttu-id="63ba0-1131">結果為正向下四捨五入。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1131">Result is positive and rounds down.</span></span> <br/> <span data-ttu-id="63ba0-1132"><strong>sqrt</strong> (v) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1132"><strong>sqrt</strong>(v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1133">Sum</span><span class="sxs-lookup"><span data-stu-id="63ba0-1133">Sum</span></span></td>
<td><span data-ttu-id="63ba0-1134">用於加法和減法。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1134">Used for addition and subtraction.</span></span><br/> <span data-ttu-id="63ba0-1135">v + p1 p2</span><span class="sxs-lookup"><span data-stu-id="63ba0-1135">v + p1 p2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1136">Sumangle</span><span class="sxs-lookup"><span data-stu-id="63ba0-1136">Sumangle</span></span></td>
<td><span data-ttu-id="63ba0-1137">現有的角度 (以 65536) 調整，其中 p1 和 p2 是以度為單位。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1137">Existing angle (scaled by 65536), where p1 and p2 are in degrees.</span></span><br/> <span data-ttu-id="63ba0-1138">v + p1 \* 65536 + p2 \* 65536</span><span class="sxs-lookup"><span data-stu-id="63ba0-1138">v + p1 \* 65536 + p2 \* 65536</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1139">Tan</span><span class="sxs-lookup"><span data-stu-id="63ba0-1139">Tan</span></span></td>
<td><span data-ttu-id="63ba0-1140">正切函數的引數為 fd 單位 (度乘以 65536) 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1140">Tangent, argument is in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="63ba0-1141">v \* tan ( p1 ) </span><span class="sxs-lookup"><span data-stu-id="63ba0-1141">v \* tan( p1 )</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1142">Val</span><span class="sxs-lookup"><span data-stu-id="63ba0-1142">Val</span></span></td>
<td><span data-ttu-id="63ba0-1143">定義其他值的輔助線值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1143">Defines a guide value from some other value.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1144">Param1</span><span class="sxs-lookup"><span data-stu-id="63ba0-1144">Param1</span></span></td>
<td><span data-ttu-id="63ba0-1145"><strong>Integer</strong> (整數)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1145"><strong>Integer</strong>.</span></span> <span data-ttu-id="63ba0-1146">第一個參數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1146">The first parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1147">Paramtype1</span><span class="sxs-lookup"><span data-stu-id="63ba0-1147">Paramtype1</span></span></td>
<td><span data-ttu-id="63ba0-1148"><strong>VgFormulaParamType</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1148"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="63ba0-1149">第一個參數的型別。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1149">The type of the first parameter.</span></span> <span data-ttu-id="63ba0-1150">支援下列值：</span><span class="sxs-lookup"><span data-stu-id="63ba0-1150">The following values are supported:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="63ba0-1151">類型</span><span class="sxs-lookup"><span data-stu-id="63ba0-1151">Type</span></span></th>
<th><span data-ttu-id="63ba0-1152">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1152">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-1153">值</span><span class="sxs-lookup"><span data-stu-id="63ba0-1153">Value</span></span></td>
<td><span data-ttu-id="63ba0-1154">參數是簡單的值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1154">Parameter is simple value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1155">AdjustmentReference</span><span class="sxs-lookup"><span data-stu-id="63ba0-1155">AdjustmentReference</span></span></td>
<td><span data-ttu-id="63ba0-1156">參數是調整的參考。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1156">Parameter is a reference to an adjustment.</span></span> <span data-ttu-id="63ba0-1157">例如，如果第一個參數是1，則會使用第一次調整的值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1157">For example, if the first parameter is 1, then the value of the first adjustment will be used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1158">FormulaReference</span><span class="sxs-lookup"><span data-stu-id="63ba0-1158">FormulaReference</span></span></td>
<td><span data-ttu-id="63ba0-1159">參數是先前公式的結果參考結果。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1159">Parameter is the result of a reference to the result of a previous formula.</span></span> <span data-ttu-id="63ba0-1160">例如，如果第一個參數是2，則會使用公式2的結果。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1160">For example, if the first parameter is 2, then the result of formula 2 will be used.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1161">Param2</span><span class="sxs-lookup"><span data-stu-id="63ba0-1161">Param2</span></span></td>
<td><span data-ttu-id="63ba0-1162"><strong>Integer</strong> (整數)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1162"><strong>Integer</strong>.</span></span> <span data-ttu-id="63ba0-1163">第二個參數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1163">The second parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1164">Paramtype2</span><span class="sxs-lookup"><span data-stu-id="63ba0-1164">Paramtype2</span></span></td>
<td><span data-ttu-id="63ba0-1165"><strong>VgFormulaParamType</strong> 參數2的型別。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1165"><strong>VgFormulaParamType</strong> The type of parameter 2.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1166">Val</span><span class="sxs-lookup"><span data-stu-id="63ba0-1166">Val</span></span></td>
<td><span data-ttu-id="63ba0-1167"><strong>Integer</strong> (整數)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1167"><strong>Integer</strong>.</span></span> <span data-ttu-id="63ba0-1168">結果。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1168">The result.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1169">Valtype2</span><span class="sxs-lookup"><span data-stu-id="63ba0-1169">Valtype2</span></span></td>
<td><span data-ttu-id="63ba0-1170"><strong>VgFormulaParamType</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1170"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="63ba0-1171">結果的類型。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1171">The type of the result.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="63ba0-1172">**IVgFixedRectangle**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1172">**IVgFixedRectangle**</span></span>

<span data-ttu-id="63ba0-1173">指定固定的矩形。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1173">Specifies a fixed rectangle.</span></span>



| <span data-ttu-id="63ba0-1174">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-1174">Attribute</span></span> | <span data-ttu-id="63ba0-1175">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1175">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba0-1176">值</span><span class="sxs-lookup"><span data-stu-id="63ba0-1176">Value</span></span>      | <span data-ttu-id="63ba0-1177">[字串](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1177">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1178">指定路徑的文字值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1178">Text value specifying the path.</span></span>         |
| <span data-ttu-id="63ba0-1179">Left</span><span class="sxs-lookup"><span data-stu-id="63ba0-1179">Left</span></span>       | <span data-ttu-id="63ba0-1180">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1180">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1181">矩形的最左邊座標。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1181">Leftmost coordinate of the rectangle.</span></span>   |
| <span data-ttu-id="63ba0-1182">頁首</span><span class="sxs-lookup"><span data-stu-id="63ba0-1182">Top</span></span>        | <span data-ttu-id="63ba0-1183">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1183">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1184">矩形的最上層座標。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1184">Topmost coordinate of the rectangle.</span></span>    |
| <span data-ttu-id="63ba0-1185">Right</span><span class="sxs-lookup"><span data-stu-id="63ba0-1185">Right</span></span>      | <span data-ttu-id="63ba0-1186">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1186">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1187">矩形的最右側座標。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1187">Rightmost coordinate of the rectangle.</span></span>  |
| <span data-ttu-id="63ba0-1188">下層</span><span class="sxs-lookup"><span data-stu-id="63ba0-1188">Bottom</span></span>     | <span data-ttu-id="63ba0-1189">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1189">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1190">矩形的最底層座標。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1190">Bottommost coordinate of the rectangle.</span></span> |



 

<span data-ttu-id="63ba0-1191">**IVgFixedRectangleArray**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1191">**IVgFixedRectangleArray**</span></span>

<span data-ttu-id="63ba0-1192">固定矩形的陣列。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1192">Array of fixed rectangles.</span></span>



| <span data-ttu-id="63ba0-1193">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-1193">Attribute</span></span> | <span data-ttu-id="63ba0-1194">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1194">Description</span></span>                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba0-1195">值</span><span class="sxs-lookup"><span data-stu-id="63ba0-1195">Value</span></span>      | <span data-ttu-id="63ba0-1196">[字串](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1196">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1197">陣列的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1197">Text representation of array.</span></span>                           |
| <span data-ttu-id="63ba0-1198">長度</span><span class="sxs-lookup"><span data-stu-id="63ba0-1198">Length</span></span>     | <span data-ttu-id="63ba0-1199">[Integer](#data-types-used-in-the-vml-object-model) (整數)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1199">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1200">此陣列中的矩形數目。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1200">Number of rectangles in this array.</span></span>                    |
| <span data-ttu-id="63ba0-1201">項目</span><span class="sxs-lookup"><span data-stu-id="63ba0-1201">Item</span></span>       | <span data-ttu-id="63ba0-1202">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1202">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1203">位於指定索引處的矩形物件。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1203">The rectangle object at the specified index.</span></span> |



 

<span data-ttu-id="63ba0-1204">**IVgFormula** 資料類型</span><span class="sxs-lookup"><span data-stu-id="63ba0-1204">**IVgFormula** data type</span></span>

<span data-ttu-id="63ba0-1205">公式的定義，可以改變形狀的路徑，或用於其他計算用途。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1205">Definitions for formulas that can vary the path of a shape or be used for other calculation purposes.</span></span> <span data-ttu-id="63ba0-1206">公式可以根據可能變更之圖形的 **形容詞** 屬性。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1206">Formulas can be based on the **Adj** attribute of a shape, which can change.</span></span> <span data-ttu-id="63ba0-1207">公式也可以參考其他公式。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1207">Formulas can reference other formulas as well.</span></span>



| <span data-ttu-id="63ba0-1208">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-1208">Attribute</span></span>| <span data-ttu-id="63ba0-1209">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1209">Description</span></span>                                           |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba0-1210">Eqn</span><span class="sxs-lookup"><span data-stu-id="63ba0-1210">Eqn</span></span>        | <span data-ttu-id="63ba0-1211">[IVgEquation](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1211">[IVgEquation](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1212">每個公式都會將單一值定義為運算式評估的結果。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1212">Each formula defines a single value as the result of the evaluation of the expression.</span></span> <span data-ttu-id="63ba0-1213">運算式是由這個屬性所定義，且具有最多三個引數的一般形式，也就是調整值 (例如， \# 2) 、先前公式的結果 (例如 @2) 、固定數位或預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1213">The expression is defined by this attribute and has the general form of an operation followed by up to three arguments, which may be adjustment values (e.g., \#2), the results of earlier formulas (e.g., @2), fixed numbers, or predefined values.</span></span> |



 

<span data-ttu-id="63ba0-1214">**IVgFormulas 資料類型**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1214">**IVgFormulas data type**</span></span>

<span data-ttu-id="63ba0-1215">公式物件的集合。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1215">A collection of formula objects.</span></span>



| <span data-ttu-id="63ba0-1216">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-1216">Attribute</span></span> | <span data-ttu-id="63ba0-1217">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1217">Description</span></span>                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba0-1218">長度</span><span class="sxs-lookup"><span data-stu-id="63ba0-1218">Length</span></span>     | <span data-ttu-id="63ba0-1219">[Integer](#data-types-used-in-the-vml-object-model) (整數)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1219">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1220">集合中的公式物件數目。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1220">Number of formula objects in collection.</span></span>                                                |
| <span data-ttu-id="63ba0-1221">項目</span><span class="sxs-lookup"><span data-stu-id="63ba0-1221">Item</span></span>       | <span data-ttu-id="63ba0-1222">[IVgFormula](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1222">[IVgFormula](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1223">特定的公式。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1223">A specific formula.</span></span> <span data-ttu-id="63ba0-1224">請注意，公式陣列可能會繼承從圖形類型。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1224">Note that the formula array may be inherited fom the shape type.</span></span> |



 

<span data-ttu-id="63ba0-1225">**IVgGradientColorArray**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1225">**IVgGradientColorArray**</span></span>

<span data-ttu-id="63ba0-1226">色彩的陣列，定義) 的漸層 (混合的色彩範圍。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1226">An array of colors that define a gradient (blended range of colors).</span></span>



| <span data-ttu-id="63ba0-1227">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-1227">Attribute</span></span> | <span data-ttu-id="63ba0-1228">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1228">Description</span></span>                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba0-1229">值</span><span class="sxs-lookup"><span data-stu-id="63ba0-1229">Value</span></span>      | <span data-ttu-id="63ba0-1230">[字串](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1230">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1231">指定色彩的陣列;例如，"red. 2;綠. 4;黑色. 7 "</span><span class="sxs-lookup"><span data-stu-id="63ba0-1231">Specifies the array of colors; for example, "red .2; green .4; black .7"</span></span> |
| <span data-ttu-id="63ba0-1232">長度</span><span class="sxs-lookup"><span data-stu-id="63ba0-1232">Length</span></span>     | <span data-ttu-id="63ba0-1233">[Integer](#data-types-used-in-the-vml-object-model) (整數)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1233">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1234">陣列中的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1234">Number of colors in the array.</span></span>                                          |



 



| <span data-ttu-id="63ba0-1235">方法</span><span class="sxs-lookup"><span data-stu-id="63ba0-1235">Method</span></span>     | <span data-ttu-id="63ba0-1236">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1236">Description</span></span>                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba0-1237">AddColor</span><span class="sxs-lookup"><span data-stu-id="63ba0-1237">AddColor</span></span>    | <span data-ttu-id="63ba0-1238">[VgFraction](msdn-online-vml-vgfraction-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1238">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="63ba0-1239">在分數指定的端點上加入新的色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1239">Adds new color at endpoint specified by fraction.</span></span> <span data-ttu-id="63ba0-1240">新的色彩預設為白色，而是傳回值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1240">The new color is white by default and is the return value.</span></span> <span data-ttu-id="63ba0-1241">然後可以透過參考來變更色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1241">The color can then be changed by reference.</span></span> |
| <span data-ttu-id="63ba0-1242">RemoveColor</span><span class="sxs-lookup"><span data-stu-id="63ba0-1242">RemoveColor</span></span> | <span data-ttu-id="63ba0-1243">[VgFraction](msdn-online-vml-vgfraction-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1243">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="63ba0-1244">移除依分數指定之端點的色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1244">Removes a color at endpoint specified by fraction.</span></span> <span data-ttu-id="63ba0-1245">注意：如果0.0 或1.0 不存在，就表示它是隱含的，而且會在該點使用白色的色彩。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1245">Note: if 0.0 or 1.0 does not exist, it is implied and the color white is used at that point.</span></span>          |



 

<span data-ttu-id="63ba0-1246">**IVgPoints 資料類型**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1246">**IVgPoints datatype**</span></span>

<span data-ttu-id="63ba0-1247">定義圖形的點陣列。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1247">Array of points that define a shape.</span></span>



| <span data-ttu-id="63ba0-1248">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-1248">Attribute</span></span> | <span data-ttu-id="63ba0-1249">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1249">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ba0-1250">值</span><span class="sxs-lookup"><span data-stu-id="63ba0-1250">Value</span></span>      | <span data-ttu-id="63ba0-1251">[字串](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1251">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1252">陣列的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1252">Text representation of array.</span></span>           |
| <span data-ttu-id="63ba0-1253">長度</span><span class="sxs-lookup"><span data-stu-id="63ba0-1253">Length</span></span>     | <span data-ttu-id="63ba0-1254">[Integer](#data-types-used-in-the-vml-object-model) (整數)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1254">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="63ba0-1255">此陣列中的點數目。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1255">Number of points in this array.</span></span>        |
| <span data-ttu-id="63ba0-1256">項目</span><span class="sxs-lookup"><span data-stu-id="63ba0-1256">Item</span></span>       | <span data-ttu-id="63ba0-1257">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1257">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="63ba0-1258">指定之索引處的點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1258">The point at the specified index.</span></span> |



 

<span data-ttu-id="63ba0-1259">**IVgSkewMatrix 資料類型**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1259">**IVgSkewMatrix datatype**</span></span>

<span data-ttu-id="63ba0-1260">用於扭曲形狀的矩陣，以 "*sxx，sxy，syx，syy，px，.py* " \[ *s* = scale， *p* = 透視圖形式的觀點轉換矩陣 \] 。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1260">A matrix used for skewing shapes, a perspective transform matrix in the form, "*sxx,sxy,syx,syy,px,py* " \[*s* =scale, *p* =perspective\].</span></span> <span data-ttu-id="63ba0-1261">如果 offset 是絕對單位，則 *px，.py* 是以 emu ^ 1 單位為單位;否則是圖形大小的反向分數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1261">If offset is in absolute units, then *px,py* are in emu ^-1 units; otherwise they are an inverse fraction of shape size.</span></span>



| <span data-ttu-id="63ba0-1262">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-1262">Attribute</span></span>   | <span data-ttu-id="63ba0-1263">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1263">Description</span></span>                                         |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="63ba0-1264">XtoX</span><span class="sxs-lookup"><span data-stu-id="63ba0-1264">XtoX</span></span>         | <span data-ttu-id="63ba0-1265">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1265">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="63ba0-1266">YtoX</span><span class="sxs-lookup"><span data-stu-id="63ba0-1266">YtoX</span></span>         | <span data-ttu-id="63ba0-1267">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1267">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="63ba0-1268">XtoY</span><span class="sxs-lookup"><span data-stu-id="63ba0-1268">XtoY</span></span>         | <span data-ttu-id="63ba0-1269">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1269">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="63ba0-1270">YtoY</span><span class="sxs-lookup"><span data-stu-id="63ba0-1270">YtoY</span></span>         | <span data-ttu-id="63ba0-1271">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1271">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="63ba0-1272">PerspectiveX</span><span class="sxs-lookup"><span data-stu-id="63ba0-1272">PerspectiveX</span></span> | <span data-ttu-id="63ba0-1273">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1273">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="63ba0-1274">PerspectiveY</span><span class="sxs-lookup"><span data-stu-id="63ba0-1274">PerspectiveY</span></span> | <span data-ttu-id="63ba0-1275">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1275">[Double](#data-types-used-in-the-vml-object-model).</span></span> |



 

<span data-ttu-id="63ba0-1276">**IVgSkewOffset**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1276">**IVgSkewOffset**</span></span>

<span data-ttu-id="63ba0-1277">指定扭曲的位移。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1277">Specifies the offset of the skew.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63ba0-1278">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-1278">Attributes</span></span></th>
<th><span data-ttu-id="63ba0-1279">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1279">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-1280">值</span><span class="sxs-lookup"><span data-stu-id="63ba0-1280">Value</span></span></td>
<td><span data-ttu-id="63ba0-1281"><a href="#data-types-used-in-the-vml-object-model">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1281"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="63ba0-1282">位移的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1282">Text representation of offset.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1283">X</span><span class="sxs-lookup"><span data-stu-id="63ba0-1283">X</span></span></td>
<td><span data-ttu-id="63ba0-1284"><a href="#data-types-used-in-the-vml-object-model">Double</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1284"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="63ba0-1285">X 元件。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1285">X component.</span></span> <span data-ttu-id="63ba0-1286">百分比或量值。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1286">Percentage or measure.</span></span> <span data-ttu-id="63ba0-1287">如果沒有單位，則隱含 ShapeRelative 類型;否則，就會隱含絕對型別。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1287">If no units, then ShapeRelative type is implied; otherwise Absolute type is implied.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1288">Y</span><span class="sxs-lookup"><span data-stu-id="63ba0-1288">Y</span></span></td>
<td><span data-ttu-id="63ba0-1289"><a href="#data-types-used-in-the-vml-object-model">Double</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1289"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="63ba0-1290">Y 元件。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1290">Y component.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1291">類型</span><span class="sxs-lookup"><span data-stu-id="63ba0-1291">Type</span></span></td>
<td><span data-ttu-id="63ba0-1292"><strong>VgSkewTransformType</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1292"><strong>VgSkewTransformType</strong>.</span></span> <span data-ttu-id="63ba0-1293">指定轉換的類型。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1293">Specifies the type of transformation.</span></span> <span data-ttu-id="63ba0-1294">有效的值是介於-無限大和無限大之間的整數點。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1294">Valid values are integer points ranging between -infinity and infinity.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="63ba0-1295">類型</span><span class="sxs-lookup"><span data-stu-id="63ba0-1295">Type</span></span></th>
<th><span data-ttu-id="63ba0-1296">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1296">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-1297">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="63ba0-1297">ShapeRelative</span></span></td>
<td><span data-ttu-id="63ba0-1298">位移的值是原始圖形大小 (比例) 的百分比;例如，值0.5 表示形狀大小的位移一半。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1298">The values of the offset are percentages (ratios) of the original shape's size; e.g., a value of 0.5 means an offset half the size of the shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1299">絕對</span><span class="sxs-lookup"><span data-stu-id="63ba0-1299">Absolute</span></span></td>
<td><span data-ttu-id="63ba0-1300">這些值是絕對單位。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1300">The values are absolute units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="63ba0-1301">**IVgVector2D 資料類型**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1301">**IVgVector2D data type**</span></span>

<span data-ttu-id="63ba0-1302">指定由兩個 **雙精度浮** 點陣列成的二維向量。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1302">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63ba0-1303">屬性</span><span class="sxs-lookup"><span data-stu-id="63ba0-1303">Attributes</span></span></th>
<th><span data-ttu-id="63ba0-1304">描述</span><span class="sxs-lookup"><span data-stu-id="63ba0-1304">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-1305">值</span><span class="sxs-lookup"><span data-stu-id="63ba0-1305">Value</span></span></td>
<td><span data-ttu-id="63ba0-1306"><strong>字串</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1306"><strong>String</strong>.</span></span> <span data-ttu-id="63ba0-1307">以空格分隔的兩個向量數位的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1307">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1308">X</span><span class="sxs-lookup"><span data-stu-id="63ba0-1308">X</span></span></td>
<td><span data-ttu-id="63ba0-1309"><a href="#data-types-used-in-the-vml-object-model">Double</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1309"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="63ba0-1310">這個向量的 X 元件。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1310">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1311">Y</span><span class="sxs-lookup"><span data-stu-id="63ba0-1311">Y</span></span></td>
<td><span data-ttu-id="63ba0-1312"><a href="#data-types-used-in-the-vml-object-model">Double</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1312"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="63ba0-1313">這個向量的 Y 元件。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1313">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1314">類型</span><span class="sxs-lookup"><span data-stu-id="63ba0-1314">Type</span></span></td>
<td><span data-ttu-id="63ba0-1315"><strong>VgVectorType</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1315"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="63ba0-1316">此向量的預期單位。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1316">Expected units for this vector.</span></span> <span data-ttu-id="63ba0-1317">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-1317">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-1318">量值</span><span class="sxs-lookup"><span data-stu-id="63ba0-1318">Measure</span></span></li>
<li><span data-ttu-id="63ba0-1319">長度</span><span class="sxs-lookup"><span data-stu-id="63ba0-1319">Length</span></span></li>
<li><span data-ttu-id="63ba0-1320">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="63ba0-1320">AngleInDegrees</span></span></li>
<li><span data-ttu-id="63ba0-1321">Fraction</span><span class="sxs-lookup"><span data-stu-id="63ba0-1321">Fraction</span></span></li>
<li><span data-ttu-id="63ba0-1322">數位百分比整數</span><span class="sxs-lookup"><span data-stu-id="63ba0-1322">Number Percentage Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="63ba0-1323">**IVgVector3D 資料類型**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1323">**IVgVector3D data type**</span></span>

<span data-ttu-id="63ba0-1324">指定由三個 **雙精度浮** 點陣列成的三維向量。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1324">Specifies a three-dimensional vector consisting of three **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63ba0-1325">值</span><span class="sxs-lookup"><span data-stu-id="63ba0-1325">Value</span></span></td>
<td><span data-ttu-id="63ba0-1326"><strong>字串</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1326"><strong>String</strong>.</span></span> <span data-ttu-id="63ba0-1327">以空格分隔的三個向量數位的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1327">Text representation of three vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1328">X</span><span class="sxs-lookup"><span data-stu-id="63ba0-1328">X</span></span></td>
<td><span data-ttu-id="63ba0-1329"><a href="#data-types-used-in-the-vml-object-model">Double</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1329"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="63ba0-1330">這個向量的 X 元件。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1330">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1331">Y</span><span class="sxs-lookup"><span data-stu-id="63ba0-1331">Y</span></span></td>
<td><span data-ttu-id="63ba0-1332"><a href="#data-types-used-in-the-vml-object-model">Double</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1332"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="63ba0-1333">這個向量的 Y 元件。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1333">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63ba0-1334">Z</span><span class="sxs-lookup"><span data-stu-id="63ba0-1334">Z</span></span></td>
<td><span data-ttu-id="63ba0-1335"><a href="#data-types-used-in-the-vml-object-model">Double</a>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1335"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="63ba0-1336">此向量的 Z 元件。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1336">Z component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63ba0-1337">類型</span><span class="sxs-lookup"><span data-stu-id="63ba0-1337">Type</span></span></td>
<td><span data-ttu-id="63ba0-1338"><strong>VgVectorType</strong>。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1338"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="63ba0-1339">此向量的預期單位。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1339">Expected units for this vector.</span></span> <span data-ttu-id="63ba0-1340">值為：</span><span class="sxs-lookup"><span data-stu-id="63ba0-1340">Values are:</span></span>
<ul>
<li><span data-ttu-id="63ba0-1341">量值</span><span class="sxs-lookup"><span data-stu-id="63ba0-1341">Measure</span></span></li>
<li><span data-ttu-id="63ba0-1342">長度</span><span class="sxs-lookup"><span data-stu-id="63ba0-1342">Length</span></span></li>
<li><span data-ttu-id="63ba0-1343">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="63ba0-1343">AngleInDegrees</span></span></li>
<li><span data-ttu-id="63ba0-1344">Fraction</span><span class="sxs-lookup"><span data-stu-id="63ba0-1344">Fraction</span></span></li>
<li><span data-ttu-id="63ba0-1345">數字</span><span class="sxs-lookup"><span data-stu-id="63ba0-1345">Number</span></span></li>
<li><span data-ttu-id="63ba0-1346">百分比</span><span class="sxs-lookup"><span data-stu-id="63ba0-1346">Percentage</span></span></li>
<li><span data-ttu-id="63ba0-1347">整數</span><span class="sxs-lookup"><span data-stu-id="63ba0-1347">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="63ba0-1348">**Length 資料類型**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1348">**Length data type**</span></span>

<span data-ttu-id="63ba0-1349">浮點數，範圍介於0到無限大之間。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1349">A floating point number with a range from 0 to infinity.</span></span>

<span data-ttu-id="63ba0-1350">**量值資料類型**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1350">**Measure data type**</span></span>

<span data-ttu-id="63ba0-1351">從-無限大到無限大的浮點數。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1351">A floating point number from -infinity to infinity.</span></span>

<span data-ttu-id="63ba0-1352">**字串資料類型**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1352">**String data type**</span></span>

<span data-ttu-id="63ba0-1353">任何長度的字元資料。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1353">Character data of any length.</span></span>

<span data-ttu-id="63ba0-1354">**VgBlackWhiteMode**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1354">**VgBlackWhiteMode**</span></span>

<span data-ttu-id="63ba0-1355">黑色和白色的呈現模式。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1355">Rendering mode for black and white.</span></span> <span data-ttu-id="63ba0-1356">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="63ba0-1356">Possible values are:</span></span>

-   <span data-ttu-id="63ba0-1357">**色彩**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1357">**Color**</span></span>
-   <span data-ttu-id="63ba0-1358">**Auto**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1358">**Auto**</span></span>
-   <span data-ttu-id="63ba0-1359">**灰度**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1359">**GrayScale**</span></span>
-   <span data-ttu-id="63ba0-1360">**LightGrayScale**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1360">**LightGrayScale**</span></span>
-   <span data-ttu-id="63ba0-1361">**InverseGray**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1361">**InverseGray**</span></span>
-   <span data-ttu-id="63ba0-1362">**GrayOutline**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1362">**GrayOutline**</span></span>
-   <span data-ttu-id="63ba0-1363">**BlackTextAndLines**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1363">**BlackTextAndLines**</span></span>
-   <span data-ttu-id="63ba0-1364">**HighContrast**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1364">**HighContrast**</span></span>
-   <span data-ttu-id="63ba0-1365">**黑色**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1365">**Black**</span></span>
-   <span data-ttu-id="63ba0-1366">**白色**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1366">**White**</span></span>
-   <span data-ttu-id="63ba0-1367">**Undrawn**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1367">**Undrawn**</span></span>

<span data-ttu-id="63ba0-1368">**VgFraction 資料類型**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1368">**VgFraction data type**</span></span>

<span data-ttu-id="63ba0-1369">浮點數，範圍從0.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1369">Floating point number with range from 0.0 to 1.0.</span></span> <span data-ttu-id="63ba0-1370">分數也可以指定為百分比;例如，"50%"。</span><span class="sxs-lookup"><span data-stu-id="63ba0-1370">Fractions can also be specified as a percentage; e.g., "50%".</span></span>

<span data-ttu-id="63ba0-1371">**VgTriState 資料類型**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1371">**VgTriState datatype**</span></span>

<span data-ttu-id="63ba0-1372">列舉值，用於可為三種狀態之一的值：</span><span class="sxs-lookup"><span data-stu-id="63ba0-1372">Enumeration used for values that can be one of three states:</span></span>

-   <span data-ttu-id="63ba0-1373">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1373">**TRUE**</span></span>
-   <span data-ttu-id="63ba0-1374">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1374">**FALSE**</span></span>
-   <span data-ttu-id="63ba0-1375">**MIXED**</span><span class="sxs-lookup"><span data-stu-id="63ba0-1375">**MIXED**</span></span>