---
title: VML 裸機屬性
description: VML 裸機屬性
ms.assetid: 4d2efaed-d391-494f-9f0c-d57ad019f71d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d318724f0a8f3c5fbce1ee9045ed5d6e0d49686
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375393"
---
# <a name="vml-metal-attribute"></a>VML 裸機屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷拉伸圖形的表面是否類似于金屬。 讀取/寫入 **VgTriState**。

**適用於**

[擠壓](msdn-online-vml-extrusion-element.md)

**標記語法**

<o： *element* 裸機 = " *expression* " >

**指令碼語法**

*元素* 。金屬 = "*expression*"

*運算式* =*元素* 裸機

**備註**

如果設定為 **True**，這個屬性會使反射反映的光線變成材質色彩，而不是光線來源色彩，讓物件看起來更材質。若要進一步瞭解材質材質，specularity 必須相對高 (大約是 1.2) ，而 diffusity 相對較低 () 0.6。 預設值為 **[False]** 。

*Microsoft Office Extensions 屬性*

 

 