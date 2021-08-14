---
title: VML 鎖定元素
description: VML 鎖定元素
ms.assetid: 1dfdc23a-0ad1-468f-a850-2068f3cc1803
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 258ad050ea59427e43faba5b92ddc93dfd62e5065c874a0c5f5d25d88e30fecc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573978"
---
# <a name="vml-locks-element"></a>VML 鎖定元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形的鎖定。

下列屬性會修改鎖定。



| 屬性                                                    | 描述                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------|
| [AdjustHandles](msdn-online-vml-adjusthandles-attribute.md) | 決定是否可以編輯圖形的控制碼。                    |
| [AspectRatio](msdn-online-vml-aspectratio-attribute.md)     | 決定是否可以透過編輯器來變更圖形的外觀比例。 |
| [裁剪](msdn-online-vml-cropping-attribute.md)           | 決定是否允許在編輯器中進行裁剪。                   |
| [內線](ext-attribute--lock--vml.md)                          | 定義圖形化編輯器鎖定動作的行為。             |
| [分組](msdn-online-vml-grouping-attribute.md)           | 決定是否可以將圖形分組在編輯器中。                      |
| [位置](position-attribute--lock--vml.md)                | 決定是否在編輯器中鎖定圖形的位置。          |
| [旋轉](rotation-attribute--lock--vml.md)                | 決定是否允許在編輯器中旋轉形狀。         |
| [選取範圍](msdn-online-vml-selection-attribute.md)         | 決定是否可在編輯器中選取圖形。                    |
| [ShapeType](msdn-online-vml-shapetype-attribute.md)         | 判斷自選圖形類型是否可由編輯器變更。         |
| [Text](msdn-online-vml-text-attribute.md)                   | 決定是否可以編輯附加至圖形的文字。              |
| [頂點](msdn-online-vml-vertices-attribute.md)           | 決定是否可以透過編輯器變更路徑的頂點。      |



 

**備註**

這個元素必須定義在 [Shape](shape-element--vml.md) 元素內。

**鎖定** 元素是 VML 的 Microsoft Office 延伸模組。

 

 