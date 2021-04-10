---
title: VML ConnectType 屬性
description: VML ConnectType 屬性
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a54135dcb4ffe0a86f781d68b8babe1259029be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092743"
---
# <a name="vml-connecttype-attribute"></a>VML ConnectType 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義用來將圖形附加至其他圖形的連接點類型。 讀取/寫入 **字串**。

**適用於**

[路徑](msdn-online-vml-path-element.md)

**標記語法**

<v： *element* o:connecttype = " *expression* " >

**備註**

數值包括：



| 值    | 描述                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| 無     | 沒有連接網站。 預設值。                                                                                                         |
| rect     | 標準四個連接點位於頂端、底部、左方和右邊的點。                                                   |
| 區段 | 使用圖形的編輯點。 編輯點是圖形化編輯器中用來選取圖形元件的黑色點。 |
| 自訂   | 連接位置的自訂陣列。                                                                                               |



 

*Microsoft Office Extensions 屬性*

 

 