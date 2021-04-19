---
title: 讀取屬性值
description: 讀取屬性值
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
keywords:
- Windows Media Player，媒體專案的屬性
- Windows Media Player 物件模型，媒體專案的屬性
- 物件模型、媒體專案的屬性
- Windows Media Player 行動裝置，媒體專案的屬性
- Windows Media Player ActiveX 控制項、媒體專案的屬性
- Windows Media Player 的行動 ActiveX 控制項、媒體專案的屬性
- ActiveX 控制項、媒體專案的屬性
- Windows Media Player 文件庫、媒體專案的屬性
- 文件庫、媒體專案的屬性
- 屬性，讀取值
- 讀取屬性值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d527429b71cff5594c127b3ad2bfb82b3f3b2ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106983289"
---
# <a name="reading-attribute-values"></a><span data-ttu-id="d9cf0-114">讀取屬性值</span><span class="sxs-lookup"><span data-stu-id="d9cf0-114">Reading Attribute Values</span></span>

<span data-ttu-id="d9cf0-115">您可以在程式庫和 Windows Media 檔案中找到的屬性具有預先定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-115">The attributes you can find in the library and in Windows Media files have predefined names.</span></span> <span data-ttu-id="d9cf0-116">您可以撰寫程式碼，藉由將該屬性的名稱傳遞給 *媒體*，以抓取一個屬性的值。**getItemInfo** 或 *媒體*。**getItemInfoByType**。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-116">You can write code that retrieves the value of one attribute by passing the name of that attribute to *Media*.**getItemInfo** or *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="d9cf0-117">您也可以撰寫程式碼，以抓取檔案或專案中的所有屬性值。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-117">You can also write code that retrieves the values of all of the attributes in a file or item.</span></span>

<span data-ttu-id="d9cf0-118">下列 c # 範例會抓取 **Title** 屬性的值，並將它顯示在訊息方塊中。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-118">The following C# example retrieves the value of the **Title** attribute and displays it in a message box.</span></span> <span data-ttu-id="d9cf0-119">在此範例中， **player** 物件已定義為 AxWMPLib. AxWindowsMediaPlayer player。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-119">In this example, the **Player** object was defined as axWMPLib.AxWindowsMediaPlayer Player.</span></span>


```C++
IWMPMedia media;
string strAttribValue = "";

// Initialize the media object
media = Player.currentMedia;

// Retrieve the object's Title attribute
strAttribValue = media.getItemInfo("Title");

// Display the title
if (strAttribValue != "")
{
    MessageBox.Show("Current title: " + strAttribValue);
}

```



<span data-ttu-id="d9cf0-120">在 **getItemInfoByType** 的呼叫中，第二個參數是指定語言的字串。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-120">In the call to **getItemInfoByType**, the second parameter is a string that specifies the language.</span></span> <span data-ttu-id="d9cf0-121">如果您傳遞空字串（如這個範例所示），此方法就會以預設語言來捕獲值。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-121">If you pass an empty string as shown in this example, the method retrieves the value in the default language.</span></span> <span data-ttu-id="d9cf0-122">如需第三個參數的詳細資訊，請參閱 [具有多個值的屬性](attributes-with-multiple-values.md)。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-122">For information about the third parameter, see [Attributes with Multiple Values](attributes-with-multiple-values.md).</span></span>

<span data-ttu-id="d9cf0-123">下列 c # 範例會在目前的媒體專案中，取得指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-123">The following C# example retrieves the values for a given attribute in the current media item.</span></span> <span data-ttu-id="d9cf0-124">它會以分號分隔的字串傳回這些值。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-124">It returns these values as a semicolon-delimited string.</span></span> <span data-ttu-id="d9cf0-125">請注意，對於以物件表示的屬性，例如 **wm/歌詞 \_ 內容**、 **Wm/圖片** 和 **wm/UserWebURL**，此函數會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-125">Note that for attributes represented as objects, such as **WM/Lyrics\_Synchronised**, **WM/Picture**, and **WM/UserWebURL**, the function returns an empty string.</span></span>


```C++
private string getAttributeValues(string strAttrName, IWMPMedia3 media)
{
    string strAttrValue = "";
    int iAttrCount = 0;

    if (media != null)
    {
        // Retrieve the count of values for this attribute
        iAttrCount = media.getAttributeCountByType(strAttrName, "");

        // Retrieve the values
        for (int i = 0; i < iAttrCount; i++)
        {
            strAttrValue += media.getItemInfoByType(strAttrName, "", i);
            strAttrValue += ";";
        }
    }

    // Return the resulting string
    return strAttrValue;
}

```



<span data-ttu-id="d9cf0-126">傳遞至 **getItemInfoByType** 方法的第三個引數是具有相同名稱的屬性集合中特定屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-126">The third argument passed to the **getItemInfoByType** method is the index of a particular attribute in a set of attributes with the same name.</span></span>

<span data-ttu-id="d9cf0-127">您可以使用類似的程式碼來取出具有唯一名稱的屬性。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-127">You can use similar code to retrieve attributes that have unique names.</span></span> <span data-ttu-id="d9cf0-128">在這些情況下， **getAttributeCountByType** 會傳回1。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-128">In those cases, **getAttributeCountByType** returns 1.</span></span> <span data-ttu-id="d9cf0-129">在稍早所示的範例中，呼叫 **getItemInfoByType** 只會執行一次。</span><span class="sxs-lookup"><span data-stu-id="d9cf0-129">In the example shown earlier, the call to **getItemInfoByType** would execute only once.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9cf0-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="d9cf0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9cf0-131">**變更屬性值**</span><span class="sxs-lookup"><span data-stu-id="d9cf0-131">**Changing Attribute Values**</span></span>](changing-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="d9cf0-132">**媒體專案屬性**</span><span class="sxs-lookup"><span data-stu-id="d9cf0-132">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="d9cf0-133">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="d9cf0-133">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="d9cf0-134">**從 CD 或 DVD 讀取屬性值**</span><span class="sxs-lookup"><span data-stu-id="d9cf0-134">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




