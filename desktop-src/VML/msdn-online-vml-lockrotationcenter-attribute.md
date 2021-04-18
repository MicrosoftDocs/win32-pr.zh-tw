---
title: VML LockRotationCenter 屬性
description: VML LockRotationCenter 屬性
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49dd6ccada3f713f1cf2384a96f131c9a7714db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968513"
---
# <a name="vml-lockrotationcenter-attribute"></a>VML LockRotationCenter 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷 [RotationAngle](msdn-online-vml-rotationangle-attribute.md) 屬性是否指定了拉伸物件的旋轉。 讀取/寫入 **VgTriState**。

**適用於**

[擠壓](msdn-online-vml-extrusion-element.md)

**標記語法**

<o： *element* lockrotationcenter = " *expression* " >

**指令碼語法**

 lockrotationcenter = "*expression*"

*運算式* =** lockrotationcenter

**備註**

如果 **為 False**，則表示旋轉是由 [方向](msdn-online-vml-orientation-attribute.md) 屬性指定。 預設值為 **True**。

請注意：


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



就如同：


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



*Microsoft Office Extensions 屬性*

 

 