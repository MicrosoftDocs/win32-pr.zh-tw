---
title: 'Ext 屬性 (扭曲)  (VML) '
description: 'Ext 屬性 (扭曲)  (VML) '
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153273f613d188ae9e6fe733b2d0337c5010295d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186026"
---
# <a name="ext-attribute-skewvml"></a>Ext 屬性 (扭曲)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義扭曲的顯示方式。 讀取/寫入 **字串**。

**適用於**

[斜](msdn-online-vml-skew-element.md)

**標記語法**

<o： *element* v:ext = " *expression* " >

**指令碼語法**

*元素* 。 ext = "*expression*"

*運算式* =*元素* ext

**備註**

這個屬性是用來告訴圖形編輯器如何處理 **扭曲** 元素。 數值包括：

-   **edit**
-   **view** (預設) 
-   **backwardCompatible**

如果延伸模組設定為 [ **編輯**]，軟體檢視器可以忽略它。 如果設定為 **view**，則檢視器必須改為呈現點陣圖表示。

*Microsoft Office Extensions 屬性*

 

 