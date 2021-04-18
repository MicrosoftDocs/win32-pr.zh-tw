---
title: VML Imagedata 元素
description: VML Imagedata 元素
ms.assetid: 91004646-b031-4973-a32d-7afdd10dab48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b416a53f97efc8a1f1875eda0e842c4cfbe96bf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965241"
---
# <a name="vml-imagedata-element"></a>VML Imagedata 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形的影像。

下列屬性會修改影像。



| 屬性                                                          | 描述                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| [AltHRef](althref-attribute--imagedata--vml.md)                   | 指定影像的替代參考。                        |
| [雙層](msdn-online-vml-bilevel-attribute.md)                   | 判斷影像是否會以黑色和白色顯示。          |
| [BlackLevel](msdn-online-vml-blacklevel-attribute.md)             | 判斷影像中的黑色濃度。                        |
| [Chromakey](msdn-online-vml-chromakey-attribute.md)               | 定義 palatte 中將視為透明的色彩。 |
| [CropBottom](msdn-online-vml-cropbottom-attribute.md)             | 定義從底部移除圖片的百分比。       |
| [CropLeft](msdn-online-vml-cropleft-attribute.md)                 | 定義從左側移除圖片的百分比。         |
| [CropRight](msdn-online-vml-cropright-attribute.md)               | 定義從右邊移除圖片的百分比。        |
| [CropTop](msdn-online-vml-croptop-attribute.md)                   | 定義從最上層移除圖片的百分比。          |
| [DetectMouseClick](detectmouseclick-attribute--imagedata--vml.md) | 決定是否會偵測到滑鼠按一下。                    |
| [EmbossColor](msdn-online-vml-embosscolor-attribute.md)           | 定義浮凸色彩效果的色彩。                         |
| [獲得](msdn-online-vml-gain-attribute.md)                         | 定義影像中所有色彩的濃度。                      |
| [伽 瑪](msdn-online-vml-gamma-attribute.md)                       | 定義影像的對比量。                          |
| [灰度](msdn-online-vml-grayscale-attribute.md)               | 決定圖片是否會以灰階模式顯示。          |
| [Href](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | 定義影像的 URL。                                           |
| [識別碼](id-attribute--image--vml.md)                                 | 定義影像的唯一識別碼。                             |
| [電影](msdn-online-vml-movie-attribute.md)                       | 定義電影影像的指標。                                   |
| [OLEID](msdn-online-vml-oleid-attribute.md)                       | 儲存影像的 OLE 識別碼。                                        |
| [Src](src-attribute--imagedata--vml.md)                           | 定義影像的來源。                                       |
| [標題](title-attribute--imagedata--vml.md)                       | 定義影像的標題。                                        |



 

**備註**

這個元素必須定義在 [Shape](shape-element--vml.md) 元素內。

此外， [**Src**](src-attribute--imagedata--vml.md) 屬性必須指向影像。

以下是產生影像所需的最少程式碼。


```HTML
   <v:rect
   style="position:relative;top:1;left:1;width:50;height:50">
   <v:imagedata src="../art/kids.jpg"/>
   </v:rect>
```



> [!Note]  
> 在 VML 的發行前版本中，這個元素稱為「 **影像** 」。

 

**範例**

-   [簡單 ImageData 範例](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/t_image.md)
-   [動態 ImageData 範例](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/x_image.md)

 

 