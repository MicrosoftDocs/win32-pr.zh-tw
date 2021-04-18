---
title: 外觀定義檔
description: 外觀定義檔
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- 面板定義檔 Windows Media Player 的外觀
- 外觀、面板定義檔
- 面板的檔案、外觀定義
- 外觀定義檔，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd06708a99a15dc9a8266278850c0507007f058
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965599"
---
# <a name="skin-definition-file"></a><span data-ttu-id="2bc9f-107">外觀定義檔</span><span class="sxs-lookup"><span data-stu-id="2bc9f-107">Skin Definition File</span></span>

<span data-ttu-id="2bc9f-108">面板定義檔包含外觀的基本指示，以及可以找到面板所使用之其他檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-108">Skin definition files contain the basic instructions for what the skin does and where other files used by the skin can be found.</span></span> <span data-ttu-id="2bc9f-109">面板只能有一個面板定義檔案，且其副檔名為 wms。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-109">There can only be one skin definition file for a skin, and it has a .wms file name extension.</span></span>

<span data-ttu-id="2bc9f-110">面板定義檔中的指示是以可延伸標記語言 (XML)  (XML) 來撰寫，類似于 HTML。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-110">The instructions in the skin definition file are written in Extensible Markup Language (XML), which is similar to HTML.</span></span> <span data-ttu-id="2bc9f-111">如果您已經使用 HTML 來建立網頁，您會發現 XML 看起來很熟悉。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-111">If you have used HTML to create webpages, you will find that XML looks familiar.</span></span>

<span data-ttu-id="2bc9f-112">面板定義檔中的 XML 會使用一組特殊元素標記，來定義面板使用者介面的元件。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-112">The XML in the skin definition file uses a set of special element tags to define parts of the skin user interface.</span></span> <span data-ttu-id="2bc9f-113">例如， [button](button-element.md) 元素會定義按鈕的行為方式、其所在位置，以及它的外觀。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-113">For example, the [BUTTON](button-element.md) element defines how a button will behave, where it will go, and what it will look like.</span></span>

<span data-ttu-id="2bc9f-114">每個元素標記都有特定屬性。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-114">Each element tag has specific attributes.</span></span> <span data-ttu-id="2bc9f-115">例如， [button](button-element.md) 元素具有 **影像** 屬性，可定義可在何處找到按鈕的圖片。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-115">For example, the [BUTTON](button-element.md) element has an **image** attribute that defines where the picture for the button can be found.</span></span> <span data-ttu-id="2bc9f-116">這類似于 HTML，其中 BODY 元素會 **有一個 background** 屬性，可定義 html 網頁的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-116">This is similar to HTML, where the BODY element will have a **bgcolor** attribute that defines the background color of the HTML page.</span></span> <span data-ttu-id="2bc9f-117">所有面板元素及其屬性的詳細資訊都包含在 [面板程式 [設計參考](skin-programming-reference.md) ] 區段中。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-117">Detailed information about all skin elements and their attributes is included in the [Skin Programming Reference](skin-programming-reference.md) section.</span></span>

<span data-ttu-id="2bc9f-118">XML 有幾個簡單的規則，您必須知道這些規則才能建立外觀。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-118">XML has a few simple rules that you need to know to create skins.</span></span> <span data-ttu-id="2bc9f-119">與 HTML 不同的是，XML 需要您完全遵循規則。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-119">Unlike HTML, XML requires you to follow the rules exactly.</span></span>

## <a name="enclose-elements-with-angle-brackets"></a><span data-ttu-id="2bc9f-120">以角括弧括住元素</span><span class="sxs-lookup"><span data-stu-id="2bc9f-120">Enclose Elements with Angle Brackets</span></span>

<span data-ttu-id="2bc9f-121">所有元素都以角括弧括住;例如， **BUTTON** 元素的類型如下：</span><span class="sxs-lookup"><span data-stu-id="2bc9f-121">All elements are enclosed by angle brackets; for example, the **BUTTON** element is typed like this:</span></span>


```C++
<BUTTON>

```



<span data-ttu-id="2bc9f-122">您不需要在所有大寫字母中輸入 "BUTTON" 一字，但在此 SDK 的範例程式碼中，會使用以全部大寫輸入元素名稱的慣例。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-122">You do not need to type the word "BUTTON" in all uppercase letters, but the convention of typing element names in all uppercase is used in the example code of this SDK.</span></span>

## <a name="put-attributes-before-the-closing-bracket"></a><span data-ttu-id="2bc9f-123">將屬性放在右括弧之前</span><span class="sxs-lookup"><span data-stu-id="2bc9f-123">Put Attributes Before the Closing Bracket</span></span>

<span data-ttu-id="2bc9f-124">特定元素的所有屬性都必須包含在右角括弧前面。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-124">All attributes for a particular element must be included before the closing angle bracket.</span></span> <span data-ttu-id="2bc9f-125">屬性是由屬性名稱後面接著等號 (=) 和屬性的值以引號括住。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-125">An attribute consists of the attribute name followed by an equal sign (=) and the value of the attribute in quotes.</span></span>


```C++
<BUTTON image="mypic.jpg">

```



<span data-ttu-id="2bc9f-126">您不需要在小寫中輸入 "image" 這個字，但在此 SDK 的範例程式碼中，會使用以小寫輸入屬性名稱的慣例。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-126">You do not need to type the word "image" in lowercase, but the convention of typing attribute names in lowercase is used in the example code of this SDK.</span></span> <span data-ttu-id="2bc9f-127">另請注意，屬性的值會以引號括住。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-127">Also note that the value of the attribute is enclosed in quotation marks.</span></span>

## <a name="opening-and-closing-elements"></a><span data-ttu-id="2bc9f-128">開啟和關閉元素</span><span class="sxs-lookup"><span data-stu-id="2bc9f-128">Opening and Closing Elements</span></span>

<span data-ttu-id="2bc9f-129">某些專案會在另一個元素內群組在一起。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-129">Some elements are grouped together inside another element.</span></span> <span data-ttu-id="2bc9f-130">例如，除非您將一或多個 **BUTTONELEMENT** 元素與它搭配使用，否則 **BUTTONGROUP** 元素不會有很大的意義。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-130">For example, the **BUTTONGROUP** element does not make a lot of sense unless you use one or more **BUTTONELEMENT** elements with it.</span></span> <span data-ttu-id="2bc9f-131">若要讓群組清楚，您需要為每個專案都有開頭和結束記號。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-131">To make the grouping clear, you need to have an opening and closing tag for each element.</span></span> <span data-ttu-id="2bc9f-132">開頭的標記只是元素名稱和任何相關的屬性（以角括弧括住）。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-132">The opening tag is just the element name and any related attributes, surrounded by angle brackets.</span></span> <span data-ttu-id="2bc9f-133">結束記號是元素名稱，前面加上正斜線 (/) ，然後以角括弧括住。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-133">The closing tag is the element name, preceded by a forward slash (/), and then enclosed by angle brackets.</span></span> <span data-ttu-id="2bc9f-134">例如， **BUTTONGROUP** 元素開啟標記如下所示：</span><span class="sxs-lookup"><span data-stu-id="2bc9f-134">For example, the **BUTTONGROUP** element opening tag looks like this:</span></span>


```C++
<BUTTONGROUP>

```



<span data-ttu-id="2bc9f-135">結尾 **BUTTONGROUP** 標記如下所示：</span><span class="sxs-lookup"><span data-stu-id="2bc9f-135">The closing **BUTTONGROUP** tag looks like this:</span></span>


```C++
</BUTTONGROUP>

```



<span data-ttu-id="2bc9f-136">您會將 **BUTTONELEMENT** 標記放在開頭和結尾的 **BUTTONGROUP** 元素標記之間。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-136">You would put the **BUTTONELEMENT** tags between the opening and closing **BUTTONGROUP** element tags.</span></span> <span data-ttu-id="2bc9f-137">例如：</span><span class="sxs-lookup"><span data-stu-id="2bc9f-137">For example:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a><span data-ttu-id="2bc9f-138">關閉元素</span><span class="sxs-lookup"><span data-stu-id="2bc9f-138">Closing Off Elements</span></span>

<span data-ttu-id="2bc9f-139">如果專案內沒有其他專案，則您必須在專案名稱的結尾加上正斜線（緊接在右角括弧前面）。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-139">If an element has no other elements inside it, you must put a forward slash at the end of the element name just before the closing angle bracket.</span></span> <span data-ttu-id="2bc9f-140">例如，在上述程式碼中，每個 **BUTTONELEMENT** 專案都有一個正斜線，表示其中沒有任何其他專案嵌套在其中。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-140">For example, in the code above, each **BUTTONELEMENT** element has a forward slash to indicate that there are no other elements nested within it.</span></span>

<span data-ttu-id="2bc9f-141">換句話說，您必須要有結尾元素標記，或關閉具有正斜線的元素。</span><span class="sxs-lookup"><span data-stu-id="2bc9f-141">In other words, you must either have a closing element tag or close off your element with a forward slash.</span></span>

<span data-ttu-id="2bc9f-142">這是正確的：</span><span class="sxs-lookup"><span data-stu-id="2bc9f-142">This is correct:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



<span data-ttu-id="2bc9f-143">不正確：</span><span class="sxs-lookup"><span data-stu-id="2bc9f-143">This is not correct:</span></span>


```C++
<BUTTONGROUP/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



<span data-ttu-id="2bc9f-144">這也不正確：</span><span class="sxs-lookup"><span data-stu-id="2bc9f-144">This is also not correct:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT>
    <BUTTONELEMENT>
</BUTTONGROUP>

```



<span data-ttu-id="2bc9f-145">下一節提供有關外觀定義檔案的詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="2bc9f-145">The following section provides more information about skin definition files:</span></span>

-   [<span data-ttu-id="2bc9f-146">外觀定義檔案結構</span><span class="sxs-lookup"><span data-stu-id="2bc9f-146">Skin Definition File Structure</span></span>](skin-definition-file-structure.md)

## <a name="related-topics"></a><span data-ttu-id="2bc9f-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="2bc9f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bc9f-148">**面板檔案**</span><span class="sxs-lookup"><span data-stu-id="2bc9f-148">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




