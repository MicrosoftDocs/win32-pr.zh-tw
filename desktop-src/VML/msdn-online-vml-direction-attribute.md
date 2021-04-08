---
title: VML 方向屬性
description: VML 方向屬性
ms.assetid: bf6e0169-f0d4-4dfb-b59e-b5601049fd7a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a5bd45d4baaed100537207a02fc4308b964dfa2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682740"
---
# <a name="vml-direction-attribute"></a>VML 方向屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義文字方塊中文字的方向。 讀取/寫入 **字串**。

**適用於**

[TextBox](msdn-online-vml-textbox-element.md)

**標記語法**

<v： *element* style = "direction： *expression* " >

**備註**

數值包括：



| 值   | 描述                                                                                |
|---------|--------------------------------------------------------------------------------------------|
| 局部     | 文字會從左至右顯示。 預設值。                                                  |
| Rtl     | 文字由右至左顯示。                                                           |
| 內容 | 指出將以 "coNtext" 值寫出 **MSO 方向的 Alt** 標記。 |



 

*Microsoft Office Extensions 屬性*

 

 