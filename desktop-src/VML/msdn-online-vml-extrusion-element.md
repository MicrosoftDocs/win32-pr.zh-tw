---
title: VML Extrusion 元素
description: VML Extrusion 元素
ms.assetid: d26b2451-383a-4ded-a46d-5ecca05ddb7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a6160a035853153c615576c3875ef9d90791245
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375745"
---
# <a name="vml-extrusion-element"></a>VML Extrusion 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形的延伸。

下列屬性會修改延伸。



| 屬性                                                              | 描述                                                                                             |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [AutoRotationCenter](msdn-online-vml-autorotationcenter-attribute.md) | 決定旋轉的中心是否為視角的幾何中心。                |
| [BackDepth](msdn-online-vml-backdepth-attribute.md)                   | 定義反向拉伸的數量。                                                               |
| [亮度](msdn-online-vml-brightness-attribute.md)                 | 指定場景的亮度量。                                                          |
| [色彩](color-attribute--extrusion--vml.md)                           | 定義拉伸臉部的色彩。                                                               |
| [ColorMode](msdn-online-vml-colormode-attribute.md)                   | 決定拉伸色彩的模式。                                                                 |
| [Diffusity](msdn-online-vml-diffusity-attribute.md)                   | 定義來自拉伸形狀的已反射光源的擴散量。                              |
| [Edge](msdn-online-vml-edge-attribute.md)                             | 定義拉伸邊緣的明顯斜面。                                                      |
| [內線](ext-attribute--extrusion--vml.md)                               | 定義圖形編輯器的預設延伸行為。                                           |
| [Facet](msdn-online-vml-facet-attribute.md)                           | 定義用來描述拉伸曲線表面的 facet 數目。                          |
| [ForeDepth](msdn-online-vml-foredepth-attribute.md)                   | 定義向前延伸的量。                                                                |
| [LightFace](msdn-online-vml-lightface-attribute.md)                   | 決定是否要對光源的正面臉部回應光線的變化。             |
| [LightHarsh](msdn-online-vml-lightharsh-attribute.md)                 | 判斷主要光源是否很粗糙。                                              |
| [LightHarsh2](msdn-online-vml-lightharsh2-attribute.md)               | 判斷次要燈光來源是否會很嚴苛。                                            |
| [LightLevel](msdn-online-vml-lightlevel-attribute.md)                 | 定義場景之主要光源的濃度。                                        |
| [LightLevel2](msdn-online-vml-lightlevel2-attribute.md)               | 定義場景之次要光源的濃度。                                      |
| [LightPosition](msdn-online-vml-lightposition-attribute.md)           | 指定主要光源在場景中的位置。                                                 |
| [LightPosition2](msdn-online-vml-lightposition2-attribute.md)         | 指定場景中次要光源的位置。                                               |
| [LockRotationCenter](msdn-online-vml-lockrotationcenter-attribute.md) | 判斷 **RotationAngle** 屬性是否指定了拉伸物件的旋轉。 |
| [金屬](msdn-online-vml-metal-attribute.md)                           | 判斷拉伸圖形的表面是否類似于金屬。                               |
| [開啟](on-attribute--extrusion--vml.md)                                 | 決定是否會顯示延伸。                                                      |
| [Orientation](msdn-online-vml-orientation-attribute.md)               | 指定將旋轉形狀的向量。                                              |
| [OrientationAngle](msdn-online-vml-orientationangle-attribute.md)     | 定義拉伸圍繞方向旋轉的角度。                                     |
| [飛機](msdn-online-vml-plane-attribute.md)                           | 將平面指定為與視角的直角。                                           |
| [轉譯](msdn-online-vml-render-attribute.md)                         | 定義延伸的呈現模式。                                                            |
| [RotationAngle](msdn-online-vml-rotationangle-attribute.md)           | 指定物件的 X 軸和 y 軸旋轉。                                           |
| [RotationCenter](msdn-online-vml-rotationcenter-attribute.md)         | 指定形狀的旋轉中心。                                                           |
| [增](msdn-online-vml-shininess-attribute.md)                   | 定義拉伸表面的反射光源的集中。                                   |
| [SkewAmt](msdn-online-vml-skewamt-attribute.md)                       | 定義拉伸的扭曲量。                                                             |
| [SkewAngle](msdn-online-vml-skewangle-attribute.md)                   | 定義拉伸的扭曲角度。                                                              |
| [Specularity](msdn-online-vml-specularity-attribute.md)               | 定義拉伸圖形的 specularity。                                                           |
| [型別](type-attribute--extrusion--vml.md)                             | 定義形狀的拉伸方式。                                                             |
| [觀點](msdn-online-vml-viewpoint-attribute.md)                   | 定義觀察者的觀點。                                                                  |
| [ViewpointOrigin](msdn-online-vml-viewpointorigin-attribute.md)       | 定義圖形周框方塊內的觀點原點。                               |



 

**備註**

這個元素必須定義在 [Shape](shape-element--vml.md) 元素內。

此外， [On](on-attribute--extrusion--vml.md) 屬性必須設定為 **True**。

以下是產生拉伸所需的最少程式碼。


```HTML
   <v:rect style="width:50px;height:50px">
   <v:extrusion on="True"/>
   </v:rect>
```



**範例**

-   [簡單圖形延伸](/previous-versions/bb229656(v=vs.85))
-   [動態形狀的延伸](/previous-versions/bb229657(v=vs.85))

 

 