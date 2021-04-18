---
title: VML ConnectorType 屬性
description: VML ConnectorType 屬性
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0be0309e478970b93324b98a5efaaae54964435
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965650"
---
# <a name="vml-connectortype-attribute"></a>VML ConnectorType 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

表示用於聯結圖形的連接器類型。 讀取/寫入 **字串**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* o:connectortype = " *expression* " >

**備註**

數值包括：



| 值    | 描述                    |
|----------|--------------------------------|
| 無     | 沒有連接器。                  |
| 直 | 預設值。 直接連接器。 |
| 肘    | 肘形接點。     |
| 彎曲   | 彎曲的接點。            |



 

圖形化編輯器的規則引擎也可以使用這個屬性。

*Microsoft Office Extensions 屬性*

**範例**

圖形會使用直線作為接點。


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 