---
title: '矩陣屬性 (扭曲)  (VML) '
description: '矩陣屬性 (扭曲)  (VML) '
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7fd3989807951f06df963c6899a2c81ce6e7faaa76432172e4391a4ce11029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768447"
---
# <a name="matrix-attribute-skewvml"></a>矩陣屬性 (扭曲)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義扭曲的觀點轉換。 讀取/寫入 **字串**。

**適用於**

[斜](msdn-online-vml-skew-element.md)

**標記語法**

<o： *element* matrix = " *expression* " >

**指令碼語法**

*element* . matrix = "*expression*"

*運算式* =*元素*。矩陣

**備註**

矩陣是以 "sxx，sxy，syx，syy，px，.py" 形式的字串，其中 s 是 scale、p 是觀點，而 x 和 y 是 x 和 y 值。 如果 [Offset](offset-attribute--skew--vml.md) 是絕對單位，則 px 和 .py 是以 emu ^-1 [單位](msdn-online-vml-units.md) (否則為圖形大小) 的反向分數。 預設值為 "1，0，0，1，0，0"。

*Microsoft OfficeExtensions 屬性*

 

 