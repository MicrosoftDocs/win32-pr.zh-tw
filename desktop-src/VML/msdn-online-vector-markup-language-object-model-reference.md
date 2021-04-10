---
title: VML 物件模型參考
description: 本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889c977260548c26bbfd8196160e4537ccb8895d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023999"
---
# <a name="vml-object-model-reference"></a><span data-ttu-id="5b6f3-104">VML 物件模型參考</span><span class="sxs-lookup"><span data-stu-id="5b6f3-104">VML Object Model Reference</span></span>

<span data-ttu-id="5b6f3-105">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-105">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5b6f3-106">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-106">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5b6f3-107">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-107">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5b6f3-108">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-108">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5b6f3-109">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-109">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5b6f3-110">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-110">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5b6f3-111">本主題內容：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-111">In this topic:</span></span>

-   [<span data-ttu-id="5b6f3-112">簡介</span><span class="sxs-lookup"><span data-stu-id="5b6f3-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="5b6f3-113">範例</span><span class="sxs-lookup"><span data-stu-id="5b6f3-113">Example</span></span>](#example)
-   [<span data-ttu-id="5b6f3-114">設定 VML</span><span class="sxs-lookup"><span data-stu-id="5b6f3-114">Setting up VML</span></span>](#setting-up-vml)
-   [<span data-ttu-id="5b6f3-115">VML OM 參考</span><span class="sxs-lookup"><span data-stu-id="5b6f3-115">VML OM Reference</span></span>](#vml-om-reference)
    -   [<span data-ttu-id="5b6f3-116">Shape 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-116">Shape element</span></span>](#shape-element)
-   [<span data-ttu-id="5b6f3-117">Shape 元素的子項目</span><span class="sxs-lookup"><span data-stu-id="5b6f3-117">Subelements of the Shape Element</span></span>](#subelements-of-the-shape-element)
    -   [<span data-ttu-id="5b6f3-118">Background 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-118">Background element</span></span>](#background-element)
    -   [<span data-ttu-id="5b6f3-119">延伸元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-119">Extrusion element</span></span>](#extrusion-element)
    -   [<span data-ttu-id="5b6f3-120">Fill 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-120">Fill element</span></span>](#fill-element)
    -   [<span data-ttu-id="5b6f3-121">Group 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-121">Group element</span></span>](#group-element)
    -   [<span data-ttu-id="5b6f3-122">Imagedata 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-122">Imagedata element</span></span>](#imagedata-element)
    -   [<span data-ttu-id="5b6f3-123">Path 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-123">Path element</span></span>](#path-element)
    -   [<span data-ttu-id="5b6f3-124">Shadow 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-124">Shadow element</span></span>](#shadow-element)
    -   [<span data-ttu-id="5b6f3-125">扭曲元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-125">Skew element</span></span>](#skew-element)
    -   [<span data-ttu-id="5b6f3-126">Stroke 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-126">Stroke element</span></span>](#stroke-element)
    -   [<span data-ttu-id="5b6f3-127">TextPath 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-127">TextPath element</span></span>](#textpath-element)
-   [<span data-ttu-id="5b6f3-128">在 VML 物件模型中使用的資料類型</span><span class="sxs-lookup"><span data-stu-id="5b6f3-128">Data Types Used in the VML Object Model</span></span>](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a><span data-ttu-id="5b6f3-129">簡介</span><span class="sxs-lookup"><span data-stu-id="5b6f3-129">Introduction</span></span>

<span data-ttu-id="5b6f3-130">[Vector Markup Language (VML) ](https://www.w3.org/TR/NOTE-datetime.html) 是以文字為基礎的語言，使用 [XML](https://www.w3.org/TR/REC-xml.mdl) 擴充 HTML 以顯示向量圖形資訊。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) is a text-based language that uses [XML](https://www.w3.org/TR/REC-xml.mdl) to extend HTML for the purpose of displaying vector graphic information.</span></span> <span data-ttu-id="5b6f3-131">[VML 檔物件模型 (DOM) 會定義用於操作檔元素的程式設計介面。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-131">The VML Document Object Model (DOM) defines a programmatic interface for the manipulation of the document elements.</span></span> <span data-ttu-id="5b6f3-132">這可讓使用者透過平臺和語言中性介面，以動態方式建立和修改向量圖形。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-132">This enables the user to dynamically create and modify vector graphics through a platform- and language-neutral interface.</span></span> <span data-ttu-id="5b6f3-133">VML DOM 符合 [檔物件模型](https://www.w3.org/TR/REC-DOM-Level-1/) 規格。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-133">The VML DOM conforms to the [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specification.</span></span>

<span data-ttu-id="5b6f3-134">VML 使用 [Shape](#shape-element) 元素作為向量圖形影像的基本建築物區塊。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-134">VML uses the [Shape](#shape-element) element as the basic building block for vector graphic images.</span></span> <span data-ttu-id="5b6f3-135">建立圖形之後，您可以透過屬性或附加的子項目來修改圖形。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-135">Once a shape is created, you can modify the shape through attributes or by attached subelements.</span></span> <span data-ttu-id="5b6f3-136">例如，若要變更圖形的色彩，請將色彩值指派給 **FillColor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-136">For example, to change the color of a shape, assign a color value to the **FillColor** attribute.</span></span>


```HTML
myshape.fillcolor = "red"
```



<span data-ttu-id="5b6f3-137">圖形的數個屬性也是子 [元素](/windows) ，而且有自己的屬性，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-137">Several of the attributes of a shape are also [subelements](/windows) and have their own attributes, including the following:</span></span>

-   [<span data-ttu-id="5b6f3-138">背景</span><span class="sxs-lookup"><span data-stu-id="5b6f3-138">Background</span></span>](#background-element)
-   [<span data-ttu-id="5b6f3-139">擠壓</span><span class="sxs-lookup"><span data-stu-id="5b6f3-139">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="5b6f3-140">填滿</span><span class="sxs-lookup"><span data-stu-id="5b6f3-140">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="5b6f3-141">群組</span><span class="sxs-lookup"><span data-stu-id="5b6f3-141">Group</span></span>](#group-element)
-   [<span data-ttu-id="5b6f3-142">Imagedata</span><span class="sxs-lookup"><span data-stu-id="5b6f3-142">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="5b6f3-143">路徑</span><span class="sxs-lookup"><span data-stu-id="5b6f3-143">Path</span></span>](#path-element)
-   [<span data-ttu-id="5b6f3-144">Shadow</span><span class="sxs-lookup"><span data-stu-id="5b6f3-144">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="5b6f3-145">斜</span><span class="sxs-lookup"><span data-stu-id="5b6f3-145">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="5b6f3-146">中風</span><span class="sxs-lookup"><span data-stu-id="5b6f3-146">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="5b6f3-147">TextPath</span><span class="sxs-lookup"><span data-stu-id="5b6f3-147">TextPath</span></span>](#textpath-element)

<span data-ttu-id="5b6f3-148">VML OM 會使用數個 [資料類型](/windows) 來定義參數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-148">The VML OM uses several [data types](/windows) to define parameters.</span></span> <span data-ttu-id="5b6f3-149">前面加上 "Vg" 的資料類型是列舉，而前面加上 "IVg" 的資料類型是物件。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-149">Datatypes prefixed with "Vg" are enumerations and those prefixed with "IVg" are objects.</span></span> <span data-ttu-id="5b6f3-150">按一下這裡以取得清單。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-150">Click here for a list.</span></span> <span data-ttu-id="5b6f3-151">次要資料類型會以特定參數列出。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-151">Minor datatypes are listed with specific parameters.</span></span>

## <a name="example"></a><span data-ttu-id="5b6f3-152">範例</span><span class="sxs-lookup"><span data-stu-id="5b6f3-152">Example</span></span>

<span data-ttu-id="5b6f3-153">下列 VBScript 程式碼顯示如何建立簡單的圖形：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-153">The following VBScript code shows how to create a simple shape:</span></span>


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



<span data-ttu-id="5b6f3-154">在上述範例中，會使用檔物件模型方法 **CreateElement** 來建立圖形。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-154">In the above example, a shape is created by using the Document Object Model method **CreateElement**.</span></span> <span data-ttu-id="5b6f3-155">圖形是一個 VML 預先定義的矩形圖形。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-155">The shape is a VML predefined Rect shape.</span></span> <span data-ttu-id="5b6f3-156">雖然物件存在，但是在附加至檔之前，它不能是檔的一部分。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-156">Even though the object exists, it cannot be part of the document until it is attached to the document.</span></span> <span data-ttu-id="5b6f3-157">使用 **AppendChild** 方法，矩形就會成為名為 MyDiv 的 **DIV** 元素的子系。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-157">Using the **AppendChild** method, the Rect is made a child of a **DIV** element called MyDiv.</span></span> <span data-ttu-id="5b6f3-158">有幾個最小樣式屬性 (**位置**、 **寬度**、 **高度**、 **Top**、 **左方**) 設定成提供圖形特定的大小。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-158">A few minimum style attributes (**Position**, **Width**, **Height**, **Top**, **Left**) are set to give the shape a specific size.</span></span> <span data-ttu-id="5b6f3-159">最後，會使用 **FillColor** 屬性來指派色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-159">Finally, a color is assigned with the **FillColor** attribute.</span></span> <span data-ttu-id="5b6f3-160">請注意，您可以使用任何可搭配檔物件模型介面使用的指令碼語言或任何語言。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-160">Note that any scripting language or any language that can work with Document Object Model interfaces can be used.</span></span>

## <a name="setting-up-vml"></a><span data-ttu-id="5b6f3-161">設定 VML</span><span class="sxs-lookup"><span data-stu-id="5b6f3-161">Setting up VML</span></span>

<span data-ttu-id="5b6f3-162">一個 VML 的執行是透過 Microsoft Internet Explorer 5.0 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-162">One implementation of VML is through Microsoft Internet Explorer 5.0 or greater.</span></span> <span data-ttu-id="5b6f3-163">若要在網頁中正確設定轉譯物件，必須進行下列新增專案：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-163">To set up the rendering object correctly in a Web page, the following additions must be made:</span></span>

1.  <span data-ttu-id="5b6f3-164">必須在初始中設定架構</span><span class="sxs-lookup"><span data-stu-id="5b6f3-164">The schema must be set up in the initial</span></span> <HTML> <span data-ttu-id="5b6f3-165">標記如下：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-165">tag as follows:</span></span>
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  <span data-ttu-id="5b6f3-166">轉譯行為必須是檔樣式的一部分：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-166">The rendering behavior must be part of the document's style:</span></span>
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

<span data-ttu-id="5b6f3-167">以下顯示針對顯示動態建立圖形的 VML 正確設定的 HTML 網頁範例。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-167">The following shows a sample HTML Web page set up correctly for VML showing the dynamic creation of a shape.</span></span>


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



<span data-ttu-id="5b6f3-168">請注意，在 Beta 版中，必須要有 ActiveX 物件標記和不同的行為樣式。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-168">Note that in beta versions, an ActiveX object tag and a different behavior style was required.</span></span>

## <a name="vml-om-reference"></a><span data-ttu-id="5b6f3-169">VML OM 參考</span><span class="sxs-lookup"><span data-stu-id="5b6f3-169">VML OM Reference</span></span>

<span data-ttu-id="5b6f3-170">這個參考定義了 VML 的物件模型所使用的 [Shape](#shape-element) 元素、子 [元素](/windows)和 [資料類型](/windows) 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-170">This reference defines the [Shape](#shape-element) element, [subelements](/windows), and [data types](/windows) that are used by the object model of VML.</span></span>

### <a name="shape-element"></a><span data-ttu-id="5b6f3-171">Shape 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-171">Shape element</span></span>

<span data-ttu-id="5b6f3-172">圖形是 Vector Markup Language (VML) 所定義之圖形影像的建立區塊。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-172">Shapes are the building blocks of graphical images defined by Vector Markup Language (VML).</span></span> <span data-ttu-id="5b6f3-173">圖形是最上層元素，而數個子項目可協助定義每個圖形的本質。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-173">The shape is the top-level element and several subelements help define the nature of each shape.</span></span>

<span data-ttu-id="5b6f3-174">VML 提供預先定義的圖形：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-174">VML provides predefined shapes:</span></span>

<span data-ttu-id="5b6f3-175">**圖形屬性**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-175">**Shape Attributes**</span></span>

-   <span data-ttu-id="5b6f3-176">**Arc**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-176">**Arc**</span></span>
-   <span data-ttu-id="5b6f3-177">**曲線**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-177">**Curve**</span></span>
-   <span data-ttu-id="5b6f3-178">**線條**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-178">**Line**</span></span>
-   <span data-ttu-id="5b6f3-179">**折線**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-179">**PolyLine**</span></span>
-   <span data-ttu-id="5b6f3-180">**Rect**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-180">**Rect**</span></span>
-   <span data-ttu-id="5b6f3-181">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-181">**RoundRect**</span></span>



|              |                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f3-182">形容詞</span><span class="sxs-lookup"><span data-stu-id="5b6f3-182">Adj</span></span>          | <span data-ttu-id="5b6f3-183">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-183">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span></span> <span data-ttu-id="5b6f3-184">以逗號分隔的數位清單，這些是用來定義圖形路徑之指南公式的參數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-184">A comma-delimited list of numbers that are the parameters for the guide formulas that define the path of the shape.</span></span> <span data-ttu-id="5b6f3-185">可能會省略值以允許使用預設值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-185">Values may be omitted to allow for using defaults.</span></span> <span data-ttu-id="5b6f3-186">最多可以有8個調整值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-186">There can be up to 8 adjustment values.</span></span>                                                                                                   |
| <span data-ttu-id="5b6f3-187">Alt</span><span class="sxs-lookup"><span data-stu-id="5b6f3-187">Alt</span></span>          | <span data-ttu-id="5b6f3-188">字串。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-188">String.</span></span> <span data-ttu-id="5b6f3-189">與圖形相關聯的替代文字。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-189">Alternative text associated with shape.</span></span> <span data-ttu-id="5b6f3-190">用於非圖形化流覽。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-190">Used for non-graphical browsing.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="5b6f3-191">按鈕</span><span class="sxs-lookup"><span data-stu-id="5b6f3-191">Button</span></span>       | <span data-ttu-id="5b6f3-192">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-192">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-193">按一下時，會顯示按鈕的行為。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-193">Displays button behavior on click.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="5b6f3-194">BWMode</span><span class="sxs-lookup"><span data-stu-id="5b6f3-194">BWMode</span></span>       | <span data-ttu-id="5b6f3-195">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-195">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="5b6f3-196">決定在應用程式中，或列印到黑白印表機時，圖形會以黑白方式呈現。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-196">Determines how shape will render in black-and-white view in apps or when printed to black-and-white printers.</span></span> <span data-ttu-id="5b6f3-197">值包括： **Color**、 **Auto**、 **灰階**、 **LightGrayScale**、 **InverseGray**、 **GrayOutline**、 **BlackTextAndLines**、 **systeminformation.highcontrast**、 **黑色**、 **白色**、 **Undrawn**。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-197">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="5b6f3-198">預設值： **Auto**。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-198">Default: **Auto**.</span></span> |
| <span data-ttu-id="5b6f3-199">BWNormal</span><span class="sxs-lookup"><span data-stu-id="5b6f3-199">BWNormal</span></span>     | <span data-ttu-id="5b6f3-200">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-200">VgBlackWhiteMode.</span></span> <span data-ttu-id="5b6f3-201">當 BWMode 為 Auto 時，會參考此屬性以瞭解如何以一般黑色和白色呈現圖形。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-201">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span> <span data-ttu-id="5b6f3-202">值包括： **Color**、 **Auto**、 **灰階**、 **LightGrayScale**、 **InverseGray**、 **GrayOutline**、 **BlackTextAndLines**、 **systeminformation.highcontrast**、 **黑色**、 **白色**、 **Undrawn**。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-202">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="5b6f3-203">預設值： **Auto**。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-203">Default: **Auto**.</span></span>                                                |
| <span data-ttu-id="5b6f3-204">BWPure</span><span class="sxs-lookup"><span data-stu-id="5b6f3-204">BWPure</span></span>       | <span data-ttu-id="5b6f3-205">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-205">VgBlackWhiteMode.</span></span> <span data-ttu-id="5b6f3-206">當 BWMode 為 Auto 時，會參考此屬性以瞭解如何以純 B/W 呈現圖形。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-206">When BWMode is Auto, this property is consulted for how to render the shape in pure B/W.</span></span> <span data-ttu-id="5b6f3-207">值包括： **Color**、 **Auto**、 **灰階**、 **LightGrayScale**、 **InverseGray**、 **GrayOutline**、 **BlackTextAndLines**、 **systeminformation.highcontrast**、 **黑色**、 **白色**、 **Undrawn**。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-207">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="5b6f3-208">預設值： **Auto**。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-208">Default: **Auto**.</span></span>                                                              |
| <span data-ttu-id="5b6f3-209">ChildShapes</span><span class="sxs-lookup"><span data-stu-id="5b6f3-209">ChildShapes</span></span>  | <span data-ttu-id="5b6f3-210">IVgGroupShapes.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-210">IVgGroupShapes.</span></span> <span data-ttu-id="5b6f3-211">此群組中其他圖形的集合。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-211">A collection of other shapes in this group.</span></span> <span data-ttu-id="5b6f3-212">此集合支援標準長度和專案方法。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-212">This collection supports the standard Length and Item methods.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="5b6f3-213">Chromakey</span><span class="sxs-lookup"><span data-stu-id="5b6f3-213">Chromakey</span></span>    | <span data-ttu-id="5b6f3-214">[IVgColor](msdn-online-vml-ivgcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-214">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="5b6f3-215">將會是透明的色彩值，並顯示圖形背後的任何事物。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-215">A color value that will be transparent and show anything behind the shape.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="5b6f3-216">Control1</span><span class="sxs-lookup"><span data-stu-id="5b6f3-216">Control1</span></span>     | <span data-ttu-id="5b6f3-217">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-217">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="5b6f3-218">曲線的控制點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-218">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5b6f3-219">Control2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-219">Control2</span></span>     | <span data-ttu-id="5b6f3-220">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-220">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="5b6f3-221">曲線的控制點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-221">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5b6f3-222">CoordOrigin</span><span class="sxs-lookup"><span data-stu-id="5b6f3-222">CoordOrigin</span></span>  | <span data-ttu-id="5b6f3-223">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) 容器矩形左上角的座標。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-223">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) The coordinates at the top left corner of the container rectangle.</span></span> <span data-ttu-id="5b6f3-224">範圍從0到無限大。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-224">Range from 0 to infinity.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="5b6f3-225">CoordSize</span><span class="sxs-lookup"><span data-stu-id="5b6f3-225">CoordSize</span></span>    | <span data-ttu-id="5b6f3-226">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-226">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="5b6f3-227">此圖形之參考矩形內的座標空間的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-227">The width and height of the coordinate space inside the reference rectangle of this shape.</span></span> <span data-ttu-id="5b6f3-228">如果未指定，則與矩形的寬度和高度相同。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-228">If it is not specified, it is the same as the width and height of the rectangle.</span></span> <span data-ttu-id="5b6f3-229">範圍從0到無限大。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-229">Range from 0 to infinity.</span></span> <span data-ttu-id="5b6f3-230">預設值： "1000，1000"。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-230">Default: "1000,1000".</span></span>                                                                                               |
| <span data-ttu-id="5b6f3-231">EndAngle</span><span class="sxs-lookup"><span data-stu-id="5b6f3-231">EndAngle</span></span>     | <span data-ttu-id="5b6f3-232">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-232">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="5b6f3-233">圖形的結束角度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-233">End angle of shape.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5b6f3-234">擠壓</span><span class="sxs-lookup"><span data-stu-id="5b6f3-234">Extrusion</span></span>    | <span data-ttu-id="5b6f3-235">IVgExtrusion.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-235">IVgExtrusion.</span></span> <span data-ttu-id="5b6f3-236">指定此圖形的延伸物件值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-236">Specifies the Extrusion object value for this shape.</span></span> <span data-ttu-id="5b6f3-237">如需詳細資訊，請參閱「 [延伸](msdn-online-vml-extrusion-element.md) 」元素。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-237">See the [Extrusion](msdn-online-vml-extrusion-element.md) element for details.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="5b6f3-238">填滿</span><span class="sxs-lookup"><span data-stu-id="5b6f3-238">Fill</span></span>         | <span data-ttu-id="5b6f3-239">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-239">VgFillFormat.</span></span> <span data-ttu-id="5b6f3-240">指定此圖形的填滿值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-240">Specifies the fill value for this shape.</span></span> <span data-ttu-id="5b6f3-241">如需詳細資訊，請參閱 [Fill](msdn-online-vml-fill-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-241">See the [Fill](msdn-online-vml-fill-element.md) element for more details.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="5b6f3-242">FillColor</span><span class="sxs-lookup"><span data-stu-id="5b6f3-242">FillColor</span></span>    | <span data-ttu-id="5b6f3-243">[IVgColor](msdn-online-vml-ivgcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-243">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="5b6f3-244">要用來填滿此圖形路徑之筆刷的主要色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-244">The primary color of the brush to use to fill the path of this shape.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5b6f3-245">已</span><span class="sxs-lookup"><span data-stu-id="5b6f3-245">Filled</span></span>       | <span data-ttu-id="5b6f3-246">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-246">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-247">若為 True，則會填滿定義圖形的路徑。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-247">If True, the path defining the shape will be filled.</span></span> <span data-ttu-id="5b6f3-248">根據預設，除非有指定更複雜填滿屬性的 Fill 子項目，否則它將會以純色填滿。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-248">By default, it will be filled using a solid color unless there is a Fill subelement that specifies more complex fill properties.</span></span> <span data-ttu-id="5b6f3-249">如果為 False，則填滿是透明的。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-249">If False, the fill is transparent.</span></span>                                                                                                           |
| <span data-ttu-id="5b6f3-250">翻轉</span><span class="sxs-lookup"><span data-stu-id="5b6f3-250">Flip</span></span>         | <span data-ttu-id="5b6f3-251">VgFlipOrientation.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-251">VgFlipOrientation.</span></span> <span data-ttu-id="5b6f3-252">值為： X Y XY YX</span><span class="sxs-lookup"><span data-stu-id="5b6f3-252">Values are: X Y XY YX</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="5b6f3-253">ForceDash</span><span class="sxs-lookup"><span data-stu-id="5b6f3-253">ForceDash</span></span>    | <span data-ttu-id="5b6f3-254">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-254">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-255">指出當圖形沒有線條且沒有填滿時，應該呈現虛線外框。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-255">Indication that a dashed outline should be rendered when there is no line and no fill for a shape.</span></span> <span data-ttu-id="5b6f3-256">這種行為通常適用于在編輯應用程式中顯示隱藏式圖形，因此可以在影像對應中加以選取和操作。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-256">This behavior is generally useful for making invisible shapes visible in editing applications so they can be selected and operated on, such as in an image map.</span></span>                                                                 |
| <span data-ttu-id="5b6f3-257">公式</span><span class="sxs-lookup"><span data-stu-id="5b6f3-257">Formulas</span></span>     | <span data-ttu-id="5b6f3-258">IVgFormulas.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-258">IVgFormulas.</span></span> <span data-ttu-id="5b6f3-259">定義圖形的公式陣列。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-259">An array of formulas that defines a shape.</span></span>                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5b6f3-260">寄件者</span><span class="sxs-lookup"><span data-stu-id="5b6f3-260">From</span></span>         | <span data-ttu-id="5b6f3-261">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-261">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="5b6f3-262">行的起點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-262">Starting point of line.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="5b6f3-263">Href</span><span class="sxs-lookup"><span data-stu-id="5b6f3-263">HRef</span></span>         | <span data-ttu-id="5b6f3-264">[字串](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-264">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-265">如果按一下此圖形，要跳到的 URL。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-265">The URL to jump to if this shape is clicked.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="5b6f3-266">ImageData</span><span class="sxs-lookup"><span data-stu-id="5b6f3-266">ImageData</span></span>    | <span data-ttu-id="5b6f3-267">IVgImageData.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-267">IVgImageData.</span></span> <span data-ttu-id="5b6f3-268">影像資訊（如果圖形是圖片的話）。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-268">Image information if the shape is a picture.</span></span> <span data-ttu-id="5b6f3-269">如需詳細資訊，請參閱 ImageData 元素。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-269">See the ImageData element for more information.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="5b6f3-270">OnEd</span><span class="sxs-lookup"><span data-stu-id="5b6f3-270">OnEd</span></span>         | <span data-ttu-id="5b6f3-271">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-271">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-272">隱藏左上角和右下方以外的所有控制碼，如同直線線段的控制碼一樣。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-272">Hides all handles except the top left and bottom right, as in the handles for a straight line segment.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="5b6f3-273">不透明度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-273">Opacity</span></span>      | <span data-ttu-id="5b6f3-274">[VgFraction](msdn-online-vml-vgfraction-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-274">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="5b6f3-275">整個圖形的不透明度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-275">The opacity of the entire shape.</span></span> <span data-ttu-id="5b6f3-276">介於0.0 到1.0 之間的數位。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-276">A number between 0.0 and 1.0.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="5b6f3-277">路徑</span><span class="sxs-lookup"><span data-stu-id="5b6f3-277">Path</span></span>         | <span data-ttu-id="5b6f3-278">IVgPath.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-278">IVgPath.</span></span> <span data-ttu-id="5b6f3-279">字串，包含定義路徑的命令。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-279">A string containing the commands that define the path.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5b6f3-280">點</span><span class="sxs-lookup"><span data-stu-id="5b6f3-280">Points</span></span>       | <span data-ttu-id="5b6f3-281">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-281">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span></span> <span data-ttu-id="5b6f3-282">定義圖形的點集合。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-282">A collection of points defining a shape.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="5b6f3-283">列印</span><span class="sxs-lookup"><span data-stu-id="5b6f3-283">Print</span></span>        | <span data-ttu-id="5b6f3-284">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-284">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-285">若為 True，表示要列印此圖形。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-285">If True, this shape is meant to be printed.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="5b6f3-286">旋轉</span><span class="sxs-lookup"><span data-stu-id="5b6f3-286">Rotation</span></span>     | <span data-ttu-id="5b6f3-287">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-287">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="5b6f3-288">設定圖形的旋轉。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-288">Sets rotation of shape.</span></span> <span data-ttu-id="5b6f3-289">值會傳播至圖形樣式。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-289">Value is propagated to the shape style.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="5b6f3-290">調整</span><span class="sxs-lookup"><span data-stu-id="5b6f3-290">Scale</span></span>        | <span data-ttu-id="5b6f3-291">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-291">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="5b6f3-292">圖形的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-292">Scale of shape.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="5b6f3-293">陰影</span><span class="sxs-lookup"><span data-stu-id="5b6f3-293">Shadow</span></span>       | <span data-ttu-id="5b6f3-294">IVgShadow.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-294">IVgShadow.</span></span> <span data-ttu-id="5b6f3-295">指定此圖形的陰影。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-295">Specifies the shadow for this shape.</span></span> <span data-ttu-id="5b6f3-296">如需詳細資料，請參閱 [Shadow](msdn-online-vml-shadow-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-296">See the [Shadow](msdn-online-vml-shadow-element.md) element for details.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="5b6f3-297">Spt</span><span class="sxs-lookup"><span data-stu-id="5b6f3-297">Spt</span></span>          | <span data-ttu-id="5b6f3-298">保留的。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-298">Reserved.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="5b6f3-299">>startangle</span><span class="sxs-lookup"><span data-stu-id="5b6f3-299">StartAngle</span></span>   | <span data-ttu-id="5b6f3-300">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-300">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="5b6f3-301">圖形的開始角度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-301">Start angle of shape.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="5b6f3-302">筆勢</span><span class="sxs-lookup"><span data-stu-id="5b6f3-302">Stroke</span></span>       | <span data-ttu-id="5b6f3-303">VgStrokeFormat.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-303">VgStrokeFormat.</span></span> <span data-ttu-id="5b6f3-304">如需詳細資料，請參閱 Stroke 元素。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-304">See Stroke element for details.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5b6f3-305">StrokeColor</span><span class="sxs-lookup"><span data-stu-id="5b6f3-305">StrokeColor</span></span>  | <span data-ttu-id="5b6f3-306">[IVgColor](msdn-online-vml-ivgcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-306">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="5b6f3-307">用來將此圖形的路徑進行筆劃之筆刷的主要色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-307">The primary color of the brush to use to stroke the path of this shape.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="5b6f3-308">撫摸</span><span class="sxs-lookup"><span data-stu-id="5b6f3-308">Stroked</span></span>      | <span data-ttu-id="5b6f3-309">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-309">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-310">若為 True，則會將定義圖形的路徑進行筆劃。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-310">If True, the path defining the shape will be stroked.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5b6f3-311">StrokeWeight</span><span class="sxs-lookup"><span data-stu-id="5b6f3-311">StrokeWeight</span></span> | <span data-ttu-id="5b6f3-312">[VGLength](msdn-online-vml-vglength.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-312">[VGLength](msdn-online-vml-vglength.md).</span></span> <span data-ttu-id="5b6f3-313">用來對路徑進行筆劃的筆刷寬度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-313">The width of the brush to use to stroke the path.</span></span> <span data-ttu-id="5b6f3-314">介於0與1584之間的範圍。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-314">Ranges between 0 and 1584.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="5b6f3-315">TextPath</span><span class="sxs-lookup"><span data-stu-id="5b6f3-315">TextPath</span></span>     | <span data-ttu-id="5b6f3-316">IVgTextPath.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-316">IVgTextPath.</span></span> <span data-ttu-id="5b6f3-317">指定圖形的 TextPath 物件。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-317">Specifies the TextPath object of the shape.</span></span> <span data-ttu-id="5b6f3-318">如需詳細資訊，請參閱 [TextPath](msdn-online-vml-textpath-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-318">See the [TextPath](msdn-online-vml-textpath-element.md) element for more information.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="5b6f3-319">收件者</span><span class="sxs-lookup"><span data-stu-id="5b6f3-319">To</span></span>           | <span data-ttu-id="5b6f3-320">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-320">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="5b6f3-321">行的結束點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-321">End point of line.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="5b6f3-322">類型</span><span class="sxs-lookup"><span data-stu-id="5b6f3-322">Type</span></span>         | <span data-ttu-id="5b6f3-323">字串。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-323">String.</span></span> <span data-ttu-id="5b6f3-324">圖形類型。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-324">Type of shape.</span></span>                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a><span data-ttu-id="5b6f3-325">Shape 元素的子項目</span><span class="sxs-lookup"><span data-stu-id="5b6f3-325">Subelements of the Shape Element</span></span>

<span data-ttu-id="5b6f3-326">下列子項目是 VML 物件模型的一部分。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-326">The following subelements are part of the VML object model.</span></span>

-   [<span data-ttu-id="5b6f3-327">背景</span><span class="sxs-lookup"><span data-stu-id="5b6f3-327">Background</span></span>](#background-element)
-   [<span data-ttu-id="5b6f3-328">擠壓</span><span class="sxs-lookup"><span data-stu-id="5b6f3-328">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="5b6f3-329">填滿</span><span class="sxs-lookup"><span data-stu-id="5b6f3-329">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="5b6f3-330">群組</span><span class="sxs-lookup"><span data-stu-id="5b6f3-330">Group</span></span>](#group-element)
-   [<span data-ttu-id="5b6f3-331">Imagedata</span><span class="sxs-lookup"><span data-stu-id="5b6f3-331">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="5b6f3-332">路徑</span><span class="sxs-lookup"><span data-stu-id="5b6f3-332">Path</span></span>](#path-element)
-   [<span data-ttu-id="5b6f3-333">Shadow</span><span class="sxs-lookup"><span data-stu-id="5b6f3-333">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="5b6f3-334">斜</span><span class="sxs-lookup"><span data-stu-id="5b6f3-334">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="5b6f3-335">中風</span><span class="sxs-lookup"><span data-stu-id="5b6f3-335">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="5b6f3-336">TextPath</span><span class="sxs-lookup"><span data-stu-id="5b6f3-336">TextPath</span></span>](#textpath-element)

### <a name="background-element"></a><span data-ttu-id="5b6f3-337">Background 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-337">Background element</span></span>

<span data-ttu-id="5b6f3-338">描述使用 VML 填滿的頁面背景填滿。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-338">Describes the fill of the background of a page using VML fills.</span></span>

<span data-ttu-id="5b6f3-339">**屬性**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-339">**Attributes**</span></span>



|           |                                                                                                                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f3-340">BWMode</span><span class="sxs-lookup"><span data-stu-id="5b6f3-340">BWMode</span></span>    | <span data-ttu-id="5b6f3-341">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-341">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="5b6f3-342">決定圖形在應用程式中的黑白外觀或列印時的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-342">Determines how shape will render in black-and-white view in applications or when printed.</span></span>                                     |
| <span data-ttu-id="5b6f3-343">BWNormal</span><span class="sxs-lookup"><span data-stu-id="5b6f3-343">BWNormal</span></span>  | <span data-ttu-id="5b6f3-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="5b6f3-345">當 BWMode 為 Auto 時，會參考此屬性以瞭解如何以一般黑色和白色呈現圖形。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-345">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span>                        |
| <span data-ttu-id="5b6f3-346">BWPure</span><span class="sxs-lookup"><span data-stu-id="5b6f3-346">BWPure</span></span>    | <span data-ttu-id="5b6f3-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="5b6f3-348">當 BWMode 為 Auto 時，會參考此屬性以瞭解如何以純黑色和白色呈現圖形。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-348">When BWMode is Auto, this property is consulted for how to render the shape in pure black and white.</span></span>                          |
| <span data-ttu-id="5b6f3-349">填滿</span><span class="sxs-lookup"><span data-stu-id="5b6f3-349">Fill</span></span>      | <span data-ttu-id="5b6f3-350">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-350">VgFillFormat.</span></span> <span data-ttu-id="5b6f3-351">指定此圖形的填滿。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-351">Specifies the fill for this shape.</span></span> <span data-ttu-id="5b6f3-352">如需詳細資訊，請參閱 [Fill](msdn-online-vml-fill-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-352">See [Fill](msdn-online-vml-fill-element.md) element for more information.</span></span>                                                             |
| <span data-ttu-id="5b6f3-353">FillColor</span><span class="sxs-lookup"><span data-stu-id="5b6f3-353">FillColor</span></span> | <span data-ttu-id="5b6f3-354">[IVgColor](msdn-online-vml-ivgcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-354">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="5b6f3-355">要用來填滿此圖形路徑之筆刷的主要色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-355">The primary color of the brush to use to fill the path of this shape.</span></span> <span data-ttu-id="5b6f3-356">Fill 元素中的色彩值重複。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-356">Duplicate of the Color value in the Fill element.</span></span> <span data-ttu-id="5b6f3-357">預設為白色。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-357">The default is white.</span></span> |



 

### <a name="extrusion-element"></a><span data-ttu-id="5b6f3-358">延伸元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-358">Extrusion element</span></span>

<span data-ttu-id="5b6f3-359">描述圖形的立體延伸。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-359">Describes a 3-D extrusion of the shape.</span></span>

<span data-ttu-id="5b6f3-360">**屬性**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-360">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-361">AutoRotationCenter</span><span class="sxs-lookup"><span data-stu-id="5b6f3-361">AutoRotationCenter</span></span></td>
<td><span data-ttu-id="5b6f3-362"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-362"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="5b6f3-363">若為 True，則3D 物件群組的旋轉中心 (事實上，群組中只有一個物件) 會自動判斷為群組的中心;否則，它是由 RotationCenter 參數決定，這是圖形的一部分，0、0、0是中心。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-363">If True, the center of rotation of the group of 3-D objects (in fact there is only ever one object in the group) is determined automatically to be the center of the group; otherwise it is determined by the RotationCenter parameters, which are a fraction of the shape with 0,0,0 being the center.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-364">BackDepth</span><span class="sxs-lookup"><span data-stu-id="5b6f3-364">BackDepth</span></span></td>
<td><span data-ttu-id="5b6f3-365"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-365"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span></span> <span data-ttu-id="5b6f3-366">反向拉伸的數量。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-366">Amount of backward extrusion.</span></span> <span data-ttu-id="5b6f3-367">範圍從0到32767。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-367">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-368">亮度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-368">Brightness</span></span></td>
<td><span data-ttu-id="5b6f3-369"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-369"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="5b6f3-370">場景的整體亮度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-370">Overall brightness of the scene.</span></span> <span data-ttu-id="5b6f3-371">預設值為 &quot; 20000 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-371">Default is &quot;20,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-372">Color</span><span class="sxs-lookup"><span data-stu-id="5b6f3-372">Color</span></span></td>
<td><span data-ttu-id="5b6f3-373"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-373"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="5b6f3-374">拉伸的色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-374">The color of the extrusion.</span></span> <span data-ttu-id="5b6f3-375">只有在 ColorMode 為 Custom 時才會使用。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-375">Only used if ColorMode is Custom.</span></span> <span data-ttu-id="5b6f3-376">否則，會自動將 [拉伸效果] 色彩設定為與 FillColor 相同。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-376">Otherwise, Auto sets the extrusion effect color to the same as FillColor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-377">ColorMode</span><span class="sxs-lookup"><span data-stu-id="5b6f3-377">ColorMode</span></span></td>
<td><span data-ttu-id="5b6f3-378">Vg3DColorMode.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-378">Vg3DColorMode.</span></span> <span data-ttu-id="5b6f3-379">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-379">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-380">Auto (預設值)</span><span class="sxs-lookup"><span data-stu-id="5b6f3-380">Auto (default)</span></span></li>
<li><span data-ttu-id="5b6f3-381">自訂</span><span class="sxs-lookup"><span data-stu-id="5b6f3-381">Custom</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-382">Diffusity</span><span class="sxs-lookup"><span data-stu-id="5b6f3-382">Diffusity</span></span></td>
<td><span data-ttu-id="5b6f3-383"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-383"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="5b6f3-384">要擴散的事件比率反映燈光。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-384">The ratio of incident to diffusely reflected light.</span></span> <span data-ttu-id="5b6f3-385">小於1.0 的值是正常的，但大於1的值可能會產生有趣的效果。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-385">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-386">Edge</span><span class="sxs-lookup"><span data-stu-id="5b6f3-386">Edge</span></span></td>
<td><span data-ttu-id="5b6f3-387"><a href="msdn-online-vml-vglength.md">VgLength</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-387"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="5b6f3-388">設定模擬圓角斜面邊緣的大小。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-388">Sets the size of a simulated rounded beveled edge.</span></span> <span data-ttu-id="5b6f3-389">浮點數中的範圍介於0到32767之間。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-389">Ranges from 0 to 32767 in floating point pts.</span></span> <span data-ttu-id="5b6f3-390">預設值為 &quot; 1pt &quot; 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-390">Default is &quot;1pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-391">Facet</span><span class="sxs-lookup"><span data-stu-id="5b6f3-391">Facet</span></span></td>
<td><span data-ttu-id="5b6f3-392"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-392"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="5b6f3-393">設定場景的 facet。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-393">Sets the facet of the scene.</span></span> <span data-ttu-id="5b6f3-394">預設值為 &quot; 30000 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-394">Default is &quot;30,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-395">ForeDepth</span><span class="sxs-lookup"><span data-stu-id="5b6f3-395">ForeDepth</span></span></td>
<td><span data-ttu-id="5b6f3-396"><a href="msdn-online-vml-vglength.md">VgLength</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-396"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="5b6f3-397">向前延伸的數量。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-397">Amount of forward extrusion.</span></span> <span data-ttu-id="5b6f3-398">範圍從0到32767。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-398">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-399">LightFace</span><span class="sxs-lookup"><span data-stu-id="5b6f3-399">LightFace</span></span></td>
<td><span data-ttu-id="5b6f3-400"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-400"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="5b6f3-401">Determimes 物件的正面臉部是否會回應3-d 照明的變更，例如，當物件旋轉時。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-401">Determimes whether the front face of the object will respond to changes in the 3-D lighting, e.g., when an object rotates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-402">LightHarsh</span><span class="sxs-lookup"><span data-stu-id="5b6f3-402">LightHarsh</span></span></td>
<td><span data-ttu-id="5b6f3-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="5b6f3-404">主要光源的光源。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-404">Harsh lighting for the primary light source.</span></span> <span data-ttu-id="5b6f3-405">預設值是 False。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-405">Default is False.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-406">LightHarsh2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-406">LightHarsh2</span></span></td>
<td><span data-ttu-id="5b6f3-407"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-407"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="5b6f3-408">次要燈光來源的粗糙光源。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-408">Harsh lighting for the secondary light source.</span></span> <span data-ttu-id="5b6f3-409">預設值是 False。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-409">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-410">LightLevel</span><span class="sxs-lookup"><span data-stu-id="5b6f3-410">LightLevel</span></span></td>
<td><span data-ttu-id="5b6f3-411"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-411"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="5b6f3-412">主要燈光來源的濃度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-412">Intensity of the primary light source.</span></span> <span data-ttu-id="5b6f3-413">預設值為 &quot; 38000 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-413">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-414">LightLevel2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-414">LightLevel2</span></span></td>
<td><span data-ttu-id="5b6f3-415"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-415"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="5b6f3-416">次要燈光來源的濃度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-416">Intensity of the secondary light source.</span></span> <span data-ttu-id="5b6f3-417">預設值為 &quot; 38000 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-417">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-418">LightPosition</span><span class="sxs-lookup"><span data-stu-id="5b6f3-418">LightPosition</span></span></td>
<td><span data-ttu-id="5b6f3-419">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-419">Vector3D.</span></span> <span data-ttu-id="5b6f3-420">主要光源來源的位置。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-420">Position of the primary light source.</span></span> <span data-ttu-id="5b6f3-421">預設值為 &quot; 50000、0、10000 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-421">Default is &quot;50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-422">LightPosition2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-422">LightPosition2</span></span></td>
<td><span data-ttu-id="5b6f3-423">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-423">Vector3D.</span></span> <span data-ttu-id="5b6f3-424">次要燈光來源的位置。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-424">Position of the secondary light source.</span></span> <span data-ttu-id="5b6f3-425">預設值為 &quot; -50000、0、10000 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-425">Default is &quot;-50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-426">LockRotationCenter</span><span class="sxs-lookup"><span data-stu-id="5b6f3-426">LockRotationCenter</span></span></td>
<td><span data-ttu-id="5b6f3-427"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-427"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="5b6f3-428">&quot;Lockrotationcenter &quot; 表示群組的旋轉會依照頁面上 y 軸的旋轉角度 [1] 角度定義，後面接著 X 軸的旋轉角度 [0] 角度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-428">&quot;Lockrotationcenter&quot; means that the rotation of the group is defined to be by rotation-angle[1] degrees about the y-axis on the page followed by rotation-angle[0] degrees about the x-axis.</span></span> <span data-ttu-id="5b6f3-429">當 LockRotationCenter 為 False 時，就會根據方向定義的向量，將旋轉定義為面向角度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-429">When LockRotationCenter is False, the rotation is defined to be by orientation-angle degrees about the vector defined by orientation.</span></span> <span data-ttu-id="5b6f3-430">因此，例如，lockrotationcenter = false orientationangle = 45 方向 = (0，1，0) 相當於 lockrotationcenter = true rotationangle = (0，45) 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-430">So, for example, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) is equivalent to lockrotationcenter=true rotationangle=(0,45).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-431">金屬</span><span class="sxs-lookup"><span data-stu-id="5b6f3-431">Metal</span></span></td>
<td><span data-ttu-id="5b6f3-432"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-432"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="5b6f3-433">使反射反映的光線成為材質色彩，而不是光線來源色彩，讓物件看起來更材質。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-433">Causes specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-434">開啟</span><span class="sxs-lookup"><span data-stu-id="5b6f3-434">On</span></span></td>
<td><span data-ttu-id="5b6f3-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="5b6f3-436">開啟和關閉延伸效果的顯示。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-436">Turns the display of the extrusion effect on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-437">Orientation</span><span class="sxs-lookup"><span data-stu-id="5b6f3-437">Orientation</span></span></td>
<td><span data-ttu-id="5b6f3-438">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-438">Vector3D.</span></span> <span data-ttu-id="5b6f3-439">攝影機的方向。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-439">Orientation of the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-440">OrientationAngle</span><span class="sxs-lookup"><span data-stu-id="5b6f3-440">OrientationAngle</span></span></td>
<td><span data-ttu-id="5b6f3-441"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-441"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="5b6f3-442">攝影機方向與 xy 平面之間的角度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-442">Angle between the orientation of the camera and the xy plane.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-443">飛機</span><span class="sxs-lookup"><span data-stu-id="5b6f3-443">Plane</span></span></td>
<td><span data-ttu-id="5b6f3-444">Vg3DExtrudePlane.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-444">Vg3DExtrudePlane.</span></span> <span data-ttu-id="5b6f3-445">允許從平面與螢幕平面垂直的拉伸。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-445">Allows extrusion from planes orthogonal to the screen plane.</span></span> <span data-ttu-id="5b6f3-446">需要以繪圖單位（而非 emus）指定 ForeDepth 和 BackDepth。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-446">Requires ForeDepth and BackDepth to be specified in drawing units instead of emus.</span></span> <span data-ttu-id="5b6f3-447">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-447">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-448">Xy</span><span class="sxs-lookup"><span data-stu-id="5b6f3-448">XY</span></span></li>
<li><span data-ttu-id="5b6f3-449">Zx</span><span class="sxs-lookup"><span data-stu-id="5b6f3-449">ZX</span></span></li>
<li><span data-ttu-id="5b6f3-450">YZ</span><span class="sxs-lookup"><span data-stu-id="5b6f3-450">YZ</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-451">轉譯</span><span class="sxs-lookup"><span data-stu-id="5b6f3-451">Render</span></span></td>
<td><span data-ttu-id="5b6f3-452">Vg3DRenderMode.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-452">Vg3DRenderMode.</span></span> <span data-ttu-id="5b6f3-453">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-453">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-454">Solid (預設值)</span><span class="sxs-lookup"><span data-stu-id="5b6f3-454">Solid (default)</span></span></li>
<li><span data-ttu-id="5b6f3-455">著色</span><span class="sxs-lookup"><span data-stu-id="5b6f3-455">WireFrame</span></span></li>
<li><span data-ttu-id="5b6f3-456">BoundingCube</span><span class="sxs-lookup"><span data-stu-id="5b6f3-456">BoundingCube</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-457">RotationAngle</span><span class="sxs-lookup"><span data-stu-id="5b6f3-457">RotationAngle</span></span></td>
<td><span data-ttu-id="5b6f3-458"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-458"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="5b6f3-459">System.windows.media.skewtransform.anglex、System.windows.media.skewtransform.angley 或 AngleZ 是由 ShapeRotation 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-459">AngleX, AngleY, or AngleZ is controlled by the ShapeRotation attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-460">RotationCenter</span><span class="sxs-lookup"><span data-stu-id="5b6f3-460">RotationCenter</span></span></td>
<td><span data-ttu-id="5b6f3-461">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-461">Vector3D.</span></span> <span data-ttu-id="5b6f3-462">旋轉的中心。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-462">Center of rotation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-463">增</span><span class="sxs-lookup"><span data-stu-id="5b6f3-463">Shininess</span></span></td>
<td><span data-ttu-id="5b6f3-464"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-464"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="5b6f3-465">決定集中或分佈反射反映的方式。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-465">Determines how concentrated or spread out specular reflection is.</span></span> <span data-ttu-id="5b6f3-466">高值會是8到10，而且近似于鏡像，而較低的值會是2至3，而且大約 sequined 服裝。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-466">A high value would be 8 to 10 and would approximate a mirror, and a low value would be 2 to 3 and would approximate sequined clothing.</span></span> <span data-ttu-id="5b6f3-467">建議使用3到7之間的值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-467">Values of 3 to 7 are recommended.</span></span> <span data-ttu-id="5b6f3-468">較高的值會反映出燈燈的來源。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-468">High values will reflect pinpoint light sources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-469">SkewAmt</span><span class="sxs-lookup"><span data-stu-id="5b6f3-469">SkewAmt</span></span></td>
<td><span data-ttu-id="5b6f3-470"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-470"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span></span> <span data-ttu-id="5b6f3-471">如果 Type 是 Parallel，屬性會決定扭曲量。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-471">If Type is Parallel, attribute determines the amount of skew.</span></span> <span data-ttu-id="5b6f3-472">範圍從0到100。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-472">Ranges from 0 to 100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-473">SkewAngle</span><span class="sxs-lookup"><span data-stu-id="5b6f3-473">SkewAngle</span></span></td>
<td><span data-ttu-id="5b6f3-474"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-474"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="5b6f3-475">如果 Type 是 Parallel，屬性會決定扭曲的程度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-475">If Type is Parallel, attribute determines the degree of skew.</span></span> <span data-ttu-id="5b6f3-476">預設值為 &quot; -45 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-476">Default is &quot;-45&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-477">Specularity</span><span class="sxs-lookup"><span data-stu-id="5b6f3-477">Specularity</span></span></td>
<td><span data-ttu-id="5b6f3-478"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-478"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="5b6f3-479">要反射的事件比率反映燈光。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-479">The ratio of incident to specularly reflected light.</span></span> <span data-ttu-id="5b6f3-480">小於1.0 的值是正常的，但大於1的值可能會產生有趣的效果。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-480">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-481">類型</span><span class="sxs-lookup"><span data-stu-id="5b6f3-481">Type</span></span></td>
<td><span data-ttu-id="5b6f3-482">VgExtrusionType.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-482">VgExtrusionType.</span></span> <span data-ttu-id="5b6f3-483">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-483">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-484">平行 (預設) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-484">Parallel (default)</span></span></li>
<li><span data-ttu-id="5b6f3-485">檢視方塊</span><span class="sxs-lookup"><span data-stu-id="5b6f3-485">Perspective</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-486">觀點</span><span class="sxs-lookup"><span data-stu-id="5b6f3-486">Viewpoint</span></span></td>
<td><span data-ttu-id="5b6f3-487">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-487">Vector3D.</span></span> <span data-ttu-id="5b6f3-488">從中查看場景的位置。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-488">The point where the scene is being viewed from.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-489">ViewpointOrigin</span><span class="sxs-lookup"><span data-stu-id="5b6f3-489">ViewpointOrigin</span></span></td>
<td><span data-ttu-id="5b6f3-490"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-490"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="5b6f3-491">可以有從0.5 到-0.5 的值，以定點陣圖形周框方塊內的觀點原點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-491">Can have values from 0.5 to -0.5 to position the origin of the viewpoint within the shape bounding box.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a><span data-ttu-id="5b6f3-492">Fill 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-492">Fill element</span></span>

<span data-ttu-id="5b6f3-493">說明如何針對填滿較純色的填滿路徑。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-493">Describes how a path should be filled for fills more complex than a solid color.</span></span>

<span data-ttu-id="5b6f3-494">**屬性**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-494">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-495">AlignShape</span><span class="sxs-lookup"><span data-stu-id="5b6f3-495">AlignShape</span></span></td>
<td><span data-ttu-id="5b6f3-496"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-496"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="5b6f3-497">將影像與圖形對齊。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-497">Align the image with the shape.</span></span> <span data-ttu-id="5b6f3-498">如果為 False，則會將影像與視窗對齊。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-498">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-499">角度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-499">Angle</span></span></td>
<td><span data-ttu-id="5b6f3-500"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-500"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="5b6f3-501">漸層沿著的角度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-501">The angle along which the gradient goes.</span></span> <span data-ttu-id="5b6f3-502">0度是沿著水準軸從左至右。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-502">0 degrees is along the horizontal axis from left to right.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-503">層面</span><span class="sxs-lookup"><span data-stu-id="5b6f3-503">Aspect</span></span></td>
<td><span data-ttu-id="5b6f3-504"><strong>VgAspectType</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-504"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="5b6f3-505">ImageSize 屬性將會調整，以保留影像的外觀。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-505">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="5b6f3-506">數值包括：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-506">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5b6f3-507">值</span><span class="sxs-lookup"><span data-stu-id="5b6f3-507">Value</span></span></th>
<th><span data-ttu-id="5b6f3-508">描述</span><span class="sxs-lookup"><span data-stu-id="5b6f3-508">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-509">忽略</span><span class="sxs-lookup"><span data-stu-id="5b6f3-509">Ignore</span></span></td>
<td><span data-ttu-id="5b6f3-510">略過外觀問題。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-510">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-511">至少</span><span class="sxs-lookup"><span data-stu-id="5b6f3-511">AtLeast</span></span></td>
<td><span data-ttu-id="5b6f3-512">映射大小至少與影像大小一樣大。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-512">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-513">有</span><span class="sxs-lookup"><span data-stu-id="5b6f3-513">AtMost</span></span></td>
<td><span data-ttu-id="5b6f3-514">影像的大小不會大於影像大小。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-514">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-515">Color</span><span class="sxs-lookup"><span data-stu-id="5b6f3-515">Color</span></span></td>
<td><span data-ttu-id="5b6f3-516"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> 主要填滿色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-516"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> The main fill color.</span></span> <span data-ttu-id="5b6f3-517">與 shape 中的 FillColor 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-517">Same as FillColor attribute in shape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-518">Color2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-518">Color2</span></span></td>
<td><span data-ttu-id="5b6f3-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="5b6f3-520">當影像類型為模式或漸層填滿時，填滿的次要色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-520">The secondary color for a fill when image type is Pattern or a gradient fill.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-521">色彩</span><span class="sxs-lookup"><span data-stu-id="5b6f3-521">Colors</span></span></td>
<td><span data-ttu-id="5b6f3-522"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-522"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span></span> <span data-ttu-id="5b6f3-523">漸層中的中繼色彩及其沿著漸層的相對位置，例如 &quot; 30% 紅色、70% 藍色、90% 綠色 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-523">Intermediate colors in the gradient and their relative positions along the gradient, e.g., &quot;30% red, 70% blue, 90% green&quot;.</span></span> <span data-ttu-id="5b6f3-524">圖形) 中的主要色彩 (色彩屬性為0%，次要色彩 (Color2 屬性) 為100%。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-524">Primary color (Color attribute in shape) is 0% and secondary color (Color2 attribute) is 100%.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-525">焦點</span><span class="sxs-lookup"><span data-stu-id="5b6f3-525">Focus</span></span></td>
<td><span data-ttu-id="5b6f3-526"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-526"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span></span> <span data-ttu-id="5b6f3-527">線性漸層填滿的焦點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-527">Focal point for linear gradient fill.</span></span> <span data-ttu-id="5b6f3-528">值從-100 到 + 100。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-528">Values go from -100 to +100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-529">FocusPosition</span><span class="sxs-lookup"><span data-stu-id="5b6f3-529">FocusPosition</span></span></td>
<td><span data-ttu-id="5b6f3-530"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-530"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="5b6f3-531">放射狀漸層的最內部矩形位置。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-531">Position of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="5b6f3-532">向量是圖形寬度和高度 (0.0-1.0) 的分數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-532">The vector is a fraction (0.0 - 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-533">FocusSize</span><span class="sxs-lookup"><span data-stu-id="5b6f3-533">FocusSize</span></span></td>
<td><span data-ttu-id="5b6f3-534"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> 放射狀漸層的最內部矩形大小。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-534"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Size of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="5b6f3-535">向量是圖形寬度和高度 (0.0 至 1.0) 的分數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-535">The vector is a fraction (0.0 to 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-536">方法</span><span class="sxs-lookup"><span data-stu-id="5b6f3-536">Method</span></span></td>
<td><span data-ttu-id="5b6f3-537">VgSigmaType.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-537">VgSigmaType.</span></span> <span data-ttu-id="5b6f3-538">數值包括：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-538">Values include:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-539">無</span><span class="sxs-lookup"><span data-stu-id="5b6f3-539">None</span></span></li>
<li><span data-ttu-id="5b6f3-540">線性</span><span class="sxs-lookup"><span data-stu-id="5b6f3-540">Linear</span></span></li>
<li><span data-ttu-id="5b6f3-541">Sigma</span><span class="sxs-lookup"><span data-stu-id="5b6f3-541">Sigma</span></span></li>
<li><span data-ttu-id="5b6f3-542">任意</span><span class="sxs-lookup"><span data-stu-id="5b6f3-542">Any</span></span></li>
</ul>
<p><span data-ttu-id="5b6f3-543">預設值為 Sigma。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-543">Default is Sigma.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-544">開啟</span><span class="sxs-lookup"><span data-stu-id="5b6f3-544">On</span></span></td>
<td><span data-ttu-id="5b6f3-545"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-545"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="5b6f3-546">開啟填滿顯示。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-546">Turns fill display on.</span></span> <span data-ttu-id="5b6f3-547">與 shape 中的 Fill 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-547">Same as Fill attribute in shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-548">不透明度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-548">Opacity</span></span></td>
<td><span data-ttu-id="5b6f3-549"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-549"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="5b6f3-550">填滿的不透明度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-550">Opacity of the fill.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-551">Opacity2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-551">Opacity2</span></span></td>
<td><span data-ttu-id="5b6f3-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="5b6f3-553">漸層的次要不透明度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-553">The secondary opacity for gradients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-554">來源</span><span class="sxs-lookup"><span data-stu-id="5b6f3-554">Origin</span></span></td>
<td><span data-ttu-id="5b6f3-555"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-555"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="5b6f3-556">視為影像來源之影像左上角的相對點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-556">Point relative to upper left corner of the image that is treated as the origin of the image.</span></span> <span data-ttu-id="5b6f3-557">預設值是影像的中心。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-557">Default is the center of the image.</span></span> <span data-ttu-id="5b6f3-558">向量是從0.0 到 1.0) 影像寬度和高度 (的分數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-558">The vector is a fraction (from 0.0 to 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-559">位置</span><span class="sxs-lookup"><span data-stu-id="5b6f3-559">Position</span></span></td>
<td><span data-ttu-id="5b6f3-560"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-560"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="5b6f3-561">指向圖形的參考矩形，以放置影像的來源。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-561">Point in the reference rectangle of the shape to position the origin of the image.</span></span> <span data-ttu-id="5b6f3-562">預設值為容器矩形的中心。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-562">Default is the center of the container rectangle.</span></span> <span data-ttu-id="5b6f3-563">向量是影像寬度和高度 (0.0-1.0) 的分數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-563">The vector is a fraction (0.0 - 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-564">大小</span><span class="sxs-lookup"><span data-stu-id="5b6f3-564">Size</span></span></td>
<td><span data-ttu-id="5b6f3-565"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-565"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="5b6f3-566">影像的大小。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-566">The size of the image.</span></span> <span data-ttu-id="5b6f3-567">預設值是影像的圖元大小。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-567">Default is pixel size of the image.</span></span> <span data-ttu-id="5b6f3-568">可以用絕對座標或百分比來指定。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-568">May be specified in absolute coordinates or percentage.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-569">來源</span><span class="sxs-lookup"><span data-stu-id="5b6f3-569">Src</span></span></td>
<td><span data-ttu-id="5b6f3-570"><a href="#data-types-used-in-the-vml-object-model">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-570"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="5b6f3-571">影像的 URL，以載入影像和模式填滿。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-571">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="5b6f3-572">這個屬性必須一律存在，並指向有效的影像資料，圖片才會出現。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-572">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-573">類型</span><span class="sxs-lookup"><span data-stu-id="5b6f3-573">Type</span></span></td>
<td><span data-ttu-id="5b6f3-574">VgFillType.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-574">VgFillType.</span></span> <span data-ttu-id="5b6f3-575">可以是下列其中一個類型：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-575">May be one of the following types:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-576">背景</span><span class="sxs-lookup"><span data-stu-id="5b6f3-576">Background</span></span></li>
<li><span data-ttu-id="5b6f3-577">Frame</span><span class="sxs-lookup"><span data-stu-id="5b6f3-577">Frame</span></span></li>
<li><span data-ttu-id="5b6f3-578">漸層</span><span class="sxs-lookup"><span data-stu-id="5b6f3-578">Gradient</span></span></li>
<li><span data-ttu-id="5b6f3-579">GradientCenter</span><span class="sxs-lookup"><span data-stu-id="5b6f3-579">GradientCenter</span></span></li>
<li><span data-ttu-id="5b6f3-580">GradientRadial</span><span class="sxs-lookup"><span data-stu-id="5b6f3-580">GradientRadial</span></span></li>
<li><span data-ttu-id="5b6f3-581">GradientTitle</span><span class="sxs-lookup"><span data-stu-id="5b6f3-581">GradientTitle</span></span></li>
<li><span data-ttu-id="5b6f3-582">GradientUnscaled</span><span class="sxs-lookup"><span data-stu-id="5b6f3-582">GradientUnscaled</span></span></li>
<li><span data-ttu-id="5b6f3-583">模式</span><span class="sxs-lookup"><span data-stu-id="5b6f3-583">Pattern</span></span></li>
<li><span data-ttu-id="5b6f3-584">實線</span><span class="sxs-lookup"><span data-stu-id="5b6f3-584">Solid</span></span></li>
<li><span data-ttu-id="5b6f3-585">磚</span><span class="sxs-lookup"><span data-stu-id="5b6f3-585">Tile</span></span></li>
</ul>
<span data-ttu-id="5b6f3-586">磚、模式和框架都需要提供影像屬性。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-586">Tile, Pattern, and Frame require the image attributes to be supplied.</span></span> <span data-ttu-id="5b6f3-587">漸層和 GradientRadial 需要提供漸層屬性。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-587">Gradient and GradientRadial require the gradient attributes to be supplied.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a><span data-ttu-id="5b6f3-588">Group 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-588">Group element</span></span>

<span data-ttu-id="5b6f3-589">群組是個別圖形的集合，可作為單位來定位和轉換。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-589">A group is a collection of individual shapes that can be positioned and transformed as a unit.</span></span>



|        |                                                                                              |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f3-590">項目</span><span class="sxs-lookup"><span data-stu-id="5b6f3-590">Item</span></span>   | <span data-ttu-id="5b6f3-591">[IVgShape](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-591">[IVgShape](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-592">圖形陣列中的指定專案。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-592">Specified item in the array of shapes.</span></span> |
| <span data-ttu-id="5b6f3-593">長度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-593">Length</span></span> | <span data-ttu-id="5b6f3-594">[Integer](#data-types-used-in-the-vml-object-model) (整數)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-594">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-595">此群組中的圖形數目。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-595">Number of shapes in this group.</span></span>         |



 

### <a name="imagedata-element"></a><span data-ttu-id="5b6f3-596">Imagedata 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-596">Imagedata element</span></span>

<span data-ttu-id="5b6f3-597">描述要在圖形之上呈現的圖片。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-597">Describes a picture to be rendered on top of a shape.</span></span>



|             |                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f3-598">雙層</span><span class="sxs-lookup"><span data-stu-id="5b6f3-598">BiLevel</span></span>     | <span data-ttu-id="5b6f3-599">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-599">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-600">只以兩種色彩顯示圖片 (通常是黑色和白色) 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-600">Display picture in only two colors (usually black and white).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="5b6f3-601">BlackLevel</span><span class="sxs-lookup"><span data-stu-id="5b6f3-601">BlackLevel</span></span>  | <span data-ttu-id="5b6f3-602">[VgFraction](msdn-online-vml-vgfraction-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-602">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="5b6f3-603">可進行調整以設定層級，讓黑色顯示為 true 黑色，而其他所有色彩則會顯示為黑色以上的陰影。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-603">Allows adjustment to set the level so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="5b6f3-604">Chromakey</span><span class="sxs-lookup"><span data-stu-id="5b6f3-604">Chromakey</span></span>   | <span data-ttu-id="5b6f3-605">[IVgColor](msdn-online-vml-ivgcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-605">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="5b6f3-606">圖片的透明色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-606">Transparent color of picture.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="5b6f3-607">CropBottom</span><span class="sxs-lookup"><span data-stu-id="5b6f3-607">CropBottom</span></span>  | <span data-ttu-id="5b6f3-608">[VgNumber](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-608">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-609">從圖片底部裁剪距離，以圖片大小的百分比表示。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-609">Crop distance from bottom of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="5b6f3-610">CropLeft</span><span class="sxs-lookup"><span data-stu-id="5b6f3-610">CropLeft</span></span>    | <span data-ttu-id="5b6f3-611">[VgNumber](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-611">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-612">從圖片的左邊緣裁剪距離，以圖片大小的比例表示 (從0.0 到 1.0) 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-612">Crop distance from left edge of picture expressed as a fraction of picture size (from 0.0 to 1.0).</span></span> <span data-ttu-id="5b6f3-613">不過，支援「退出裁剪」，因此支援小於0且大於1的值。例如，-5、20會將圖片大小25X 在圖片的一端，以4/5 來裁剪界限。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-613">However, "out-cropping" is supported and thus values of less than 0 and greater than 1 are supported; e.g., -5, 20 would out-crop the bounds 25X the picture size with 4/5 on one side of the picture.</span></span> |
| <span data-ttu-id="5b6f3-614">CropRight</span><span class="sxs-lookup"><span data-stu-id="5b6f3-614">CropRight</span></span>   | <span data-ttu-id="5b6f3-615">[VgNumber](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-616">從圖片右邊裁剪的距離，以圖片大小的百分比表示。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-616">Crop distance from right of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="5b6f3-617">CropTop</span><span class="sxs-lookup"><span data-stu-id="5b6f3-617">CropTop</span></span>     | <span data-ttu-id="5b6f3-618">[VgNumber](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-619">從圖片頂端裁剪的距離，以圖片大小的百分比表示。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-619">Crop distance from top of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="5b6f3-620">EmbossColor</span><span class="sxs-lookup"><span data-stu-id="5b6f3-620">EmbossColor</span></span> | <span data-ttu-id="5b6f3-621">[IVgColor](msdn-online-vml-ivgcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-621">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="5b6f3-622">這會設定為陰影色彩的百分比，以建立浮凸圖片效果。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-622">This is set to a percentage of the shadow color to create an embossed picture effect.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="5b6f3-623">獲得</span><span class="sxs-lookup"><span data-stu-id="5b6f3-623">Gain</span></span>        | <span data-ttu-id="5b6f3-624">[VgPositiveNumber](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-624">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-625">調整所有色彩的濃度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-625">Adjusts the intensity of all colors.</span></span> <span data-ttu-id="5b6f3-626">基本上會設定白色的明暗程度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-626">Essentially sets how bright white will be.</span></span> <span data-ttu-id="5b6f3-627">範圍從0到32767。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-627">Ranges from 0 to 32767.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="5b6f3-628">色差補正</span><span class="sxs-lookup"><span data-stu-id="5b6f3-628">Gamma</span></span>       | <span data-ttu-id="5b6f3-629">[VgFraction](msdn-online-vml-vgfraction-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-629">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="5b6f3-630">Gamma 修正。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-630">Gamma correction.</span></span> <span data-ttu-id="5b6f3-631">增加它可讓影像更對比。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-631">Increasing it gives an image more contrast.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="5b6f3-632">GrayScale</span><span class="sxs-lookup"><span data-stu-id="5b6f3-632">GrayScale</span></span>   | <span data-ttu-id="5b6f3-633">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-633">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-634">顯示灰階色彩的圖片。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-634">Display picture in grayscale colors.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5b6f3-635">來源</span><span class="sxs-lookup"><span data-stu-id="5b6f3-635">Src</span></span>         | <span data-ttu-id="5b6f3-636">[字串](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-636">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-637">影像的 URL，以載入影像和模式填滿。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-637">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="5b6f3-638">這個屬性必須一律存在，並指向有效的影像資料，圖片才會出現。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-638">This attribute must always be present and point to valid image data for a picture to appear.</span></span>                                                                                                                                                           |



 

### <a name="path-element"></a><span data-ttu-id="5b6f3-639">Path 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-639">Path element</span></span>

<span data-ttu-id="5b6f3-640">使用包含一組豐富的「畫筆移動」命令的字串，定義組成圖形的路徑。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-640">Defines the path that makes up the shape, using a string that contains a rich set of "pen movement" commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-641">豪華 轎車</span><span class="sxs-lookup"><span data-stu-id="5b6f3-641">Limo</span></span></td>
<td><span data-ttu-id="5b6f3-642"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-642"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span></span> <span data-ttu-id="5b6f3-643">定義圖案伸展的點;例如，針對 giraffe 圖形，limo 點會在頸部上，因此當調整形狀大小時，頸部將會延展，而圖形的其餘部分將會維持其尺寸。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-643">Defines the point where the shape is stretched; e.g., for a giraffe shape, the limo point would be on the neck so when the shape is resized, the neck will stretch and the rest of the shape will maintain its dimensions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-644">TextBoxRect</span><span class="sxs-lookup"><span data-stu-id="5b6f3-644">TextBoxRect</span></span></td>
<td><span data-ttu-id="5b6f3-645"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-645"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span></span> <span data-ttu-id="5b6f3-646">陣列，包含定義文字應該移至何處的矩形。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-646">Array containing the rectangles that define where text should go.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-647">V</span><span class="sxs-lookup"><span data-stu-id="5b6f3-647">V</span></span></td>
<td><span data-ttu-id="5b6f3-648"><a href="#data-types-used-in-the-vml-object-model">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-648"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="5b6f3-649">符合路徑標記上的 v 屬性。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-649">Matches the v attribute on the Path tag.</span></span> <span data-ttu-id="5b6f3-650">請注意，路徑可能對應至 Path 屬性或元素。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-650">Note that path may correspond to Path attribute or element.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-651">值</span><span class="sxs-lookup"><span data-stu-id="5b6f3-651">Value</span></span></td>
<td><span data-ttu-id="5b6f3-652"><a href="#data-types-used-in-the-vml-object-model">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-652"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="5b6f3-653">定義路徑的命令文字表示。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-653">A text representation of the commands that define the path.</span></span> <span data-ttu-id="5b6f3-654">X 或 y 座標值可以是表單中公式的參考 &quot; @# &quot; ，其中 # 是公式的序數，例如， &quot; @2 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-654">X or y-coordinate values can be a reference to a formula in the form &quot;@#&quot; where # is the formula's ordinal number, e.g., &quot;@2&quot;.</span></span> <span data-ttu-id="5b6f3-655">這個屬性字串是由一組豐富的命令所組成，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-655">This attribute string is made up of a rich set of commands including the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5b6f3-656">命令</span><span class="sxs-lookup"><span data-stu-id="5b6f3-656">Command</span></span></th>
<th><span data-ttu-id="5b6f3-657">描述</span><span class="sxs-lookup"><span data-stu-id="5b6f3-657">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-658">ae (angleellipseto) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-658">ae (angleellipseto)</span></span></td>
<td><span data-ttu-id="5b6f3-659"><strong>中央</strong> (x、y) <strong>大小</strong> (w、h) <strong>開始角度</strong>、 <strong>終點</strong></span><span class="sxs-lookup"><span data-stu-id="5b6f3-659"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span></span><br/> <span data-ttu-id="5b6f3-660">繪製橢圓形的線段。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-660">Draw a segment of an ellipse.</span></span> <span data-ttu-id="5b6f3-661">從目前的點將直線繪製到區段的起點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-661">A straight line is drawn from the current point to the start point of the segment.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-662">al (angleelipse) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-662">al (angleelipse)</span></span></td>
<td><span data-ttu-id="5b6f3-663">與 ae 相同，不同之處在于區段的起點有隱含的 m。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-663">Same as ae except that there is an implied m to the starting point of the segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-664">ar (arc) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-664">ar (arc)</span></span></td>
<td><span data-ttu-id="5b6f3-665">與相同。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-665">Same as at.</span></span> <span data-ttu-id="5b6f3-666">不過，新的子路徑會由隱含的 m 啟動至弧線的起點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-666">However, a new subpath is started by an implied m to the start point of the arc.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-667">在 (arcto) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-667">at (arcto)</span></span></td>
<td><span data-ttu-id="5b6f3-668"><strong>左</strong>、 <strong>上</strong>、 <strong>右</strong>、 <strong>下</strong>、 <strong>開始</strong> (x、y) <strong>end</strong> (x，y) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-668"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="5b6f3-669">前四個值會定義橢圓形的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-669">The first four values define the bounding box of an ellipse.</span></span> <span data-ttu-id="5b6f3-670">最後四個定義兩個放射狀向量。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-670">The last four define two radial vectors.</span></span> <span data-ttu-id="5b6f3-671">繪製的橢圓形區段會從開始半徑向量所定義的角度開始，並以結束向量所定義的角度結束。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-671">A segment of the ellipse is drawn that starts at the angle defined by the start radius vector and ends at the angle defined by the end vector.</span></span> <span data-ttu-id="5b6f3-672">從目前的點到弧形開頭繪製直線。弧線一律會以逆時針方向繪製。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-672">A straight line is drawn from the current point to the start of the arc. The arc is always drawn in a counterclockwise direction.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-673">c (curveto) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-673">c (curveto)</span></span></td>
<td><span data-ttu-id="5b6f3-674"><strong>control1</strong> (x，y) <strong>control2</strong> (x，y) <strong>至</strong> (x，y) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-674"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y)</span></span> <br/> <span data-ttu-id="5b6f3-675">從目前的點繪製三次方貝茲曲線到最後兩個參數所指定的座標，也就是前四個參數所指定的控制點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-675">Draw a cubic bezier curve from the current point to the coordinate given by the final two parameters, the control points given by the first four parameters.</span></span> <span data-ttu-id="5b6f3-676">目前的點會成為貝塞爾的端點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-676">The current point becomes the endpoint of the bezier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-677">e (結束) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-677">e (end)</span></span></td>
<td><span data-ttu-id="5b6f3-678">結束目前的子路徑集。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-678">End the current set of subpaths.</span></span> <span data-ttu-id="5b6f3-679">會使用 eofill 填滿一組指定的子路徑，並以 end) 分隔 (。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-679">A given set of subpaths (as delimited by end) are filled using eofill.</span></span> <span data-ttu-id="5b6f3-680">後續的子路徑集合會獨立填入，並在現有的子路徑上重迭。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-680">Subsequent sets of subpaths are filled independently and superimposed on existing ones.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-681">l (lineto) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-681">l (lineto)</span></span></td>
<td><span data-ttu-id="5b6f3-682">x、y</span><span class="sxs-lookup"><span data-stu-id="5b6f3-682">x,y</span></span><br/> <span data-ttu-id="5b6f3-683">從目前的點將直線繪製到指定的 x，y 座標，以成為新的目前點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-683">Draw a line from the current point to the given x,y-coordinate, which becomes the new current point.</span></span> <span data-ttu-id="5b6f3-684">您可以指定其他座標配對來形成聚合線條，例如， &quot; l 10、13、45、27、89、-12 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-684">Additional coordinate pairs may be specified to form a polyline, e.g., &quot;l 10,13,45,27,89,-12&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-685">m (moveto) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-685">m (moveto)</span></span></td>
<td><span data-ttu-id="5b6f3-686">x、y</span><span class="sxs-lookup"><span data-stu-id="5b6f3-686">x,y</span></span><br/> <span data-ttu-id="5b6f3-687">在指定的 x，y 座標開始新的子路徑。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-687">Start a new subpath at the given x,y-coordinate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-688">nofill) 的 nf-e (</span><span class="sxs-lookup"><span data-stu-id="5b6f3-688">nf (nofill)</span></span></td>
<td><span data-ttu-id="5b6f3-689">將不會填入以 end) 分隔 (目前的子路徑集合。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-689">The current set of subpaths (delimited by end) will not be filled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-690">ns (nostroke) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-690">ns (nostroke)</span></span></td>
<td><span data-ttu-id="5b6f3-691">將不會對目前的子路徑組合 (以 end) 分隔。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-691">The current set of subpaths (delimited by end) will not be stroked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-692">qb (quadraticbezier) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-692">qb (quadraticbezier)</span></span></td>
<td><span data-ttu-id="5b6f3-693"> (<strong>controlpoint</strong> (x、y) )\ *、<strong>end</strong> (x、y) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-693">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="5b6f3-694">藉由控制點和端點，定義一或多個二次方貝茲曲線。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-694">Defines one or more quadratic bezier curves by means of control points and an endpoint.</span></span> <span data-ttu-id="5b6f3-695">中間的 (曲線) 點是透過類似 TrueType 字型的連續控制點來取得。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-695">Intermediate (on-curve) points are obtained by interpolation between successive control points similar to TrueType fonts.</span></span> <span data-ttu-id="5b6f3-696">子路徑不需要是開始的，在此情況下，會關閉子路徑，而最後一個點則會定義起始點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-696">The subpath need not be a start, in which case the subpath is closed and the last point defines the start point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-697">qx (ellipticalquadrantx) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-697">qx (ellipticalquadrantx)</span></span></td>
<td><span data-ttu-id="5b6f3-698"><strong>end</strong> (x，y) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-698"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="5b6f3-699">從目前的點到指定端點繪製的四分之一橢圓形。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-699">A quarter ellipse is drawn from the current point to the given endpoint.</span></span> <span data-ttu-id="5b6f3-700">橢圓區段一開始會與 X 軸平行的直線相切;亦即，區段開始水準。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-700">The elliptical segment is initially tangential to a line parallel to the x-axis; i.e., the segment starts out horizontal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-701">qy (ellipticalquadranty) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-701">qy (ellipticalquadranty)</span></span></td>
<td><span data-ttu-id="5b6f3-702"><strong>end</strong> (x，y) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-702"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="5b6f3-703">與 qx 相同，不同之處在于橢圓區段一開始會與 y 軸平行的直線相切;亦即，區段開始垂直。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-703">Same as qx except that the elliptical segment is initially tangential to a line parallel to the y-axis; i.e., the segment starts out vertical.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-704">r (rlineto) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-704">r (rlineto)</span></span></td>
<td><span data-ttu-id="5b6f3-705">x、y</span><span class="sxs-lookup"><span data-stu-id="5b6f3-705">x,y</span></span> <br/> <span data-ttu-id="5b6f3-706">從目前的點繪製一條直線到相對座標 (cpx + x，cpy + y) 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-706">Draw a line from the current point to the relative coordinate (cpx + x, cpy + y).</span></span> <span data-ttu-id="5b6f3-707">如果指定了其他座標組，每個新點都會相對於最後一個點來計算。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-707">If additional coordinate pairs are given, each new point is computed relative to the last one.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-708">t (rmoveto) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-708">t (rmoveto)</span></span></td>
<td><span data-ttu-id="5b6f3-709">x、y</span><span class="sxs-lookup"><span data-stu-id="5b6f3-709">x,y</span></span><br/> <span data-ttu-id="5b6f3-710">在相對座標開始新的子路徑 ( cpx + x，cpy + y) 其中 cpx，cpy 是目前的位置。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-710">Start a new subpath at the relative coordinates ( cpx + x, cpy + y) where cpx, cpy is the current position.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-711">v (curveto) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-711">v (curveto)</span></span></td>
<td><span data-ttu-id="5b6f3-712"><strong>control1</strong> (x，y) <strong>control2</strong> (x，y) <strong>至</strong> (x，y) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-712"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span></span> <br/> <span data-ttu-id="5b6f3-713">使用相對於目前點之指定座標的三次方貝茲曲線。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-713">Cubic bezier curve using the given coordinates relative to the current point.</span></span> <span data-ttu-id="5b6f3-714">所有點都是相對於相同的起點來計算。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-714">All the points are computed relative to the same starting point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-715">wa (clockwisearcto) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-715">wa (clockwisearcto)</span></span></td>
<td><span data-ttu-id="5b6f3-716">與相同，但弧線以順時針方向繪製。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-716">Same as at but the arc is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-717">wr (clockwisearc) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-717">wr (clockwisearc)</span></span></td>
<td><span data-ttu-id="5b6f3-718">與 ar 相同，但以順時針方向繪製。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-718">Same as ar but is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-719">x (關閉) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-719">x (close)</span></span></td>
<td><span data-ttu-id="5b6f3-720">從目前點到原始的 moveto 點繪製一條直線，以關閉目前的子路徑。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-720">Close the current subpath by drawing a straight line from the current point to the original moveto point.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a><span data-ttu-id="5b6f3-721">Shadow 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-721">Shadow element</span></span>

<span data-ttu-id="5b6f3-722">描述圖形上的陰影效果。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-722">Describes a shadow effect on a shape.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-723">Color</span><span class="sxs-lookup"><span data-stu-id="5b6f3-723">Color</span></span></td>
<td><span data-ttu-id="5b6f3-724"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-724"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="5b6f3-725">主要陰影的色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-725">Color of the primary shadow.</span></span> <span data-ttu-id="5b6f3-726">預設值為 RGB (128128128) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-726">Default is RGB(128,128,128)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-727">Color2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-727">Color2</span></span></td>
<td><span data-ttu-id="5b6f3-728"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-728"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="5b6f3-729">第二個陰影的色彩，或反白顯示于浮凸或陰文的陰影。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-729">Color of the second shadow, or highlight in an embossed or engraved shadow.</span></span> <span data-ttu-id="5b6f3-730">預設值為 RGB (203203203) 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-730">Default is RGB(203,203,203).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-731">Matrix</span><span class="sxs-lookup"><span data-stu-id="5b6f3-731">Matrix</span></span></td>
<td><span data-ttu-id="5b6f3-732"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-732"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span></span> <span data-ttu-id="5b6f3-733">&quot;Sxx、sxy、syx、syy、px、.py &quot; [s = scale、p = 透視圖] 格式的透視圖轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-733">A perspective transform matrix in the form, &quot;sxx,sxy,syx,syy,px,py&quot; [s=scale, p=perspective].</span></span> <span data-ttu-id="5b6f3-734">專案指定陰影應該如何隨著圖形而調整，而 p 專案則指定陰影應該如何與圖形相對應的扭曲。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-734">The s items specify how the shadow should scale with respect to the shape, and the p items specify how the shadow should skew with respect to the shape.</span></span> <span data-ttu-id="5b6f3-735">例如，下列矩陣會以2的因數來調整圖形的大小，並以4的因數將其傾斜：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-735">For example, the following matrix resizes the shape by a factor of 2 and skews it by a factor of 4 in all directions:</span></span> <br/> <span data-ttu-id="5b6f3-736">&quot;2、2、2、2、4、4&quot;</span><span class="sxs-lookup"><span data-stu-id="5b6f3-736">&quot;2,2,2,2,4,4&quot;</span></span><br/> <span data-ttu-id="5b6f3-737">只有當陰影的類型設定為 [透視圖] 時，才會使用這個矩陣。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-737">This matrix is only used if the type of the shadow is set to perspective.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-738">遮蔽</span><span class="sxs-lookup"><span data-stu-id="5b6f3-738">Obscured</span></span></td>
<td><span data-ttu-id="5b6f3-739"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-739"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="5b6f3-740">如果圖形沒有填滿，就可以看到陰影。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-740">The shadow can be seen through if there is no fill on the shape.</span></span> <span data-ttu-id="5b6f3-741">預設值是 False。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-741">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-742">Offset</span><span class="sxs-lookup"><span data-stu-id="5b6f3-742">Offset</span></span></td>
<td><span data-ttu-id="5b6f3-743"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-743"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span></span> <span data-ttu-id="5b6f3-744">X 的數量，y 位移自圖形的位置。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-744">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="5b6f3-745">預設值為 &quot; 2pt、2pt &quot; 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-745">Default is &quot;2pt,2pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-746">Offset2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-746">Offset2</span></span></td>
<td><span data-ttu-id="5b6f3-747"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-747"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="5b6f3-748">X 的數量，y 第二個從圖形的位置位移。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-748">Amount of x,y second offset from the shape?s location.</span></span> <span data-ttu-id="5b6f3-749">值可以是絕對測量值，或是 shape (-0.5 到 + 0.5) 的小數值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-749">Values are either an absolute measurement, or a fractional value of shape (-0.5 to +0.5).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-750">開啟</span><span class="sxs-lookup"><span data-stu-id="5b6f3-750">On</span></span></td>
<td><span data-ttu-id="5b6f3-751"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-751"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="5b6f3-752">開啟和關閉陰影的顯示。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-752">Turns the display of the shadow on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-753">不透明度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-753">Opacity</span></span></td>
<td><span data-ttu-id="5b6f3-754"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-754"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="5b6f3-755">陰影效果的不透明度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-755">Opacity of the shadow effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-756">來源</span><span class="sxs-lookup"><span data-stu-id="5b6f3-756">Origin</span></span></td>
<td><span data-ttu-id="5b6f3-757"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> 從-0.5 到 + 0.5 之圖形的一對小數值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-757"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> A pair of fractional values of shape from -0.5 to +0.5.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-758">類型</span><span class="sxs-lookup"><span data-stu-id="5b6f3-758">Type</span></span></td>
<td><span data-ttu-id="5b6f3-759"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-759"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span></span> <span data-ttu-id="5b6f3-760">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-760">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-761">單一 (預設) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-761">Single (default)</span></span></li>
<li><span data-ttu-id="5b6f3-762">Double</span><span class="sxs-lookup"><span data-stu-id="5b6f3-762">Double</span></span></li>
<li><span data-ttu-id="5b6f3-763">檢視方塊</span><span class="sxs-lookup"><span data-stu-id="5b6f3-763">Perspective</span></span></li>
<li><span data-ttu-id="5b6f3-764">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="5b6f3-764">ShapeRelative</span></span></li>
<li><span data-ttu-id="5b6f3-765">DrawingRelative</span><span class="sxs-lookup"><span data-stu-id="5b6f3-765">DrawingRelative</span></span></li>
<li><span data-ttu-id="5b6f3-766">Emboss</span><span class="sxs-lookup"><span data-stu-id="5b6f3-766">Emboss</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a><span data-ttu-id="5b6f3-767">扭曲元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-767">Skew element</span></span>

<span data-ttu-id="5b6f3-768">描述圖形上的觀點扭曲效果。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-768">Describes a perspective skew effect on a shape.</span></span> <span data-ttu-id="5b6f3-769">扭曲會套用至向量圖形資料，而不會套用至影像資料。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-769">The skew is applied to vector graphic data, not image data.</span></span>



|        |                                                                                                                                                                                                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f3-770">Matrix</span><span class="sxs-lookup"><span data-stu-id="5b6f3-770">Matrix</span></span> | <span data-ttu-id="5b6f3-771">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-771">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-772">以 "sxx，sxy，syx，syy，px，.py" \[ s = scale，p = 透視圖形式的觀點轉換矩陣 \] 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-772">A perspective transform matrix in the form, "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective\].</span></span> <span data-ttu-id="5b6f3-773">如果位移的單位為絕對單位，則為 px，.py 則為 emu ^-1 個單位;否則是圖形大小的反向分數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-773">If offset is in absolute units then px,py are in emu ^ -1 units; otherwise they are an inverse fraction of shape size.</span></span> |
| <span data-ttu-id="5b6f3-774">Offset</span><span class="sxs-lookup"><span data-stu-id="5b6f3-774">Offset</span></span> | <span data-ttu-id="5b6f3-775">[IvgSkewOffset](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-775">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-776">X 的數量，y 位移自圖形的位置。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-776">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="5b6f3-777">預設值為 "2pt，2pt"。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-777">Default is "2pt,2pt".</span></span>                                                                                                                                                   |
| <span data-ttu-id="5b6f3-778">開啟</span><span class="sxs-lookup"><span data-stu-id="5b6f3-778">On</span></span>     | <span data-ttu-id="5b6f3-779">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-779">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-780">開啟或關閉扭曲的顯示。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-780">Turns the display of the skew on or off.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="5b6f3-781">來源</span><span class="sxs-lookup"><span data-stu-id="5b6f3-781">Origin</span></span> | <span data-ttu-id="5b6f3-782">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-782">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="5b6f3-783">從-0.5 到 + 0.5 之圖形的一對小數值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-783">A pair of fractional values of shape from -0.5 to +0.5.</span></span>                                                                                                                                                                     |



 

### <a name="stroke-element"></a><span data-ttu-id="5b6f3-784">Stroke 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-784">Stroke element</span></span>

<span data-ttu-id="5b6f3-785">描述如何在需要純色的實線之外繪製路徑。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-785">Describes how to draw the path if something beyond a solid line with a solid color is desired.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-786">Color</span><span class="sxs-lookup"><span data-stu-id="5b6f3-786">Color</span></span></td>
<td><span data-ttu-id="5b6f3-787"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-787"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="5b6f3-788">線條的色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-788">The color of the line.</span></span> <span data-ttu-id="5b6f3-789">與 Shape 中的 StrokeColor 屬性相同，但會覆寫它。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-789">Same as StrokeColor attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-790">Color2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-790">Color2</span></span></td>
<td><span data-ttu-id="5b6f3-791"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-791"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="5b6f3-792">次要色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-792">Secondary color.</span></span> <span data-ttu-id="5b6f3-793">當 FillType 為模式時使用。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-793">Used when FillType is Pattern.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-794">DashStyle</span><span class="sxs-lookup"><span data-stu-id="5b6f3-794">DashStyle</span></span></td>
<td><span data-ttu-id="5b6f3-795"><strong>VgLineDashStyle</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-795"><strong>VgLineDashStyle</strong>.</span></span> <span data-ttu-id="5b6f3-796">虛線樣式格式。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-796">Dash style format.</span></span> <span data-ttu-id="5b6f3-797">可能是特定的值，或是具有使用者定義虛線模式的數位序列。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-797">May be a specific value or a sequence of numbers with a user-defined dash pattern.</span></span> <span data-ttu-id="5b6f3-798">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-798">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-799">Solid (預設值)</span><span class="sxs-lookup"><span data-stu-id="5b6f3-799">Solid (default)</span></span></li>
<li><span data-ttu-id="5b6f3-800">ShortDash</span><span class="sxs-lookup"><span data-stu-id="5b6f3-800">ShortDash</span></span></li>
<li><span data-ttu-id="5b6f3-801">ShortDot</span><span class="sxs-lookup"><span data-stu-id="5b6f3-801">ShortDot</span></span></li>
<li><span data-ttu-id="5b6f3-802">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="5b6f3-802">ShortDashDot</span></span></li>
<li><span data-ttu-id="5b6f3-803">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="5b6f3-803">ShortDashDotDot</span></span></li>
<li><span data-ttu-id="5b6f3-804">點</span><span class="sxs-lookup"><span data-stu-id="5b6f3-804">Dot</span></span></li>
<li><span data-ttu-id="5b6f3-805">虛線</span><span class="sxs-lookup"><span data-stu-id="5b6f3-805">Dash</span></span></li>
<li><span data-ttu-id="5b6f3-806">DashDot</span><span class="sxs-lookup"><span data-stu-id="5b6f3-806">DashDot</span></span></li>
<li><span data-ttu-id="5b6f3-807">LongDash</span><span class="sxs-lookup"><span data-stu-id="5b6f3-807">LongDash</span></span></li>
<li><span data-ttu-id="5b6f3-808">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="5b6f3-808">LongDashDot</span></span></li>
<li><span data-ttu-id="5b6f3-809">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="5b6f3-809">LongDashDotDot</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-810">EndArrow</span><span class="sxs-lookup"><span data-stu-id="5b6f3-810">EndArrow</span></span></td>
<td><span data-ttu-id="5b6f3-811"><strong>VgArrowheadStyle</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-811"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="5b6f3-812">行尾的箭頭。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-812">Arrowhead for the end of the line.</span></span> <span data-ttu-id="5b6f3-813">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-813">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-814">[無] (預設值)</span><span class="sxs-lookup"><span data-stu-id="5b6f3-814">None (default)</span></span></li>
<li><span data-ttu-id="5b6f3-815">封鎖</span><span class="sxs-lookup"><span data-stu-id="5b6f3-815">Block</span></span></li>
<li><span data-ttu-id="5b6f3-816">傳統</span><span class="sxs-lookup"><span data-stu-id="5b6f3-816">Classic</span></span></li>
<li><span data-ttu-id="5b6f3-817">菱形</span><span class="sxs-lookup"><span data-stu-id="5b6f3-817">Diamond</span></span></li>
<li><span data-ttu-id="5b6f3-818">橢圓形</span><span class="sxs-lookup"><span data-stu-id="5b6f3-818">Oval</span></span></li>
<li><span data-ttu-id="5b6f3-819">開啟</span><span class="sxs-lookup"><span data-stu-id="5b6f3-819">Open</span></span></li>
<li><span data-ttu-id="5b6f3-820">&gt; 形箭號</span><span class="sxs-lookup"><span data-stu-id="5b6f3-820">Chevron</span></span></li>
<li><span data-ttu-id="5b6f3-821">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="5b6f3-821">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-822">EndArrowLength</span><span class="sxs-lookup"><span data-stu-id="5b6f3-822">EndArrowLength</span></span></td>
<td><span data-ttu-id="5b6f3-823"><strong>VgArrowHeadLength</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-823"><strong>VgArrowHeadLength</strong>.</span></span> <span data-ttu-id="5b6f3-824">線條結尾的箭頭長度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-824">Arrowhead length for the end of the line.</span></span> <span data-ttu-id="5b6f3-825">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-825">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-826">Short</span><span class="sxs-lookup"><span data-stu-id="5b6f3-826">Short</span></span></li>
<li><span data-ttu-id="5b6f3-827">中 (預設)</span><span class="sxs-lookup"><span data-stu-id="5b6f3-827">Medium (default)</span></span></li>
<li><span data-ttu-id="5b6f3-828">long</span><span class="sxs-lookup"><span data-stu-id="5b6f3-828">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-829">EndArrowWidth</span><span class="sxs-lookup"><span data-stu-id="5b6f3-829">EndArrowWidth</span></span></td>
<td><span data-ttu-id="5b6f3-830"><strong>VgArrowheadWidth</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-830"><strong>VgArrowheadWidth</strong>.</span></span> <span data-ttu-id="5b6f3-831">線條結尾的箭頭寬度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-831">Arrowhead width for the end of the line.</span></span> <span data-ttu-id="5b6f3-832">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-832">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-833">狹窄</span><span class="sxs-lookup"><span data-stu-id="5b6f3-833">Narrow</span></span></li>
<li><span data-ttu-id="5b6f3-834">中 (預設)</span><span class="sxs-lookup"><span data-stu-id="5b6f3-834">Medium (default)</span></span></li>
<li><span data-ttu-id="5b6f3-835">寬</span><span class="sxs-lookup"><span data-stu-id="5b6f3-835">Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-836">EndCap</span><span class="sxs-lookup"><span data-stu-id="5b6f3-836">EndCap</span></span></td>
<td><span data-ttu-id="5b6f3-837"><strong>VgLineEndCapStyle</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-837"><strong>VgLineEndCapStyle</strong>.</span></span> <span data-ttu-id="5b6f3-838">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-838">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-839">一般</span><span class="sxs-lookup"><span data-stu-id="5b6f3-839">Flat</span></span></li>
<li><span data-ttu-id="5b6f3-840">Square</span><span class="sxs-lookup"><span data-stu-id="5b6f3-840">Square</span></span></li>
<li><span data-ttu-id="5b6f3-841">Round</span><span class="sxs-lookup"><span data-stu-id="5b6f3-841">Round</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-842">FillType</span><span class="sxs-lookup"><span data-stu-id="5b6f3-842">FillType</span></span></td>
<td><span data-ttu-id="5b6f3-843"><strong>VgLineFillType</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-843"><strong>VgLineFillType</strong>.</span></span> <span data-ttu-id="5b6f3-844">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-844">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-845">Solid (預設值)</span><span class="sxs-lookup"><span data-stu-id="5b6f3-845">Solid (default)</span></span></li>
<li><span data-ttu-id="5b6f3-846">磚</span><span class="sxs-lookup"><span data-stu-id="5b6f3-846">Tile</span></span></li>
<li><span data-ttu-id="5b6f3-847">模式</span><span class="sxs-lookup"><span data-stu-id="5b6f3-847">Pattern</span></span></li>
<li><span data-ttu-id="5b6f3-848">Frame</span><span class="sxs-lookup"><span data-stu-id="5b6f3-848">Frame</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-849">ImageAlignShape</span><span class="sxs-lookup"><span data-stu-id="5b6f3-849">ImageAlignShape</span></span></td>
<td><span data-ttu-id="5b6f3-850"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-850"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="5b6f3-851">將影像與圖形對齊。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-851">Align the image with the shape.</span></span> <span data-ttu-id="5b6f3-852">如果為 False，則會將影像與視窗對齊。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-852">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-853">ImageAspect</span><span class="sxs-lookup"><span data-stu-id="5b6f3-853">ImageAspect</span></span></td>
<td><span data-ttu-id="5b6f3-854"><strong>VgAspectType</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-854"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="5b6f3-855">ImageSize 屬性將會調整，以保留影像的外觀。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-855">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="5b6f3-856">數值包括：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-856">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5b6f3-857">值</span><span class="sxs-lookup"><span data-stu-id="5b6f3-857">Value</span></span></th>
<th><span data-ttu-id="5b6f3-858">描述</span><span class="sxs-lookup"><span data-stu-id="5b6f3-858">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-859">忽略</span><span class="sxs-lookup"><span data-stu-id="5b6f3-859">Ignore</span></span></td>
<td><span data-ttu-id="5b6f3-860">略過外觀問題。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-860">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-861">至少</span><span class="sxs-lookup"><span data-stu-id="5b6f3-861">AtLeast</span></span></td>
<td><span data-ttu-id="5b6f3-862">映射大小至少與影像大小一樣大。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-862">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-863">有</span><span class="sxs-lookup"><span data-stu-id="5b6f3-863">AtMost</span></span></td>
<td><span data-ttu-id="5b6f3-864">影像的大小不會大於影像大小。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-864">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-865">ImageSize</span><span class="sxs-lookup"><span data-stu-id="5b6f3-865">ImageSize</span></span></td>
<td><span data-ttu-id="5b6f3-866"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-866"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="5b6f3-867">用來形成筆刷的影像大小。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-867">Size of the image to form the brush with.</span></span> <span data-ttu-id="5b6f3-868">預設值是影像的大小。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-868">Default is the size of the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-869">JoinStyle</span><span class="sxs-lookup"><span data-stu-id="5b6f3-869">JoinStyle</span></span></td>
<td><span data-ttu-id="5b6f3-870"><strong>VgLineJoinStyle</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-870"><strong>VgLineJoinStyle</strong>.</span></span> <span data-ttu-id="5b6f3-871">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-871">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-872">舍入 (圓角接合) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-872">Round (rounded joint)</span></span></li>
<li><span data-ttu-id="5b6f3-873">斜面 (斜角接點) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-873">Bevel (beveled joint)</span></span></li>
<li><span data-ttu-id="5b6f3-874">斜接 (斜接接點) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-874">Miter (miter joint)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-875">線條樣式</span><span class="sxs-lookup"><span data-stu-id="5b6f3-875">LineStyle</span></span></td>
<td><span data-ttu-id="5b6f3-876"><strong>VgLineStyle</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-876"><strong>VgLineStyle</strong>.</span></span> <span data-ttu-id="5b6f3-877">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-877">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-878">Single</span><span class="sxs-lookup"><span data-stu-id="5b6f3-878">Single</span></span></li>
<li><span data-ttu-id="5b6f3-879">ThinThin (1:1:1) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-879">ThinThin (1:1:1)</span></span></li>
<li><span data-ttu-id="5b6f3-880">ThinThick (1:1:2) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-880">ThinThick (1:1:2)</span></span></li>
<li><span data-ttu-id="5b6f3-881">ThickThin (2:1:1) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-881">ThickThin (2:1:1)</span></span></li>
<li><span data-ttu-id="5b6f3-882">ThickBetweenThin (1:1:2:1:1) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-882">ThickBetweenThin (1:1:2:1:1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-883">MiterLimit</span><span class="sxs-lookup"><span data-stu-id="5b6f3-883">MiterLimit</span></span></td>
<td><span data-ttu-id="5b6f3-884"><a href="msdn-online-vml-vglength.md">長度</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-884"><a href="msdn-online-vml-vglength.md">Length</a>.</span></span> <span data-ttu-id="5b6f3-885">聯合的內部點和外部點之間的最大距離。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-885">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="5b6f3-886">此數位是線條粗細的倍數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-886">This number is a multiple of the thickness of the line.</span></span> <span data-ttu-id="5b6f3-887">範圍從0到32767。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-887">Ranges from 0 to 32,767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-888">開啟</span><span class="sxs-lookup"><span data-stu-id="5b6f3-888">On</span></span></td>
<td><span data-ttu-id="5b6f3-889"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-889"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="5b6f3-890">開啟和關閉行的顯示。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-890">Turns the display of the line on and off.</span></span> <span data-ttu-id="5b6f3-891">與 Shape 中的 Stroke 屬性相同，但會覆寫它。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-891">Same as Stroke attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-892">不透明度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-892">Opacity</span></span></td>
<td><span data-ttu-id="5b6f3-893"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-893"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="5b6f3-894">筆劃的不透明度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-894">Opacity of the stroke.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-895">來源</span><span class="sxs-lookup"><span data-stu-id="5b6f3-895">Src</span></span></td>
<td><span data-ttu-id="5b6f3-896">字串。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-896">String.</span></span> <span data-ttu-id="5b6f3-897">影像的 URL，以載入影像和模式填滿。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-897">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="5b6f3-898">這個屬性必須一律存在，並指向有效的影像資料，圖片才會出現。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-898">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-899">StartArrow</span><span class="sxs-lookup"><span data-stu-id="5b6f3-899">StartArrow</span></span></td>
<td><span data-ttu-id="5b6f3-900"><strong>VgArrowheadStyle</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-900"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="5b6f3-901">直線開頭的箭頭。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-901">Arrowhead for the start of the line.</span></span> <span data-ttu-id="5b6f3-902">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-902">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-903">[無] (預設值)</span><span class="sxs-lookup"><span data-stu-id="5b6f3-903">None (default)</span></span></li>
<li><span data-ttu-id="5b6f3-904">封鎖</span><span class="sxs-lookup"><span data-stu-id="5b6f3-904">Block</span></span></li>
<li><span data-ttu-id="5b6f3-905">傳統</span><span class="sxs-lookup"><span data-stu-id="5b6f3-905">Classic</span></span></li>
<li><span data-ttu-id="5b6f3-906">菱形</span><span class="sxs-lookup"><span data-stu-id="5b6f3-906">Diamond</span></span></li>
<li><span data-ttu-id="5b6f3-907">橢圓形</span><span class="sxs-lookup"><span data-stu-id="5b6f3-907">Oval</span></span></li>
<li><span data-ttu-id="5b6f3-908">開啟</span><span class="sxs-lookup"><span data-stu-id="5b6f3-908">Open</span></span></li>
<li><span data-ttu-id="5b6f3-909">&gt; 形箭號</span><span class="sxs-lookup"><span data-stu-id="5b6f3-909">Chevron</span></span></li>
<li><span data-ttu-id="5b6f3-910">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="5b6f3-910">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-911">StartArrowLength</span><span class="sxs-lookup"><span data-stu-id="5b6f3-911">StartArrowLength</span></span></td>
<td><span data-ttu-id="5b6f3-912">VgArrowHeadLength.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-912">VgArrowHeadLength.</span></span> <span data-ttu-id="5b6f3-913">直線開頭的箭頭長度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-913">Arrowhead length for the start of the line.</span></span> <span data-ttu-id="5b6f3-914">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-914">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-915">Short</span><span class="sxs-lookup"><span data-stu-id="5b6f3-915">Short</span></span></li>
<li><span data-ttu-id="5b6f3-916">中 (預設)</span><span class="sxs-lookup"><span data-stu-id="5b6f3-916">Medium (default)</span></span></li>
<li><span data-ttu-id="5b6f3-917">long</span><span class="sxs-lookup"><span data-stu-id="5b6f3-917">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-918">StartArrowWidth</span><span class="sxs-lookup"><span data-stu-id="5b6f3-918">StartArrowWidth</span></span></td>
<td><span data-ttu-id="5b6f3-919">VgArrowheadWidth.</span><span class="sxs-lookup"><span data-stu-id="5b6f3-919">VgArrowheadWidth.</span></span> <span data-ttu-id="5b6f3-920">線條開頭的箭頭寬度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-920">Arrowhead width for the start of the line.</span></span> <span data-ttu-id="5b6f3-921">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-921">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-922">窄中型 (預設) 寬</span><span class="sxs-lookup"><span data-stu-id="5b6f3-922">Narrow Medium (default) Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-923">Weight</span><span class="sxs-lookup"><span data-stu-id="5b6f3-923">Weight</span></span></td>
<td><span data-ttu-id="5b6f3-924"><a href="msdn-online-vml-vglength.md">VgLength</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-924"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="5b6f3-925">線條的寬度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-925">Width of line.</span></span> <span data-ttu-id="5b6f3-926">範圍從0到1584。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-926">Ranges from 0 to 1584.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="5b6f3-927">DashStyle 屬性可讓使用者指定自訂定義的虛線模式。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-927">The DashStyle attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="5b6f3-928">這是使用一連串的數位來完成。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-928">This is done using a series of numbers.</span></span> <span data-ttu-id="5b6f3-929">虛線樣式是以虛線的長度來定義， (筆觸的繪製部分) 和虛線之間的空間長度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-929">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="5b6f3-930">長度是相對於線條寬度;長度為 &quot; 1 &quot; 等於線條寬度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-930">The lengths are relative to the line width; a length of &quot;1&quot; is equal to the line width.</span></span> <span data-ttu-id="5b6f3-931">EndCap 樣式會套用至每個虛線，而箭號樣式則不適用。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-931">The EndCap style is applied to each dash, arrow styles are not.</span></span> <span data-ttu-id="5b6f3-932">字串會先定義虛線的長度，然後再定義空間的長度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-932">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="5b6f3-933">這可能會重複形成複雜的虛線樣式。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-933">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="5b6f3-934">字串應該一律包含成對的數位;如果它包含奇數數目的數位，則可能會忽略最後一個。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-934">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span> <span data-ttu-id="5b6f3-935">下表列出一些一般值和預期效果的描述。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-935">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="5b6f3-936">&quot;0 &quot; 表示應該 epirus 對稱的點 (使用 round endcaps，它應該是圓形) 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-936">&quot;0&quot; implies a dot that should be fourfold symmetrical (with round endcaps it should be a circle).</span></span> <span data-ttu-id="5b6f3-937">如果行 endcap 是平面的，則檢視器應該 (盡可能選擇內建的作業系統虛線，也就是可快速繪製) 的東西。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-937">If the line endcap is Flat, a viewer should choose a built-in operating system dash where possible (i.e., something that is fast to draw).</span></span> <span data-ttu-id="5b6f3-938">以下顯示一些範例。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-938">The following shows some examples.</span></span>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-939">&quot;2 2&quot;</span><span class="sxs-lookup"><span data-stu-id="5b6f3-939">&quot;2 2&quot;</span></span></td>
<td><span data-ttu-id="5b6f3-940">虛線 (每個虛線，而介於兩者之間的空格是線條寬度的兩倍) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-940">short-dashes (each dash and the space in between is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-941">&quot;1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="5b6f3-941">&quot;1 2&quot;</span></span></td>
<td><span data-ttu-id="5b6f3-942">點 (每個虛線都是線條的寬度，而每個空格是線條寬度的兩倍) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-942">dot (each dash is the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-943">&quot;4 2&quot;</span><span class="sxs-lookup"><span data-stu-id="5b6f3-943">&quot;4 2&quot;</span></span></td>
<td><span data-ttu-id="5b6f3-944">虛線 (每個虛線的寬度會是線條寬度的四倍，而每個空格是線條寬度的兩倍) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-944">dash (each dash is four times the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-945">&quot;8 2&quot;</span><span class="sxs-lookup"><span data-stu-id="5b6f3-945">&quot;8 2&quot;</span></span></td>
<td><span data-ttu-id="5b6f3-946">長虛線</span><span class="sxs-lookup"><span data-stu-id="5b6f3-946">long-dash</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-947">&quot;4 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="5b6f3-947">&quot;4 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="5b6f3-948">虛線點</span><span class="sxs-lookup"><span data-stu-id="5b6f3-948">dash dot</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-949">&quot;8 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="5b6f3-949">&quot;8 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="5b6f3-950">長虛線點</span><span class="sxs-lookup"><span data-stu-id="5b6f3-950">long-dash dot</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-951">&quot;8 2 1 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="5b6f3-951">&quot;8 2 1 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="5b6f3-952">長虛線點點</span><span class="sxs-lookup"><span data-stu-id="5b6f3-952">long-dash dot dot</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a><span data-ttu-id="5b6f3-953">TextPath 元素</span><span class="sxs-lookup"><span data-stu-id="5b6f3-953">TextPath element</span></span>

<span data-ttu-id="5b6f3-954">描述以提供的文字資料、字型和樣式為基礎的向量路徑。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-954">Describes a vector path based on the text data, font, and styles supplied.</span></span> <span data-ttu-id="5b6f3-955">如果有提供，則會扭曲文字路徑以符合 **路徑** 元素。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-955">The text path is warped to conform to a **Path** element if supplied.</span></span>



|          |                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f3-956">FitPath</span><span class="sxs-lookup"><span data-stu-id="5b6f3-956">FitPath</span></span>  | <span data-ttu-id="5b6f3-957">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-957">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-958">調整文字大小以填滿其所在的路徑。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-958">Sizes the text to fill the path it lies out on.</span></span>                                 |
| <span data-ttu-id="5b6f3-959">FitShape</span><span class="sxs-lookup"><span data-stu-id="5b6f3-959">FitShape</span></span> | <span data-ttu-id="5b6f3-960">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-960">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-961">將文字路徑延伸至圖形方塊的邊緣。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-961">Stretches the text path out to the edges of the shape box.</span></span>                      |
| <span data-ttu-id="5b6f3-962">開啟</span><span class="sxs-lookup"><span data-stu-id="5b6f3-962">On</span></span>       | <span data-ttu-id="5b6f3-963">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-963">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-964">決定是否要顯示字元路徑。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-964">Determines whether the character paths are displayed or not.</span></span>                    |
| <span data-ttu-id="5b6f3-965">String</span><span class="sxs-lookup"><span data-stu-id="5b6f3-965">String</span></span>   | <span data-ttu-id="5b6f3-966">字串。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-966">String.</span></span> <span data-ttu-id="5b6f3-967">要轉譯為文字路徑的文字。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-967">The text to render as a text path.</span></span>                                                                                    |
| <span data-ttu-id="5b6f3-968">Trim</span><span class="sxs-lookup"><span data-stu-id="5b6f3-968">Trim</span></span>     | <span data-ttu-id="5b6f3-969">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-969">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-970">如果未使用，則移除保留給 ascenders 和下行的任何其他空間。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-970">Removes any additional space reserved for ascenders and descenders if not used.</span></span> |
| <span data-ttu-id="5b6f3-971">XScale</span><span class="sxs-lookup"><span data-stu-id="5b6f3-971">XScale</span></span>   | <span data-ttu-id="5b6f3-972">[VgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-972">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-973">使用直接 x 度量，而不是沿著路徑進行測量。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-973">Use straight x measurement instead of measuring along the path.</span></span>                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a><span data-ttu-id="5b6f3-974">在 VML 物件模型中使用的資料類型</span><span class="sxs-lookup"><span data-stu-id="5b6f3-974">Data Types Used in the VML Object Model</span></span>

<span data-ttu-id="5b6f3-975">VML 物件模型會使用下列資料類型。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-975">The following data types are used by the VML Object Model.</span></span>

-   [<span data-ttu-id="5b6f3-976">Double</span><span class="sxs-lookup"><span data-stu-id="5b6f3-976">Double</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-977">固定</span><span class="sxs-lookup"><span data-stu-id="5b6f3-977">Fixed</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-978">整數</span><span class="sxs-lookup"><span data-stu-id="5b6f3-978">Integer</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-979">IVgAdjustments</span><span class="sxs-lookup"><span data-stu-id="5b6f3-979">IVgAdjustments</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-980">IVgColor</span><span class="sxs-lookup"><span data-stu-id="5b6f3-980">IVgColor</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-981">IVgEquation</span><span class="sxs-lookup"><span data-stu-id="5b6f3-981">IVgEquation</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-982">IVgFixedRectangle</span><span class="sxs-lookup"><span data-stu-id="5b6f3-982">IVgFixedRectangle</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-983">IVgFixedRectangleArray</span><span class="sxs-lookup"><span data-stu-id="5b6f3-983">IVgFixedRectangleArray</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-984">IVgFormula</span><span class="sxs-lookup"><span data-stu-id="5b6f3-984">IVgFormula</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-985">IVgFormulas</span><span class="sxs-lookup"><span data-stu-id="5b6f3-985">IVgFormulas</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-986">IVgGradientColorArray</span><span class="sxs-lookup"><span data-stu-id="5b6f3-986">IVgGradientColorArray</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-987">IVgPoints</span><span class="sxs-lookup"><span data-stu-id="5b6f3-987">IVgPoints</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-988">IVgSkewMatrix</span><span class="sxs-lookup"><span data-stu-id="5b6f3-988">IVgSkewMatrix</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-989">IVgSkewOffset</span><span class="sxs-lookup"><span data-stu-id="5b6f3-989">IVgSkewOffset</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-990">IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="5b6f3-990">IVgVector2D</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-991">IVgVector3D</span><span class="sxs-lookup"><span data-stu-id="5b6f3-991">IVgVector3D</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-992">長度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-992">Length</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-993">Measure</span><span class="sxs-lookup"><span data-stu-id="5b6f3-993">Measure</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-994">String</span><span class="sxs-lookup"><span data-stu-id="5b6f3-994">String</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-995">VgBlackWhiteMode</span><span class="sxs-lookup"><span data-stu-id="5b6f3-995">VgBlackWhiteMode</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-996">VgFraction</span><span class="sxs-lookup"><span data-stu-id="5b6f3-996">VgFraction</span></span>](/windows)
-   [<span data-ttu-id="5b6f3-997">VgTriState</span><span class="sxs-lookup"><span data-stu-id="5b6f3-997">VgTriState</span></span>](/windows)

<span data-ttu-id="5b6f3-998">**Double 資料類型**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-998">**Double data type**</span></span>

<span data-ttu-id="5b6f3-999">雙精確度整數，其範圍從-無限大到無限大。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-999">A double precision integer with range from -infinity to infinity.</span></span>

<span data-ttu-id="5b6f3-1000">**固定資料類型**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1000">**Fixed data type**</span></span>

<span data-ttu-id="5b6f3-1001">浮點數，範圍從-32766.0 到32766.0。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1001">Floating point number with range from -32,766.0 to 32,766.0.</span></span>

<span data-ttu-id="5b6f3-1002">**整數資料類型**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1002">**Integer data type**</span></span>

<span data-ttu-id="5b6f3-1003">範圍從-無限大到無限大的整數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1003">An integer with a range from -infinity to infinity.</span></span>

<span data-ttu-id="5b6f3-1004">**IVgAdjustments 資料類型**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1004">**IVgAdjustments data type**</span></span>

<span data-ttu-id="5b6f3-1005">圖形的調整集合，可以用來變更圖形的維度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1005">Collection of adjustments to a shape that can be used to change the dimensions of a shape.</span></span> <span data-ttu-id="5b6f3-1006">調整可用來作為暫時預留位置，或因任何原因而使用變數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1006">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="5b6f3-1007">集合中只有8項調整。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1007">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="5b6f3-1008">屬性</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1008">Attributes</span></span> | <span data-ttu-id="5b6f3-1009">Description</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1009">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f3-1010">Exists</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1010">Exists</span></span>     | <span data-ttu-id="5b6f3-1011">[IVgTriState](msdn-online-vml-vgtristate.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1011">[IVgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="5b6f3-1012">判斷指定的調整是否存在。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1012">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="5b6f3-1013">請注意，必須使用索引;也就是說， ( 專案 ) 必須用來取出專案的存在。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1013">Note that an index must be used; that is, exists( item ) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="5b6f3-1014">項目</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1014">Item</span></span>       | <span data-ttu-id="5b6f3-1015">[Long](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1015">[Long](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1016">從0到7的索引調整陣列。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1016">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="5b6f3-1017">請注意，可能會 sparcely 指定調整;也就是說，中繼陣列值可能不一定會填滿。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1017">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="5b6f3-1018">例如，專案1、3和5的值可能是3，而專案 (0) 、專案 (2) 和專案 (4) 指定。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1018">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="5b6f3-1019">若要查看專案是否存在，請使用 Exists 屬性。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1019">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="5b6f3-1020">長度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1020">Length</span></span>     | <span data-ttu-id="5b6f3-1021">[Integer](#data-types-used-in-the-vml-object-model) (整數)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1021">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1022">調整的數目。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1022">Number of adjustments.</span></span> <span data-ttu-id="5b6f3-1023">不能大於8。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1023">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5b6f3-1024">值</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1024">Value</span></span>      | <span data-ttu-id="5b6f3-1025">[字串](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1025">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1026">數值的文字標記法，每個數位之間都有逗號。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1026">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="5b6f3-1027">**IVgColor**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1027">**IVgColor**</span></span>

<span data-ttu-id="5b6f3-1028">指定色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1028">Specifies a color.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b6f3-1029">屬性</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1029">Attributes</span></span></th>
<th><span data-ttu-id="5b6f3-1030">Description</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1030">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1031">RGB</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1031">RGB</span></span></td>
<td><span data-ttu-id="5b6f3-1032"><strong>VgRGBType</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1032"><strong>VgRGBType</strong>.</span></span> <span data-ttu-id="5b6f3-1033">RGB 值 (色彩的長) 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1033">RGB value (Long) of the color.</span></span> <span data-ttu-id="5b6f3-1034">只有當類型為 RGB 時才有效。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1034">Only valid if Type is RGB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1035">R</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1035">R</span></span></td>
<td><span data-ttu-id="5b6f3-1036"><a href="#data-types-used-in-the-vml-object-model">Integer</a> (整數)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1036"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="5b6f3-1037">色彩的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1037">Red component of the color.</span></span> <span data-ttu-id="5b6f3-1038">的範圍可以介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1038">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1039">G</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1039">G</span></span></td>
<td><span data-ttu-id="5b6f3-1040"><a href="#data-types-used-in-the-vml-object-model">Integer</a> (整數)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1040"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="5b6f3-1041">色彩的綠色元件。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1041">Green component of the color.</span></span> <span data-ttu-id="5b6f3-1042">的範圍可以介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1042">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1043">B</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1043">B</span></span></td>
<td><span data-ttu-id="5b6f3-1044"><a href="#data-types-used-in-the-vml-object-model">Integer</a> (整數)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1044"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="5b6f3-1045">色彩的藍色元件。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1045">Blue component of the color.</span></span> <span data-ttu-id="5b6f3-1046">的範圍可以介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1046">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1047">String</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1047">String</span></span></td>
<td><span data-ttu-id="5b6f3-1048"><a href="#data-types-used-in-the-vml-object-model">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1048"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="5b6f3-1049">色彩的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1049">Text representation of the color.</span></span> <span data-ttu-id="5b6f3-1050">以下是支援的命名色彩類型：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1050">The following named color types are supported:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-1051">黑色 (#000000) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1051">Black (#000000)</span></span></li>
<li><span data-ttu-id="5b6f3-1052">銀級 (#C0C0C0) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1052">Silver (#C0C0C0)</span></span></li>
<li><span data-ttu-id="5b6f3-1053">灰色 (#808080) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1053">Gray (#808080)</span></span></li>
<li><span data-ttu-id="5b6f3-1054">白色 (#FFFFFF) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1054">White (#FFFFFF)</span></span></li>
<li><span data-ttu-id="5b6f3-1055"> (#800000) 的暗紫紅色</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1055">Maroon (#800000)</span></span></li>
<li><span data-ttu-id="5b6f3-1056">紅色 (#FF0000) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1056">Red (#FF0000)</span></span></li>
<li><span data-ttu-id="5b6f3-1057">紫色 (#800080) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1057">Purple (#800080)</span></span></li>
<li><span data-ttu-id="5b6f3-1058">Fuchsia (#FF00FF) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1058">Fuchsia (#FF00FF)</span></span></li>
<li><span data-ttu-id="5b6f3-1059">綠色 (#008000) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1059">Green (#008000)</span></span></li>
<li><span data-ttu-id="5b6f3-1060"> (#00FF00) 的橙色</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1060">Lime (#00FF00)</span></span></li>
<li><span data-ttu-id="5b6f3-1061">) 的橄欖綠 (#808000</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1061">Olive (#808000)</span></span></li>
<li><span data-ttu-id="5b6f3-1062">黃色 (#FFFF00) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1062">Yellow (#FFFF00)</span></span></li>
<li><span data-ttu-id="5b6f3-1063">Navy (#000080) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1063">Navy (#000080)</span></span></li>
<li><span data-ttu-id="5b6f3-1064">藍色 (#0000FF) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1064">Blue (#0000FF)</span></span></li>
<li><span data-ttu-id="5b6f3-1065">青色 (#008080) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1065">Teal (#008080)</span></span></li>
<li><span data-ttu-id="5b6f3-1066">綠色 (#00FFFF) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1066">Aqua (#00FFFF)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1067">類型</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1067">Type</span></span></td>
<td><span data-ttu-id="5b6f3-1068"><strong>VgColorType</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1068"><strong>VgColorType</strong>.</span></span> <span data-ttu-id="5b6f3-1069">色彩的類型。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1069">Type of color.</span></span> <span data-ttu-id="5b6f3-1070">下列其中一種類型：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1070">One of the following types:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-1071">Mixed</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1071">Mixed</span></span></li>
<li><span data-ttu-id="5b6f3-1072">已命名</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1072">Named</span></span></li>
<li><span data-ttu-id="5b6f3-1073">RGB</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1073">RGB</span></span></li>
<li><span data-ttu-id="5b6f3-1074">配置</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1074">Scheme</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5b6f3-1075">**IVgEquation**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1075">**IVgEquation**</span></span>

<span data-ttu-id="5b6f3-1076">用於公式的方程式。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1076">Equations used for formulas.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1077">作業</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1077">Operation</span></span></td>
<td><span data-ttu-id="5b6f3-1078"><strong>VgEquationOperationType</strong> 要在參數上執行的作業名稱。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1078"><strong>VgEquationOperationType</strong> Name of operation to perform on the parameters.</span></span> <span data-ttu-id="5b6f3-1079">下列作業可用於方程式：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1079">The following operations can be used in an equation:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5b6f3-1080">作業</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1080">Operation</span></span></th>
<th><span data-ttu-id="5b6f3-1081">描述</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1081">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1082">Abs</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1082">Abs</span></span></td>
<td><span data-ttu-id="5b6f3-1083">絕對值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1083">Absolute value.</span></span> <br/> <span data-ttu-id="5b6f3-1084"><strong>abs</strong> (v) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1084"><strong>abs</strong>(v)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1085">Atan2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1085">Atan2</span></span></td>
<td><span data-ttu-id="5b6f3-1086">極座標：以 fd 單位 (度乘以 65536) 的結果。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1086">Polar arithmetic--results in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="5b6f3-1087"><strong>atan2</strong> (p1，v) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1087"><strong>atan2</strong>(p1,v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1088">Cos</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1088">Cos</span></span></td>
<td><span data-ttu-id="5b6f3-1089">在 fd 單位中的余弦值、引數 (度乘以 65536) 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1089">Cosine, argument in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="5b6f3-1090">v \* <strong>cos</strong> (p1) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1090">v \* <strong>cos</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1091">Cosatan2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1091">Cosatan2</span></span></td>
<td><span data-ttu-id="5b6f3-1092">在中繼計算中保留完整的精確度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1092">Preserves full accuracy in intermediate calculation.</span></span><br/> <span data-ttu-id="5b6f3-1093">v \* <strong>cos (atan2 (</strong> p2，p1 <strong>) ) </strong></span><span class="sxs-lookup"><span data-stu-id="5b6f3-1093">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1094">橢圓形</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1094">Ellipse</span></span></td>
<td><span data-ttu-id="5b6f3-1095">橢圓形</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1095">Ellipse</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1096">如果</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1096">If</span></span></td>
<td><span data-ttu-id="5b6f3-1097">如果條件測試。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1097">If Condition test.</span></span> <span data-ttu-id="5b6f3-1098">v > 0 <strong>？</strong></span><span class="sxs-lookup"><span data-stu-id="5b6f3-1098">v > 0 <strong>?</strong></span></span> <span data-ttu-id="5b6f3-1099">p1： p2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1099">p1 : p2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1100">最大值</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1100">Max</span></span></td>
<td><span data-ttu-id="5b6f3-1101">兩個值中較大的一個。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1101">The greater of two values.</span></span> <br/> <span data-ttu-id="5b6f3-1102"><strong>max</strong> (v，p1) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1102"><strong>max</strong>(v,p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1103">Mid</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1103">Mid</span></span></td>
<td><span data-ttu-id="5b6f3-1104">平均 ( v + p1) /2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1104">Average ( v + p1)/2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1105">Min</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1105">Min</span></span></td>
<td><span data-ttu-id="5b6f3-1106">兩個值的較小者。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1106">The lesser of two values.</span></span> <span data-ttu-id="5b6f3-1107"><strong>min</strong> (v，p1) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1107"><strong>min</strong>(v,p1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1108">Mod</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1108">Mod</span></span></td>
<td><span data-ttu-id="5b6f3-1109">模數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1109">Modulus.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1110">產品</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1110">Product</span></span></td>
<td><span data-ttu-id="5b6f3-1111">用於乘法和除法。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1111">Used for multiplication and division.</span></span> <span data-ttu-id="5b6f3-1112">v \* p1/p2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1112">v \* p1 / p2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1113">Sin</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1113">Sin</span></span></td>
<td><span data-ttu-id="5b6f3-1114">在 fd 單位中的正弦值、引數 (度乘以 65536) 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1114">Sine, argument in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="5b6f3-1115">v \* <strong>sin</strong> (p1) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1115">v \* <strong>sin</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1116">Sinatan2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1116">Sinatan2</span></span></td>
<td><span data-ttu-id="5b6f3-1117">在中繼計算中保留完整的精確度。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1117">Preserves full accuracy in intermediate calculation.</span></span> <span data-ttu-id="5b6f3-1118">v \* <strong>sin</strong> (<strong>atan2</strong> (p2，p1) ) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1118">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1119">Sqrt</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1119">Sqrt</span></span></td>
<td><span data-ttu-id="5b6f3-1120">結果為正向下四捨五入。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1120">Result is positive and rounds down.</span></span> <br/> <span data-ttu-id="5b6f3-1121"><strong>sqrt</strong> (v) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1121"><strong>sqrt</strong>(v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1122">Sum</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1122">Sum</span></span></td>
<td><span data-ttu-id="5b6f3-1123">用於加法和減法。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1123">Used for addition and subtraction.</span></span><br/> <span data-ttu-id="5b6f3-1124">v + p1 p2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1124">v + p1 p2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1125">Sumangle</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1125">Sumangle</span></span></td>
<td><span data-ttu-id="5b6f3-1126">現有的角度 (以 65536) 調整，其中 p1 和 p2 是以度為單位。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1126">Existing angle (scaled by 65536), where p1 and p2 are in degrees.</span></span><br/> <span data-ttu-id="5b6f3-1127">v + p1 \* 65536 + p2 \* 65536</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1127">v + p1 \* 65536 + p2 \* 65536</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1128">Tan</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1128">Tan</span></span></td>
<td><span data-ttu-id="5b6f3-1129">正切函數的引數為 fd 單位 (度乘以 65536) 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1129">Tangent, argument is in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="5b6f3-1130">v \* tan ( p1 ) </span><span class="sxs-lookup"><span data-stu-id="5b6f3-1130">v \* tan( p1 )</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1131">Val</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1131">Val</span></span></td>
<td><span data-ttu-id="5b6f3-1132">定義其他值的輔助線值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1132">Defines a guide value from some other value.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1133">Param1</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1133">Param1</span></span></td>
<td><span data-ttu-id="5b6f3-1134"><strong>Integer</strong> (整數)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1134"><strong>Integer</strong>.</span></span> <span data-ttu-id="5b6f3-1135">第一個參數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1135">The first parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1136">Paramtype1</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1136">Paramtype1</span></span></td>
<td><span data-ttu-id="5b6f3-1137"><strong>VgFormulaParamType</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1137"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="5b6f3-1138">第一個參數的型別。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1138">The type of the first parameter.</span></span> <span data-ttu-id="5b6f3-1139">支援下列值：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1139">The following values are supported:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5b6f3-1140">類型</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1140">Type</span></span></th>
<th><span data-ttu-id="5b6f3-1141">描述</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1142">值</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1142">Value</span></span></td>
<td><span data-ttu-id="5b6f3-1143">參數是簡單的值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1143">Parameter is simple value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1144">AdjustmentReference</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1144">AdjustmentReference</span></span></td>
<td><span data-ttu-id="5b6f3-1145">參數是調整的參考。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1145">Parameter is a reference to an adjustment.</span></span> <span data-ttu-id="5b6f3-1146">例如，如果第一個參數是1，則會使用第一次調整的值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1146">For example, if the first parameter is 1, then the value of the first adjustment will be used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1147">FormulaReference</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1147">FormulaReference</span></span></td>
<td><span data-ttu-id="5b6f3-1148">參數是先前公式的結果參考結果。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1148">Parameter is the result of a reference to the result of a previous formula.</span></span> <span data-ttu-id="5b6f3-1149">例如，如果第一個參數是2，則會使用公式2的結果。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1149">For example, if the first parameter is 2, then the result of formula 2 will be used.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1150">Param2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1150">Param2</span></span></td>
<td><span data-ttu-id="5b6f3-1151"><strong>Integer</strong> (整數)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1151"><strong>Integer</strong>.</span></span> <span data-ttu-id="5b6f3-1152">第二個參數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1152">The second parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1153">Paramtype2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1153">Paramtype2</span></span></td>
<td><span data-ttu-id="5b6f3-1154"><strong>VgFormulaParamType</strong> 參數2的型別。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1154"><strong>VgFormulaParamType</strong> The type of parameter 2.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1155">Val</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1155">Val</span></span></td>
<td><span data-ttu-id="5b6f3-1156"><strong>Integer</strong> (整數)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1156"><strong>Integer</strong>.</span></span> <span data-ttu-id="5b6f3-1157">結果。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1157">The result.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1158">Valtype2</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1158">Valtype2</span></span></td>
<td><span data-ttu-id="5b6f3-1159"><strong>VgFormulaParamType</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1159"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="5b6f3-1160">結果的類型。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1160">The type of the result.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5b6f3-1161">**IVgFixedRectangle**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1161">**IVgFixedRectangle**</span></span>

<span data-ttu-id="5b6f3-1162">指定固定的矩形。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1162">Specifies a fixed rectangle.</span></span>



| <span data-ttu-id="5b6f3-1163">屬性</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1163">Attributes</span></span> | <span data-ttu-id="5b6f3-1164">描述</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1164">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f3-1165">值</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1165">Value</span></span>      | <span data-ttu-id="5b6f3-1166">[字串](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1166">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1167">指定路徑的文字值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1167">Text value specifying the path.</span></span>         |
| <span data-ttu-id="5b6f3-1168">Left</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1168">Left</span></span>       | <span data-ttu-id="5b6f3-1169">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1169">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1170">矩形的最左邊座標。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1170">Leftmost coordinate of the rectangle.</span></span>   |
| <span data-ttu-id="5b6f3-1171">頁首</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1171">Top</span></span>        | <span data-ttu-id="5b6f3-1172">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1172">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1173">矩形的最上層座標。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1173">Topmost coordinate of the rectangle.</span></span>    |
| <span data-ttu-id="5b6f3-1174">Right</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1174">Right</span></span>      | <span data-ttu-id="5b6f3-1175">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1175">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1176">矩形的最右側座標。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1176">Rightmost coordinate of the rectangle.</span></span>  |
| <span data-ttu-id="5b6f3-1177">下層</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1177">Bottom</span></span>     | <span data-ttu-id="5b6f3-1178">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1178">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1179">矩形的最底層座標。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1179">Bottommost coordinate of the rectangle.</span></span> |



 

<span data-ttu-id="5b6f3-1180">**IVgFixedRectangleArray**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1180">**IVgFixedRectangleArray**</span></span>

<span data-ttu-id="5b6f3-1181">固定矩形的陣列。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1181">Array of fixed rectangles.</span></span>



| <span data-ttu-id="5b6f3-1182">屬性</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1182">Attributes</span></span> | <span data-ttu-id="5b6f3-1183">描述</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1183">Description</span></span>                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f3-1184">值</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1184">Value</span></span>      | <span data-ttu-id="5b6f3-1185">[字串](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1185">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1186">陣列的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1186">Text representation of array.</span></span>                           |
| <span data-ttu-id="5b6f3-1187">長度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1187">Length</span></span>     | <span data-ttu-id="5b6f3-1188">[Integer](#data-types-used-in-the-vml-object-model) (整數)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1188">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1189">此陣列中的矩形數目。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1189">Number of rectangles in this array.</span></span>                    |
| <span data-ttu-id="5b6f3-1190">項目</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1190">Item</span></span>       | <span data-ttu-id="5b6f3-1191">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1191">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1192">位於指定索引處的矩形物件。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1192">The rectangle object at the specified index.</span></span> |



 

<span data-ttu-id="5b6f3-1193">**IVgFormula** 資料類型</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1193">**IVgFormula** data type</span></span>

<span data-ttu-id="5b6f3-1194">公式的定義，可以改變形狀的路徑，或用於其他計算用途。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1194">Definitions for formulas that can vary the path of a shape or be used for other calculation purposes.</span></span> <span data-ttu-id="5b6f3-1195">公式可以根據可能變更之圖形的 **形容詞** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1195">Formulas can be based on the **Adj** attribute of a shape, which can change.</span></span> <span data-ttu-id="5b6f3-1196">公式也可以參考其他公式。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1196">Formulas can reference other formulas as well.</span></span>



| <span data-ttu-id="5b6f3-1197">屬性</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1197">Attributes</span></span> | <span data-ttu-id="5b6f3-1198">Description</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1198">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f3-1199">Eqn</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1199">Eqn</span></span>        | <span data-ttu-id="5b6f3-1200">[IVgEquation](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1200">[IVgEquation](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1201">每個公式都會將單一值定義為運算式評估的結果。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1201">Each formula defines a single value as the result of the evaluation of the expression.</span></span> <span data-ttu-id="5b6f3-1202">運算式是由這個屬性所定義，且具有最多三個引數的一般形式，也就是調整值 (例如， \# 2) 、先前公式的結果 (例如 @2) 、固定數位或預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1202">The expression is defined by this attribute and has the general form of an operation followed by up to three arguments, which may be adjustment values (e.g., \#2), the results of earlier formulas (e.g., @2), fixed numbers, or predefined values.</span></span> |



 

<span data-ttu-id="5b6f3-1203">**IVgFormulas 資料類型**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1203">**IVgFormulas data type**</span></span>

<span data-ttu-id="5b6f3-1204">公式物件的集合。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1204">A collection of formula objects.</span></span>



| <span data-ttu-id="5b6f3-1205">屬性</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1205">Attributes</span></span> | <span data-ttu-id="5b6f3-1206">Description</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1206">Description</span></span>                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f3-1207">長度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1207">Length</span></span>     | <span data-ttu-id="5b6f3-1208">[Integer](#data-types-used-in-the-vml-object-model) (整數)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1208">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1209">集合中的公式物件數目。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1209">Number of formula objects in collection.</span></span>                                                |
| <span data-ttu-id="5b6f3-1210">項目</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1210">Item</span></span>       | <span data-ttu-id="5b6f3-1211">[IVgFormula](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1211">[IVgFormula](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1212">特定的公式。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1212">A specific formula.</span></span> <span data-ttu-id="5b6f3-1213">請注意，公式陣列可能會繼承從圖形類型。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1213">Note that the formula array may be inherited fom the shape type.</span></span> |



 

<span data-ttu-id="5b6f3-1214">**IVgGradientColorArray**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1214">**IVgGradientColorArray**</span></span>

<span data-ttu-id="5b6f3-1215">色彩的陣列，定義) 的漸層 (混合的色彩範圍。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1215">An array of colors that define a gradient (blended range of colors).</span></span>



| <span data-ttu-id="5b6f3-1216">屬性</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1216">Attributes</span></span> | <span data-ttu-id="5b6f3-1217">描述</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1217">Description</span></span>                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f3-1218">值</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1218">Value</span></span>      | <span data-ttu-id="5b6f3-1219">[字串](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1219">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1220">指定色彩的陣列;例如，"red. 2;綠. 4;黑色. 7 "</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1220">Specifies the array of colors; for example, "red .2; green .4; black .7"</span></span> |
| <span data-ttu-id="5b6f3-1221">長度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1221">Length</span></span>     | <span data-ttu-id="5b6f3-1222">[Integer](#data-types-used-in-the-vml-object-model) (整數)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1222">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1223">陣列中的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1223">Number of colors in the array.</span></span>                                          |



 



| <span data-ttu-id="5b6f3-1224">方法</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1224">Methods</span></span>     | <span data-ttu-id="5b6f3-1225">描述</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1225">Description</span></span>                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f3-1226">AddColor</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1226">AddColor</span></span>    | <span data-ttu-id="5b6f3-1227">[VgFraction](msdn-online-vml-vgfraction-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1227">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="5b6f3-1228">在分數指定的端點上加入新的色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1228">Adds new color at endpoint specified by fraction.</span></span> <span data-ttu-id="5b6f3-1229">新的色彩預設為白色，而是傳回值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1229">The new color is white by default and is the return value.</span></span> <span data-ttu-id="5b6f3-1230">然後可以透過參考來變更色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1230">The color can then be changed by reference.</span></span> |
| <span data-ttu-id="5b6f3-1231">RemoveColor</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1231">RemoveColor</span></span> | <span data-ttu-id="5b6f3-1232">[VgFraction](msdn-online-vml-vgfraction-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1232">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="5b6f3-1233">移除依分數指定之端點的色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1233">Removes a color at endpoint specified by fraction.</span></span> <span data-ttu-id="5b6f3-1234">注意：如果0.0 或1.0 不存在，就表示它是隱含的，而且會在該點使用白色的色彩。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1234">Note: if 0.0 or 1.0 does not exist, it is implied and the color white is used at that point.</span></span>          |



 

<span data-ttu-id="5b6f3-1235">**IVgPoints 資料類型**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1235">**IVgPoints datatype**</span></span>

<span data-ttu-id="5b6f3-1236">定義圖形的點陣列。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1236">Array of points that define a shape.</span></span>



| <span data-ttu-id="5b6f3-1237">屬性</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1237">Attributes</span></span> | <span data-ttu-id="5b6f3-1238">描述</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1238">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f3-1239">值</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1239">Value</span></span>      | <span data-ttu-id="5b6f3-1240">[字串](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1240">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1241">陣列的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1241">Text representation of array.</span></span>           |
| <span data-ttu-id="5b6f3-1242">長度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1242">Length</span></span>     | <span data-ttu-id="5b6f3-1243">[Integer](#data-types-used-in-the-vml-object-model) (整數)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1243">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="5b6f3-1244">此陣列中的點數目。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1244">Number of points in this array.</span></span>        |
| <span data-ttu-id="5b6f3-1245">項目</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1245">Item</span></span>       | <span data-ttu-id="5b6f3-1246">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1246">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="5b6f3-1247">指定之索引處的點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1247">The point at the specified index.</span></span> |



 

<span data-ttu-id="5b6f3-1248">**IVgSkewMatrix 資料類型**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1248">**IVgSkewMatrix datatype**</span></span>

<span data-ttu-id="5b6f3-1249">用於扭曲形狀的矩陣，以 "*sxx，sxy，syx，syy，px，.py* " \[ *s* = scale， *p* = 透視圖形式的觀點轉換矩陣 \] 。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1249">A matrix used for skewing shapes, a perspective transform matrix in the form, "*sxx,sxy,syx,syy,px,py* " \[*s* =scale, *p* =perspective\].</span></span> <span data-ttu-id="5b6f3-1250">如果 offset 是絕對單位，則 *px，.py* 是以 emu ^ 1 單位為單位;否則是圖形大小的反向分數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1250">If offset is in absolute units, then *px,py* are in emu ^-1 units; otherwise they are an inverse fraction of shape size.</span></span>



| <span data-ttu-id="5b6f3-1251">屬性</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1251">Attributes</span></span>   | <span data-ttu-id="5b6f3-1252">Description</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1252">Description</span></span>                                         |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="5b6f3-1253">XtoX</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1253">XtoX</span></span>         | <span data-ttu-id="5b6f3-1254">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1254">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="5b6f3-1255">YtoX</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1255">YtoX</span></span>         | <span data-ttu-id="5b6f3-1256">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1256">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="5b6f3-1257">XtoY</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1257">XtoY</span></span>         | <span data-ttu-id="5b6f3-1258">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1258">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="5b6f3-1259">YtoY</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1259">YtoY</span></span>         | <span data-ttu-id="5b6f3-1260">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1260">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="5b6f3-1261">PerspectiveX</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1261">PerspectiveX</span></span> | <span data-ttu-id="5b6f3-1262">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1262">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="5b6f3-1263">PerspectiveY</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1263">PerspectiveY</span></span> | <span data-ttu-id="5b6f3-1264">[Double](#data-types-used-in-the-vml-object-model)。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1264">[Double](#data-types-used-in-the-vml-object-model).</span></span> |



 

<span data-ttu-id="5b6f3-1265">**IVgSkewOffset**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1265">**IVgSkewOffset**</span></span>

<span data-ttu-id="5b6f3-1266">指定扭曲的位移。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1266">Specifies the offset of the skew.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b6f3-1267">屬性</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1267">Attributes</span></span></th>
<th><span data-ttu-id="5b6f3-1268">描述</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1268">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1269">值</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1269">Value</span></span></td>
<td><span data-ttu-id="5b6f3-1270"><a href="#data-types-used-in-the-vml-object-model">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1270"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="5b6f3-1271">位移的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1271">Text representation of offset.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1272">X</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1272">X</span></span></td>
<td><span data-ttu-id="5b6f3-1273"><a href="#data-types-used-in-the-vml-object-model">Double</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1273"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="5b6f3-1274">X 元件。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1274">X component.</span></span> <span data-ttu-id="5b6f3-1275">百分比或量值。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1275">Percentage or measure.</span></span> <span data-ttu-id="5b6f3-1276">如果沒有單位，則隱含 ShapeRelative 類型;否則，就會隱含絕對型別。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1276">If no units, then ShapeRelative type is implied; otherwise Absolute type is implied.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1277">Y</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1277">Y</span></span></td>
<td><span data-ttu-id="5b6f3-1278"><a href="#data-types-used-in-the-vml-object-model">Double</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1278"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="5b6f3-1279">Y 元件。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1279">Y component.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1280">類型</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1280">Type</span></span></td>
<td><span data-ttu-id="5b6f3-1281"><strong>VgSkewTransformType</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1281"><strong>VgSkewTransformType</strong>.</span></span> <span data-ttu-id="5b6f3-1282">指定轉換的類型。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1282">Specifies the type of transformation.</span></span> <span data-ttu-id="5b6f3-1283">有效的值是介於-無限大和無限大之間的整數點。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1283">Valid values are integer points ranging between -infinity and infinity.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5b6f3-1284">類型</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1284">Type</span></span></th>
<th><span data-ttu-id="5b6f3-1285">Description</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1285">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1286">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1286">ShapeRelative</span></span></td>
<td><span data-ttu-id="5b6f3-1287">位移的值是原始圖形大小 (比例) 的百分比;例如，值0.5 表示形狀大小的位移一半。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1287">The values of the offset are percentages (ratios) of the original shape's size; e.g., a value of 0.5 means an offset half the size of the shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1288">絕對</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1288">Absolute</span></span></td>
<td><span data-ttu-id="5b6f3-1289">這些值是絕對單位。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1289">The values are absolute units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5b6f3-1290">**IVgVector2D 資料類型**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1290">**IVgVector2D data type**</span></span>

<span data-ttu-id="5b6f3-1291">指定由兩個 **雙精度浮** 點陣列成的二維向量。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1291">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b6f3-1292">屬性</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1292">Attributes</span></span></th>
<th><span data-ttu-id="5b6f3-1293">描述</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1293">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1294">值</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1294">Value</span></span></td>
<td><span data-ttu-id="5b6f3-1295"><strong>字串</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1295"><strong>String</strong>.</span></span> <span data-ttu-id="5b6f3-1296">以空格分隔的兩個向量數位的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1296">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1297">X</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1297">X</span></span></td>
<td><span data-ttu-id="5b6f3-1298"><a href="#data-types-used-in-the-vml-object-model">Double</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1298"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="5b6f3-1299">這個向量的 X 元件。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1299">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1300">Y</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1300">Y</span></span></td>
<td><span data-ttu-id="5b6f3-1301"><a href="#data-types-used-in-the-vml-object-model">Double</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1301"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="5b6f3-1302">這個向量的 Y 元件。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1302">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1303">類型</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1303">Type</span></span></td>
<td><span data-ttu-id="5b6f3-1304"><strong>VgVectorType</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1304"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="5b6f3-1305">此向量的預期單位。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1305">Expected units for this vector.</span></span> <span data-ttu-id="5b6f3-1306">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1306">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-1307">Measure</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1307">Measure</span></span></li>
<li><span data-ttu-id="5b6f3-1308">長度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1308">Length</span></span></li>
<li><span data-ttu-id="5b6f3-1309">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1309">AngleInDegrees</span></span></li>
<li><span data-ttu-id="5b6f3-1310">Fraction</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1310">Fraction</span></span></li>
<li><span data-ttu-id="5b6f3-1311">數位百分比整數</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1311">Number Percentage Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5b6f3-1312">**IVgVector3D 資料類型**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1312">**IVgVector3D data type**</span></span>

<span data-ttu-id="5b6f3-1313">指定由三個 **雙精度浮** 點陣列成的三維向量。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1313">Specifies a three-dimensional vector consisting of three **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1314">值</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1314">Value</span></span></td>
<td><span data-ttu-id="5b6f3-1315"><strong>字串</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1315"><strong>String</strong>.</span></span> <span data-ttu-id="5b6f3-1316">以空格分隔的三個向量數位的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1316">Text representation of three vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1317">X</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1317">X</span></span></td>
<td><span data-ttu-id="5b6f3-1318"><a href="#data-types-used-in-the-vml-object-model">Double</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1318"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="5b6f3-1319">這個向量的 X 元件。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1319">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1320">Y</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1320">Y</span></span></td>
<td><span data-ttu-id="5b6f3-1321"><a href="#data-types-used-in-the-vml-object-model">Double</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1321"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="5b6f3-1322">這個向量的 Y 元件。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1322">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b6f3-1323">Z</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1323">Z</span></span></td>
<td><span data-ttu-id="5b6f3-1324"><a href="#data-types-used-in-the-vml-object-model">Double</a>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1324"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="5b6f3-1325">此向量的 Z 元件。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1325">Z component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b6f3-1326">類型</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1326">Type</span></span></td>
<td><span data-ttu-id="5b6f3-1327"><strong>VgVectorType</strong>。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1327"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="5b6f3-1328">此向量的預期單位。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1328">Expected units for this vector.</span></span> <span data-ttu-id="5b6f3-1329">值為：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1329">Values are:</span></span>
<ul>
<li><span data-ttu-id="5b6f3-1330">Measure</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1330">Measure</span></span></li>
<li><span data-ttu-id="5b6f3-1331">長度</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1331">Length</span></span></li>
<li><span data-ttu-id="5b6f3-1332">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1332">AngleInDegrees</span></span></li>
<li><span data-ttu-id="5b6f3-1333">Fraction</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1333">Fraction</span></span></li>
<li><span data-ttu-id="5b6f3-1334">數字</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1334">Number</span></span></li>
<li><span data-ttu-id="5b6f3-1335">百分比</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1335">Percentage</span></span></li>
<li><span data-ttu-id="5b6f3-1336">整數</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1336">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5b6f3-1337">**Length 資料類型**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1337">**Length data type**</span></span>

<span data-ttu-id="5b6f3-1338">浮點數，範圍介於0到無限大之間。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1338">A floating point number with a range from 0 to infinity.</span></span>

<span data-ttu-id="5b6f3-1339">**量值資料類型**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1339">**Measure data type**</span></span>

<span data-ttu-id="5b6f3-1340">從-無限大到無限大的浮點數。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1340">A floating point number from -infinity to infinity.</span></span>

<span data-ttu-id="5b6f3-1341">**字串資料類型**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1341">**String data type**</span></span>

<span data-ttu-id="5b6f3-1342">任何長度的字元資料。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1342">Character data of any length.</span></span>

<span data-ttu-id="5b6f3-1343">**VgBlackWhiteMode**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1343">**VgBlackWhiteMode**</span></span>

<span data-ttu-id="5b6f3-1344">黑色和白色的呈現模式。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1344">Rendering mode for black and white.</span></span> <span data-ttu-id="5b6f3-1345">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1345">Possible values are:</span></span>

-   <span data-ttu-id="5b6f3-1346">**色彩**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1346">**Color**</span></span>
-   <span data-ttu-id="5b6f3-1347">**Auto**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1347">**Auto**</span></span>
-   <span data-ttu-id="5b6f3-1348">**灰度**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1348">**GrayScale**</span></span>
-   <span data-ttu-id="5b6f3-1349">**LightGrayScale**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1349">**LightGrayScale**</span></span>
-   <span data-ttu-id="5b6f3-1350">**InverseGray**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1350">**InverseGray**</span></span>
-   <span data-ttu-id="5b6f3-1351">**GrayOutline**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1351">**GrayOutline**</span></span>
-   <span data-ttu-id="5b6f3-1352">**BlackTextAndLines**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1352">**BlackTextAndLines**</span></span>
-   <span data-ttu-id="5b6f3-1353">**HighContrast**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1353">**HighContrast**</span></span>
-   <span data-ttu-id="5b6f3-1354">**黑**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1354">**Black**</span></span>
-   <span data-ttu-id="5b6f3-1355">**白色**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1355">**White**</span></span>
-   <span data-ttu-id="5b6f3-1356">**Undrawn**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1356">**Undrawn**</span></span>

<span data-ttu-id="5b6f3-1357">**VgFraction 資料類型**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1357">**VgFraction data type**</span></span>

<span data-ttu-id="5b6f3-1358">浮點數，範圍從0.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1358">Floating point number with range from 0.0 to 1.0.</span></span> <span data-ttu-id="5b6f3-1359">分數也可以指定為百分比;例如，"50%"。</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1359">Fractions can also be specified as a percentage; e.g., "50%".</span></span>

<span data-ttu-id="5b6f3-1360">**VgTriState 資料類型**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1360">**VgTriState datatype**</span></span>

<span data-ttu-id="5b6f3-1361">列舉值，用於可為三種狀態之一的值：</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1361">Enumeration used for values that can be one of three states:</span></span>

-   <span data-ttu-id="5b6f3-1362">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1362">**TRUE**</span></span>
-   <span data-ttu-id="5b6f3-1363">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1363">**FALSE**</span></span>
-   <span data-ttu-id="5b6f3-1364">**MIXED**</span><span class="sxs-lookup"><span data-stu-id="5b6f3-1364">**MIXED**</span></span>