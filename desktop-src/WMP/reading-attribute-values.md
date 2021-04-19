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
# <a name="reading-attribute-values"></a>讀取屬性值

您可以在程式庫和 Windows Media 檔案中找到的屬性具有預先定義的名稱。 您可以撰寫程式碼，藉由將該屬性的名稱傳遞給 *媒體*，以抓取一個屬性的值。**getItemInfo** 或 *媒體*。**getItemInfoByType**。 您也可以撰寫程式碼，以抓取檔案或專案中的所有屬性值。

下列 c # 範例會抓取 **Title** 屬性的值，並將它顯示在訊息方塊中。 在此範例中， **player** 物件已定義為 AxWMPLib. AxWindowsMediaPlayer player。


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



在 **getItemInfoByType** 的呼叫中，第二個參數是指定語言的字串。 如果您傳遞空字串（如這個範例所示），此方法就會以預設語言來捕獲值。 如需第三個參數的詳細資訊，請參閱 [具有多個值的屬性](attributes-with-multiple-values.md)。

下列 c # 範例會在目前的媒體專案中，取得指定之屬性的值。 它會以分號分隔的字串傳回這些值。 請注意，對於以物件表示的屬性，例如 **wm/歌詞 \_ 內容**、 **Wm/圖片** 和 **wm/UserWebURL**，此函數會傳回空字串。


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



傳遞至 **getItemInfoByType** 方法的第三個引數是具有相同名稱的屬性集合中特定屬性的索引。

您可以使用類似的程式碼來取出具有唯一名稱的屬性。 在這些情況下， **getAttributeCountByType** 會傳回1。 在稍早所示的範例中，呼叫 **getItemInfoByType** 只會執行一次。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**變更屬性值**](changing-attribute-values.md)
</dt> <dt>

[**媒體專案屬性**](media-item-attributes.md)
</dt> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**從 CD 或 DVD 讀取屬性值**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




