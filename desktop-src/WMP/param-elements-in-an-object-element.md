---
title: OBJECT 元素中的 PARAM 元素
description: OBJECT 元素中的 PARAM 元素
ms.assetid: f9229d92-3a7e-4ba4-a84c-20e60f2482dc
keywords:
- Windows Media Player，OBJECT 元素中的 PARAM 元素
- Windows Media Player 物件模型、OBJECT 元素中的 PARAM 元素
- 物件模型、OBJECT 元素中的 PARAM 專案
- Windows Media Player Mobile、OBJECT 元素中的 PARAM 元素
- Windows Media Player ActiveX 控制項、OBJECT 元素中的 PARAM 元素
- Windows Media Player 行動 ActiveX 控制項、OBJECT 元素中的 PARAM 元素
- ActiveX 控制項、OBJECT 元素中的 PARAM 元素
- 內嵌、網頁
- 物件元素中的網頁內嵌、PARAM 元素
- OBJECT 元素中的 PARAM 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f0fc5b9f64fa462386ec037eba34ed4e0659bb1
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "103840931"
---
# <a name="param-elements-in-an-object-element"></a>OBJECT 元素中的 PARAM 元素

Windows Media Player 使用 PARAM 元素來定義控制項的特定啟動條件。 PARAM 元素內嵌在 OBJECT 元素內。

例如，如果您想要定義 **autoStart** 屬性是否為 True，您可以將 PARAM 專案內嵌在 OBJECT 元素內。


```HTML
<OBJECT ID="Player"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
    <PARAM name="autoStart" value="True">
</OBJECT>
```



您可以依需要在物件專案中擁有任意數量的 PARAM 元素。 PARAM 有兩個屬性：名稱和值。 這兩個屬性都必須設定。

在瀏覽器和 mime 類型之間，支援的 PARAM 屬性會稍有不同。 下表顯示 Internet Explorer 與 Firefox 瀏覽器所支援的屬性。 Firefox 瀏覽器的慣用 mime 類型為 application/x------------（其他）有數種 mime 類型可用來將 Player 控制項內嵌在 Firefox 瀏覽器所裝載的網頁中。 資料表的第四個數據行顯示當您使用非 application/x---wmp 以外的 mime 類型時，所支援的屬性。



| 參數名稱                                            | Internet Explorer | 使用 mime 類型 application/x-ms-wmp 的 Firefox | Firefox 與任何其他 mime 類型 |
|-------------------------------------------------------|-------------------|---------------------------------------------|----------------------------------|
| [啟動](settings-autostart.md)                   | 是               | 是                                         | 是                              |
| [平衡](settings-balance.md)                       | 是               | 是                                         | 是                              |
| [baseURL](settings-baseurl.md)                       | 是               | 是                                         | 是                              |
| [captioningID](closedcaption-captioningid.md)        | 是               | 是                                         | 是                              |
| [currentMarker](controls-currentmarker.md)           | 是               | 是                                         | 是                              |
| [currentPosition](controls-currentposition.md)       | 是               | 是                                         | 是                              |
| [defaultFrame](settings-defaultframe.md)             | 是               | 否                                          | 不可以                               |
| [enableCoNtextMenu](player-enablecontextmenu.md)     | 是               | 是                                         | 是                              |
| [啟用](player-enabled.md)                         | 是               | 是                                         | 是                              |
| [enableErrorDialogs](settings-enableerrordialogs.md) | 是               | 是                                         | 不可以                               |
| **檔案名**                                          | 不可以                | 是                                         | 是                              |
| [全屏](player-fullscreen.md)                   | 是               | 否                                          | 不可以                               |
| [invokeURLs](settings-invokeurls.md)                 | 是               | 否                                          | 不可以                               |
| [靜音](settings-mute.md)                             | 是               | 是                                         | 是                              |
| [playCount](settings-playcount.md)                   | 是               | 是                                         | 不可以                               |
| [率](settings-rate.md)                             | 是               | 是                                         | 是                              |
| [SAMIFileName](closedcaption-samifilename.md)        | 是               | 是                                         | 是                              |
| [SAMILang](closedcaption-samilang.md)                | 是               | 是                                         | 是                              |
| [SAMIStyle](closedcaption-samistyle.md)              | 是               | 是                                         | 是                              |
| **Src**                                               | 不可以                | 是                                         | 是                              |
| [stretchToFit](player-stretchtofit.md)               | 是               | 是                                         | 不可以                               |
| [URL](player-url.md)                                 | 是               | 是                                         | 是                              |
| [體積](settings-volume.md)                         | 是               | 是                                         | 是                              |
| [windowlessVideo](player-windowlessvideo.md)         | 是               | 是                                         | 是                              |



 

> [!Note]  
> Firefox 外掛程式支援 **fileName** 和 **SRC** PARAM 元素，但 Internet Explorer 不支援。 它們都執行與 **URL** PARAM 元素相同的功能。

 

如需有關每個名稱屬性值的詳細資訊，請參閱 [腳本的物件模型參考](object-model-reference-for-scripting.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**在 Web 網頁中使用 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




