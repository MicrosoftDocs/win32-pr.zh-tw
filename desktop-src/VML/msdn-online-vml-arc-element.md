---
title: VML 弧線元素
description: VML 弧線元素
ms.assetid: 46b5b78a-9a69-432b-9008-0ce7a658b9dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee714d536d758b1f121b9a4afe106911e6e643c1745579cfc2b19de33bd6818
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680998"
---
# <a name="vml-arc-element"></a>VML 弧線元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

預先定義的弧線圖形。

**Arc** 會使用 [>startangle](msdn-online-vml-startangle-attribute.md) 和 [endangle](msdn-online-vml-endangle-attribute.md) 屬性。

以下是產生影像所需的最少程式碼。


```HTML
   <v:arc
   style="top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```





 

 