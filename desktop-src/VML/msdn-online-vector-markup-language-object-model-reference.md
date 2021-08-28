---
title: VML 物件模型參考
description: 本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa8c608a60cbdb5af0fa5699fb1d458a5f18552
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884169"
---
# <a name="vml-object-model-reference"></a>VML 物件模型參考

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

本主題內容：

-   [簡介](#introduction)
-   [範例](#example)
-   [設定 VML](#setting-up-vml)
-   [VML OM 參考](#vml-om-reference)
    -   [Shape 元素](#shape-element)
-   [Shape 元素的子項目](#subelements-of-the-shape-element)
    -   [Background 元素](#background-element)
    -   [延伸元素](#extrusion-element)
    -   [Fill 元素](#fill-element)
    -   [Group 元素](#group-element)
    -   [Imagedata 元素](#imagedata-element)
    -   [Path 元素](#path-element)
    -   [Shadow 元素](#shadow-element)
    -   [扭曲元素](#skew-element)
    -   [Stroke 元素](#stroke-element)
    -   [TextPath 元素](#textpath-element)
-   [在 VML 物件模型中使用的資料類型](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a>簡介

[Vector Markup Language (VML) ](https://www.w3.org/TR/NOTE-datetime.html) 是以文字為基礎的語言，使用 [XML](https://www.w3.org/TR/REC-xml.mdl) 擴充 HTML 以顯示向量圖形資訊。 [VML 檔物件模型 (DOM) 會定義用於操作檔元素的程式設計介面。 這可讓使用者透過平臺和語言中性介面，以動態方式建立和修改向量圖形。 VML DOM 符合 [檔物件模型](https://www.w3.org/TR/REC-DOM-Level-1/) 規格。

VML 使用 [Shape](#shape-element) 元素作為向量圖形影像的基本建築物區塊。 建立圖形之後，您可以透過屬性或附加的子項目來修改圖形。 例如，若要變更圖形的色彩，請將色彩值指派給 **FillColor** 屬性。


```HTML
myshape.fillcolor = "red"
```



圖形的數個屬性也是子 [元素](/windows) ，而且有自己的屬性，包括下列各項：

-   [背景](#background-element)
-   [擠壓](#extrusion-element)
-   [填滿](#fill-element)
-   [群組](#group-element)
-   [Imagedata](#imagedata-element)
-   [路徑](#path-element)
-   [Shadow](#shadow-element)
-   [斜](#skew-element)
-   [中風](#stroke-element)
-   [TextPath](#textpath-element)

VML OM 會使用數個 [資料類型](/windows) 來定義參數。 前面加上 "Vg" 的資料類型是列舉，而前面加上 "IVg" 的資料類型是物件。 按一下這裡以取得清單。 次要資料類型會以特定參數列出。

## <a name="example"></a>範例

下列 VBScript 程式碼顯示如何建立簡單的圖形：


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



在上述範例中，會使用檔物件模型方法 **CreateElement** 來建立圖形。 圖形是一個 VML 預先定義的矩形圖形。 雖然物件存在，但是在附加至檔之前，它不能是檔的一部分。 使用 **AppendChild** 方法，矩形就會成為名為 MyDiv 的 **DIV** 元素的子系。 有幾個最小樣式屬性 (**位置**、 **寬度**、 **高度**、 **Top**、 **左方**) 設定成提供圖形特定的大小。 最後，會使用 **FillColor** 屬性來指派色彩。 請注意，您可以使用任何可搭配檔物件模型介面使用的指令碼語言或任何語言。

## <a name="setting-up-vml"></a>設定 VML

一個 VML 的執行是透過 Microsoft Internet Explorer 5.0 或更高版本。 若要在網頁中正確設定轉譯物件，必須進行下列新增專案：

1.  架構必須在初始 HTML 標籤中設定，如下所示 &lt; &gt; ：
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  轉譯行為必須是檔樣式的一部分：
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

以下顯示針對顯示動態建立圖形的 VML 正確設定的 HTML 網頁範例。


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



請注意，在 Beta 版中，需要 ActiveX 的物件標記和不同的行為樣式。

## <a name="vml-om-reference"></a>VML OM 參考

這個參考定義了 VML 的物件模型所使用的 [Shape](#shape-element) 元素、子 [元素](/windows)和 [資料類型](/windows) 。

### <a name="shape-element"></a>Shape 元素

圖形是 Vector Markup Language (VML) 所定義之圖形影像的建立區塊。 圖形是最上層元素，而數個子項目可協助定義每個圖形的本質。

VML 提供預先定義的圖形：

**圖形屬性**

-   **Arc**
-   **曲線**
-   **線條**
-   **折線**
-   **Rect**
-   **RoundRect**



|   Subelement           |    描述                                                                                                                                                                                                                                                                                                                                                                              |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 形容詞          | [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md)。 以逗號分隔的數位清單，這些是用來定義圖形路徑之指南公式的參數。 可能會省略值以允許使用預設值。 最多可以有8個調整值。                                                                                                   |
| Alt          | 字串。 與圖形相關聯的替代文字。 用於非圖形化流覽。                                                                                                                                                                                                                                                                                                 |
| Button       | [VgTriState](msdn-online-vml-vgtristate.md)。 按一下時，會顯示按鈕的行為。                                                                                                                                                                                                                                                                                                 |
| BWMode       | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。 決定在應用程式中，或列印到黑白印表機時，圖形會以黑白方式呈現。 值包括： **Color**、 **Auto**、 **灰階**、 **LightGrayScale**、 **InverseGray**、 **GrayOutline**、 **BlackTextAndLines**、 **systeminformation.highcontrast**、 **黑色**、 **白色**、 **Undrawn**。 預設值： **Auto**。 |
| BWNormal     | VgBlackWhiteMode. 當 BWMode 為 Auto 時，會參考此屬性以瞭解如何以一般黑色和白色呈現圖形。 值包括： **Color**、 **Auto**、 **灰階**、 **LightGrayScale**、 **InverseGray**、 **GrayOutline**、 **BlackTextAndLines**、 **systeminformation.highcontrast**、 **黑色**、 **白色**、 **Undrawn**。 預設值： **Auto**。                                                |
| BWPure       | VgBlackWhiteMode. 當 BWMode 為 Auto 時，會參考此屬性以瞭解如何以純 B/W 呈現圖形。 值包括： **Color**、 **Auto**、 **灰階**、 **LightGrayScale**、 **InverseGray**、 **GrayOutline**、 **BlackTextAndLines**、 **systeminformation.highcontrast**、 **黑色**、 **白色**、 **Undrawn**。 預設值： **Auto**。                                                              |
| ChildShapes  | IVgGroupShapes. 此群組中其他圖形的集合。 此集合支援標準長度和專案方法。                                                                                                                                                                                                                                                       |
| Chromakey    | [IVgColor](msdn-online-vml-ivgcolor.md)。 將會是透明的色彩值，並顯示圖形背後的任何事物。                                                                                                                                                                                                                                                             |
| Control1     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。 曲線的控制點。                                                                                                                                                                                                                                                                                                  |
| Control2     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。 曲線的控制點。                                                                                                                                                                                                                                                                                                  |
| CoordOrigin  | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md) 容器矩形左上角的座標。 範圍從0到無限大。                                                                                                                                                                                                                               |
| CoordSize    | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。 此圖形之參考矩形內的座標空間的寬度和高度。 如果未指定，則與矩形的寬度和高度相同。 範圍從0到無限大。 預設值： "1000，1000"。                                                                                               |
| EndAngle     | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md)。 圖形的結束角度。                                                                                                                                                                                                                                                                                          |
| 擠壓    | IVgExtrusion. 指定此圖形的延伸物件值。 如需詳細資訊，請參閱「 [延伸](msdn-online-vml-extrusion-element.md) 」元素。                                                                                                                                                                                                                               |
| 填滿         | VgFillFormat. 指定此圖形的填滿值。 如需詳細資訊，請參閱 [Fill](msdn-online-vml-fill-element.md) 元素。                                                                                                                                                                                                                                                |
| FillColor    | [IVgColor](msdn-online-vml-ivgcolor.md)。 要用來填滿此圖形路徑之筆刷的主要色彩。                                                                                                                                                                                                                                                                  |
| 已       | [VgTriState](msdn-online-vml-vgtristate.md)。 若為 True，則會填滿定義圖形的路徑。 根據預設，除非有指定更複雜填滿屬性的 Fill 子項目，否則它將會以純色填滿。 如果為 False，則填滿是透明的。                                                                                                           |
| 翻轉         | VgFlipOrientation. 值為： X Y XY YX                                                                                                                                                                                                                                                                                                                                         |
| ForceDash    | [VgTriState](msdn-online-vml-vgtristate.md)。 指出當圖形沒有線條且沒有填滿時，應該呈現虛線外框。 這種行為通常適用于在編輯應用程式中顯示隱藏式圖形，因此可以在影像對應中加以選取和操作。                                                                 |
| 公式     | IVgFormulas. 定義圖形的公式陣列。                                                                                                                                                                                                                                                                                                                          |
| 寄件者         | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。 行的起點。                                                                                                                                                                                                                                                                                                   |
| Href         | [字串](#data-types-used-in-the-vml-object-model)。 如果按一下此圖形，要跳到的 URL。                                                                                                                                                                                                                                                                                 |
| ImageData    | IVgImageData. 影像資訊（如果圖形是圖片的話）。 如需詳細資訊，請參閱 ImageData 元素。                                                                                                                                                                                                                                                                       |
| OnEd         | [VgTriState](msdn-online-vml-vgtristate.md)。 隱藏左上角和右下方以外的所有控制碼，如同直線線段的控制碼一樣。                                                                                                                                                                                                                             |
| 不透明度      | [VgFraction](msdn-online-vml-vgfraction-data-type.md)。 整個圖形的不透明度。 介於0.0 到1.0 之間的數位。                                                                                                                                                                                                                                                           |
| 路徑         | IVgPath. 字串，包含定義路徑的命令。                                                                                                                                                                                                                                                                                                                  |
| 點       | [IVgPoints](msdn-online-vml-ivgpoints-data-type.md)。 定義圖形的點集合。                                                                                                                                                                                                                                                                                   |
| 列印        | [VgTriState](msdn-online-vml-vgtristate.md)。 若為 True，表示要列印此圖形。                                                                                                                                                                                                                                                                                        |
| 旋轉     | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md)。 設定圖形的旋轉。 值會傳播至圖形樣式。                                                                                                                                                                                                                                              |
| 調整        | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。 圖形的縮放比例。                                                                                                                                                                                                                                                                                                           |
| 陰影       | IVgShadow. 指定此圖形的陰影。 如需詳細資料，請參閱 [Shadow](msdn-online-vml-shadow-element.md) 元素。                                                                                                                                                                                                                                                        |
| Spt          | 保留的。                                                                                                                                                                                                                                                                                                                                                                        |
| >startangle   | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md)。 圖形的開始角度。                                                                                                                                                                                                                                                                                        |
| 筆勢       | VgStrokeFormat. 如需詳細資料，請參閱 Stroke 元素。                                                                                                                                                                                                                                                                                                                                  |
| StrokeColor  | [IVgColor](msdn-online-vml-ivgcolor.md)。 用來將此圖形的路徑進行筆劃之筆刷的主要色彩。                                                                                                                                                                                                                                                                |
| 撫摸      | [VgTriState](msdn-online-vml-vgtristate.md)。 若為 True，則會將定義圖形的路徑進行筆劃。                                                                                                                                                                                                                                                                              |
| StrokeWeight | [VGLength](msdn-online-vml-vglength.md)。 用來對路徑進行筆劃的筆刷寬度。 介於0與1584之間的範圍。                                                                                                                                                                                                                                                           |
| TextPath     | IVgTextPath. 指定圖形的 TextPath 物件。 如需詳細資訊，請參閱 [TextPath](msdn-online-vml-textpath-element.md) 元素。                                                                                                                                                                                                                                  |
| 收件者           | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。 行的結束點。                                                                                                                                                                                                                                                                                                        |
| 類型         | 字串。 圖形類型。                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a>Shape 元素的子項目

下列子項目是 VML 物件模型的一部分。

-   [背景](#background-element)
-   [擠壓](#extrusion-element)
-   [填滿](#fill-element)
-   [群組](#group-element)
-   [Imagedata](#imagedata-element)
-   [路徑](#path-element)
-   [Shadow](#shadow-element)
-   [斜](#skew-element)
-   [中風](#stroke-element)
-   [TextPath](#textpath-element)

### <a name="background-element"></a>Background 元素

描述使用 VML 填滿的頁面背景填滿。


|   屬性        |   說明                                                                                                                                                                                      |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BWMode    | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。 決定圖形在應用程式中的黑白外觀或列印時的呈現方式。                                     |
| BWNormal  | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。 當 BWMode 為 Auto 時，會參考此屬性以瞭解如何以一般黑色和白色呈現圖形。                        |
| BWPure    | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。 當 BWMode 為 Auto 時，會參考此屬性以瞭解如何以純黑色和白色呈現圖形。                          |
| 填滿      | VgFillFormat. 指定此圖形的填滿。 如需詳細資訊，請參閱 [Fill](msdn-online-vml-fill-element.md) 元素。                                                             |
| FillColor | [IVgColor](msdn-online-vml-ivgcolor.md)。 要用來填滿此圖形路徑之筆刷的主要色彩。 Fill 元素中的色彩值重複。 預設為白色。 |



 

### <a name="extrusion-element"></a>延伸元素

描述圖形的立體延伸。

**屬性**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>AutoRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。 若為 True，則3D 物件群組的旋轉中心 (事實上，群組中只有一個物件) 會自動判斷為群組的中心;否則，它是由 RotationCenter 參數決定，這是圖形的一部分，0、0、0是中心。</td>
</tr>
<tr class="even">
<td>BackDepth</td>
<td><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>。 反向拉伸的數量。 範圍從0到32767。</td>
</tr>
<tr class="odd">
<td>亮度</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。 場景的整體亮度。 預設值為 &quot; 20000 &quot; 。</td>
</tr>
<tr class="even">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。 拉伸的色彩。 只有在 ColorMode 為 Custom 時才會使用。 否則，會自動將 [拉伸效果] 色彩設定為與 FillColor 相同。</td>
</tr>
<tr class="odd">
<td>ColorMode</td>
<td>Vg3DColorMode. 值為：
<ul>
<li>Auto (預設值)</li>
<li>自訂</li>
</ul></td>
</tr>
<tr class="even">
<td>Diffusity</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。 要擴散的事件比率反映燈光。 小於1.0 的值是正常的，但大於1的值可能會產生有趣的效果。</td>
</tr>
<tr class="odd">
<td>Edge</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>。 設定模擬圓角斜面邊緣的大小。 浮點數中的範圍介於0到32767之間。 預設值為 &quot; 1pt &quot; 。</td>
</tr>
<tr class="even">
<td>Facet</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。 設定場景的 facet。 預設值為 &quot; 30000 &quot; 。</td>
</tr>
<tr class="odd">
<td>ForeDepth</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>。 向前延伸的數量。 範圍從0到32767。</td>
</tr>
<tr class="even">
<td>LightFace</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。 Determimes 物件的正面臉部是否會回應3-d 照明的變更，例如，當物件旋轉時。</td>
</tr>
<tr class="odd">
<td>LightHarsh</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。 主要光源的光源。 預設值是 False。</td>
</tr>
<tr class="even">
<td>LightHarsh2</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。 次要燈光來源的粗糙光源。 預設值是 False。</td>
</tr>
<tr class="odd">
<td>LightLevel</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>。 主要燈光來源的濃度。 預設值為 &quot; 38000 &quot; 。</td>
</tr>
<tr class="even">
<td>LightLevel2</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>。 次要燈光來源的濃度。 預設值為 &quot; 38000 &quot; 。</td>
</tr>
<tr class="odd">
<td>LightPosition</td>
<td>Vector3D. 主要光源來源的位置。 預設值為 &quot; 50000、0、10000 &quot; 。</td>
</tr>
<tr class="even">
<td>LightPosition2</td>
<td>Vector3D. 次要燈光來源的位置。 預設值為 &quot; -50000、0、10000 &quot; 。</td>
</tr>
<tr class="odd">
<td>LockRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。 &quot;Lockrotationcenter &quot; 表示群組的旋轉會依照頁面上 y 軸的旋轉角度 [1] 角度定義，後面接著 X 軸的旋轉角度 [0] 角度。 當 LockRotationCenter 為 False 時，就會根據方向定義的向量，將旋轉定義為面向角度。 因此，例如，lockrotationcenter = false orientationangle = 45 方向 = (0，1，0) 相當於 lockrotationcenter = true rotationangle = (0，45) 。</td>
</tr>
<tr class="even">
<td>金屬</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。 使反射反映的光線成為材質色彩，而不是光線來源色彩，讓物件看起來更材質。</td>
</tr>
<tr class="odd">
<td>開啟</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。 開啟和關閉延伸效果的顯示。</td>
</tr>
<tr class="even">
<td>Orientation</td>
<td>Vector3D. 攝影機的方向。</td>
</tr>
<tr class="odd">
<td>OrientationAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>。 攝影機方向與 xy 平面之間的角度。</td>
</tr>
<tr class="even">
<td>飛機</td>
<td>Vg3DExtrudePlane. 允許從平面與螢幕平面垂直的拉伸。 需要以繪圖單位（而非 emus）指定 ForeDepth 和 BackDepth。 值為：
<ul>
<li>XY</li>
<li>ZX</li>
<li>YZ</li>
</ul></td>
</tr>
<tr class="odd">
<td>轉譯</td>
<td>Vg3DRenderMode. 值為：
<ul>
<li>Solid (預設值)</li>
<li>著色</li>
<li>BoundingCube</li>
</ul></td>
</tr>
<tr class="even">
<td>RotationAngle</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。 System.windows.media.skewtransform.anglex、System.windows.media.skewtransform.angley 或 AngleZ 是由 ShapeRotation 屬性所控制。</td>
</tr>
<tr class="odd">
<td>RotationCenter</td>
<td>Vector3D. 旋轉的中心。</td>
</tr>
<tr class="even">
<td>增</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。 決定集中或分佈反射反映的方式。 高值會是8到10，而且近似于鏡像，而較低的值會是2至3，而且大約 sequined 服裝。 建議使用3到7之間的值。 較高的值會反映出燈燈的來源。</td>
</tr>
<tr class="odd">
<td>SkewAmt</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>。 如果 Type 是 Parallel，屬性會決定扭曲量。 範圍從0到100。</td>
</tr>
<tr class="even">
<td>SkewAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>。 如果 Type 是 Parallel，屬性會決定扭曲的程度。 預設值為 &quot; -45 &quot; 。</td>
</tr>
<tr class="odd">
<td>Specularity</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>。 要反射的事件比率反映燈光。 小於1.0 的值是正常的，但大於1的值可能會產生有趣的效果。</td>
</tr>
<tr class="even">
<td>類型</td>
<td>VgExtrusionType. 值為：
<ul>
<li>平行 (預設) </li>
<li>檢視方塊</li>
</ul></td>
</tr>
<tr class="odd">
<td>觀點</td>
<td>Vector3D. 從中查看場景的位置。</td>
</tr>
<tr class="even">
<td>ViewpointOrigin</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。 可以有從0.5 到-0.5 的值，以定點陣圖形周框方塊內的觀點原點。</td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a>Fill 元素

說明如何針對填滿較純色的填滿路徑。

**屬性**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>AlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。 將影像與圖形對齊。 如果為 False，則會將影像與視窗對齊。</td>
</tr>
<tr class="even">
<td>角度</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>。 漸層沿著的角度。 0度是沿著水準軸從左至右。</td>
</tr>
<tr class="odd">
<td>層面</td>
<td><strong>VgAspectType</strong>。 ImageSize 屬性將會調整，以保留影像的外觀。 數值包括：
<table>
<thead>
<tr class="header">
<th>值</th>
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>忽略</td>
<td>略過外觀問題。</td>
</tr>
<tr class="even">
<td>至少</td>
<td>映射大小至少與影像大小一樣大。</td>
</tr>
<tr class="odd">
<td>有</td>
<td>影像的大小不會大於影像大小。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> 主要填滿色彩。 與 shape 中的 FillColor 屬性相同。</td>
</tr>
<tr class="odd">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。 當影像類型為模式或漸層填滿時，填滿的次要色彩。</td>
</tr>
<tr class="even">
<td>色彩</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>。 漸層中的中繼色彩及其沿著漸層的相對位置，例如 &quot; 30% 紅色、70% 藍色、90% 綠色 &quot; 。 圖形) 中的主要色彩 (色彩屬性為0%，次要色彩 (Color2 屬性) 為100%。</td>
</tr>
<tr class="odd">
<td>焦點</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>。 線性漸層填滿的焦點。 值從-100 到 + 100。</td>
</tr>
<tr class="even">
<td>FocusPosition</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。 放射狀漸層的最內部矩形位置。 向量是圖形寬度和高度 (0.0-1.0) 的分數。</td>
</tr>
<tr class="odd">
<td>FocusSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> 放射狀漸層的最內部矩形大小。 向量是圖形寬度和高度 (0.0 至 1.0) 的分數。</td>
</tr>
<tr class="even">
<td>方法</td>
<td>VgSigmaType. 數值包括：
<ul>
<li>無</li>
<li>線性</li>
<li>Sigma</li>
<li>任意</li>
</ul>
<p>預設值為 Sigma。</p></td>
</tr>
<tr class="odd">
<td>開啟</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。 開啟填滿顯示。 與 shape 中的 Fill 屬性相同。</td>
</tr>
<tr class="even">
<td>不透明度</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>。 填滿的不透明度。</td>
</tr>
<tr class="odd">
<td>Opacity2</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>。 漸層的次要不透明度。</td>
</tr>
<tr class="even">
<td>來源</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。 視為影像來源之影像左上角的相對點。 預設值是影像的中心。 向量是從0.0 到 1.0) 影像寬度和高度 (的分數。</td>
</tr>
<tr class="odd">
<td>位置</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。 指向圖形的參考矩形，以放置影像的來源。 預設值為容器矩形的中心。 向量是影像寬度和高度 (0.0-1.0) 的分數。</td>
</tr>
<tr class="even">
<td>大小</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。 影像的大小。 預設值是影像的圖元大小。 可以用絕對座標或百分比來指定。</td>
</tr>
<tr class="odd">
<td>來源</td>
<td><a href="#data-types-used-in-the-vml-object-model">字串</a>。 影像的 URL，以載入影像和模式填滿。 這個屬性必須一律存在，並指向有效的影像資料，圖片才會出現。</td>
</tr>
<tr class="even">
<td>類型</td>
<td>VgFillType. 可以是下列其中一個類型：
<ul>
<li>背景</li>
<li>Frame</li>
<li>漸層</li>
<li>GradientCenter</li>
<li>GradientRadial</li>
<li>GradientTitle</li>
<li>GradientUnscaled</li>
<li>模式</li>
<li>實線</li>
<li>磚</li>
</ul>
磚、模式和框架都需要提供影像屬性。 漸層和 GradientRadial 需要提供漸層屬性。</td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a>Group 元素

群組是個別圖形的集合，可作為單位來定位和轉換。



|   屬性        |   描述                                                                                                                                                                                      |
|--------|----------------------------------------------------------------------------------------------|
| Item   | [IVgShape](#data-types-used-in-the-vml-object-model)。 圖形陣列中的指定專案。 |
| 長度 | [Integer](#data-types-used-in-the-vml-object-model) (整數)。 此群組中的圖形數目。         |



 

### <a name="imagedata-element"></a>Imagedata 元素

描述要在圖形之上呈現的圖片。



|   屬性        |   說明                                                                                                                                                                                      |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 雙層     | [VgTriState](msdn-online-vml-vgtristate.md)。 只以兩種色彩顯示圖片 (通常是黑色和白色) 。                                                                                                                                                                                                                                                     |
| BlackLevel  | [VgFraction](msdn-online-vml-vgfraction-data-type.md)。 可進行調整以設定層級，讓黑色顯示為 true 黑色，而其他所有色彩則會顯示為黑色以上的陰影。                                                                                                                                                                        |
| Chromakey   | [IVgColor](msdn-online-vml-ivgcolor.md)。 圖片的透明色彩。                                                                                                                                                                                                                                                                                         |
| CropBottom  | [VgNumber](#data-types-used-in-the-vml-object-model)。 從圖片底部裁剪距離，以圖片大小的百分比表示。                                                                                                                                                                                                                           |
| CropLeft    | [VgNumber](#data-types-used-in-the-vml-object-model)。 從圖片的左邊緣裁剪距離，以圖片大小的比例表示 (從0.0 到 1.0) 。 不過，支援「退出裁剪」，因此支援小於0且大於1的值。例如，-5、20會將圖片大小25X 在圖片的一端，以4/5 來裁剪界限。 |
| CropRight   | [VgNumber](#data-types-used-in-the-vml-object-model)。 從圖片右邊裁剪的距離，以圖片大小的百分比表示。                                                                                                                                                                                                                            |
| CropTop     | [VgNumber](#data-types-used-in-the-vml-object-model)。 從圖片頂端裁剪的距離，以圖片大小的百分比表示。                                                                                                                                                                                                                              |
| EmbossColor | [IVgColor](msdn-online-vml-ivgcolor.md)。 這會設定為陰影色彩的百分比，以建立浮凸圖片效果。                                                                                                                                                                                                                                 |
| 獲得        | [VgPositiveNumber](#data-types-used-in-the-vml-object-model)。 調整所有色彩的濃度。 基本上會設定白色的明暗程度。 範圍從0到32767。                                                                                                                                                                                           |
| 色差補正       | [VgFraction](msdn-online-vml-vgfraction-data-type.md)。 Gamma 修正。 增加它可讓影像更對比。                                                                                                                                                                                                                                           |
| GrayScale   | [VgTriState](msdn-online-vml-vgtristate.md)。 顯示灰階色彩的圖片。                                                                                                                                                                                                                                                                              |
| 來源         | [字串](#data-types-used-in-the-vml-object-model)。 影像的 URL，以載入影像和模式填滿。 這個屬性必須一律存在，並指向有效的影像資料，圖片才會出現。                                                                                                                                                           |



 

### <a name="path-element"></a>Path 元素

使用包含一組豐富的「畫筆移動」命令的字串，定義組成圖形的路徑。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>豪華 轎車</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>。 定義圖案伸展的點;例如，針對 giraffe 圖形，limo 點會在頸部上，因此當調整形狀大小時，頸部將會延展，而圖形的其餘部分將會維持其尺寸。</td>
</tr>
<tr class="even">
<td>TextBoxRect</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>。 陣列，包含定義文字應該移至何處的矩形。</td>
</tr>
<tr class="odd">
<td>V</td>
<td><a href="#data-types-used-in-the-vml-object-model">字串</a>。 符合路徑標記上的 v 屬性。 請注意，路徑可能對應至 Path 屬性或元素。</td>
</tr>
<tr class="even">
<td>值</td>
<td><a href="#data-types-used-in-the-vml-object-model">字串</a>。 定義路徑的命令文字表示。 X 或 y 座標值可以是表單中公式的參考 &quot; @# &quot; ，其中 # 是公式的序數，例如， &quot; @2 &quot; 。 這個屬性字串是由一組豐富的命令所組成，包括下列各項： <br/> 
<table>
<thead>
<tr class="header">
<th>命令</th>
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ae (angleellipseto) </td>
<td><strong>中央</strong> (x、y) <strong>大小</strong> (w、h) <strong>開始角度</strong>、 <strong>終點</strong><br/> 繪製橢圓形的線段。 從目前的點將直線繪製到區段的起點。<br/></td>
</tr>
<tr class="even">
<td>al (angleelipse) </td>
<td>與 ae 相同，不同之處在于區段的起點有隱含的 m。</td>
</tr>
<tr class="odd">
<td>ar (arc) </td>
<td>與相同。 不過，新的子路徑會由隱含的 m 啟動至弧線的起點。</td>
</tr>
<tr class="even">
<td>在 (arcto) </td>
<td><strong>左</strong>、 <strong>上</strong>、 <strong>右</strong>、 <strong>下</strong>、 <strong>開始</strong> (x、y) <strong>end</strong> (x，y)  <br/> 前四個值會定義橢圓形的周框方塊。 最後四個定義兩個放射狀向量。 繪製的橢圓形區段會從開始半徑向量所定義的角度開始，並以結束向量所定義的角度結束。 從目前的點到弧形開頭繪製直線。弧線一律會以逆時針方向繪製。 <br/></td>
</tr>
<tr class="odd">
<td>c (curveto) </td>
<td><strong>control1</strong> (x，y) <strong>control2</strong> (x，y) <strong>至</strong> (x，y)  <br/> 從目前的點繪製三次方貝茲曲線到最後兩個參數所指定的座標，也就是前四個參數所指定的控制點。 目前的點會成為貝塞爾的端點。<br/></td>
</tr>
<tr class="even">
<td>e (結束) </td>
<td>結束目前的子路徑集。 會使用 eofill 填滿一組指定的子路徑，並以 end) 分隔 (。 後續的子路徑集合會獨立填入，並在現有的子路徑上重迭。</td>
</tr>
<tr class="odd">
<td>l (lineto) </td>
<td>x、y<br/> 從目前的點將直線繪製到指定的 x，y 座標，以成為新的目前點。 您可以指定其他座標配對來形成聚合線條，例如， &quot; l 10、13、45、27、89、-12 &quot; 。<br/></td>
</tr>
<tr class="even">
<td>m (moveto) </td>
<td>x、y<br/> 在指定的 x，y 座標開始新的子路徑。<br/></td>
</tr>
<tr class="odd">
<td>nofill) 的 nf-e (</td>
<td>將不會填入以 end) 分隔 (目前的子路徑集合。</td>
</tr>
<tr class="even">
<td>ns (nostroke) </td>
<td>將不會對目前的子路徑組合 (以 end) 分隔。</td>
</tr>
<tr class="odd">
<td>qb (quadraticbezier) </td>
<td> (<strong>controlpoint</strong> (x、y) ) *、<strong>end</strong> (x、y)  <br/> 藉由控制點和端點，定義一或多個二次方貝茲曲線。 中間的 (曲線) 點是透過類似 TrueType 字型的連續控制點來取得。 子路徑不需要是開始的，在此情況下，會關閉子路徑，而最後一個點則會定義起始點。<br/></td>
</tr>
<tr class="even">
<td>qx (ellipticalquadrantx) </td>
<td><strong>end</strong> (x，y)  <br/> 從目前的點到指定端點繪製的四分之一橢圓形。 橢圓區段一開始會與 X 軸平行的直線相切;亦即，區段開始水準。<br/></td>
</tr>
<tr class="odd">
<td>qy (ellipticalquadranty) </td>
<td><strong>end</strong> (x，y)  <br/> 與 qx 相同，不同之處在于橢圓區段一開始會與 y 軸平行的直線相切;亦即，區段開始垂直。<br/></td>
</tr>
<tr class="even">
<td>r (rlineto) </td>
<td>x、y <br/> 從目前的點繪製一條直線到相對座標 (cpx + x，cpy + y) 。 如果指定了其他座標組，每個新點都會相對於最後一個點來計算。<br/></td>
</tr>
<tr class="odd">
<td>t (rmoveto) </td>
<td>x、y<br/> 在相對座標開始新的子路徑 ( cpx + x，cpy + y) 其中 cpx，cpy 是目前的位置。 <br/></td>
</tr>
<tr class="even">
<td>v (curveto) </td>
<td><strong>control1</strong> (x，y) <strong>control2</strong> (x，y) <strong>至</strong> (x，y)  <br/> 使用相對於目前點之指定座標的三次方貝茲曲線。 所有點都是相對於相同的起點來計算。<br/></td>
</tr>
<tr class="odd">
<td>wa (clockwisearcto) </td>
<td>與相同，但弧線以順時針方向繪製。</td>
</tr>
<tr class="even">
<td>wr (clockwisearc) </td>
<td>與 ar 相同，但以順時針方向繪製。</td>
</tr>
<tr class="odd">
<td>x (關閉) </td>
<td>從目前點到原始的 moveto 點繪製一條直線，以關閉目前的子路徑。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a>Shadow 元素

描述圖形上的陰影效果。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。 主要陰影的色彩。 預設值為 RGB (128128128) </td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。 第二個陰影的色彩，或反白顯示于浮凸或陰文的陰影。 預設值為 RGB (203203203) 。</td>
</tr>
<tr class="odd">
<td>矩陣</td>
<td><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>。 &quot;Sxx、sxy、syx、syy、px、.py &quot; [s = scale、p = 透視圖] 格式的透視圖轉換矩陣。 專案指定陰影應該如何隨著圖形而調整，而 p 專案則指定陰影應該如何與圖形相對應的扭曲。 例如，下列矩陣會以2的因數來調整圖形的大小，並以4的因數將其傾斜： <br/> &quot;2、2、2、2、4、4&quot;<br/> 只有當陰影的類型設定為 [透視圖] 時，才會使用這個矩陣。<br/></td>
</tr>
<tr class="even">
<td>遮蔽</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。 如果圖形沒有填滿，就可以看到陰影。 預設值是 False。</td>
</tr>
<tr class="odd">
<td>Offset</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>。 X 的數量，y 位移自圖形的位置。 預設值為 &quot; 2pt、2pt &quot; 。</td>
</tr>
<tr class="even">
<td>Offset2</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。 X 的數量，y 第二個從圖形的位置位移。 值可以是絕對測量值，或是 shape (-0.5 到 + 0.5) 的小數值。</td>
</tr>
<tr class="odd">
<td>開啟</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。 開啟和關閉陰影的顯示。</td>
</tr>
<tr class="even">
<td>不透明度</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>。 陰影效果的不透明度。</td>
</tr>
<tr class="odd">
<td>來源</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> 從-0.5 到 + 0.5 之圖形的一對小數值。</td>
</tr>
<tr class="even">
<td>類型</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>。 值為：
<ul>
<li>單一 (預設) </li>
<li>Double</li>
<li>檢視方塊</li>
<li>ShapeRelative</li>
<li>DrawingRelative</li>
<li>Emboss</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a>扭曲元素

描述圖形上的觀點扭曲效果。 扭曲會套用至向量圖形資料，而不會套用至影像資料。



|   屬性        |   說明                                                                                                                                                                                      |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 矩陣 | [IVgSkewMatrix](#data-types-used-in-the-vml-object-model)。 以 "sxx，sxy，syx，syy，px，.py" \[ s = scale，p = 透視圖形式的觀點轉換矩陣 \] 。 如果位移的單位為絕對單位，則為 px，.py 則為 emu ^-1 個單位;否則是圖形大小的反向分數。 |
| Offset | [IvgSkewOffset](#data-types-used-in-the-vml-object-model)。 X 的數量，y 位移自圖形的位置。 預設值為 "2pt，2pt"。                                                                                                                                                   |
| 開啟     | [VgTriState](msdn-online-vml-vgtristate.md)。 開啟或關閉扭曲的顯示。                                                                                                                                                                                             |
| 來源 | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md)。 從-0.5 到 + 0.5 之圖形的一對小數值。                                                                                                                                                                     |



 

### <a name="stroke-element"></a>Stroke 元素

描述如何在需要純色的實線之外繪製路徑。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Color</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。 線條的色彩。 與 Shape 中的 StrokeColor 屬性相同，但會覆寫它。</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>。 次要色彩。 當 FillType 為模式時使用。</td>
</tr>
<tr class="odd">
<td>DashStyle</td>
<td><strong>VgLineDashStyle</strong>。 虛線樣式格式。 可能是特定的值，或是具有使用者定義虛線模式的數位序列。 值為：
<ul>
<li>Solid (預設值)</li>
<li>ShortDash</li>
<li>ShortDot</li>
<li>ShortDashDot</li>
<li>ShortDashDotDot</li>
<li>點</li>
<li>虛線</li>
<li>DashDot</li>
<li>LongDash</li>
<li>LongDashDot</li>
<li>LongDashDotDot</li>
</ul></td>
</tr>
<tr class="even">
<td>EndArrow</td>
<td><strong>VgArrowheadStyle</strong>。 行尾的箭頭。 值為：
<ul>
<li>[無] (預設值)</li>
<li>封鎖</li>
<li>傳統</li>
<li>菱形</li>
<li>橢圓形</li>
<li>開啟</li>
<li>&gt; 形箭號</li>
<li>DoubleChevron</li>
</ul></td>
</tr>
<tr class="odd">
<td>EndArrowLength</td>
<td><strong>VgArrowHeadLength</strong>。 線條結尾的箭頭長度。 值為：
<ul>
<li>Short</li>
<li>中 (預設)</li>
<li>long</li>
</ul></td>
</tr>
<tr class="even">
<td>EndArrowWidth</td>
<td><strong>VgArrowheadWidth</strong>。 線條結尾的箭頭寬度。 值為：
<ul>
<li>狹窄</li>
<li>中 (預設)</li>
<li>寬</li>
</ul></td>
</tr>
<tr class="odd">
<td>EndCap</td>
<td><strong>VgLineEndCapStyle</strong>。 值為：
<ul>
<li>一般</li>
<li>Square</li>
<li>Round</li>
</ul></td>
</tr>
<tr class="even">
<td>FillType</td>
<td><strong>VgLineFillType</strong>。 值為：
<ul>
<li>Solid (預設值)</li>
<li>磚</li>
<li>模式</li>
<li>Frame</li>
</ul></td>
</tr>
<tr class="odd">
<td>ImageAlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。 將影像與圖形對齊。 如果為 False，則會將影像與視窗對齊。</td>
</tr>
<tr class="even">
<td>ImageAspect</td>
<td><strong>VgAspectType</strong>。 ImageSize 屬性將會調整，以保留影像的外觀。 數值包括：
<table>
<thead>
<tr class="header">
<th>值</th>
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>忽略</td>
<td>略過外觀問題。</td>
</tr>
<tr class="even">
<td>至少</td>
<td>映射大小至少與影像大小一樣大。</td>
</tr>
<tr class="odd">
<td>有</td>
<td>影像的大小不會大於影像大小。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>ImageSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>。 用來形成筆刷的影像大小。 預設值是影像的大小。</td>
</tr>
<tr class="even">
<td>JoinStyle</td>
<td><strong>VgLineJoinStyle</strong>。 值為：
<ul>
<li>舍入 (圓角接合) </li>
<li>斜面 (斜角接點) </li>
<li>斜接 (斜接接點) </li>
</ul></td>
</tr>
<tr class="odd">
<td>線條樣式</td>
<td><strong>VgLineStyle</strong>。 值為：
<ul>
<li>Single</li>
<li>ThinThin (1:1:1) </li>
<li>ThinThick (1:1:2) </li>
<li>ThickThin (2:1:1) </li>
<li>ThickBetweenThin (1:1:2:1:1) </li>
</ul></td>
</tr>
<tr class="even">
<td>MiterLimit</td>
<td><a href="msdn-online-vml-vglength.md">長度</a>。 聯合的內部點和外部點之間的最大距離。 此數位是線條粗細的倍數。 範圍從0到32767。</td>
</tr>
<tr class="odd">
<td>開啟</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>。 開啟和關閉行的顯示。 與 Shape 中的 Stroke 屬性相同，但會覆寫它。</td>
</tr>
<tr class="even">
<td>不透明度</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>。 筆劃的不透明度。</td>
</tr>
<tr class="odd">
<td>來源</td>
<td>字串。 影像的 URL，以載入影像和模式填滿。 這個屬性必須一律存在，並指向有效的影像資料，圖片才會出現。</td>
</tr>
<tr class="even">
<td>StartArrow</td>
<td><strong>VgArrowheadStyle</strong>。 直線開頭的箭頭。 值為：
<ul>
<li>[無] (預設值)</li>
<li>封鎖</li>
<li>傳統</li>
<li>菱形</li>
<li>橢圓形</li>
<li>開啟</li>
<li>&gt; 形箭號</li>
<li>DoubleChevron</li>
</ul></td>
</tr>
<tr class="odd">
<td>StartArrowLength</td>
<td>VgArrowHeadLength. 直線開頭的箭頭長度。 值為：
<ul>
<li>Short</li>
<li>中 (預設)</li>
<li>long</li>
</ul></td>
</tr>
<tr class="even">
<td>StartArrowWidth</td>
<td>VgArrowheadWidth. 線條開頭的箭頭寬度。 值為：
<ul>
<li>窄中型 (預設) 寬</li>
</ul></td>
</tr>
<tr class="odd">
<td>Weight</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>。 線條的寬度。 範圍從0到1584。
<div class="alert">
<blockquote>
[!Note]<br />
DashStyle 屬性可讓使用者指定自訂定義的虛線模式。 這是使用一連串的數位來完成。 虛線樣式是以虛線的長度來定義， (筆觸的繪製部分) 和虛線之間的空間長度。 長度是相對於線條寬度;長度為 &quot; 1 &quot; 等於線條寬度。 EndCap 樣式會套用至每個虛線，而箭號樣式則不適用。 字串會先定義虛線的長度，然後再定義空間的長度。 這可能會重複形成複雜的虛線樣式。 字串應該一律包含成對的數位;如果它包含奇數數目的數位，則可能會忽略最後一個。 下表列出一些一般值和預期效果的描述。 &quot;0 &quot; 表示應該 epirus 對稱的點 (使用 round endcaps，它應該是圓形) 。 如果行 endcap 是平面的，則檢視器應該 (盡可能選擇內建的作業系統虛線，也就是可快速繪製) 的東西。 以下顯示一些範例。
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td>&quot;2 2&quot;</td>
<td>虛線 (每個虛線，而介於兩者之間的空格是線條寬度的兩倍) </td>
</tr>
<tr class="even">
<td>&quot;1 2&quot;</td>
<td>點 (每個虛線都是線條的寬度，而每個空格是線條寬度的兩倍) </td>
</tr>
<tr class="odd">
<td>&quot;4 2&quot;</td>
<td>虛線 (每個虛線的寬度會是線條寬度的四倍，而每個空格是線條寬度的兩倍) </td>
</tr>
<tr class="even">
<td>&quot;8 2&quot;</td>
<td>長虛線</td>
</tr>
<tr class="odd">
<td>&quot;4 2 1 2&quot;</td>
<td>虛線點</td>
</tr>
<tr class="even">
<td>&quot;8 2 1 2&quot;</td>
<td>長虛線點</td>
</tr>
<tr class="odd">
<td>&quot;8 2 1 2 1 2&quot;</td>
<td>長虛線點點</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a>TextPath 元素

描述以提供的文字資料、字型和樣式為基礎的向量路徑。 如果有提供，則會扭曲文字路徑以符合 **路徑** 元素。



|   屬性        |   描述                                                                                                                                                                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| FitPath  | [VgTriState](msdn-online-vml-vgtristate.md)。 調整文字大小以填滿其所在的路徑。                                 |
| FitShape | [VgTriState](msdn-online-vml-vgtristate.md)。 將文字路徑延伸至圖形方塊的邊緣。                      |
| 開啟       | [VgTriState](msdn-online-vml-vgtristate.md)。 決定是否要顯示字元路徑。                    |
| String   | 字串。 要轉譯為文字路徑的文字。                                                                                    |
| Trim     | [VgTriState](msdn-online-vml-vgtristate.md)。 如果未使用，則移除保留給 ascenders 和下行的任何其他空間。 |
| XScale   | [VgTriState](msdn-online-vml-vgtristate.md)。 使用直接 x 度量，而不是沿著路徑進行測量。                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a>在 VML 物件模型中使用的資料類型

VML 物件模型會使用下列資料類型。

-   [Double](/windows)
-   [固定](/windows)
-   [整數](/windows)
-   [IVgAdjustments](/windows)
-   [IVgColor](/windows)
-   [IVgEquation](/windows)
-   [IVgFixedRectangle](/windows)
-   [IVgFixedRectangleArray](/windows)
-   [IVgFormula](/windows)
-   [IVgFormulas](/windows)
-   [IVgGradientColorArray](/windows)
-   [IVgPoints](/windows)
-   [IVgSkewMatrix](/windows)
-   [IVgSkewOffset](/windows)
-   [IVgVector2D](/windows)
-   [IVgVector3D](/windows)
-   [長度](/windows)
-   [Measure](/windows)
-   [String](/windows)
-   [VgBlackWhiteMode](/windows)
-   [VgFraction](/windows)
-   [VgTriState](/windows)

**Double 資料類型**

雙精確度整數，其範圍從-無限大到無限大。

**固定資料類型**

浮點數，範圍從-32766.0 到32766.0。

**整數資料類型**

範圍從-無限大到無限大的整數。

**IVgAdjustments 資料類型**

圖形的調整集合，可以用來變更圖形的維度。 調整可用來作為暫時預留位置，或因任何原因而使用變數。 集合中只有8項調整。



| 屬性 | 描述                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exists     | [IVgTriState](msdn-online-vml-vgtristate.md)。 判斷指定的調整是否存在。 請注意，必須使用索引;也就是說， ( 專案 ) 必須用來取出專案的存在。                                                                                                                                                                   |
| 項目       | [Long](#data-types-used-in-the-vml-object-model)。 從0到7的索引調整陣列。 請注意，可能會 sparcely 指定調整;也就是說，中繼陣列值可能不一定會填滿。 例如，專案1、3和5的值可能是3，而專案 (0) 、專案 (2) 和專案 (4) 指定。 若要查看專案是否存在，請使用 Exists 屬性。 |
| 長度     | [Integer](#data-types-used-in-the-vml-object-model) (整數)。 調整的數目。 不能大於8。                                                                                                                                                                                                                                                                          |
| 值      | [字串](#data-types-used-in-the-vml-object-model)。 數值的文字標記法，每個數位之間都有逗號。                                                                                                                                                                                                                                                    |



 

**IVgColor**

指定色彩。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>RGB</td>
<td><strong>VgRGBType</strong>。 RGB 值 (色彩的長) 。 只有當類型為 RGB 時才有效。</td>
</tr>
<tr class="even">
<td>R</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a> (整數)。 色彩的紅色元件。 的範圍可以介於0到255之間。</td>
</tr>
<tr class="odd">
<td>G</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a> (整數)。 色彩的綠色元件。 的範圍可以介於0到255之間。</td>
</tr>
<tr class="even">
<td>B</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a> (整數)。 色彩的藍色元件。 的範圍可以介於0到255之間。</td>
</tr>
<tr class="odd">
<td>String</td>
<td><a href="#data-types-used-in-the-vml-object-model">字串</a>。 色彩的文字標記法。 以下是支援的命名色彩類型：
<ul>
<li>黑色 (#000000) </li>
<li>銀級 (#C0C0C0) </li>
<li>灰色 (#808080) </li>
<li>白色 (#FFFFFF) </li>
<li> (#800000) 的暗紫紅色</li>
<li>紅色 (#FF0000) </li>
<li>紫色 (#800080) </li>
<li>Fuchsia (#FF00FF) </li>
<li>綠色 (#008000) </li>
<li> (#00FF00) 的橙色</li>
<li>) 的橄欖綠 (#808000</li>
<li>黃色 (#FFFF00) </li>
<li>Navy (#000080) </li>
<li>藍色 (#0000FF) </li>
<li>青色 (#008080) </li>
<li>綠色 (#00FFFF) </li>
</ul></td>
</tr>
<tr class="even">
<td>類型</td>
<td><strong>VgColorType</strong>。 色彩的類型。 下列其中一種類型：
<ul>
<li>Mixed</li>
<li>已命名</li>
<li>RGB</li>
<li>配置</li>
</ul></td>
</tr>
</tbody>
</table>



 

**IVgEquation**

用於公式的方程式。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>作業</td>
<td><strong>VgEquationOperationType</strong> 要在參數上執行的作業名稱。 下列作業可用於方程式：
<table>
<thead>
<tr class="header">
<th>作業</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Abs</td>
<td>絕對值。 <br/> <strong>abs</strong> (v)  <br/></td>
</tr>
<tr class="even">
<td>Atan2</td>
<td>極座標：以 fd 單位 (度乘以 65536) 的結果。<br/> <strong>atan2</strong> (p1，v)  <br/></td>
</tr>
<tr class="odd">
<td>Cos</td>
<td>在 fd 單位中的余弦值、引數 (度乘以 65536) 。<br/> v * <strong>cos</strong> (p1)  <br/></td>
</tr>
<tr class="even">
<td>Cosatan2</td>
<td>在中繼計算中保留完整的精確度。<br/> v * <strong>cos (atan2 (</strong> p2，p1 <strong>) ) </strong><br/></td>
</tr>
<tr class="odd">
<td>橢圓形</td>
<td>橢圓形</td>
</tr>
<tr class="even">
<td>如果</td>
<td>如果條件測試。 v > 0 <strong>？</strong> p1： p2</td>
</tr>
<tr class="odd">
<td>最大值</td>
<td>兩個值中較大的一個。 <br/> <strong>max</strong> (v，p1)  <br/></td>
</tr>
<tr class="even">
<td>Mid</td>
<td>平均 ( v + p1) /2</td>
</tr>
<tr class="odd">
<td>Min</td>
<td>兩個值的較小者。 <strong>min</strong> (v，p1) </td>
</tr>
<tr class="even">
<td>Mod</td>
<td>模數。</td>
</tr>
<tr class="odd">
<td>產品</td>
<td>用於乘法和除法。 v * p1/p2</td>
</tr>
<tr class="even">
<td>Sin</td>
<td>在 fd 單位中的正弦值、引數 (度乘以 65536) 。 <br/> v * <strong>sin</strong> (p1)  <br/></td>
</tr>
<tr class="odd">
<td>Sinatan2</td>
<td>在中繼計算中保留完整的精確度。 v * <strong>sin</strong> (<strong>atan2</strong> (p2，p1) ) </td>
</tr>
<tr class="even">
<td>Sqrt</td>
<td>結果為正向下四捨五入。 <br/> <strong>sqrt</strong> (v)  <br/></td>
</tr>
<tr class="odd">
<td>Sum</td>
<td>用於加法和減法。<br/> v + p1 p2<br/></td>
</tr>
<tr class="even">
<td>Sumangle</td>
<td>現有的角度 (以 65536) 調整，其中 p1 和 p2 是以度為單位。<br/> v + p1 * 65536 + p2 * 65536<br/></td>
</tr>
<tr class="odd">
<td>Tan</td>
<td>正切函數的引數為 fd 單位 (度乘以 65536) 。 <br/> v * tan ( p1 ) <br/></td>
</tr>
<tr class="even">
<td>Val</td>
<td>定義其他值的輔助線值。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Param1</td>
<td><strong>Integer</strong> (整數)。 第一個參數。</td>
</tr>
<tr class="odd">
<td>Paramtype1</td>
<td><strong>VgFormulaParamType</strong>。 第一個參數的型別。 支援下列值：
<table>
<thead>
<tr class="header">
<th>類型</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>值</td>
<td>參數是簡單的值。</td>
</tr>
<tr class="even">
<td>AdjustmentReference</td>
<td>參數是調整的參考。 例如，如果第一個參數是1，則會使用第一次調整的值。</td>
</tr>
<tr class="odd">
<td>FormulaReference</td>
<td>參數是先前公式的結果參考結果。 例如，如果第一個參數是2，則會使用公式2的結果。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Param2</td>
<td><strong>Integer</strong> (整數)。 第二個參數。</td>
</tr>
<tr class="odd">
<td>Paramtype2</td>
<td><strong>VgFormulaParamType</strong> 參數2的型別。</td>
</tr>
<tr class="even">
<td>Val</td>
<td><strong>Integer</strong> (整數)。 結果。</td>
</tr>
<tr class="odd">
<td>Valtype2</td>
<td><strong>VgFormulaParamType</strong>。 結果的類型。</td>
</tr>
</tbody>
</table>



 

**IVgFixedRectangle**

指定固定的矩形。



| 屬性 | 描述                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| 值      | [字串](#data-types-used-in-the-vml-object-model)。 指定路徑的文字值。         |
| Left       | [Double](#data-types-used-in-the-vml-object-model)。 矩形的最左邊座標。   |
| 頁首        | [Double](#data-types-used-in-the-vml-object-model)。 矩形的最上層座標。    |
| Right      | [Double](#data-types-used-in-the-vml-object-model)。 矩形的最右側座標。  |
| 下層     | [Double](#data-types-used-in-the-vml-object-model)。 矩形的最底層座標。 |



 

**IVgFixedRectangleArray**

固定矩形的陣列。



| 屬性 | 描述                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| 值      | [字串](#data-types-used-in-the-vml-object-model)。 陣列的文字標記法。                           |
| 長度     | [Integer](#data-types-used-in-the-vml-object-model) (整數)。 此陣列中的矩形數目。                    |
| 項目       | [IVgFixedRectangle](#data-types-used-in-the-vml-object-model)。 位於指定索引處的矩形物件。 |



 

**IVgFormula** 資料類型

公式的定義，可以改變形狀的路徑，或用於其他計算用途。 公式可以根據可能變更之圖形的 **形容詞** 屬性。 公式也可以參考其他公式。



| 屬性| 說明                                           |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eqn        | [IVgEquation](#data-types-used-in-the-vml-object-model)。 每個公式都會將單一值定義為運算式評估的結果。 運算式是由這個屬性所定義，且具有最多三個引數的一般形式，也就是調整值 (例如， \# 2) 、先前公式的結果 (例如 @2) 、固定數位或預先定義的值。 |



 

**IVgFormulas 資料類型**

公式物件的集合。



| 屬性 | 說明                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 長度     | [Integer](#data-types-used-in-the-vml-object-model) (整數)。 集合中的公式物件數目。                                                |
| 項目       | [IVgFormula](#data-types-used-in-the-vml-object-model)。 特定的公式。 請注意，公式陣列可能會繼承從圖形類型。 |



 

**IVgGradientColorArray**

色彩的陣列，定義) 的漸層 (混合的色彩範圍。



| 屬性 | 描述                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| 值      | [字串](#data-types-used-in-the-vml-object-model)。 指定色彩的陣列;例如，"red. 2;綠. 4;黑色. 7 " |
| 長度     | [Integer](#data-types-used-in-the-vml-object-model) (整數)。 陣列中的色彩數目。                                          |



 



| 方法     | 描述                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AddColor    | [VgFraction](msdn-online-vml-vgfraction-data-type.md)。 在分數指定的端點上加入新的色彩。 新的色彩預設為白色，而是傳回值。 然後可以透過參考來變更色彩。 |
| RemoveColor | [VgFraction](msdn-online-vml-vgfraction-data-type.md)。 移除依分數指定之端點的色彩。 注意：如果0.0 或1.0 不存在，就表示它是隱含的，而且會在該點使用白色的色彩。          |



 

**IVgPoints 資料類型**

定義圖形的點陣列。



| 屬性 | 描述                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| 值      | [字串](#data-types-used-in-the-vml-object-model)。 陣列的文字標記法。           |
| 長度     | [Integer](#data-types-used-in-the-vml-object-model) (整數)。 此陣列中的點數目。        |
| 項目       | [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md)。 指定之索引處的點。 |



 

**IVgSkewMatrix 資料類型**

用於扭曲形狀的矩陣，以 "*sxx，sxy，syx，syy，px，.py* " \[ *s* = scale， *p* = 透視圖形式的觀點轉換矩陣 \] 。 如果 offset 是絕對單位，則 *px，.py* 是以 emu ^ 1 單位為單位;否則是圖形大小的反向分數。



| 屬性   | 描述                                         |
|--------------|-----------------------------------------------------|
| XtoX         | [Double](#data-types-used-in-the-vml-object-model)。 |
| YtoX         | [Double](#data-types-used-in-the-vml-object-model)。 |
| XtoY         | [Double](#data-types-used-in-the-vml-object-model)。 |
| YtoY         | [Double](#data-types-used-in-the-vml-object-model)。 |
| PerspectiveX | [Double](#data-types-used-in-the-vml-object-model)。 |
| PerspectiveY | [Double](#data-types-used-in-the-vml-object-model)。 |



 

**IVgSkewOffset**

指定扭曲的位移。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>值</td>
<td><a href="#data-types-used-in-the-vml-object-model">字串</a>。 位移的文字標記法。</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>。 X 元件。 百分比或量值。 如果沒有單位，則隱含 ShapeRelative 類型;否則，就會隱含絕對型別。</td>
</tr>
<tr class="odd">
<td>Y</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>。 Y 元件。</td>
</tr>
<tr class="even">
<td>類型</td>
<td><strong>VgSkewTransformType</strong>。 指定轉換的類型。 有效的值是介於-無限大和無限大之間的整數點。 
<table>
<thead>
<tr class="header">
<th>類型</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShapeRelative</td>
<td>位移的值是原始圖形大小 (比例) 的百分比;例如，值0.5 表示形狀大小的位移一半。</td>
</tr>
<tr class="even">
<td>絕對</td>
<td>這些值是絕對單位。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

**IVgVector2D 資料類型**

指定由兩個 **雙精度浮** 點陣列成的二維向量。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>值</td>
<td><strong>字串</strong>。 以空格分隔的兩個向量數位的文字標記法。</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>。 這個向量的 X 元件。</td>
</tr>
<tr class="odd">
<td>Y</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>。 這個向量的 Y 元件。</td>
</tr>
<tr class="even">
<td>類型</td>
<td><strong>VgVectorType</strong>。 此向量的預期單位。 值為：
<ul>
<li>量值</li>
<li>長度</li>
<li>AngleInDegrees</li>
<li>Fraction</li>
<li>數位百分比整數</li>
</ul></td>
</tr>
</tbody>
</table>



 

**IVgVector3D 資料類型**

指定由三個 **雙精度浮** 點陣列成的三維向量。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>值</td>
<td><strong>字串</strong>。 以空格分隔的三個向量數位的文字標記法。</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>。 這個向量的 X 元件。</td>
</tr>
<tr class="odd">
<td>Y</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>。 這個向量的 Y 元件。</td>
</tr>
<tr class="even">
<td>Z</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>。 此向量的 Z 元件。</td>
</tr>
<tr class="odd">
<td>類型</td>
<td><strong>VgVectorType</strong>。 此向量的預期單位。 值為：
<ul>
<li>量值</li>
<li>長度</li>
<li>AngleInDegrees</li>
<li>Fraction</li>
<li>數字</li>
<li>百分比</li>
<li>整數</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Length 資料類型**

浮點數，範圍介於0到無限大之間。

**量值資料類型**

從-無限大到無限大的浮點數。

**字串資料類型**

任何長度的字元資料。

**VgBlackWhiteMode**

黑色和白色的呈現模式。 可能的值包括：

-   **色彩**
-   **Auto**
-   **灰度**
-   **LightGrayScale**
-   **InverseGray**
-   **GrayOutline**
-   **BlackTextAndLines**
-   **HighContrast**
-   **黑色**
-   **白色**
-   **Undrawn**

**VgFraction 資料類型**

浮點數，範圍從0.0 到1.0。 分數也可以指定為百分比;例如，"50%"。

**VgTriState 資料類型**

列舉值，用於可為三種狀態之一的值：

-   **TRUE**
-   **FALSE**
-   **MIXED**
