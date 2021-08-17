---
title: VML 曲線元素
description: VML 曲線元素
ms.assetid: 37197ef0-7597-465a-bc37-7ffcde2e736b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fd06480b0d4bcf062f1f64eb9fa0b22862cf2b338b2c2f5ea0bf1c3cd2a1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655528"
---
# <a name="vml-curve-element"></a>VML 曲線元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

預先定義的曲線圖形。

**曲線** 使用 [to](to-attribute--curve--vml.md)、 [from](from-attribute--curve--vml.md)、 [control1](msdn-online-vml-control1-attribute.md)和 [control2](msdn-online-vml-control2-attribute.md) 屬性。

以下是產生影像所需的最少程式碼。


```HTML
   <v:curve
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```





 

 