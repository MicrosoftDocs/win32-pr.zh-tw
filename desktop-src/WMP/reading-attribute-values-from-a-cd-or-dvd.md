---
title: 從 CD 或 DVD 讀取屬性值
description: 從 CD 或 DVD 讀取屬性值
ms.assetid: 441916fb-f66d-4a12-a95c-b47561c93e64
keywords:
- Windows Media Player，媒體專案的屬性
- Windows Media Player 物件模型，媒體專案的屬性
- 物件模型、媒體專案的屬性
- Windows Media Player行動電話，媒體專案的屬性
- Windows Media Player ActiveX 控制項、媒體專案的屬性
- Windows Media Player行動 ActiveX 控制項、媒體專案的屬性
- ActiveX 控制項，媒體專案的屬性
- Windows Media Player 文件庫、媒體專案的屬性
- 文件庫、媒體專案的屬性
- 屬性，讀取值
- 讀取屬性值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800fda1bf3002f015873b69e29503ecba637a978bac1b167724c04f5f15228b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861768"
---
# <a name="reading-attribute-values-from-a-cd-or-dvd"></a>從 CD 或 DVD 讀取屬性值

在本主題中， **Player** 物件是以下列方式定義：


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



下列 c # 範例程式碼會抓取磁片磁碟機中目前光碟的所有屬性值，並將它們寫入檔案。


```C++
private void logDiscAttributes()
{
    int iCDCount = 0; // Count of CD and DVD drives
    int iAttrCount = 0; // Attribute count.
    int iPLCount = 0; // Playlist item count.

    IWMPCdromCollection cdCollection;
    IWMPPlaylist playlist;
    IWMPMedia media;
    string strAttribName = "";
    string strAttribValue = "";
    string strText = "";

    // Create a StreamWriter object to write
    // the output to a file.
    StreamWriter sw = new StreamWriter(strOutFile, true);

    cdCollection = Player.cdromCollection;
    iCDCount = cdCollection.count;

    // Loop through the CD and DVD drives.
    for (int i = 0; i < iCDCount; i++)
    {
        playlist = cdCollection.Item(i).Playlist;

        // Loop through the playlist attributes.
        iAttrCount = playlist.attributeCount;
        for (int j = 0; j < iAttrCount; j++)
        {
            strText += "Playlist Attribute: \t";
            strAttribName = playlist.get_attributeName(j);
            strText += "\t" + strAttribName + "\t";
            strAttribValue = playlist.getItemInfo(strAttribName);
            strText += strAttribValue + "\n";
        }

        // Loop through the playlist.
        iPLCount = playlist.count;
        for (int k = 0; k < iPLCount; k++)
        {
            media = playlist.get_Item(k);

            // Loop through the media attributes.
            iAttrCount = media.attributeCount;
            for (int m = 0; m < iAttrCount; m++)
            {
                strText += "Track or Chapter [" + m.ToString() + "]";
                strAttribName = media.getAttributeName(m);
                strText += "\t" + strAttribName + "\t";
                strText += "Read Only: " + media.isReadOnlyItem(strAttribName) + "\t";
                strAttribValue = media.getItemInfo(strAttribName);
                strText += strAttribValue + "\n";
            }
        }
    }

    sw.Write(strText);
    sw.Close();

    MessageBox.Show(strOutFile + " created");
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**媒體專案屬性**](media-item-attributes.md)
</dt> <dt>

[**媒體物件**](media-object.md)
</dt> </dl>

 

 




