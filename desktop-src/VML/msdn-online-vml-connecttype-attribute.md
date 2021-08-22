---
title: VML ConnectType 屬性
description: VML ConnectType 屬性
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76910977c0673500be2e91d9f387b1e61782a1460e5de0d513784caa6f0f1633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999258"
---
# <a name="vml-connecttype-attribute"></a>VML ConnectType 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

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



 

*Microsoft OfficeExtensions 屬性*

 

 