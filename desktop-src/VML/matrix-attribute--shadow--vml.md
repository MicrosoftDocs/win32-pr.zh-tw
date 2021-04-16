---
title: '矩陣屬性 (陰影)  (VML) '
description: '矩陣屬性 (陰影)  (VML) '
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d599aa817e87481aefdec43dbe345b7235fc54bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382677"
---
# <a name="matrix-attribute-shadowvml"></a>矩陣屬性 (陰影)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義陰影的觀點轉換。 讀取/寫入 **字串**。

**適用於**

[Shadow](msdn-online-vml-shadow-element.md)

**標記語法**

<v： *element* matrix = " *expression* " >

**指令碼語法**

*element* . matrix = "*expression*"

*運算式* =*元素*。矩陣

**備註**

以 "sxx，sxy，syx，syy，px，.py" 形式的透視圖轉換矩陣，其中 s = scale 和 p = 透視圖。 如果位移的單位為絕對單位，則為 px，.py 則為 1/emu 單位;否則是圖形大小的反向分數。

*VML 標準屬性*

 

 