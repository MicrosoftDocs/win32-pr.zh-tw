---
title: 'Position 屬性 (H)  (VML) '
description: 'Position 屬性 (H)  (VML) '
ms.assetid: 0bae708d-5409-4609-a102-7f799f2c1fbb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac310c0fad457beaf3b9aeb04671b7ffbb1dbd8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967495"
---
# <a name="position-attribute-hvml"></a>Position 屬性 (H)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定控制碼的 thex 和 y 值。 讀取/寫入 **VgVector2D**。

**適用於**

[H](msdn-online-vml-h-element.md) ([控制碼](msdn-online-vml-handles-element.md) 的子項目) 

**標記語法**

<v： *element* position = " *expression* " >

**備註**

x 和 y 值可以是下列其中一種類型：

-   常數
-   公式 (例如， @2) 
-   調整 (例如， \# 3) 
-   中心
-   下拉式功能表
-   bottomright

如果指定了以上的任何類型（除了 *調整* ），則該維度中的控制碼位置是固定的。 如果指定了調整控點，控制碼就可以在該維度中自由移動，而調整值是由控制碼的位置決定。

如果指定了 [極座標](msdn-online-vml-polar-attribute.md) 屬性， **Position** 屬性代表控制碼的半徑和角度值，而不是 x 和 y。

預設值為 0,0。

*VML 標準屬性*

 

 